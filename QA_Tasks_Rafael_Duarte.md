# 🧪 QA Backend Tasks - Rafael Duarte

## 📋 Status das Sprints

### 🟨 Sprint 0: Setup de Infraestrutura (05-07 junho)
**Status:** 🔄 Em andamento

#### Preparação QA
- [x] Configurar ambiente de testes local
- [x] Estudar documentação dos endpoints planejados
- [x] Preparar templates de teste para API REST
- [ ] Configurar Postman/Insomnia collections
- [ ] Definir estratégia de testes com Mariana Alves

#### ✅ Backend Analisado (Carlos)
- [x] Estrutura base Fastify configurada
- [x] Rota `GET /health-check` implementada
- [x] Rota `POST /employees` implementada
- [x] Rota `GET /employees` (teste básico)
- [x] Configuração Cloudinary e PostgreSQL
- [x] Validação de campos obrigatórios
- [x] Upload de imagens (JPEG/PNG)
- [x] Tratamento de erros básico

---

### 🟩 Sprint 1: Cadastro de Funcionários e Crachás (10-14 junho)
**Status:** 📅 Planejada

#### Endpoints para Testar

##### 📝 POST `/employees`
**Prioridade:** 🔴 Alta

**Cenários de Teste:**
- [ ] ✅ Cadastro válido com todos os campos obrigatórios
- [ ] ✅ Upload de imagem válida (JPG, PNG)
- [ ] ❌ Payload sem campos obrigatórios
- [ ] ❌ Upload de arquivo inválido (PDF, TXT, etc.)
- [ ] ❌ Imagem muito grande (> limite definido)
- [ ] ❌ Dados inválidos (email malformado, etc.)
- [ ] 🔍 Verificar persistência no PostgreSQL
- [ ] 🔍 Verificar upload no Cloudinary
- [ ] ⚡ Performance (< 2s para upload)

**Validações Técnicas:**
- [ ] Status Code: 201 Created
- [ ] Headers: Content-Type application/json
- [ ] Response body contém ID do funcionário
- [ ] Logs no Railway sem erros
- [ ] Imagem acessível via URL do Cloudinary

##### 📄 GET `/employees/:id/badge`
**Prioridade:** 🔴 Alta

**Cenários de Teste:**
- [ ] ✅ Gerar crachá para funcionário existente
- [ ] ❌ ID inexistente (404)
- [ ] ❌ ID inválido (formato incorreto)
- [ ] 🔍 Verificar conteúdo do PDF gerado
- [ ] 🔍 Verificar formatação e layout
- [ ] ⚡ Performance (< 3s para geração)

**Validações Técnicas:**
- [ ] Status Code: 200 OK
- [ ] Headers: Content-Type application/pdf
- [ ] PDF válido e abrível
- [ ] Dados corretos no crachá (nome, foto, etc.)
- [ ] Puppeteer funcionando corretamente

---

### 🟦 Sprint 2: Documentos e Checklists (17-21 junho)
**Status:** 📅 Futura

#### Endpoints Planejados
- [ ] GET `/employees/:id/document` (PDF contábil)
- [ ] GET `/employees/:id/checklist-entry`
- [ ] GET `/employees/:id/checklist-exit`
- [ ] GET `/employees` (listagem com filtros)

---

## 🛠 Ferramentas de Teste

### Configuradas
- [ ] Postman Collection para endpoints
- [ ] Insomnia Workspace
- [ ] Newman para testes automatizados
- [ ] Acesso ao Railway (logs e DB)
- [ ] Acesso ao Cloudinary (verificar uploads)

### Pendentes
- [ ] Jest + Supertest (testes automatizados)
- [ ] Sentry (monitoramento de erros)
- [ ] GitHub Actions (CI/CD)

---

## 📊 Métricas de Qualidade

### Critérios de Aceitação
- ✅ **Cobertura de testes:** > 80%
- ✅ **Performance API:** < 2s por endpoint
- ✅ **Uptime:** > 99%
- ✅ **Logs limpos:** Sem erros críticos

### Cenários Críticos
1. **Upload de imagem + persistência** (fluxo completo)
2. **Geração de PDF** (Puppeteer + dados corretos)
3. **Validação de dados** (campos obrigatórios)
4. **Tratamento de erros** (responses adequados)

---

## 🚨 Issues Encontradas

### 🐛 Bugs Reportados
*Nenhum bug reportado ainda*

### ⚠️ Melhorias Sugeridas
*Aguardando início dos testes*

---

## 📝 Notas e Observações

- **Lema:** "Se algo pode dar errado, eu vou testar esse caminho primeiro."
- **Foco:** Cenários de borda e validação rigorosa
- **Comunicação:** Alinhamento constante com Carlos (Backend) e Mariana (PO)

---

**Última atualização:** 06/06/2025  
**Próxima revisão:** Início da Sprint 1 (10/06)



---

## 🧪 Testes Iniciais - Validação do Backend

### 📋 Checklist de Validação Imediata

#### 🔍 Rota GET /health-check
- [x] Endpoint responde com status 200
- [x] Response contém `status: "ok"`
- [x] Response contém timestamp válido
- [x] Headers corretos (Content-Type: application/json)
- [x] CORS habilitado (access-control-allow-origin: *)
- [x] Tempo de resposta < 1s

**✅ Resultado:** PASSOU - Health check funcionando perfeitamente

