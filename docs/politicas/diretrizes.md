## Histórico de versões

| Versão | Alteração       | Responsável         | Data Alteração |
|--------|-----------------|---------------------|----------------|
| 1.0    | Criação do documento de política de commits  | Diógenes Dantas Lélis Júnior | 08/06/2025 |

## Diretrizes do Projeto
Esse documento abrange as diretrizes que devem ser seguidas no projeto, abordando temas como estrutura do código, estrutura de diretórios, organização e importação de código

## Diretrizes de Padronização de Código
Estas diretrizes estabelecem os padrões de codificação a serem adotados em todo o Projeto MDS para garantir consistência, legibilidade e manutenibilidade da base de código.

### Regras Gerais
- Todos os comentários e nomes de variáveis devem ser escritos em inglês.
- Comentários devem ser úteis e explicativos, elucidando o porquê do segmento de código, e não meramente reafirmando sua função.

### Python
- Variáveis: Empregue nomes descritivos utilizando snake_case (letras minúsculas com palavras separadas por sublinhado). Exemplo: test_file
- Funções: Nomeie funções utilizando snake_case. Exemplo: calculate_total
- Classes: Utilize PascalCase (cada palavra começa com letra maiúscula, sem separadores). Exemplo: UserProfile
- Nomes de Arquivos: Use snake_case.py. Exemplo: data_parser.py

### Estrutura do Módulo Back-end FastAPI
Para a organização de projetos backend em Python utilizando FastAPI, recomenda-se a seguinte estrutura de diretórios para modularização e separação de responsabilidades:

#### Models
- Função: Define os modelos de dados da aplicação, representando a estrutura das tabelas do banco de dados e suas relações. Geralmente, contém classes que mapeiam para o banco de dados através de um ORM(Object-Relational Mapper), como SQLAlchemy, e são usadas pelos services para interagir com o banco.
- Conteúdo Típico: Arquivos Python definindo classes que representam entidades do sistema (ex: user_model.py, product_model.py).