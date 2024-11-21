# Documentação do Django em Português do Brasil. 🇧🇷

No meu tempo livre quero me dedicar a tradução da documentação do framework Django para o português brasileiro. Solicitei a participação na tradução oficial no Transifex, mas ainda não me aceitaram, então, vou iniciando meus trabalhos por aqui.
Claro que você irá encontrar muitos erros de português, digitação, sintaxe, contexto entre outro, fique á vontade para abrir uma issue com um pull request, vamos construir juntos uma documentação melhor.
Algumas palavras eu não consigo achar uma equivalente na nossa língua, outras vocês podem perceber que talvez teria uma palavra mais adequada, enfim... Vamos nessa juntos 😀

# Django Documentação

Tudo que você precisa saber sobre o Django.

## Primeiros passos

Se você é novo em programação ou usuário novo do Django? Esse é o lugar para começar!

- Do inicio: [Visão Geral](ResumoSobreDjango.md) | [Instalação](https://docs.djangoproject.com/en/5.1/intro/install/)
- Tutorial:

## Como conseguir ajuda

Está tendo dificuldades? Nós podemos te ajudar.

- Tente o [FAQ](https://docs.djangoproject.com/en/5.1/faq/) - Nele você encontra as respostas para as perguntas comuns.
- Quer uma ajuda especifica? Tente [Index](https://docs.djangoproject.com/en/5.1/genindex/), [Module Index](https://docs.djangoproject.com/en/5.1/py-modindex/) ou o [tabela de conteúdo](https://docs.djangoproject.com/en/5.1/contents/).
- Não encontrou nada? Veja [FAQ: Obtendo ajuda](https://docs.djangoproject.com/en/5.1/contents/) para obter ajuda e responder perguntas da comunidade.
- Reportar erros com o Django [aqui](https://code.djangoproject.com/).

## Como a documentação é organizada

Django possui uma documentação extensa. Uma visão geral em alto nível de como a documentação está organizada poderá te ajudar a entender onde certas coisas estão:

- [Tutoriais](https://docs.djangoproject.com/en/5.1/intro/) te pegam pelas mãos e te ajuda a criar uma aplicação web passo a passo. Comece pelo tutorial se você é novo usuário de Django ou também não tem experiência com desenvolvimento de aplicações web. Também de uma olhada em ["Primeiros Passos"](https://docs.djangoproject.com/en/5.1/#index-first-steps).
- [Guia de tópicos](https://docs.djangoproject.com/en/5.1/topics/) discussão de pontos chaves e conceitos em alto nível, dando boas ideias.
- [Guia de referências](https://docs.djangoproject.com/en/5.1/ref/) nela você encontra referências técnicas para API e outros assuntos do Django. Eles descrevem como funciona e como usa o Django, assumindo que você tenha um entendimento básico de conceitos importantes.
- [Guia de como fazer](https://docs.djangoproject.com/en/5.1/howto/) te dão uma ideia dos passos envolvidos e problemas chaves de caso de uso. São tutoriais avançados e assumem que você sabe como Django funciona.

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

## A camada _"template"_

A camada _template_ fornece uma sintaxe de design amigável para renderizar as informações que serão mostradas ao usuário. Aprenda mais a seguir:

- O básico: [Visão geral](https://docs.djangoproject.com/en/5.1/topics/templates/)
- Para designers: [Visão geral da linguagem](https://docs.djangoproject.com/en/5.1/ref/templates/language/) | [Tags e filtros nativos](https://docs.djangoproject.com/en/5.1/ref/templates/builtins/) | [Humanização](https://docs.djangoproject.com/en/5.1/ref/contrib/humanize/)
- Para programadores: [Modelo API](https://docs.djangoproject.com/en/5.1/ref/templates/api/) | [Tags e Filtros customizados](https://docs.djangoproject.com/en/5.1/howto/custom-template-tags/) | [Modelo customizado backend](https://docs.djangoproject.com/en/5.1/howto/custom-template-backend/)

## Formulários

Django fornece um boas ferramentas para facilitar a criação de forms e manipulação de dados.

- O básico: [Visão geral](https://docs.djangoproject.com/en/5.1/topics/forms/) | [API de formulários](https://docs.djangoproject.com/en/5.1/ref/forms/api/) | [Campos nativos](https://docs.djangoproject.com/en/5.1/ref/forms/fields/) | [Widgets nativos](https://docs.djangoproject.com/en/5.1/ref/forms/widgets/)
- Avançado: [Modelo de formulários](https://docs.djangoproject.com/en/5.1/topics/forms/modelforms/) | [Integração de arquivos](https://docs.djangoproject.com/en/5.1/topics/forms/media/) | [Configuração de formulário](https://docs.djangoproject.com/en/5.1/topics/forms/formsets/) | [Customizar validação](https://docs.djangoproject.com/en/5.1/ref/forms/validation/)

## Processo de desenvolvimento

Aprenda sobre vários componentes e ferramentas que te podem te ajudar no desenvolvimento e teste de aplicações Django:

- Configuração: [Visão geral](https://docs.djangoproject.com/en/5.1/topics/settings/) | [Lista completa de configuração](https://docs.djangoproject.com/en/5.1/ref/settings/)
- Aplicações: [Visão geral](https://docs.djangoproject.com/en/5.1/ref/applications/)
- Execeções: [Visão geral](https://docs.djangoproject.com/en/5.1/ref/exceptions/)
- `django-admin e manage.py`: [Visão geral](https://docs.djangoproject.com/en/5.1/ref/django-admin/) | [Adicionando comandos customizados](https://docs.djangoproject.com/en/5.1/howto/custom-management-commands/)
- Testes: [Introdução](https://docs.djangoproject.com/en/5.1/topics/testing/) | [Escrevendo e Rodando testes](https://docs.djangoproject.com/en/5.1/topics/testing/overview/) | [Ferramentas de testes nativas](https://docs.djangoproject.com/en/5.1/topics/testing/tools/) | [Pontos avançados](https://docs.djangoproject.com/en/5.1/topics/testing/advanced/)
- Deploy: [Visão geral](https://docs.djangoproject.com/en/5.1/howto/deployment/) | [Servidores WSGI](https://docs.djangoproject.com/en/5.1/howto/deployment/wsgi/) | [Servidores ASGI](https://docs.djangoproject.com/en/5.1/howto/deployment/asgi/) | [Deploy de arquivos estáticos](https://docs.djangoproject.com/en/5.1/howto/static-files/deployment/) | [Acompanhamento de erros por email](https://docs.djangoproject.com/en/5.1/howto/error-reporting/) | [Checklist de deploy](https://docs.djangoproject.com/en/5.1/howto/deployment/checklist/)

## O "admin"

Encontre tudo o que você precisa saber sobre a interface de "admin", uma das ferramentas mais popular do Django:

- [Admin site](https://docs.djangoproject.com/en/5.1/ref/contrib/admin/)
- [Ações de admin](https://docs.djangoproject.com/en/5.1/ref/contrib/admin/actions/)
- [Documentação de geração de admin](https://docs.djangoproject.com/en/5.1/ref/contrib/admin/admindocs/)

## Segurança

Segurança é um ponto de importância no desenvolvimento de aplicações web e o Django fornece múltiplas ferramentas e mecanismo:

- [Visão geral de segurança](https://docs.djangoproject.com/en/5.1/topics/security/)
- [Abertura de erros de segurança no Django](https://docs.djangoproject.com/en/5.1/releases/security/)
- [Proteção _Clickjacking_](https://docs.djangoproject.com/en/5.1/ref/clickjacking/)
- [Proteção contra requisições falsas](https://docs.djangoproject.com/en/5.1/ref/csrf/)
- [Assinatura Criptográfica](https://docs.djangoproject.com/en/5.1/topics/signing/)
- [Middleware de segurança](https://docs.djangoproject.com/en/5.1/ref/middleware/#security-middleware)

## Internacionalização e localização

Django oferece uma grande ferramenta de internacionalização e localização to auxiliar no desenvolvimento para múltiplas linguagens e regiões do mundo:

- [Visão geral](https://docs.djangoproject.com/en/5.1/topics/i18n/) | [Internacionalização](https://docs.djangoproject.com/en/5.1/topics/i18n/translation/) | [Localização](https://docs.djangoproject.com/en/5.1/topics/i18n/translation/#how-to-create-language-files) | [UI e entratdas de formulários adaptados](https://docs.djangoproject.com/en/5.1/topics/i18n/formatting/) |
- [Regiões](https://docs.djangoproject.com/en/5.1/topics/i18n/timezones/) |

## Performance e otimização

Temos uma variedade de técnicas e ferramentas que podem auxiliar em um tornar seu código mais eficiente - rápido, usando poucos recursos do sistema

- [Visão geral de performance e otimização](https://docs.djangoproject.com/en/5.1/topics/performance/)

## Ferramentas geográficas

[GeoDjango](https://docs.djangoproject.com/en/5.1/ref/contrib/gis/) pretende ser a maior classe de ferramentas de geográfica. Esse objetivo está sendo possível graças aplicações poderosas de dados geográficos aberto.

## Ferramentas de desenvolvimento web

Django oferece múltiplas ferramentas que você irá usar no desenvolvimento de aplicações web:

- Autenticação: [Visão geral](https://docs.djangoproject.com/en/5.1/topics/auth/) | [Sistema de autenticação](https://docs.djangoproject.com/en/5.1/topics/auth/default/) | [Gerenciador de senhas](https://docs.djangoproject.com/en/5.1/topics/auth/passwords/) | [Autenticação personalizada](https://docs.djangoproject.com/en/5.1/topics/auth/customizing/) | [API](https://docs.djangoproject.com/en/5.1/ref/contrib/auth/)

- [Caching](https://docs.djangoproject.com/en/5.1/topics/cache/)
- [Logging](https://docs.djangoproject.com/en/5.1/topics/logging/)
- [Envio de emails](https://docs.djangoproject.com/en/5.1/topics/email/)
- [Feeds (RSS/Atom)](https://docs.djangoproject.com/en/5.1/ref/contrib/syndication/)
- [Paginação](https://docs.djangoproject.com/en/5.1/topics/pagination/)
- [Ferramenta para avisos](https://docs.djangoproject.com/en/5.1/ref/contrib/messages/)
- [Serialização](https://docs.djangoproject.com/en/5.1/topics/serialization/)
- [Sessões](https://docs.djangoproject.com/en/5.1/topics/http/sessions/)
- [Sitemaps](https://docs.djangoproject.com/en/5.1/ref/contrib/sitemaps/)
- [Gerenciamento de arquivos estáticos](https://docs.djangoproject.com/en/5.1/ref/contrib/staticfiles/)
- [Validação de dados](https://docs.djangoproject.com/en/5.1/ref/validators/)

## Outras funcionalidades importantes

Aprenda sobre outras funcionalidades importantes do Django

- [Processamento condicional](https://docs.djangoproject.com/en/5.1/topics/conditional-view-processing/)
- [Tipagem de conteúdo e relações genéricas](https://docs.djangoproject.com/en/5.1/ref/contrib/contenttypes/)
- [Flatpages](https://docs.djangoproject.com/en/5.1/ref/contrib/flatpages/)
- [Redirecionamento](https://docs.djangoproject.com/en/5.1/ref/contrib/redirects/)
- [Sinais](https://docs.djangoproject.com/en/5.1/topics/signals/)
- [Checagem de sistema](https://docs.djangoproject.com/en/5.1/topics/checks/)
- [Ferramentas para sites](https://docs.djangoproject.com/en/5.1/ref/contrib/sites/)
- [Unicode em Django](https://docs.djangoproject.com/en/5.1/ref/unicode/)

## Projeto aberto ao público

Aprenda sobre o processo de desenvolvimento do Django e como você pode contribuir:

- Comunidade: [Contribua com Django](https://docs.djangoproject.com/en/5.1/internals/contributing/) | [Processo de lançamento](https://docs.djangoproject.com/en/5.1/internals/release-process/) | [Time](https://docs.djangoproject.com/en/5.1/internals/organization/) | [Repositório com código](https://docs.djangoproject.com/en/5.1/internals/git/) | [Politicas de segurança](https://docs.djangoproject.com/en/5.1/internals/security/) | [Lista de email e fórum](https://docs.djangoproject.com/en/5.1/internals/mailing-lists/)

- Filosofia de Design:[Visão geral](https://docs.djangoproject.com/en/5.1/misc/design-philosophies/)
- Documentação: [Sobre a documentação](https://docs.djangoproject.com/en/5.1/internals/contributing/writing-documentation/)
- Distribuição: [Visão geral](https://docs.djangoproject.com/en/5.1/misc/distributions/)
- Linha do tempo: [Estabilidade da API](https://docs.djangoproject.com/en/5.1/misc/api-stability/) | [Avisos de lançamento e instruções para atualização](https://docs.djangoproject.com/en/5.1/releases/) | [Desuso](https://docs.djangoproject.com/en/5.1/internals/deprecation/)