#### 🔍 Rota POST /employees
**Cenários Positivos:**
- [ ] Cadastro com dados válidos + imagem JPG (⚠️ Bloqueado - credenciais)
- [ ] Cadastro com dados válidos + imagem PNG (⚠️ Bloqueado - credenciais)
- [ ] Verificar persistência no banco (⚠️ Bloqueado - credenciais)
- [ ] Verificar upload no Cloudinary (⚠️ Bloqueado - credenciais)
- [ ] Response 201 Created com dados corretos (⚠️ Bloqueado - credenciais)

**Cenários Negativos:**
- [x] Sem campo obrigatório (fullName) - ✅ 400 Bad Request
- [x] Sem campo obrigatório (jobFunctions) - ✅ 400 Bad Request  
- [x] Sem arquivo de imagem - ✅ 400 Bad Request
- [x] Formato de arquivo inválido (TXT) - ✅ 400 Bad Request
- [ ] Arquivo muito grande (> 10MB)

**Validações Técnicas:**
- [x] Headers multipart/form-data aceitos - ✅ Funcionando
- [x] Logs detalhados funcionando - ✅ Visíveis nos testes
- [ ] Tratamento de erro do Cloudinary (⚠️ Credenciais inválidas)
- [ ] Tratamento de erro do PostgreSQL (⚠️ Credenciais inválidas)
- [x] Códigos de status corretos (400) - ✅ Validações OK
- [x] Mensagens de erro claras - ✅ Específicas e úteis

**🐛 Bugs/Melhorias Identificados:**
- ❌ Content-Type JSON retorna 500 (deveria ser 400)
- ⚠️ Credenciais de teste impedem testes de integração
- ✅ Validações de campo funcionando perfeitamente

#### 🔍 Rota GET /employees
- [x] Response básico funcionando
- [x] Status 200 OK
- [x] Message: "GET /employees works!"
- [x] Estrutura para listagem futura

**✅ Resultado:** PASSOU - Endpoint básico funcionando

### 🛠 Próximos Passos de Teste
1. **Configurar ambiente local** - ✅ Concluído
2. **Criar .env de teste** - ✅ Concluído
3. **Testar health-check** - ✅ Concluído
4. **Testar POST /employees** - 🔄 Em andamento
5. **Documentar resultados** - 🔄 Em andamento

### 📊 Ambiente de Teste Configurado
- **Servidor:** Rodando na porta 4000 ✅
- **Dependências:** Instaladas com sucesso ✅
- **Health Check:** Funcionando perfeitamente ✅
- **GET /employees:** Endpoint básico OK ✅
- **Próximo:** Testes de POST /employees com upload

### 📝 Observações Técnicas
- **Stack confirmada:** Fastify + PostgreSQL + Cloudinary + Puppeteer
- **Validações implementadas:** Campos obrigatórios, tipos de arquivo
- **Logs detalhados:** Facilitam debugging
- **Error handling:** Códigos HTTP apropriados
- **Multipart:** Configurado para uploads até 10MB



---

## 🚨 Issues Encontradas - Atualização

### 🐛 Bug #001: Content-Type Incorreto
**Descrição:** Endpoint POST /employees retorna 500 quando recebe Content-Type application/json ao invés de multipart/form-data

**Comportamento Atual:**
- Request: `Content-Type: application/json`
- Response: `500 Internal Server Error`

**Comportamento Esperado:**
- Response: `400 Bad Request` com mensagem explicativa sobre multipart/form-data

**Prioridade:** 🟡 Média (melhoria de UX)

### ⚠️ Bloqueio #001: Credenciais de Integração
**Descrição:** Testes de integração (Cloudinary + PostgreSQL) bloqueados por credenciais inválidas

**Impacto:** 
- Não é possível testar cenários positivos completos
- Upload de imagens retorna 500
- Persistência no banco não pode ser validada

**Próximos Passos:**
- Solicitar credenciais válidas para ambiente de teste
- Ou configurar mocks para testes isolados

**Prioridade:** 🔴 Alta (bloqueia testes críticos)

### ✅ Validações Funcionando Corretamente
- Campos obrigatórios (fullName, jobFunctions)
- Validação de arquivo obrigatório
- Validação de formato de arquivo (JPEG/PNG)
- Mensagens de erro claras e específicas
- Códigos HTTP apropriados (400 Bad Request)

---

## 📊 Resumo dos Testes Realizados

### ✅ Testes Concluídos (7/12)
1. Health Check - PASSOU
2. GET /employees básico - PASSOU  
3. POST validação fullName - PASSOU
4. POST validação jobFunctions - PASSOU
5. POST validação arquivo obrigatório - PASSOU
6. POST validação formato arquivo - PASSOU
7. POST Content-Type incorreto - BUG IDENTIFICADO

### ⏳ Testes Pendentes (5/12)
1. POST com dados válidos + JPG (bloqueado)
2. POST com dados válidos + PNG (bloqueado)
3. Verificação persistência PostgreSQL (bloqueado)
4. Verificação upload Cloudinary (bloqueado)
5. Teste arquivo muito grande (>10MB)

### 🎯 Taxa de Cobertura Atual
- **Validações:** 100% testadas ✅
- **Integrações:** 0% testadas (bloqueadas) ⚠️
- **Cenários de erro:** 85% testados ✅

