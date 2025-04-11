# Plataforma Kituroish

**Kituroish** é uma plataforma fictícia de autenticação de usuários, que permite criar ou logar em uma conta para realizar pedidos com qualidade e segurança. O objetivo do projeto é simular um gerenciamento de produto e qualidade utilizando ferramentas como Jira, Miro e GitHub.

## Objetivos
- Criar um fluxo de gerenciamento com ferramentas ágeis
- Documentar o fluxo e modelo de tarefas
- Criar testes com Zephyr Scale (Jira)

- # Fluxo de Trabalho

Este é o fluxo básico da plataforma Kituroish, conforme desenhado no Miro:

1. Usuário acessa a plataforma
2. Escolhe entre "Entrar" ou "Inscrever-se"
3. Ao entrar:
   - Insere email e senha
   - É redirecionado para a área de pedidos
4. Ao se inscrever:
   - Insere nome, email, senha, confirma senha
   - Recebe acesso à plataforma

No perfil, o usuário pode acompanhar o andamento das suas compras.

Ferramentas utilizadas:
- **Miro**: Diagrama do fluxo de usuário
- **Jira**: Gerenciamento de tarefas e testes

# Template de Tarefa - Kituroish

**Título da Tarefa:** [Funcionalidade: Login de Usuário]

**Descrição:** Criar página de login com campos de email e senha, além de validações.

**Checklist:**
- [ ] Campo de email
- [ ] Campo de senha
- [ ] Botão de login
- [ ] Redirecionamento após login

**Prioridade:** Alta  
**Responsável:** @equipeKituroish  
**Status:** Em andamento

 Casos de Teste - Zephyr Scale (Jira)

## 🔹 Step-by-Step

**Caso 1:** Login com sucesso  
**Passos:**
1. Acessar site
2. Clicar em “Entrar”
3. Inserir email válido
4. Inserir senha válida
5. Clicar em “Entrar”  
**Resultado esperado:** Redirecionar para tela inicial

**Caso 2:** Inscrição com sucesso  
**Passos:**
1. Acessar site
2. Clicar em “Inscrever-se”
3. Preencher nome, email, senha, confirmar senha
4. Clicar em “Registrar”  
**Resultado esperado:** Conta criada e redirecionamento

# Casos de Teste - Zephyr Scale (Jira)

## 🔹 Step-by-Step

**Caso 1:** Login com sucesso  
**Passos:**
1. Acessar site
2. Clicar em “Entrar”
3. Inserir email válido
4. Inserir senha válida
5. Clicar em “Entrar”  
**Resultado esperado:** Redirecionar para tela inicial

**Caso 2:** Inscrição com sucesso  
**Passos:**
1. Acessar site
2. Clicar em “Inscrever-se”
3. Preencher nome, email, senha, confirmar senha
4. Clicar em “Registrar”  
**Resultado esperado:** Conta criada e redirecionamento

---

## 🔹 BDD

```gherkin
Funcionalidade: Login de usuário

Cenário: Login com credenciais válidas
Dado que o usuário está na página de login
Quando insere email e senha corretos
Então ele deve acessar a área de pedidos
gherkin
Copiar
Editar

Funcionalidade: Cadastro de usuário

Cenário: Cadastro com dados válidos
Dado que o usuário está na página de cadastro
Quando preenche os campos corretamente
E clica em "Registrar"
Então a conta deve ser criada com sucesso
---
