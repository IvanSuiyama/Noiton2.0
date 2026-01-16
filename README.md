# 📱 Noiton2 - Task Management App

> Aplicativo mobile completo de gerenciamento de tarefas com workspaces colaborativos, IA por voz, sincronização offline e sistema de gamificação.

**⚠️ Desafio Técnico:** Desenvolvido sem dependência de bibliotecas prontas do React Native - todos os módulos nativos foram implementados manualmente em Java.

---

## 🎯 Sobre o Projeto

Noiton2 é a segunda iteração de um sistema completo de gerenciamento de tarefas, inspirado no Notion, mas focado em produtividade individual e colaborativa. Desenvolvido como projeto acadêmico do 5º semestre (FATEC-SJC), o aplicativo implementa funcionalidades avançadas de apps comerciais, incluindo sincronização offline, assistente de IA, gamificação e administração de conteúdo.

**Diferencial:** Todo o projeto foi desenvolvido **solo**, com implementação manual de módulos nativos para máximo controle e aprendizado técnico.

---

## ✨ Funcionalidades Principais

### 🔄 Sincronização & Offline
- ✅ **Cache offline inteligente** com SQLite local
- ✅ **Sincronização automática via WiFi** (dados móveis não implementados por escolha)
- ✅ Funcionamento 100% offline com sync quando reconectar

### 🤖 Assistente de IA
- ✅ **Criação de tarefas por voz** usando IA
- ✅ **Consulta inteligente** de tarefas existentes
- ✅ Processamento de linguagem natural

### 👥 Workspaces Colaborativos
- ✅ **Workspaces individuais** e **em equipe**
- ✅ **Níveis de acesso granulares:**
  - Visualização apenas
  - Edição de tarefas
  - Administração total
- ✅ **Regras de negócio:**
  - Apenas criador pode excluir tarefas próprias
  - Apenas criador pode excluir workspace
  - Permissões por usuário dentro do workspace

### 🎮 Sistema de Gamificação
- ✅ **Sistema de pontos** por conclusão de tarefas
- ✅ **Loja de temas e ícones** customizáveis
- ✅ Incentivo à produtividade através de recompensas visuais

### 🔐 Autenticação & Segurança
- ✅ **Login com Google** (OAuth 2.0)
- ✅ Criação de conta tradicional
- ✅ Sessões seguras com tokens JWT

### 🛡️ Sistema de Moderação
- ✅ **Sistema de denúncias funcional**
- ✅ **Painel administrativo** para aprovação/reprovação de denúncias
- ✅ Moderação de conteúdo inadequado

### 📊 Métricas & Produtividade
- ✅ **Dashboard individual** com estatísticas pessoais
- ✅ **Métricas de equipe** em workspaces colaborativos
- ✅ Visualização de progresso e tendências

### 📋 Gestão de Tarefas
- ✅ **CRUD completo** com validações
- ✅ **Comentários** em tarefas
- ✅ **Anexos:** 1 PDF + 1 imagem por tarefa
- ✅ **Categorização** customizada por workspace
- ✅ **Filtros avançados:** palavras-chave, categoria, data, status
- ✅ **Tarefas recorrentes** (diária, semanal, mensal)
- ✅ **Favoritos:** até 10 tarefas marcadas
- ✅ **Fixar no topo:** até 3 tarefas prioritárias

### 📅 Calendário & Notificações
- ✅ **Calendário integrado** mostrando datas de criação
- ✅ **Alertas de vencimento** próximo
- ✅ **Integração com Google Calendar** (Agenda Android)
- ✅ **Push notifications** para lembretes

### 🎨 Interface & UX
- ✅ **Sistema de temas responsivo** - altera globalmente
- ✅ **4 cards superiores:** Workspaces | Membros | Métricas | Usuário
- ✅ **2 cards informativos:** Lojinha | Ajuda
- ✅ **Menu principal:** Home | Tarefas | Favoritos | Calendário
- ✅ **Card de ajuda** explicando funcionalidades
- ✅ Design intuitivo e moderno

---

## 🏗️ Arquitetura Técnica

