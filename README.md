# EBAC-SHOP — Especificação de Cenários BDD

## 📌 Sobre o Projeto
Este repositório contém a documentação viva dos cenários de teste em **Behavior-Driven Development (BDD)** para a plataforma e-commerce **EBAC-SHOP**. Os ficheiros estão escritos na sintaxe **Gherkin** (`.feature`) e definem os requisitos funcionais, critérios de aceite e regras de negócio do sistema.

---

## 📋 Funcionalidades Mapeadas

### 1. Tela de Cadastro / Checkout (`checkout.feature`)
Garante a validação dos dados de registo do cliente para conclusão da compra.
* **Validação de Formato de E-mail**: Impede o registo com e-mails num formato inválido e exibe a mensagem `"e-mail inválido"`.
* **Campos Obrigatórios Em Branco**: Exibe a mensagem de alerta `"campo sem preenchimento"` ao tentar submeter o formulário sem preencher os campos obrigatórios.
* **Cadastro com Sucesso (Esquema do Cenário)**: Valida a conclusão de registo para múltiplos utilizadores com dados válidos marcados com asteriscos.

### 2. Login na Plataforma (`login.feature`)
Define as regras de autenticação de utilizadores na plataforma.
* **Autenticação com Sucesso**: Valida o direcionamento para a tela de checkout após introdução de credenciais válidas.
* **Credenciais Inválidas**: Exibe a mensagem de alerta `"Usuário ou senha inválidos"` quando introduzido um utilizador ou palavra-passe incorreta.

### 3. Configurar Produto (`config.feature`)
Regula a seleção e personalização de artigos antes da adição ao carrinho.
* **Seleção Obrigatória**: Obriga a escolha de cor, tamanho e quantidade para que as opções sejam exibidas.
* **Limite de Quantidade por Venda**: Restringe a compra a um máximo de 10 unidades por venda, exibindo a mensagem `"Permitido comprar até 10 produtos"` caso o limite seja ultrapassado.
* **Limpeza de Seleção**: Valida se o botão "limpar" restaura os campos de seleção ao seu estado original/em branco.

---

## 💡 Objetivos da Documentação
* **Fonte Única da Verdade**: Alinhar os requisitos funcionais entre equipas de produto, desenvolvimento e garantia de qualidade (QA).
* **Critérios de Aceite Claros**: Facilitar a validação visual e funcional das histórias de utilizador.
* **Pronto para Automação**: Estruturado em sintaxe Gherkin (`.feature`) padrão para futura integração com frameworks como Cucumber.
