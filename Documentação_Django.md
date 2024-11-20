# Django Documentação

Tudo que você precisa saber sobre o Django.

## Primeiros passos

Se você é novo em programação ou usuário novo do Django? Esse é o lugar para começar!

- Do inicio: [Visão Geral](https://docs.djangoproject.com/en/5.1/intro/overview/) | [Instalação](https://docs.djangoproject.com/en/5.1/intro/install/)
- Tutorial:

## Como conseguir ajuda

Está tendo dificuldades? Nós podemos te ajudar.

- Tente o [FAQ](https://docs.djangoproject.com/en/5.1/faq/) - Nele você encontra as respostas para as perguntas mais comuns.
- Quer uma ajuda especifica? Tente [Index](https://docs.djangoproject.com/en/5.1/genindex/), [Module Index](https://docs.djangoproject.com/en/5.1/py-modindex/) ou o [tabela de conteúdo](https://docs.djangoproject.com/en/5.1/contents/).
- Não encontrou nada? Veja [FAQ: Obtendo ajuda](https://docs.djangoproject.com/en/5.1/contents/) para obter ajuda e responder perguntas da comunidade.
- Reportar erros com o Django [aqui](https://code.djangoproject.com/).

## Como a documentação é organizada

Django possui uma documentação extensa. Uma visão geral em alto nível de como a documentação está organizada poderá te ajudar a etender onde certas coisas estão:

- [Tutoriais](https://docs.djangoproject.com/en/5.1/intro/) te pegam pelas mãos e te ajuda a criar uma aplicação web passo a passo. Comece pelo tutorial se você é novo usuário de Django ou também não tem experiência com desenvolvimento de aplicações web. Também de uma olhada em ["Primeiros Passos"](https://docs.djangoproject.com/en/5.1/#index-first-steps).
- [Guia de tópicos](https://docs.djangoproject.com/en/5.1/topics/) discussão de pontos chaves e conceitos em alto nível, dando boas ideias.
- [Guia de referências](https://docs.djangoproject.com/en/5.1/ref/) nela você encontra referências tecnicas para API e outros assuntos do Django. Eles descrevem como funciona e como usa o Django, assumindo que vocˆ´tenha um entendimento básico de conceitos importantes.
- [Guia de como fazer](https://docs.djangoproject.com/en/5.1/howto/) te dão uma idéia dos passos envolvidos e problemas chaves de caso de uso. São tutoriais avançados e assumem que você sabe como Django funciona.

_Algumas palavras a seguir não serão traduzidas. Existe uma arquitetura MVC (Model, View e Control) e faz sentido que você saiba o que é. Para mais informações veja esse vídeo: [YouTube - MVC](https://youtu.be/m5ZcrbiD41E?si=zEovsamN3MJD4cft&t=163)_

## A camada "_model_"

Django fornece uma camada de abstração (os "modelos") para estruturação e manipulação de dados da sua aplicação web. Aprenda mais a seguir:

- Modelos (_models_): [Introdução aos modelos](https://docs.djangoproject.com/en/5.1/topics/db/models/) | [Tipos de campos](https://docs.djangoproject.com/en/5.1/ref/models/fields/) | [Indices](https://docs.djangoproject.com/en/5.1/ref/models/indexes/) | [Meta opcões](https://docs.djangoproject.com/en/5.1/ref/models/options/) | [Classe modelo](https://docs.djangoproject.com/en/5.1/ref/models/class/)
- Configuração de consultas (_QuerySets_): [Construindo Querys](https://docs.djangoproject.com/en/5.1/topics/db/queries/) | [Método de referência QuerySet](https://docs.djangoproject.com/en/5.1/ref/models/querysets/) | [Expressões de busca](https://docs.djangoproject.com/en/5.1/ref/models/lookups/)
- Modelo de Instâncias (_Model Instances_): [Métodos de Instância](https://docs.djangoproject.com/en/5.1/ref/models/instances/) | [Acesso a objetos relacionados](https://docs.djangoproject.com/en/5.1/ref/models/relations/)
- Migrações (_Migrations_):[Introdução a Migração](https://docs.djangoproject.com/en/5.1/topics/migrations/) | [Operações de referência](https://docs.djangoproject.com/en/5.1/ref/migration-operations/) | [Editor de Schema](https://docs.djangoproject.com/en/5.1/ref/schema-editor/) | [Escreevendo migrações](https://docs.djangoproject.com/en/5.1/howto/writing-migrations/)
- Avançado: [Gerentes](https://docs.djangoproject.com/en/5.1/topics/db/managers/) | [Escrevendo SQL](https://docs.djangoproject.com/en/5.1/topics/db/sql/) | [Transações](https://docs.djangoproject.com/en/5.1/topics/db/transactions/) | [Agregação](https://docs.djangoproject.com/en/5.1/topics/db/aggregation/) | [Busca](https://docs.djangoproject.com/en/5.1/topics/db/search/) | [Campos customizados](https://docs.djangoproject.com/en/5.1/howto/custom-model-fields/) | [Multiplas Base de dados](https://docs.djangoproject.com/en/5.1/topics/db/multi-db/) | [Busca personalizada](https://docs.djangoproject.com/en/5.1/howto/custom-lookups/) | [Expressões em Querys](https://docs.djangoproject.com/en/5.1/ref/models/expressions/) | [Expressões Condicionais](https://docs.djangoproject.com/en/5.1/ref/models/conditional-expressions/) | [Funções de banco de dados](https://docs.djangoproject.com/en/5.1/ref/models/database-functions/)
- Outros: [Bases de dados Suportadas](https://docs.djangoproject.com/en/5.1/ref/databases/) | [Base de dados Legais](https://docs.djangoproject.com/en/5.1/howto/legacy-databases/) | [Consumindo dados](https://docs.djangoproject.com/en/5.1/howto/initial-data/) | [Acesso otimizado a banco de dados](https://docs.djangoproject.com/en/5.1/topics/db/optimization/) | [Recursos especifícos do PostgresSQL](https://docs.djangoproject.com/en/5.1/ref/contrib/postgres/)

## A camada "_view_"

Django adota o conceito de _views_ para encapsular a parte lógica de uma _request_ de um usuário e retornar um _response_. Aprenda mais a seguir:

- O básico: [URLconfs](https://docs.djangoproject.com/pt-br/5.1/topics/http/urls/) | [Funções de view](https://docs.djangoproject.com/pt-br/5.1/topics/http/views/) | [Atalhos](https://docs.djangoproject.com/pt-br/5.1/topics/http/shortcuts/) | [Decorators](https://docs.djangoproject.com/pt-br/5.1/topics/http/decorators/) | [Suporte assíncrono](https://docs.djangoproject.com/pt-br/5.1/topics/async/)
- Referência: [Views nativas](https://docs.djangoproject.com/pt-br/5.1/ref/views/) | [Objetos request/response](https://docs.djangoproject.com/pt-br/5.1/ref/request-response/) | [Objetos TemplateResponse](https://docs.djangoproject.com/pt-br/5.1/ref/template-response/)
- Envio de arquivos: [Visão Geral](https://docs.djangoproject.com/pt-br/5.1/topics/http/file-uploads/) | [Arquivos Objetos](https://docs.djangoproject.com/pt-br/5.1/ref/files/file/) | [Amarzenamento API]() | [Gerenciamento de arquivos](https://docs.djangoproject.com/pt-br/5.1/topics/files/) | [Armazenamento personalizado](https://docs.djangoproject.com/pt-br/5.1/howto/custom-file-storage/)
- Base-classes views: [Visão Geral](https://docs.djangoproject.com/pt-br/5.1/topics/class-based-views/) | [Modo Interno para views](https://docs.djangoproject.com/pt-br/5.1/topics/class-based-views/generic-display/) | [Edição interna para views](https://docs.djangoproject.com/pt-br/5.1/topics/class-based-views/generic-editing/) | [Usando mixins](https://docs.djangoproject.com/pt-br/5.1/topics/class-based-views/mixins/) | [API referência](https://docs.djangoproject.com/pt-br/5.1/ref/class-based-views/) | [Index plano?](https://docs.djangoproject.com/pt-br/5.1/ref/class-based-views/flattened-index/)
- Avançado: [Gerando CSV](https://docs.djangoproject.com/pt-br/5.1/howto/outputting-csv/) | [Gerando PDF](https://docs.djangoproject.com/pt-br/5.1/howto/outputting-pdf/)
- Middleware: [Visão geral](https://docs.djangoproject.com/pt-br/5.1/topics/http/middleware/) | [Classes de Middleware embutidas](https://docs.djangoproject.com/pt-br/5.1/ref/middleware/)
