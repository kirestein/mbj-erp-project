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
- [ ] Endpoint responde com status 200
- [ ] Response contém `status: "ok"`
- [ ] Response contém timestamp válido
- [ ] Headers corretos (Content-Type: application/json)

#### 🔍 Rota POST /employees
**Cenários Positivos:**
- [ ] Cadastro com dados válidos + imagem JPG
- [ ] Cadastro com dados válidos + imagem PNG
- [ ] Verificar persistência no banco
- [ ] Verificar upload no Cloudinary
- [ ] Response 201 Created com dados corretos

**Cenários Negativos:**
- [ ] Sem campo obrigatório (fullName)
- [ ] Sem campo obrigatório (jobFunctions)
- [ ] Sem arquivo de imagem
- [ ] Formato de arquivo inválido (PDF, TXT)
- [ ] Arquivo muito grande (> 10MB)

**Validações Técnicas:**
- [ ] Headers multipart/form-data aceitos
- [ ] Logs detalhados funcionando
- [ ] Tratamento de erro do Cloudinary
- [ ] Tratamento de erro do PostgreSQL
- [ ] Códigos de status corretos (400, 409, 500)

#### 🔍 Rota GET /employees
- [ ] Response básico funcionando
- [ ] Estrutura para listagem futura

### 🛠 Próximos Passos de Teste
1. **Configurar ambiente local** - Instalar dependências
2. **Criar .env de teste** - Configurar variáveis
3. **Testar health-check** - Validar servidor funcionando
4. **Testar POST /employees** - Cenários completos
5. **Documentar resultados** - Atualizar tracking

### 📝 Observações Técnicas
- **Stack confirmada:** Fastify + PostgreSQL + Cloudinary + Puppeteer
- **Validações implementadas:** Campos obrigatórios, tipos de arquivo
- **Logs detalhados:** Facilitam debugging
- **Error handling:** Códigos HTTP apropriados
- **Multipart:** Configurado para uploads até 10MB

