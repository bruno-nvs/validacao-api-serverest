# Automação de API - ServeRest

Projeto de automação de testes de API utilizando a plataforma ServeRest, com foco na validação de autenticação, manipulação de dados e integração contínua.

---

## Objetivo

Validar operações essenciais de backend através de testes automatizados:

- Consulta de produtos
- Autenticação de usuário
- Cadastro de produtos autenticados

---

## Tecnologias Utilizadas

- Postman
- Newman
- Newman Reporter HTML Extra
- GitHub Actions

---

## Cenários Automatizados

### Consulta de Produtos
- Requisição GET para listagem de produtos
- Validação de status code
- Validação da estrutura de resposta da API

### Autenticação
- Login com credenciais válidas
- Captura automática do token JWT
- Armazenamento do token em variável de ambiente

### Cadastro de Produto
- Requisição POST autenticada via Bearer Token
- Utilização dinâmica do token obtido no login
- Validação da criação do recurso

---

## Integração Contínua (CI)

O projeto possui pipeline automatizada utilizando GitHub Actions.

A cada novo push ou pull request na branch `main`, o fluxo executa automaticamente:

1. Configuração do ambiente Ubuntu
2. Instalação do Node.js
3. Instalação das dependências do projeto
4. Execução da suíte de testes automatizados
5. Geração do relatório HTML
6. Publicação do relatório como artifact no GitHub Actions

---

## Estrutura do Projeto

```txt
.
├── serverest.json
├── README.md
└── .github
    └── workflows
