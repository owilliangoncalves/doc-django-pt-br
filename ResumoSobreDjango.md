# Resumo sobre o Django

Porquê o Django foi desenvolvido de forma acelerada em uma sala, isso tornou o Django em uma ferramenta projetada para o desenvolvimento de tarefas rápido e fácil. Aqui está uma descrição mais informal de como escrever uma aplicação baseada em banco de dados com Django.
O objetivo desse documento e te dar um entendimento sobre técnicas especificas sobre como o Django funciona, mas sem a intenção de ser um tutorial (passo a passo) ou referência - mas vamos nessa! Se você se acha pronto para começar um projeto, você pode começar com o [tutorial](https://docs.djangoproject.com/en/5.1/intro/tutorial01/) ou ir direto para um [documentação mais detalhada](https://docs.djangoproject.com/en/5.1/topics/).

## Construindo seu modelo

Você também pode usar o Django sem um banco de dados, mas saiba que ele vem com [mapeador de objetos relacionais](https://en.wikipedia.org/wiki/Object-relational_mapping) que permite que você descreva seu banco de dados (se houver) em código Python.

A [sintaxe da modelagem de dados](https://docs.djangoproject.com/en/5.1/topics/db/models/) oferece uma rica representação dos seus modelos - isso economiza alguns anos na resolução de problemas com esquema de banco de dados. Veja um exemplo básico:

**Arquivo**: `news/models.py`

```python
from django.db import models


class Reporter(models.Model):
    full_name = models.CharField(max_length=70)

    def __str__(self):
        return self.full_name


class Article(models.Model):
    pub_date = models.DateField()
    headline = models.CharField(max_length=200)
    content = models.TextField()
    reporter = models.ForeignKey(Reporter, on_delete=models.CASCADE)

    def __str__(self):
        return self.headline
```

## Instalação

A seguir, rode os comandos para que o Django crie um banco de dados com tabelas automaticamente.

O comando `makemigrations` busca todos os seus modelos disponíveis e inicia a migração se as tabelas ainda não existirem.

```bash
 python3 manage.py makemigrations
```

O comando `migrate`inicia a migração e create as tabelas in seus banco de dados como uma opção de controle de esquema

```bash
python3 manage.py migrate
```

## Aproveite uma API gratuita

Assim, você tem uma API grátis para acessar seus dados. Essa API é criada durante o voo (durante o processo), sem necessidade de código.

```python

# Import o modelo que foi em seu app "news"
from news.models import Article, Reporter

# Nenhum repórter ainda foi cadastrado
Reporter.objects.all()
<QuerySet []>

# Cadastrando um novo reporter
r = Reporter(full_name="John Smith")

# Salve o objeto em seu banco de dados, para isso você tem que chamar save().
r.save()

# Agora temos um ID.
r.id
1

# Agora existe um repórter em seu banco de dados.
Reporter.objects.all()
<QuerySet [<Reporter: John Smith>]>

#Os campos estão representando atributos em programação orientada a objeto em Python.
r.full_name
'John Smith'

# Django fornece um rica API de pesquisa em base de dados.
Reporter.objects.get(id=1)
<Reporter: John Smith>
Reporter.objects.get(full_name__startswith="John")
<Reporter: John Smith>
Reporter.objects.get(full_name__contains="mith")
<Reporter: John Smith>
Reporter.objects.get(id=2)
Traceback (most recent call last):
    ...
DoesNotExist: Reporter matching query does not exist.

# Criando uma postagem.
from datetime import date
a = Article(
...     pub_date=date.today(), headline="Django é legal?", content="Sim!", reporter=r
... )
a.save()

# Agora a postagem esta no banco de dados
Article.objects.all()
<QuerySet [<Article: Django is cool>]>

# Postagem podem ter seus acesso aos atributos de Reporter através da API.
r = a.reporter
r.full_name
'John Smith'

# E vice e versa
r.article_set.all()
<QuerySet [<Article: Django is cool>]>

# A API identifica relacionamentos de forma perfomáatica
# JOINs por trás dos panos.
# Buscando todas as postagens de um reporter que o nome começa com "John".
Article.objects.filter(reporter__full_name__startswith="John")
<QuerySet [<Article: Django is cool>]>

# Mudando atributos de um objeto com save().
r.full_name = "Billy Goat"
r.save()

# Deletando um objeto com delete().
r.delete()
```

## Uma interface de "admin" dinâmica:

Uma vez que seus modelos estão definidos, Django pode automaticamente criar uma interface administrativa pronta para produção de forma profissional. Um site que possibilita que usuários autenticados, adicionem, deletem e alterem objetos. O único passo obrigatório é registrar seu modelo no site administrativo:

**Arquivo**: `news/models.py`

```python
from django.db import models


class Article(models.Model):
   pub_date = models.DateField()
   headline = models.CharField(max_length=200)
   content = models.TextField()
   reporter = models.ForeignKey(Reporter, on_delete=models.CASCADE)
```

**Arquivo**: `news/admin.py`

```python
from django.contrib import admin

from . import models

admin.site.register(models.Article)
```

A ideia aqui é que caso o seu site seja administrado por uma equipe, cliente ou apenas você - não tenha o trabalho de criar uma interface para o backend apenas gerencie o conteúdo.
Em um típico fluxo de trabalho de desenvolvimento de aplicações com Django é para criação de modelos e melhoras sites da forma mais rápido possível.

## Construindo suas URLs

Um esquema de URLs limpa e elegante é um detalhe importante in uma aplicação de alta qualidade. Django incentiva você no desenvolvimento dessas URLs e não coloca nenhum detalhe nas URls como .php ou .asp

Para a criação das URLs, você pode criar um módulo em Python chamado [`URLconf`](https://docs.djangoproject.com/en/5.1/topics/http/urls/). Um tabela de conteúdos para seu aplicativo que contenha o relacionamento entre as URL padrões e funções de callback em Python. `URLconf` também é utilizada para separar URLs de código Python.

Aqui está como uma `URLconf` deveria parecer para a aplicação `Reporter/Article`:

**Arquivo**: `news/urls.py`

```python news/url.py
from django.urls import path

from . import views

urlpatterns = [
    path("articles/<int:year>/", views.year_archive),
    path("articles/<int:year>/<int:month>/", views.month_archive),
    path("articles/<int:year>/<int:month>/<int:pk>/", views.article_detail),
]
```
