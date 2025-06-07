# 📘 Projeto ERP - Escola Maple Bear Jardins

## 🔧 Repositórios

- **Frontend (Angular + Angular Material)**  
  `git@github.com:kirestein/Maple_ERP_frontend.git`

- **Backend (Node.js + Fastify)**  
  `git@github.com:kirestein/maple-erp-backend.git`

---

## 📅 Estrutura de Sprints

### 🟨 Sprint 0: Setup de Infraestrutura e Ambientes (05 a 07 de junho)

**Carlos – Backend**

- [ ] Criar repositório `maple-erp-backend`
- [ ] Setup inicial com Fastify, PostgreSQL (Railway), Cloudinary
- [ ] Criar `.env.example`
- [ ] Setup GitHub Actions (lint, build, testes)
- [ ] Documentar backend no Notion

**Manus – Frontend**

- [ ] Criar repositório `maple-erp-frontend`
- [ ] Setup Angular CLI + Angular Material
- [ ] Conectar com Netlify
- [ ] Setup GitHub Actions
- [ ] Criar estrutura de módulos e serviços iniciais
- [ ] Documentar front no Notion

---

### 🟩 Sprint 1: Cadastro de Funcionários e Crachás (10 a 14 de junho)

**Carlos – Backend**

- [ ] POST `/employees` (FormData com foto + dados)
- [ ] GET `/employees/:id/badge` (geração de PDF)
- [ ] Testes unitários e integração
- [ ] Atualização da documentação no Notion

**Manus – Frontend**

- [ ] Criar tela de cadastro
- [ ] Integração com backend (upload de imagem + dados)
- [ ] Tela de detalhes com botão "Gerar Crachá"
- [ ] Download automático de PDF

---

### 🟦 Sprint 2: Documentos Contábeis e Checklist Entrada/Saída (17 a 21 de junho)

**Carlos – Backend**

- [ ] GET `/employees/:id/document` (PDF contábil)
- [ ] GET `/employees/:id/checklist-entry`
- [ ] GET `/employees/:id/checklist-exit`
- [ ] GET `/employees` com filtro e paginação

**Manus – Frontend**

- [ ] Integração com endpoints de checklist e documento
- [ ] Layout PDF entrada/saída
- [ ] Botões de geração de PDF nas telas de funcionário

---

## 🧪 QA - Tarefas Iniciais

**Rafael Duarte – QA Backend**

- [ ] Criar plano de testes por endpoint
- [ ] Validar responses da API (`status`, headers, corpo)
- [ ] Testar integração com Cloudinary e PostgreSQL
- [ ] Validar PDFs (conteúdo, formatação, headers)

**Lívia Takeda – QA Frontend**

- [ ] Validar formulário de cadastro (UX e regras)
- [ ] Testar upload de imagem
- [ ] Validar downloads e formato dos PDFs
- [ ] Testar consistência visual com Angular Material

---

## 🧾 Templates de Issue para GitHub

### 📌 Template: Feature

```md
## ✨ Feature: [TÍTULO DA FEATURE]

**Descrição**
Descreva aqui o que precisa ser implementado e qual valor entrega.

**Critérios de Aceitação**

- [ ] ...
- [ ] ...
- [ ] ...

**Notas Técnicas**

- Rota esperada:
- Campos obrigatórios:
```

### 🐞 Template: Bug

```md
## 🐛 Bug Report: [TÍTULO DO BUG]

**Descrição do problema**
Explique o erro observado.

**Passos para reproduzir**

1. Acesse [rota/tela]
2. Faça [ação]
3. Resultado: [comportamento inesperado]

**Comportamento Esperado**
Descreva o comportamento esperado.

**Ambiente**

- Navegador/SO/Versão:
```

### ✅ Template: QA Checklist

```md
## ✅ QA Checklist: [TÍTULO DO TESTE]

**Cenário**
Descreva o contexto do teste.

**Verificações**

- [ ] Endpoint retorna 200
- [ ] Headers corretos
- [ ] Validação de campos obrigatórios
- [ ] Teste com payload inválido
- [ ] Performance adequada (< 1s)
```

---

Lembrete: gerar um novo token de acesso ao GitHub até 06/07/2025.
