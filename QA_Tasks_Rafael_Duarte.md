# 🧪 QA Backend Tasks - Rafael Duarte

## 📋 Status das Sprints

### 🟨 Sprint 0: Setup de Infraestrutura (05-07 junho)
**Status:** 🔄 Em andamento

#### Preparação QA
- [ ] Configurar ambiente de testes local
- [ ] Estudar documentação dos endpoints planejados
- [ ] Preparar templates de teste para API REST
- [ ] Configurar Postman/Insomnia collections
- [ ] Definir estratégia de testes com Mariana Alves

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

