# Avaliação — Engenharia de Software

**Sistema Integrado de Gestão de Farmácia — MVP**

Aluno: Grazielly Zambello Fuzato

RA: 24000211

Data: 26/03/2026

---

# 1. Definição do MVP

Neste trabalho, o MVP foi focado no processo de venda de uma farmácia, que é a principal atividade do sistema.

A ideia foi incluir apenas o essencial para que uma venda aconteça do início ao fim, sem entrar em partes mais complexas do sistema.

### O que está dentro do MVP:

* Cadastro de cliente
* Consulta de produtos
* Verificação de estoque
* Realização da venda
* Finalização da venda
* Atualização do estoque
* Geração de contas a receber (quando a venda é a prazo)
* Emissão de comprovante
* Validação de receita (quando necessário)

### O que ficou fora do MVP:

* Controle completo de fornecedores
* Relatórios mais avançados
* Controle financeiro detalhado
* Integração com outros sistemas

### Justificativa:

Escolhi esse recorte porque a venda é o processo mais importante da farmácia. Garantindo que isso funcione bem, o sistema já atende a necessidade principal do negócio.

---

# 2. Regras de Negócio

**RN01 —** Não é permitido vender produtos sem estoque.

**RN02 —** Toda venda deve atualizar o estoque automaticamente.

**RN03 —** Vendas a prazo devem gerar contas a receber.

**RN04 —** Para vender a prazo, o cliente precisa estar cadastrado.

**RN05 —** Produtos controlados precisam de validação do farmacêutico.

**RN06 —** O sistema deve avisar quando o estoque estiver baixo.

---

# 3. Requisitos Funcionais

**RF01 —** Cadastrar clientes

**RF02 —** Consultar clientes

**RF03 —** Consultar produtos

**RF04 —** Verificar estoque

**RF05 —** Realizar venda

**RF06 —** Finalizar venda

**RF07 —** Gerar contas a receber

**RF08 —** Emitir comprovante

**RF09 —** Validar receita

---

# 🛡 4. Requisitos Não Funcionais

**RNF01 —** O sistema deve estar disponível na maior parte do tempo (mínimo 99%).

**RNF02 —** As operações devem ser rápidas (até 2 segundos).

**RNF03 —** Deve haver login e controle de acesso.

**RNF04 —** Os dados não podem ficar inconsistentes.

**RNF05 —** A interface deve ser fácil de usar.

---

# 5. Casos de Uso

Casos considerados no sistema:

* UC01 — Realizar Venda
* UC02 — Registrar Cliente
* UC03 — Consultar Produto
* UC04 — Validar Receita
* UC05 — Finalizar Venda
* UC06 — Atualizar Estoque
* UC07 — Gerar Contas a Receber
* UC08 — Emitir Comprovante
* UC09 — Verificar Estoque
* UC10 — Autenticar Usuário

### Relacionamentos

**Include:**

* Realizar Venda inclui Consultar Produto
* Realizar Venda inclui Finalizar Venda
* Finalizar Venda inclui Emitir Comprovante

**Extend:**

* Validar Receita estende Realizar Venda
* Registrar Cliente estende Realizar Venda
* Gerar Contas a Receber estende Finalizar Venda

📌 Inserir aqui o diagrama de casos de uso.

---

# 6. Documentação dos Casos de Uso

---

## UC01 — Realizar Venda

**Ator:** Atendente
**Descrição:** Processo de venda de produtos ao cliente.
**Pré-condição:** Usuário logado no sistema.
**Pós-condição:** Venda registrada.

### Fluxo Principal

1. Iniciar venda
2. Informar produto
3. Sistema verifica estoque
4. Informar quantidade
5. Sistema calcula valor

### Fluxos Alternativos

* Produto sem estoque → venda não é realizada
* Cliente não cadastrado → precisa cadastrar

### Relacionamentos

* Include: Consultar Produto, Finalizar Venda
* Extend: Validar Receita

📌 Inserir diagrama de atividade

---

## UC02 — Registrar Cliente

**Ator:** Atendente

### Fluxo Principal

1. Informar dados
2. Salvar cadastro

---

## UC03 — Consultar Produto

**Ator:** Atendente

### Fluxo Principal

1. Buscar produto
2. Exibir resultado

---

## UC04 — Validar Receita

**Ator:** Farmacêutico

### Fluxo Principal

1. Analisar receita
2. Aprovar ou reprovar

---

## UC05 — Finalizar Venda

**Ator:** Atendente

### Fluxo Principal

1. Escolher pagamento
2. Confirmar venda

---

## UC06 — Atualizar Estoque

**Ator:** Sistema

### Fluxo Principal

1. Atualizar quantidade

---

## UC07 — Gerar Contas a Receber

**Ator:** Sistema

### Fluxo Principal

1. Registrar valor

---

## UC08 — Emitir Comprovante

**Ator:** Sistema

### Fluxo Principal

1. Gerar comprovante

---

## UC09 — Verificar Estoque

**Ator:** Sistema

### Fluxo Principal

1. Consultar estoque

---

## UC10 — Autenticar Usuário

**Ator:** Usuário

### Fluxo Principal

1. Inserir login
2. Acessar sistema

---
