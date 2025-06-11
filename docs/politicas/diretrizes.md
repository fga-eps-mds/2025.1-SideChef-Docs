## Histórico de versões

| Versão | Alteração       | Responsável         | Data Alteração |
|--------|-----------------|---------------------|----------------|
| 1.0    | Criação do documento de política de commits  | Diógenes Dantas Lélis Júnior | 08/06/2025 |
| 1.1    | Criação da Diretrizes de padronização de código | Pedro Amaral e João Marcelo Naves | 27/05/2025 |
| 1.2    | Adiciona o restante da documentação da Diretrizes do Projeto | Diógenes Dantas Lélis Júnior | 10/06/2025 |
| 1.3    | Correções padronização e nas tecnologias do mobile | Bruno Seiji Kishibe | 11/06/2025 |

## Diretrizes do Projeto
Esse documento abrange as diretrizes que devem ser seguidas no projeto, abordando temas como estrutura do código, estrutura de diretórios, organização e importação de código

## Diretrizes de Padronização de Código
Estas diretrizes estabelecem os padrões de codificação a serem adotados em todo o Projeto MDS para garantir consistência, legibilidade e manutenibilidade da base de código.

### 1. Regras Gerais
- Todos os comentários e nomes de variáveis devem ser escritos em inglês.
- Comentários devem ser úteis e explicativos, elucidando o porquê do segmento de código, e não meramente reafirmando sua função.

### 2. Python
- Variáveis: Empregue nomes descritivos utilizando snake_case (letras minúsculas com palavras separadas por sublinhado). Exemplo: test_file
- Funções: Nomeie funções utilizando snake_case. Exemplo: calculate_total
- Classes: Utilize PascalCase (cada palavra começa com letra maiúscula, sem separadores). Exemplo: UserProfile
- Nomes de Arquivos: Use snake_case.py. Exemplo: data_parser.py

### 2.1 Estrutura do Módulo Back-end FastAPI
Para a organização de projetos backend em Python utilizando FastAPI, recomenda-se a seguinte estrutura de diretórios para modularização e separação de responsabilidades:

#### Models
- Função: Define os modelos de dados da aplicação, representando a estrutura das tabelas do banco de dados e suas relações. Geralmente, contém classes que mapeiam para o banco de dados através de um ORM(Object-Relational Mapper), como SQLAlchemy, e são usadas pelos services para interagir com o banco.
- Conteúdo Típico: Arquivos Python definindo classes que representam entidades do sistema (ex: user_model.py, product_model.py).

#### Routes
- Função: Define os endpoints (URLs) da API. Responsável por receber as requisições HTTP (GET, POST, PUT, DELETE, etc.) utilizando os decoradores do FastAPI (ex: @router.get). Realiza a validação dos dados de entrada e formatação dos dados de saída com a ajuda de schemas (Pydantic) e direciona a requisição para a lógica de negócio apropriada nos services.
- Conteúdo Típico: Arquivos Python que implementam os endpoints para cada recurso da aplicação (ex: user_routes.py, auth_routes.py), utilizando APIRouter do FastAPI para agrupar rotas relacionadas.

#### Schemas
- Função: Define a estrutura, tipos de dados e regras de validação para os dados que entram e saem da API, utilizando classes Pydantic. São cruciais para a validação automática de requests e responses do FastAPI, além de serem utilizados para gerar a documentação interativa da API (Swagger UI / OpenAPI).
- Conteúdo Típico: Arquivos Python com classes Pydantic que definem a forma dos dados para criação, atualização e visualização de recursos (ex: user_schemas.py contendo UserCreate, UserUpdate, UserResponse).

#### Services
- Função: Contém a lógica de negócio principal da aplicação. Os serviços orquestram as operações, interagem com os models para acessar e manipular dados do banco de dados, e executam as regras de negócio. São chamados pelas routes para processar as requisições de forma desacoplada do framework HTTP.
- Conteúdo Típico: Arquivos Python com funções ou classes que implementam as operações específicas para cada recurso (ex: user_service.py com funções como create_user_service,
get_user_by_id_service).

#### Arquivo Principal
O arquivo principal da aplicação (comumente main.py ou app.py na raiz do diretório da aplicação) é o ponto de entrada e é responsável por:

- Inicialização da Aplicação: 
    - Criar a instância principal do FastAPI: app = FastAPI().

- Configuração Global:
    - Carregar configurações da aplicação (ex: variáveis de ambiente, segredos).
    - Configurar middlewares (ex: CORS, autenticação, tratamento de erros).
    - Estabelecer e gerenciar conexões com bancos de dados (ex: definir engine e SessionLocal do SQLAlchemy) e outros serviços externos.
    - Opcionalmente, pode incluir lógica para criar tabelas no banco de dados durante a inicialização (ex: Base.metadata.create_all(bind=engine)), embora em produção migrações (com Alembic, por exemplo) sejam preferíveis.

- Registro de Rotas:
    - Importar os objetos APIRouter definidos nos módulos de routes e registrá-los na instância principal da aplicação usando app.include_router(router_object).

- Ponto de Paretida do Servidor (em Contexto Docker):
    - Ao usar Docker, o comando para iniciar o servidor ASGI (como Uvicorn) é geralmente especificado no Dockerfile (ex: CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "80"]). O arquivo main.py em si não precisa conter a lógica explícita uvicorn.run() para este cenário, pois o Docker gerencia o ciclo de vida do processo.

### 3. TypeScript

#### Funções
- Use camelCase (a primeira palavra em minúscula, as demais com inicial maiúscula). 
    - Exemplo: loadUserData

#### Classes
- Nomeie classes utilizando PascalCase.
    - Exemplo: MainComponent

#### Nome de Arquivos
- Componentes React: PascalCase.tsx
    - Exemplo: UserCard.tsx
- Utilitários ou Funções Auxiliares: camelCase.ts
    - Exemplo: formatDate.ts

### 4. React + StyleSheet

#### React
O React adere às convenções de nomenclatura do TypeScript previamente delineadas:
- Funções são nomeadas utilizando camelCase.
- Componentes e classes são nomeados utilizando PascalCase

#### StyleSheet
- Os estilos devem ser definidos em arquivos .ts separados.
- Empregue nomes de classes descritivos utilizando kebab-case (palavras em minúsculo separadas por hífens).
    - Exemplo: .main-container

#### Organização e importação
- O StyleSheet deve ser importado no topo do arquivo do componente correspondente.
    - Exemplo: import './UserCard.ts';
- Evite estilos inline sempre que possível, priorizando o uso de classes.
- Agrupe estilos relacionados no mesmo arquivo para facilitar a manutenção.
