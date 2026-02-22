# Agendas para Barbearia - SaaS Multi-Tenant

## Objetivo

Plataforma SaaS para gestão de barbearias com agendamento público, controle financeiro integrado e automação de lembretes.

## Telas

### Login e Autenticação

**Rota:** `/`

**Objetivo:** Ponto de entrada central para gestão administrativa.

**Componentes:**

- **Input Email, Input Senha, Botão Login, Link Esqueci Senha**: Autentica o usuário e redireciona para o dashboard com base no perfil (admin_master, dono, barbeiro).

### Agenda Administrativa

**Rota:** `/appointments`

**Objetivo:** Visualização geral e gestão de compromissos da barbearia.

**Componentes:**

- **Calendário de Agendamentos, Botão Novo Corte, Card de Filtro por Barbeiro**: Abre formulário para novo agendamento, bloqueando horários ocupados.

### Landing Page e Agendamento Público

**Rota:** `/b/:slug`

**Objetivo:** Interface externa para clientes agendarem serviços via slug da barbearia.

**Componentes:**

- **Lista de Serviços, Seletor de Profissional, DatePicker de Horários Disponíveis, Mapa do Google Maps**: Redireciona para o checkout do agendamento após seleção.

### Checkout de Agendamento

**Rota:** `/b/:slug/checkout`

**Objetivo:** Finalização do agendamento com integração de pagamento.

**Componentes:**

- **Resumo do Serviço, Botão Pagar com PIX, Botão Confirmar via WhatsApp**: Processa o pagamento via Mercado Pago e confirma o agendamento.

### Carteira e Financeiro (Tenant)

**Rota:** `/finance`

**Objetivo:** Gestão financeira interna da barbearia e solicitações de repasse.

**Componentes:**

- **Card Saldo Disponível, Card Saldo Pendente, Tabela de Transações, Botão Solicitar Saque**: Solicita transferência de saldo disponível.

### Configurações da Barbearia

**Rota:** `/settings/profile`

**Objetivo:** Gerenciar perfil de negócio, regras de agendamento e automações.

**Componentes:**

- **Input Nome, Upload de Logo, Seletor de Horários de Turno, Configuração de WhatsApp API**: Salva horários de funcionamento e regras de antecedência mínima.

### Gestão de Equipe e Serviços

**Rota:** `/settings/team`

**Objetivo:** Administrar profissionais e o catálogo de serviços oferecidos.

**Componentes:**

- **Tabela de Barbeiros, Botão Adicionar Barbeiro, Checkbox de Serviços Prestados**: Cria ou edita perfis de barbeiros e seus serviços vinculados.

### Painel Admin Master

**Rota:** `/admin/master`

**Objetivo:** Visão macro da plataforma para o dono do SaaS gerir assinaturas e saques.

**Componentes:**

- **Gráfico de Receita Global, Tabela de Solicitações de Saque, Lista de Assinaturas Ativas**: Aprova ou nega solicitações de saque de todas as barbearias.

