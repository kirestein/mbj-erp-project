# 🟨 Sprint 0: Setup de Infraestrutura e Ambientes (05 a 07 de junho)

## 🎯 Objetivos
Configurar toda a infraestrutura necessária para o desenvolvimento do projeto, incluindo repositórios, ambientes de desenvolvimento, CI/CD e documentação inicial.

## 📋 Tarefas Backend (Carlos)

### ✅ Criar repositório `maple-erp-backend`
- **Status**: Concluído
- **Responsável**: Carlos
- **Link**: [https://github.com/kirestein/maple-erp-backend](https://github.com/kirestein/maple-erp-backend)

### ✅ Setup inicial com Fastify, PostgreSQL, Cloudinary
- **Status**: Concluído
- **Responsável**: Carlos
- **Detalhes**:
  - Fastify configurado com plugins necessários (@fastify/cors, @fastify/multipart)
  - PostgreSQL configurado no Neon (alternativa ao Railway)
  - Cloudinary integrado para armazenamento de imagens
  - Estrutura de pastas organizada (src/routes, src/config)

### ✅ Criar `.env.example`
- **Status**: Concluído
- **Responsável**: Carlos
- **Detalhes**: Arquivo criado com placeholders para todas as variáveis de ambiente necessárias

### ✅ Setup GitHub Actions (CI/CD)
- **Status**: Concluído
- **Responsável**: Carlos
- **Detalhes**:
  - Workflow configurado para lint, build e testes
  - Preparado para deploy automático (comentado até estar pronto)
  - Badge de status adicionado ao README

### ✅ Implementar endpoint POST /employees
- **Status**: Concluído (adiantado da Sprint 1)
- **Responsável**: Carlos
- **Detalhes**:
  - Endpoint implementado com validação de campos
  - Upload de imagem para Cloudinary funcionando
  - Persistência no banco de dados Neon
  - Tratamento de erros implementado

### ✅ Configurar deploy no Render
- **Status**: Concluído
- **Responsável**: Carlos
- **Detalhes**:
  - Arquivo render.yaml criado
  - Instruções de deploy documentadas
  - Configuração de variáveis de ambiente

### 🔄 Documentar backend no Notion
- **Status**: Pendente
- **Responsável**: Carlos
- **Detalhes**: Será concluído após validação do deploy

## 📋 Tarefas Frontend (Manus)

### 🔄 Criar repositório `maple-erp-frontend`
- **Status**: Pendente
- **Responsável**: Manus

### 🔄 Setup Angular CLI + Angular Material
- **Status**: Pendente
- **Responsável**: Manus

### 🔄 Conectar com Netlify
- **Status**: Pendente
- **Responsável**: Manus

### 🔄 Setup GitHub Actions
- **Status**: Pendente
- **Responsável**: Manus

### 🔄 Criar estrutura de módulos e serviços iniciais
- **Status**: Pendente
- **Responsável**: Manus

### 🔄 Documentar front no Notion
- **Status**: Pendente
- **Responsável**: Manus

## 📊 Métricas da Sprint
- **Tarefas Backend Concluídas**: 6/7 (85.7%)
- **Tarefas Frontend Iniciadas**: 0/6 (0%)
- **Total da Sprint**: 6/13 (46.2%)

## 🚀 Próximos Passos
- Concluir documentação no Notion
- Iniciar desenvolvimento do frontend
- Preparar para Sprint 1 (Cadastro de Funcionários e Crachás)
