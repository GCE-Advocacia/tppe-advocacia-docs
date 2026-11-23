# Sprint 4

*Período:* 29/10/2026 a 16/11/2026

## Entregas da Sprint

| Trio/Equipe de Desenvolvedores | Qtd. de US | US | Assunto das US |
|---|---:|---|---|
| Artur / Bessa / Isabelle | 1 | [US27](./backlog/us27.md) | Migração das contas de nuvem e do Google para o cliente |
| Gabriel / Fabio / Daniel | 4 | [US14](./backlog/us14.md), [US26](./backlog/us26.md), [US06](./backlog/us06.md), [US17](./backlog/us17.md) | Sincronização dos temas com o sistema e login, Blindagem da personalização e preview responsivo, Reposicionamento e upload de imagens (auditoria e BUG-08), Preview multi-dispositivo |

---

## Detalhamento por história

| US | Assunto | Responsáveis | Status | PR/Commits |
|---|---|---|---|---|
| [US14](./backlog/us14.md) | Sincronização dos temas com o sistema e login | Gabriel, Fabio, Daniel | Concluído | [PR Backend #29](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/29), [PR Frontend #27](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/27), [PR Frontend #37](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/37), [PR Frontend #38](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/38) |
| [US26](./backlog/us26.md) | Blindagem da personalização e preview responsivo | Gabriel, Fabio, Daniel | Concluído | [PR Backend #30](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/30), [PR Frontend #28](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/28), [PR Frontend #29](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/29), [PR Frontend #31](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/31) |
| [US26.1](./backlog/us26.md#us261-temas-cores-validacoes-de-midia-e-novos-testes) | Auditoria de temas, paleta de cores e validações de mídia | Fabio | Concluído | [PR Backend #30](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/30), [PR Frontend #28](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/28) |
| [US26.2](./backlog/us26.md#us262-logos-botoes-preview-responsivo-e-guardas-de-rota) | Preview responsivo, upload com corte e múltiplos viewports | Daniel | Concluído | [PR Frontend #31](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/31) |
| [US26.3](./backlog/us26.md#us263-conteudo-institucional-enquadramento-de-fotos-bug-08-e-testes-e2e) | Auditoria de conteúdo institucional, BUG-08 e suíte E2E | Gabriel | Concluído | [PR Frontend #29](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/29) |
| [US06](./backlog/us06.md) | Reposicionamento e upload de imagens (auditoria e BUG-08) | Gabriel, Fabio, Daniel | Concluído | [PR Frontend #29](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/29) |
| [US15](./backlog/us15.md) | Preset de tema e logos do novo escritório | Gabriel, Fabio, Daniel | Despriorizada | - |
| [US17](./backlog/us17.md) | Preview multi-dispositivo (Desktop, Tablet e Mobile) | Gabriel, Fabio, Daniel | Concluído | [PR Frontend #23](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/23), [PR Frontend #29](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/29) |
| [US27](./backlog/us27.md) | Migração das contas de nuvem e do Google para o cliente | Artur, Bessa, Isabelle | Concluído | Configuração nos painéis do Google Cloud, Render, Netlify e Neon (sem PR) |

---

## Correções de bugs

| Bug | Descrição | Responsável | Status | PR/Commits |
|---|---|---|---|---|
| Validação de CPF/CNPJ | O cadastro de clientes só conferia a quantidade de dígitos e aceitava CPFs e CNPJs inválidos. Agora o backend e o frontend validam os dígitos verificadores e rejeitam sequências repetidas | Isabelle | Concluído | [PR Backend #36](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/36), [PR Frontend #35](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/35) |
| XSS nos artigos | O conteúdo dos artigos era salvo e exibido sem sanitização, permitindo executar scripts no navegador de quem abrisse o artigo. Agora o backend sanitiza o HTML ao salvar (`bleach`) e o frontend ao exibir (`DOMPurify`) | Isabelle | Concluído | [PR Backend #38](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/38), [PR Frontend #36](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/36) |
| Pasta duplicada no Google Drive | A pasta raiz dos documentos era criada de novo ao reconectar o Drive ou quando dois uploads aconteciam ao mesmo tempo. Agora o sistema procura a pasta existente no Drive antes de criar e trava a criação no banco | Artur | Concluído | [PR Backend #39](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/39) |
| Deadlock ao salvar/descartar na personalização | O salvamento de conteúdo e temas concorriam no estado do formulário gerando travamento da interface. O fluxo foi desacoplado isolando persistência de temas e reset de estado | Gabriel | Concluído | [PR Frontend #29](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/29) |
| Aviso de alterações não salvas por aba | O pop-up de alerta de alterações pendentes era exibido apenas na aba de conteúdo da personalização. O guard foi estendido para interceptar navegações em todas as abas e rotas do sistema | Gabriel | Concluído | [PR Frontend #27](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/27) |
| Leitura de configuração vazia no backend | A rota `GET /office-config` e o payload de atualização falhavam quando `office_title` era nulo ou vazio. Agora o backend trata o campo opcionalmente sem interromper o carregamento da personalização | Gabriel | Concluído | [PR Backend #37](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/37) |

---

## Resumo

- *Líder da Apresentação*: A definir
- *Total de US concluídas*: 5 de 6
- *Bugs corrigidos*: 6
- *US em revisão*: 0
- *Início da Sprint*: 29/10/2026
- *Fim da Sprint*: 16/11/2026

---

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) |
|---|---|---|---|
| `1.0` | 16/11/2026 | Criação do relatório da Sprint 4 | [Gabriel Fernando](https://github.com/MMcLovin) |
| `1.1` | 17/11/2026 | Inclusão da US27 e das correções de bugs do subgrupo 3 | [Artur H. Krauspenhar](https://github.com/Arturhk05) |
| `1.2` | 17/11/2026 | Inclusão de correções de bugs de personalização/backend e PRs complementares da US14 | [Gabriel Fernando](https://github.com/MMcLovin) |
