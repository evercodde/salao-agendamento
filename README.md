# 💇‍♀️ Sistema de Agendamento para Salão de Cabeleireiro

Sistema web **mobile-first** para gestão de agenda, portfólio de serviços e agendamento online de um salão especializado em **tranças, tratamentos capilares e mega hair**.

O projeto foi desenvolvido seguindo um fluxo estruturado de **Product Discovery e Engenharia de Software**, com foco na construção de um **MVP funcional** que resolva problemas reais da empreendedora parceira.

---

# 📌 Objetivo do Projeto

Criar uma plataforma simples e eficiente que permita:

### Para clientes

* visualizar portfólio de trabalhos
* conhecer serviços disponíveis
* realizar agendamentos online
* descrever o serviço desejado antes do atendimento

### Para a empreendedora

* centralizar a agenda
* evitar conflitos de horário
* organizar serviços oferecidos
* manter um portfólio atualizado
* reduzir trabalho manual via WhatsApp

---

# 🧩 Problema Identificado

A empreendedora atualmente gerencia seus atendimentos usando:

* WhatsApp
* agenda manual
* um sistema pago limitado

Isso gera problemas como:

* conflitos de horário
* dificuldade de organização da agenda
* ausência de portfólio digital estruturado
* trabalho manual excessivo
* risco de no-show de clientes

---

# 🚀 Proposta de Solução

Criar um **sistema web mobile-first** que centralize:

* portfólio de serviços
* agendamento online
* gestão da agenda
* organização de serviços

O sistema foi planejado para evoluir futuramente para:

* automação de WhatsApp com IA
* histórico capilar das clientes
* plataforma de gestão para salões

---

# 🏗 Arquitetura do Sistema

Arquitetura moderna baseada em aplicações web desacopladas.

```
Frontend (React + Vite + Tailwind)
        │
        ▼
Supabase (API + Auth + Storage)
        │
        ▼
PostgreSQL (Banco de Dados)
```

Futuras integrações:

```
n8n / Zapier
        │
        ▼
WhatsApp API
        │
        ▼
Envio automático de lembretes
```

---

# 🧪 Escopo do MVP

Funcionalidades que fazem parte do MVP:

1. Portfólio público de serviços
2. Cadastro de serviços
3. Agendamento online
4. Cálculo automático de horários disponíveis
5. Painel administrativo com agenda

Funcionalidades futuras:

* lembretes automáticos via WhatsApp
* integração com Google Agenda
* IA para atendimento automático
* histórico capilar
* passaporte capilar

---

# 👥 Usuários do Sistema

## Cliente

Pode:

* visualizar portfólio
* escolher serviços
* agendar horários
* descrever o atendimento desejado

## Empreendedora (Admin)

Pode:

* cadastrar serviços
* gerenciar agenda
* visualizar agendamentos
* gerenciar portfólio

---

# 🗂 Estrutura do Repositório

```
.
├── docs
│   ├── 01_ideia_produto.md
│   ├── 02_product_discovery.md
│   ├── 03_visao_produto.md
│   ├── 04_mvp_escopo.md
│   ├── 05_product_backlog.md
│   ├── 06_modelo_dominio.md
│   ├── 07_modelo_dados.md
│   ├── 08_regras_negocio.md
│   ├── 09_arquitetura_sistema.md
│   ├── 10_prompt_lovable.md
│   └── 11_diagramas_sistema.md
│
├── database
│   ├── schema.sql
│   └── seeds.sql
│
├── frontend
│   └── aplicação React
│
└── README.md
```

---

# 🛠 Tecnologias Utilizadas

Frontend

* React
* Vite
* TailwindCSS

Backend / Infraestrutura

* Supabase
* PostgreSQL

Automação (futuro)

* n8n
* WhatsApp API

---

# ⚙️ Como Executar o Projeto

### 1️⃣ Clonar o repositório

```
git clone <url-do-repositorio>
cd salao-agendamento
```

---

### 2️⃣ Instalar dependências

```
cd frontend
npm install
```

---

### 3️⃣ Configurar Supabase

Criar um projeto em **Supabase** e obter:

* SUPABASE_URL
* SUPABASE_ANON_KEY

Criar arquivo:

```
src/services/supabaseClient.js
```

---

### 4️⃣ Criar banco de dados

Executar no Supabase SQL Editor:

```
database/schema.sql
```

---

### 5️⃣ Rodar aplicação

```
npm run dev
```

---

# 📊 Fluxo do Usuário

```
Cliente acessa o site
        │
        ▼
Visualiza portfólio
        │
        ▼
Escolhe serviço
        │
        ▼
Seleciona data
        │
        ▼
Seleciona horário disponível
        │
        ▼
Confirma agendamento
        │
        ▼
Agendamento salvo no banco
```

---

# 📈 Roadmap do Projeto

### Fase 1

Portfólio + painel admin

### Fase 2

Agendamento online + agenda administrativa

### Fase 3

Automação WhatsApp

### Fase 4

Assistente capilar com IA

### Fase 5

Passaporte capilar digital

---

# 📚 Metodologia Utilizada

O projeto foi desenvolvido seguindo o fluxo:

```
Ideia
↓
Product Discovery
↓
Documentação
↓
Prompt para geração de sistema
↓
Protótipo
↓
Implementação
```

---

# 👨‍💻 Equipe

Projeto desenvolvido por estudantes de Engenharia de Software em parceria com uma empreendedora do setor de beleza.

Integrantes da equipe:

* A preencher

---

# 📄 Licença

Projeto acadêmico desenvolvido para fins educacionais.
