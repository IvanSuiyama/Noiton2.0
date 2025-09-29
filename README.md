
# Objetivo
O projeto Noiton tem como objetivo a criação de um app para gerenciar tarefas do dia a dia, permitindo organização pessoal e colaboração em equipe, com foco em produtividade.

<br>

## Requisitos do Projeto

| ID  | Requisito |
|-----|-----------|
| 1   | O sistema deve permitir cadastro de usuários com autenticação via e-mail e senha. |
| 2   | O sistema deve permitir login via Google e redes sociais, com autenticação segura. |
| 3   | O usuário deve visualizar suas tarefas criadas ou compartilhadas em um painel inicial. |
| 4   | O sistema deve permitir a criação, edição e exclusão de tarefas (CRUD). |
| 5   | O sistema deve permitir criar workspaces e adicionar membros. |
| 6   | O usuário deve poder compartilhar tarefas com membros do workspace. |
| 7   | O sistema deve permitir atribuir responsáveis a tarefas (um ou mais usuários). |
| 8   | O usuário deve receber notificações automáticas (prazos, alterações, comentários). |
| 9   | O sistema deve permitir visualizar tarefas em calendário (dia, semana, mês). |
| 10  | O sistema deve permitir organizar tarefas em listas personalizadas e aplicar filtros básicos. |
| 11  | O usuário deve poder criar tarefas recorrentes (diárias, semanais, mensais). |
| 12  | O sistema deve permitir comentários e anexos (arquivos, links, imagens) em tarefas. |
| 13  | O sistema deve destacar visualmente tarefas prioritárias. |
| 14  | O sistema deve permitir uso offline, com sincronização posterior. |
| 15  | O sistema deve exibir estatísticas de progresso (tarefas concluídas, pendentes, desempenho da equipe). |
| 16  | O sistema deve integrar com calendários externos (Google Calendar, Outlook). |
| 17  | O sistema deve permitir filtros avançados (palavra-chave, prazo, responsável, categoria). |
| 18  | O sistema deve sugerir replanejamento ou reatribuição de tarefas atrasadas (alertas inteligentes). |
| 19  | O usuário deve poder exportar relatórios em PDF ou planilhas. |
| 20  | O sistema deve permitir integração com assistentes virtuais (voz). |
| 21  | O sistema deve incluir gamificação (pontos, conquistas por tarefas concluídas). |
| 22  | O usuário deve poder fixar tarefas prioritárias no topo da lista. |
| 23  | O sistema deve permitir personalização da interface (tema claro/escuro, cores). |
| 24  | O sistema deve oferecer dicas de produtividade. |
| 25  | O usuário deve poder denunciar conteúdos inadequados ou spam. |

<br>

## Backlog do Produto

| Rank | Prioridade | User Story | Estimativa (h) | Sprint | Requisito Atendido |
|------|------------|------------|----------------|--------|--------------------|
| 1    | Alto       | Como usuário, quero criar uma conta com e-mail e senha para acessar o app. | 8  | 1 | 1 |
| 2    | Alto       | Como usuário, quero criar, editar e excluir tarefas para organizar minhas atividades. | 10 | 1 | 4 |
| 3    | Alto       | Como líder de equipe, quero criar workspaces e adicionar membros para organizar a colaboração. | 12 | 1 | 5 |
| 4    | Médio      | Como usuário, quero compartilhar tarefas com membros do workspace para permitir colaboração básica. | 6  | 1 | 6 |
| 5    | Médio      | Como usuário, quero autenticar com Google ou redes sociais para facilitar login. | 8  | 2 | 2 |
| 6    | Alto       | Como usuário, quero ver todas as minhas tarefas no painel inicial para acompanhar meu trabalho. | 6  | 2 | 3 |
| 7    | Alto       | Como usuário, quero atribuir responsáveis às tarefas para organizar responsabilidades. | 8  | 2 | 7 |
| 8    | Alto       | Como usuário, quero receber notificações automáticas sobre prazos e alterações para não perder nada importante. | 10 | 2 | 8 |
| 9    | Alto       | Como usuário, quero visualizar tarefas no calendário (dia, semana, mês) para planejar melhor. | 12 | 2 | 9 |
| 10   | Médio      | Como usuário, quero organizar tarefas em listas personalizadas com filtros básicos para facilitar busca. | 8  | 2 | 10 |
| 11   | Alto       | Como usuário, quero configurar tarefas recorrentes (diárias, semanais, mensais) para automatizar rotinas. | 10 | 3 | 11 |
| 12   | Médio      | Como usuário, quero comentar e anexar arquivos às tarefas para facilitar a colaboração. | 8  | 3 | 12 |
| 13   | Médio      | Como usuário, quero visualizar destaque em tarefas prioritárias para identificar urgências. | 5  | 3 | 13 |
| 14   | Alto       | Como usuário, quero acessar e editar tarefas offline para não depender de internet. | 12 | 3 | 14 |
| 15   | Alto       | Como líder de equipe, quero visualizar estatísticas de progresso para acompanhar desempenho. | 10 | 3 | 15 |
| 16   | Médio      | Como usuário, quero integrar minhas tarefas ao Google Calendar e Outlook para centralizar compromissos. | 12 | 3 | 16 |
| 17   | Médio      | Como usuário, quero filtrar tarefas por palavra-chave, prazo e responsável para encontrar facilmente. | 8  | 3 | 17 |
| 18   | Baixo      | Como usuário, quero receber alertas inteligentes para reorganizar tarefas atrasadas. | 6  | 3 | 18 |
| 19   | Baixo      | Como usuário, quero exportar listas e relatórios em PDF ou planilhas para acompanhar em outros contextos. | 6  | 3 | 19 |
| 20   | Baixo      | Como usuário, quero adicionar e consultar tarefas por comando de voz via assistentes virtuais. | 10 | 3 | 20 |
| 21   | Baixo      | Como usuário, quero ganhar pontos e conquistas por concluir tarefas para aumentar meu engajamento. | 8  | 3 | 21 |
| 22   | Baixo      | Como usuário, quero fixar tarefas prioritárias no topo da lista para não perdê-las de vista. | 4  | 3 | 22 |
| 23   | Baixo      | Como usuário, quero personalizar a interface com temas e cores para deixá-la confortável. | 6  | 3 | 23 |
| 24   | Baixo      | Como usuário, quero visualizar dicas de produtividade no app para aproveitar melhor as funcionalidades. | 4  | 3 | 24 |
| 25   | Baixo      | Como usuário, quero denunciar conteúdos inadequados para manter o ambiente seguro. | 4  | 3 | 25 |
