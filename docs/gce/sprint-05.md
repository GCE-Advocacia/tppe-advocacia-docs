# Sprint 5

*Período:* 17/11/2026 a 28/11/2026

## Entregas da Sprint

| Trio/Equipe de Desenvolvedores | Qtd. de US | US | Assunto das US |
|---|---:|---|---|
| A preencher | 0 | - | - |

---

## Correções de bugs

| Bug | Descrição | Responsável | Status | PR/Commits |
|---|---|---|---|---|
| Validação de temas e cores na API | Evita HTTP 500 ao enviar `theme_id` excluído (retorna 404), padroniza `_HexColor` em todas as cores e rejeita nomes de tema em branco | Gabriel | Concluído | [PR Backend #40](https://github.com/GCE-Advocacia/tppe-advocacia-backend/pull/40) |
| Edição nos inputs do ColorPicker | Libera digitação com `Backspace`, colagem sem `#`, limpeza de transparência no HEX e edição nos campos numéricos (`RGB`/`HSL`/`HSB`/`Alpha`) | Gabriel | Concluído | [PR Frontend #39](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/39) |
| Fluxo de temas, fork e cota | Corrige exclusão do tema ativo, dirty state dos botões do sistema, badge `Em Uso`, duplicação em falha parcial do fork, cota `6/6`, limites/overflow nos cards e remove `alert()` | Gabriel | Concluído | [PR Frontend #40](https://github.com/GCE-Advocacia/tppe-advocacia-frontend/pull/40) |

---

## Resumo

- *Líder da Apresentação*: A definir
- *Total de US concluídas*: 0
- *Bugs corrigidos*: 3
- *US em revisão*: 0
- *Início da Sprint*: 17/11/2026
- *Fim da Sprint*: 28/11/2026

---

## Histórico de Versão

| Versão | Data | Descrição | Autor(es) |
|---|---|---|---|
| `1.0` | 22/11/2026 | Criação do relatório da Sprint 5 com registro das correções de bugs de personalização | [Gabriel Fernando](https://github.com/MMcLovin) |
