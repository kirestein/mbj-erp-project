# 🟩 Sprint 1: Cadastro de Funcionários e Crachás (10 a 14 de junho)

## 🎯 Objetivos
Implementar as funcionalidades core do módulo de Gestão de Funcionários, incluindo cadastro com foto e geração de crachás em PDF.

## 📋 Tarefas Backend (Carlos)

### ✅ POST `/employees` (FormData com foto + dados)
- **Status**: Concluído (adiantado da Sprint 0)
- **Responsável**: Carlos
- **Detalhes**:
  - Endpoint implementado com validação de campos
  - Upload de imagem para Cloudinary funcionando
  - Persistência no banco de dados Neon
  - Tratamento de erros implementado

### 🔄 GET `/employees/:id/badge` (geração de PDF)
- **Status**: Pendente
- **Responsável**: Carlos
- **Detalhes**:
  - Implementar geração de PDF com Puppeteer
  - Criar template HTML para o crachá
  - Configurar headers para download do arquivo

### 🔄 Testes unitários e integração
- **Status**: Pendente
- **Responsável**: Carlos
- **Detalhes**:
  - Configurar Jest para testes
  - Implementar testes para endpoints existentes
  - Garantir cobertura mínima de código

### 🔄 Atualização da documentação no Notion
- **Status**: Pendente
- **Responsável**: Carlos
- **Detalhes**: Documentar endpoints implementados

## 📋 Tarefas Frontend (Manus)

### 🔄 Criar tela de cadastro
- **Status**: Pendente
- **Responsável**: Manus
- **Detalhes**:
  - Formulário com validação
  - Upload de imagem com preview
  - Feedback visual de sucesso/erro

### 🔄 Integração com backend (upload de imagem + dados)
- **Status**: Pendente
- **Responsável**: Manus
- **Detalhes**:
  - Serviço para comunicação com API
  - Tratamento de erros
  - Loading states

### 🔄 Tela de detalhes com botão "Gerar Crachá"
- **Status**: Pendente
- **Responsável**: Manus
- **Detalhes**:
  - Layout responsivo
  - Exibição de dados do funcionário
  - Botão para geração de crachá

### 🔄 Download automático de PDF
- **Status**: Pendente
- **Responsável**: Manus
- **Detalhes**:
  - Integração com endpoint de geração de PDF
  - Tratamento de download no navegador

## 📊 Métricas da Sprint
- **Tarefas Backend Concluídas**: 1/4 (25%)
- **Tarefas Frontend Iniciadas**: 0/4 (0%)
- **Total da Sprint**: 1/8 (12.5%)

## 🚀 Próximos Passos
- Implementar geração de crachás em PDF
- Iniciar desenvolvimento do frontend
- Preparar testes automatizados