### Frontend (Mobile)
```
React Native + Módulos Nativos Java
├── UI Layer: React Native (TypeScript)
├── Native Modules: Java (Android)
│   ├── Sincronização offline
│   ├── Notificações push
│   ├── Integração com Google Calendar
│   └── Gerenciamento de cache
└── Local Database: SQLite
    └── Cache offline de tarefas
```

### Backend (API REST)
```
Node.js + TypeScript
├── Express.js (framework)
├── JWT Authentication
├── OAuth 2.0 (Google)
├── Upload de arquivos (PDF/imagem)
└── Integração com IA para processamento de voz
```

### Banco de Dados
```
PostgreSQL (local)
├── Usuários & Autenticação
├── Workspaces & Membros
├── Tarefas & Categorias
├── Comentários & Anexos
├── Sistema de pontos & Loja
├── Denúncias & Moderação
└── Métricas & Logs
```

### Ferramentas Auxiliares
```python
# Script Python para troca automática de IPs
# Facilita desenvolvimento em diferentes redes
python change_ip.py --new-ip 192.168.1.100
```

---

## 🛠️ Tecnologias Utilizadas

### Mobile
- **React Native** - Framework mobile
- **TypeScript** - Type safety
- **Java** - Módulos nativos Android
- **SQLite** - Cache local

### Backend
- **Node.js** - Runtime
- **TypeScript** - Linguagem
- **Express.js** - Framework web
- **JWT** - Autenticação
- **OAuth 2.0** - Login social

### Banco de Dados
- **PostgreSQL** - Banco relacional principal

### Integrações
- **Google Calendar API** - Integração com agenda
- **IA (API externa)** - Processamento de voz
- **Firebase Cloud Messaging** - Push notifications

---

## 🚀 Como Rodar o Projeto

### Pré-requisitos
```bash
- Node.js 16+
- PostgreSQL 14+
- Android Studio (para emulador)
- React Native CLI
- Python 3.8+ (para script de IP)
```

### 1. Clone o Repositório
```bash
git clone https://github.com/IvanSuiyama/API5-Io.git
cd API5-Io
```

### 2. Configure o Banco de Dados
```sql
-- Crie o banco no PostgreSQL
CREATE DATABASE noiton2_db;

-- Execute as migrations (se houver)
-- ou importe o schema fornecido
```

### 3. Configure o Backend
```bash
cd backend
npm install

# Configure as variáveis de ambiente
cp .env.example .env
# Edite .env com suas credenciais:
# - DATABASE_URL
# - JWT_SECRET
# - GOOGLE_CLIENT_ID
# - GOOGLE_CLIENT_SECRET

# Inicie o servidor
npm run dev
```

### 4. Configure o Frontend
```bash
cd mobile
npm install

# Troque o IP do backend (se necessário)
python ../scripts/change_ip.py --new-ip SEU_IP_LOCAL

# Inicie o Metro Bundler
npm start

# Em outro terminal, rode no Android
npm run android
```

### 5. (Opcional) Configurar IA
```bash
# Configure a API key da IA no .env do backend
AI_API_KEY=sua_chave_aqui
```

---

## 🎓 Desafios Técnicos Superados

### 1. Desenvolvimento sem Bibliotecas Prontas
**Desafio:** Restrição de não utilizar bibliotecas React Native prontas.

**Solução:** Implementação manual de todos os módulos nativos em Java:
- Sistema de cache offline com sincronização
- Integração com Google Calendar
- Sistema de notificações push
- Gerenciamento de arquivos e uploads

**Aprendizado:** Compreensão profunda da bridge React Native ↔ Java e arquitetura mobile nativa.

---

### 2. Sincronização Offline Robusta
**Desafio:** Garantir consistência de dados entre cache local (SQLite) e servidor (PostgreSQL).

**Solução:**
- Implementação de sistema de versionamento de tarefas
- Filas de sincronização com retry automático
- Detecção de conflitos com estratégia "last-write-wins"
- Sincronização apenas via WiFi para economizar dados móveis

**Aprendizado:** Arquitetura offline-first e resolução de conflitos distribuídos.

---

### 3. Banco de Dados Gratuito para Produção
**Desafio:** Serviços gratuitos online não atendiam requisitos de performance/confiabilidade.

