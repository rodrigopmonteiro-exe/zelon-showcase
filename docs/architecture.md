# Architecture

## Visão Geral

O Zelon foi projetado como uma plataforma modular de evolução financeira.

Ao invés de concentrar toda a lógica em uma única aplicação monolítica, o sistema foi estruturado em módulos especializados que trabalham em conjunto para transformar dados financeiros em decisões, estratégias e progresso mensurável.

O objetivo da arquitetura é permitir:

- Evolução contínua
- Escalabilidade
- Facilidade de manutenção
- Reutilização de componentes
- Crescimento do ecossistema

---

# Filosofia Arquitetural

O Zelon segue alguns princípios fundamentais.

## Modularidade

Cada domínio financeiro possui responsabilidades bem definidas.

## Separação de Contextos

Planejamento, patrimônio, dívidas, evolução e gamificação possuem fluxos independentes.

## Escalabilidade Progressiva

Novos módulos podem ser adicionados sem necessidade de reestruturar o sistema inteiro.

## Experiência Unificada

Apesar da separação interna, o usuário enxerga uma única jornada integrada.

---

# Visão de Alto Nível

```text
Usuário
    │
    ▼
Frontend (React)
    │
    ▼
Camada de Aplicação
    │
    ├── Meu Mês
    ├── Patrimônio
    ├── Dívidas
    ├── Reserva
    ├── Planejamento
    ├── Estratégias
    ├── Simulador
    ├── Evolução
    └── Alliance
    │
    ▼
Supabase
    │
    ├── Authentication
    ├── PostgreSQL
    ├── Storage
    └── Edge Functions
```

---

# Frontend

O frontend foi construído utilizando tecnologias modernas focadas em performance, produtividade e escalabilidade.

## Tecnologias

- React
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui

## Responsabilidades

O frontend é responsável por:

- Interface do usuário
- Navegação
- Gerenciamento de estado
- Visualização de dados
- Experiência responsiva
- Progressive Web App (PWA)

---

# Backend

O backend utiliza Supabase como plataforma principal.

Essa escolha permitiu acelerar o desenvolvimento sem abrir mão de escalabilidade e segurança.

## Componentes

### Authentication

Gerenciamento de usuários e sessões.

Responsável por:

- Cadastro
- Login
- Recuperação de acesso
- Controle de permissões

### PostgreSQL

Banco de dados principal.

Armazena:

- Usuários
- Planejamento
- Patrimônio
- Dívidas
- Estratégias
- Evolução
- Alliance

### Storage

Responsável pelo armazenamento de arquivos.

Utilizado para:

- Relatórios
- Documentos
- Recursos futuros

### Edge Functions

Executam lógicas específicas do sistema.

Exemplos:

- Processamento de relatórios
- Integrações
- Automatizações
- Serviços futuros de IA

---

# Estrutura Modular

O Zelon foi dividido em domínios de negócio.

## Capture

Responsável pela entrada rápida de dados financeiros.

**Objetivo:** reduzir atrito na coleta de informações.

## Meu Mês

Camada operacional do planejamento financeiro.

Responsável por:

- Receitas
- Despesas
- Investimentos
- Saldo

## Patrimônio

Gerencia ativos e passivos.

Responsável por:

- Patrimônio líquido
- Distribuição patrimonial
- Liquidez

## Dívidas

Responsável pela gestão de passivos financeiros.

Inclui:

- Parcelamentos
- Financiamentos
- Simulações de quitação

## Reserva

Gerencia a reserva de emergência.

Inclui:

- Meta
- Cobertura
- Evolução

## Planejamento

Motor de distribuição financeira.

Considera:

- Perfil de risco
- Renda
- Dependentes
- Endividamento
- Objetivos

## Estratégias

Camada de recomendações.

Transforma dados financeiros em ações sugeridas.

## Simulador

Responsável por projeções de longo prazo.

Inclui:

- Independência financeira
- Crescimento patrimonial
- Cenários futuros

## Evolução

Monitora o progresso do usuário.

Inclui:

- Histórico
- Indicadores
- Score financeiro

## Alliance

Camada de engajamento e gamificação.

Inclui:

- XP
- Coins
- Níveis
- Loja
- Ranking
- Clube Lenda

---

# Fluxo de Dados

O Zelon foi desenhado para que uma única ação possa gerar impacto em múltiplos módulos.

## Exemplo

```text
Capture
    │
    ▼
Meu Mês
    │
    ▼
Planejamento
    │
    ▼
Estratégias
    │
    ▼
Evolução
    │
    ▼
Alliance
```

Isso permite transformar dados simples em inteligência financeira.

---

# Progressive Web App (PWA)

O Zelon foi desenvolvido como Progressive Web App.

## Benefícios

- Instalação em dispositivos móveis
- Experiência semelhante a aplicativo nativo
- Atualizações simplificadas
- Compatibilidade multiplataforma

---

# Segurança

A segurança é tratada em múltiplas camadas.

## Autenticação

Controle de acesso baseado em usuário.

## Isolamento de Dados

Cada usuário possui acesso apenas aos seus próprios registros.

## Regras de Permissão

Implementadas através da infraestrutura do Supabase.

## Comunicação Segura

Transmissão de dados utilizando conexões seguras.

---

# Escalabilidade

A arquitetura foi planejada para suportar expansão gradual.

Novos módulos podem ser adicionados sem impactar os componentes existentes.

## Exemplos Futuros

- IA Financeira
- Insights Preditivos
- Integrações Bancárias
- Novos Produtos do Ecossistema Zelon

---

# Decisões Técnicas

## Por que React?

Flexibilidade, ecossistema maduro e alta produtividade.

## Por que TypeScript?

Maior segurança e escalabilidade do código.

## Por que Supabase?

Rapidez de desenvolvimento sem abrir mão de recursos avançados.

## Por que PWA?

Permite entregar experiência próxima a aplicativos nativos com menor complexidade operacional.

---

# Arquitetura em Evolução

A arquitetura do Zelon não é estática.

Ela evolui continuamente conforme novas necessidades surgem.

Nosso objetivo não é apenas construir um aplicativo financeiro.

Estamos construindo a infraestrutura tecnológica necessária para sustentar um ecossistema completo de evolução financeira.

---

# Controle. Clareza. Liberdade.
