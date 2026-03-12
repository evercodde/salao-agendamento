# 🤝 Contribuindo com o Projeto

Obrigado por contribuir com o **Sistema de Agendamento para Salão de Cabeleireiro**.

Este documento descreve como colaborar com o desenvolvimento do projeto.

---

# 📌 Objetivo do Projeto

Este projeto tem como objetivo desenvolver um **MVP funcional de sistema de agendamento para salão de beleza**, utilizando tecnologias web modernas.

O sistema permite:

* visualização de portfólio
* agendamento online
* gestão de agenda pela empreendedora

---

# 🧭 Fluxo de Desenvolvimento

O desenvolvimento segue o fluxo:

```
main → develop → feature/*
```

### Branches

**main**

* versão estável
* pronta para produção

**develop**

* integração das novas funcionalidades

**feature/**

* desenvolvimento de funcionalidades específicas

Exemplo:

```
feature/agendamento-online
feature/painel-admin
feature/portfolio
```

---

# 🛠 Processo de Contribuição

### 1️⃣ Criar uma branch

```
git checkout develop
git checkout -b feature/nome-da-feature
```

---

### 2️⃣ Desenvolver a funcionalidade

* seguir estrutura do projeto
* manter código organizado
* usar nomes claros

---

### 3️⃣ Fazer commit

Padrão de commit:

```
tipo: descrição curta
```

Exemplos:

```
feat: adicionar página de agendamento
fix: corrigir cálculo de horários disponíveis
style: ajustar layout do portfólio
```

---

### 4️⃣ Enviar para o repositório

```
git push origin feature/nome-da-feature
```

---

### 5️⃣ Abrir Pull Request

Criar um **Pull Request para a branch `develop`**.

Descrever:

* funcionalidade implementada
* arquivos alterados
* possíveis impactos

---

# 📂 Estrutura do Projeto

```
frontend
│
├── components
├── pages
├── services
├── hooks
└── utils

database
│
├── schema.sql
└── seeds.sql

docs
```

---

# 🧪 Testes

Antes de enviar código:

* verificar se o projeto roda localmente
* validar fluxo principal de agendamento
* verificar se não há erros no console

---

# 📋 Boas Práticas

* código simples e legível
* nomes claros de variáveis
* componentes reutilizáveis
* evitar duplicação de código

---

# 📣 Comunicação

Qualquer dúvida ou sugestão pode ser discutida através de:

* Issues do GitHub
* Discussões da equipe

---

Obrigado por contribuir com o projeto 🚀
