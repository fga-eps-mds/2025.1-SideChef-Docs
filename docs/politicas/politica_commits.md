## Histórico de versões

| Versão | Alteração       | Responsável         | Data Alteração |
|--------|-----------------|---------------------|----------------|
| 1.0    | Criação do documento de política de commits  | Diógenes Dantas Lélis Júnior | 16/04/2025 |
| 1.1    | Adição das políticas de commits: elementos estruturais e exemplos   | Diógenes Dantas Lélis Júnior | 17/04/2025 |

## Política de Commits

No projeto será utilizado o Padrão de [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/). 

A especificação do Conventional Commits é uma convenção simples para utilizar nas mensagens de commit. Ela define um conjunto de regras para criar um histórico de commit explícito, o que facilita a criação de ferramentas automatizadas baseadas na especificação. Esta convenção se encaixa com o SemVer, descrevendo os recursos, correções e modificações que quebram a compatibilidade nas mensagens de commit.

A mensagem do commit deve seguir a seguinte estrutura

```
<tipo>[escopo opcional]: <descrição>

[corpo opcional]

[rodapé(s) opcional(is)]
```

### Elementos Estruturais dos Commits

- fix: um commit do tipo fix soluciona um problema na sua base de código (isso se correlaciona com PATCH do versionamento semântico).

- feat: um commit do tipo feat inclui um novo recurso na sua base de código (isso se correlaciona com MINOR do versionamento semântico).

- BREAKING CHANGE: um commit que contém no rodapé opcional o texto BREAKING CHANGE:, ou contém o símbolo ! depois do tipo/escopo, introduz uma modificação que quebra a compatibilidade da API (isso se correlaciona com MAJOR do versionamento semântico). Uma BREAKING CHANGE pode fazer parte de commits de qualquer tipo.

- Outros tipos adicionais são permitidos além de fix: e feat:, por exemplo @commitlint/config-conventional (baseado na Convenção do Angular) recomenda-se build:, chore:, ci:, docs:, style:, refactor:, perf:, test:, entre outros.

### Exemplos

Mensagem de commit com descrição e modificação que quebra a compatibilidade no rodapé
```
feat: permitir que o objeto de configuração fornecido estenda outras configurações
BREAKING CHANGE: a chave `extends`, no arquivo de configuração, agora é utilizada para estender outro arquivo de configuração
```

Mensagem de commit com ! para chamar a atenção para quebra a compatibilidade
```
feat!: envia email para o cliente quando o produto é enviado
```

Mensagem de commit com escopo e ! para chamar a atenção para quebra a compatibilidade
```
feat(api)!: envia email para o cliente quando o produto é enviado
```

Mensagem de commit com ! e BREAKING CHANGE no rodapé
```
chore!: remove suporte para Node 6
BREAKING CHANGE: refatorar para usar recursos do JavaScript não disponíveis no Node 6.
```

Mensagem de commit sem corpo
```
docs: ortografia correta de CHANGELOG
```

Mensagem de commit com escopo
```
feat(lang): adiciona tradução para português brasileiro
```


