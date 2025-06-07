# 🧪 Checklist QA Frontend - ERP Maple Bear Jardins

## 📋 Sprint 1: Cadastro de Funcionários e Crachás

### 🔍 Tela de Cadastro de Funcionários

#### Validação de Formulário
- [ ] **Campos obrigatórios** - Verificar se todos os campos obrigatórios estão marcados com asterisco (*)
- [ ] **Validação em tempo real** - Campos mostram erro enquanto usuário digita (se aplicável)
- [ ] **Mensagens de erro claras** - Textos de erro são compreensíveis e específicos
- [ ] **Validação de CPF** - Formato correto e validação de dígitos verificadores
- [ ] **Validação de email** - Formato de email válido
- [ ] **Validação de telefone** - Formato brasileiro correto
- [ ] **Campos de data** - Formato DD/MM/AAAA e validação de datas válidas
- [ ] **Botão submit** - Só fica habilitado quando formulário está válido

#### Upload de Imagem
- [ ] **Área de upload visível** - Interface clara para upload de foto
- [ ] **Drag & drop funcional** - Usuário pode arrastar imagem para área
- [ ] **Botão de seleção** - Alternativa ao drag & drop
- [ ] **Preview da imagem** - Mostra preview após upload
- [ ] **Validação de formato** - Aceita apenas JPG, PNG, WebP
- [ ] **Validação de tamanho** - Limite máximo de arquivo (ex: 5MB)
- [ ] **Feedback de erro** - Mensagem clara quando arquivo é inválido
- [ ] **Loading state** - Indicador visual durante upload
- [ ] **Possibilidade de trocar** - Usuário pode substituir imagem selecionada

#### UX e Responsividade
- [ ] **Layout responsivo** - Funciona bem em desktop, tablet e mobile
- [ ] **Navegação por teclado** - Tab order lógico entre campos
- [ ] **Acessibilidade** - Labels associados aos inputs, contraste adequado
- [ ] **Estados de loading** - Feedback visual durante submissão
- [ ] **Confirmação de sucesso** - Mensagem clara após cadastro bem-sucedido
- [ ] **Tratamento de erro** - Feedback adequado se cadastro falhar

### 🆔 Funcionalidade de Geração de Crachá

#### Tela de Detalhes do Funcionário
- [ ] **Dados exibidos corretamente** - Todas as informações do funcionário aparecem
- [ ] **Foto do funcionário** - Imagem carregada e exibida corretamente
- [ ] **Botão "Gerar Crachá"** - Visível e bem posicionado
- [ ] **Estado do botão** - Loading durante geração do PDF

#### Download do PDF
- [ ] **Download automático** - PDF baixa automaticamente após geração
- [ ] **Nome do arquivo** - Nome descritivo (ex: cracha_joao_silva.pdf)
- [ ] **Conteúdo do PDF** - Verificar se dados estão corretos no crachá
- [ ] **Qualidade da imagem** - Foto aparece com boa resolução no PDF
- [ ] **Layout do crachá** - Design está conforme especificação
- [ ] **Tratamento de erro** - Feedback se geração falhar

---

## 📋 Sprint 2: Documentos Contábeis e Checklists

### 📄 Geração de Documentos
- [ ] **Botão documento contábil** - Visível na tela do funcionário
- [ ] **Download documento** - PDF baixa corretamente
- [ ] **Conteúdo documento** - Dados corretos e formatação adequada
- [ ] **Botão checklist entrada** - Funcional e bem posicionado
- [ ] **Botão checklist saída** - Funcional e bem posicionado
- [ ] **PDFs de checklist** - Conteúdo e layout corretos

### 📊 Lista de Funcionários
- [ ] **Exibição da lista** - Funcionários aparecem corretamente
- [ ] **Paginação** - Funciona se houver muitos registros
- [ ] **Filtros** - Se implementados, funcionam corretamente
- [ ] **Performance** - Lista carrega rapidamente
- [ ] **Links para detalhes** - Navegação para tela individual funciona

---

## 🎨 Validação Visual (Angular Material)

### Componentes UI
- [ ] **Botões** - Estilo consistente com Material Design
- [ ] **Inputs** - Aparência e comportamento padrão Material
- [ ] **Cards** - Layout e sombras corretos
- [ ] **Tipografia** - Fontes e tamanhos consistentes
- [ ] **Cores** - Paleta de cores da aplicação aplicada
- [ ] **Ícones** - Material Icons carregando corretamente
- [ ] **Espaçamentos** - Margins e paddings consistentes

### Estados Interativos
- [ ] **Hover effects** - Botões e links respondem ao hover
- [ ] **Focus states** - Elementos focáveis têm indicação visual
- [ ] **Disabled states** - Elementos desabilitados têm aparência adequada
- [ ] **Loading states** - Spinners e skeletons funcionam
- [ ] **Animações** - Transições suaves onde aplicável

---

## 📱 Testes de Responsividade

### Breakpoints
- [ ] **Mobile (320px-768px)** - Layout funcional em telas pequenas
- [ ] **Tablet (768px-1024px)** - Adaptação adequada para tablets
- [ ] **Desktop (1024px+)** - Aproveitamento do espaço em telas grandes

### Funcionalidades Mobile
- [ ] **Touch targets** - Botões têm tamanho adequado para toque
- [ ] **Scroll behavior** - Rolagem suave e natural
- [ ] **Orientação** - Funciona em portrait e landscape
- [ ] **Zoom** - Não quebra layout quando usuário faz zoom

---

## ✅ Critérios de Aceitação Gerais

### Performance
- [ ] **Tempo de carregamento** - Páginas carregam em menos de 3 segundos
- [ ] **Tamanho de bundle** - JavaScript otimizado
- [ ] **Imagens otimizadas** - Compressão adequada

### Compatibilidade
- [ ] **Chrome** - Funciona na versão mais recente
- [ ] **Firefox** - Funciona na versão mais recente
- [ ] **Safari** - Funciona na versão mais recente
- [ ] **Edge** - Funciona na versão mais recente

### Segurança Frontend
- [ ] **Validação client-side** - Não é a única validação (backend valida também)
- [ ] **Sanitização** - Dados exibidos são tratados contra XSS
- [ ] **HTTPS** - Aplicação roda em conexão segura

---

**Última atualização:** 06/06/2025  
**QA Responsável:** Lívia Takeda  
**Status:** Em andamento

