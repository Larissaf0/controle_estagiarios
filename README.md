# Sistema de Controle de Estagiários 🎓

Plataforma web desenvolvida para otimizar a gestão de estagiários no gabinete. O sistema permite o acompanhamento de contratos, controle de folhas de ponto, identificação de pendências e a geração automatizada de memorandos de pagamento.

## 🚀 Funcionalidades

- **Dashboard Central:** Visão geral com o total de estagiários, distribuição por setor e alertas automáticos para contratos com vencimento em menos de 30 dias.
- **Gestão de Pagamentos:** Controle de status da competência mensal (Aptos, Pendentes), folha de ponto e valor das bolsas.
- **Geração de Memorandos:** Criação automatizada de memorandos de pagamento para os estagiários sem pendências.
- **Controle de Contratos:** Cadastro detalhado com informações de CPF, curso, faculdade, setor, convênio e período do termo de compromisso.
- **Armazenamento Seguro:** Upload e gerenciamento de documentos de estagiários (PDF, Word e Imagens) de forma privada e segura.
- **Painel Administrativo Segregado:** Sistema de segurança com acesso restrito apenas para administradores autorizados.

## 🛠️ Tecnologias Utilizadas

**Front-end:**
- HTML, CSS e JavaScript
- Interface baseada em componentes de Dashboard

**Back-end & Banco de Dados (BaaS):**
- **[Supabase](https://supabase.com/):** 
  - Banco de Dados PostgreSQL (Tabelas: `estagiarios`, `memorandos`).
  - **Authentication:** Controle de sessão e verificação de permissões via RLS (Row Level Security) limitando acesso à tabela `app_admins`.
  - **Storage:** Bucket privado `documentos-estagiarios` protegido por políticas de segurança.

## ⚙️ Configuração do Banco de Dados (Supabase)

Para garantir que a segurança do sistema funcione corretamente, é necessário rodar o script SQL de permissões.

1. Acesse o painel do seu projeto no Supabase.
2. Navegue até o **SQL Editor**.
3. Execute o script `supabase_security.sql` fornecido junto com o projeto.
   - *Nota:* O primeiro usuário criado no `Authentication` do Supabase se tornará automaticamente o administrador inicial do sistema.

## 🚀 Como executar o projeto

Como o sistema utiliza Supabase no backend, o front-end pode ser executado facilmente:

1. Clone este repositório:
   ```bash
   git clone [https://github.com/seu-usuario/controle-estagiarios.git](https://github.com/seu-usuario/controle-estagiarios.git)