**Solução:** 
- PostgreSQL local com URL configurável via variável de ambiente
- Arquitetura preparada para fácil migração para serviços cloud (AWS RDS, Supabase, etc)
- Script Python para facilitar troca de IPs em desenvolvimento

**Aprendizado:** Flexibilidade arquitetural e preparação para deploy em diferentes ambientes.

---

### 4. Sistema de Permissões Granulares
**Desafio:** Implementar níveis de acesso complexos sem bibliotecas de ACL.

**Solução:**
- Modelagem de relacionamentos N:N (User ↔ Workspace)
- Middleware de verificação de permissões no backend
- Validações no frontend para UX responsiva
- Regras de negócio claras (apenas criador pode excluir)

**Aprendizado:** Design de sistemas multiusuário com segurança em camadas.

---

## 📊 Modelagem de Dados (Resumida)

```
Users                    Workspaces               Tasks
├── id                   ├── id                   ├── id
├── name                 ├── name                 ├── title
├── email                ├── creator_id (FK)      ├── description
├── google_id            ├── type (individual     ├── workspace_id (FK)
├── points                      /team)            ├── creator_id (FK)
└── created_at           └── created_at           ├── category_id (FK)
                                                  ├── due_date
UserWorkspace (M:N)      Categories               ├── status
├── user_id (FK)         ├── id                   ├── is_recurring
├── workspace_id (FK)    ├── name                 ├── attachment_pdf
├── role (viewer         ├── workspace_id (FK)    ├── attachment_image
       /editor/admin)    └── color                └── created_at
└── joined_at
                         Comments                 Favorites
                         ├── id                   ├── user_id (FK)
                         ├── task_id (FK)         ├── task_id (FK)
                         ├── user_id (FK)         └── pinned (boolean)
                         ├── content
                         └── created_at           Reports
                                                  ├── id
                         Themes                   ├── task_id (FK)
                         ├── id                   ├── reporter_id (FK)
                         ├── name                 ├── reason
                         ├── price (points)       ├── status
                         ├── preview_image        └── reviewed_by (FK)
                         └── is_unlocked
```

---

## 📈 Métricas do Projeto

- **Linhas de Código:** ~15.000+ (estimativa)
- **Tempo de Desenvolvimento:** 1 semestre acadêmico
- **Desenvolvedores:** 1 (solo)
- **Telas Implementadas:** 15+
- **Módulos Nativos Java:** 8+
- **Endpoints API:** 40+
- **Tabelas no Banco:** 12+

---

## 🎯 Funcionalidades Futuras (Roadmap)

- [ ] Sincronização via dados móveis (4G/5G)
- [ ] Integração com Trello/Notion (importação de tarefas)
- [ ] Modo escuro automático por horário
- [ ] Suporte a subtarefas (tarefas aninhadas)
- [ ] Chat em tempo real dentro de workspaces
- [ ] Versão web (Progressive Web App)
- [ ] Deploy em produção (Google Play Store)
- [ ] Relatórios exportáveis (PDF/Excel)

---

## 📝 Licença

Este projeto foi desenvolvido para fins acadêmicos como parte do curso de Desenvolvimento de Software Multiplataforma da FATEC-SJC.

---

## 👨‍💻 Autor

**Ivan Suiyama Silva**  
Estudante de Desenvolvimento de Software Multiplataforma - FATEC-SJC  
Foco em DevSecOps e Desenvolvimento Full Stack

📧 ivan.suiya@gmail.com  
💼 [LinkedIn](https://linkedin.com/in/ivan-suiyama-silva-248042186)  
🐙 [GitHub](https://github.com/IvanSuiyama)

---

## 🙏 Agradecimentos

- **FATEC-SJC** - Pelo incentivo a criação do aplicativo

---

**⭐ Se este projeto te ajudou de alguma forma, considere dar uma estrela!**

## Atalhos para outros repositórios do projeto

- [Noiton2_backend](https://github.com/IvanSuiyama/noiton2.0_Backend)
- [Noiton2_frontend](https://github.com/IvanSuiyama/noiton2_frontend)
