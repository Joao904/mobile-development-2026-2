# SPRINT 07 — Final Integration, Quality & Delivery — Team 03 (Wiflux)

> **Equipe:** Célia Hiromi (@hiromilly) e Geovanna Gaspar (@gegwspar)
> **Prazo final:** 23/11/2026
> **Especificação:** [`docs/specs/SPEC-007.md`](docs/specs/SPEC-007.md)

## 1. Objetivo da Sprint

Integrar o produto acumulado, remover problemas críticos, validar o aplicativo completo e preparar a entrega final. Não há funcionalidade nova: a SPEC-007 define requisitos de qualidade.

## 2. Revisão de todas as SPECs

O status das SPECs 001 a 006 vem do que cada Sprint já validou. O teste de regressão da seção 3 confirma que continuam valendo no app final.

| Specification | Main feature | Current status | Evidence |
| --- | --- | --- | --- |
| SPEC-001 | Primeira tela do produto | PASS | `evidence/sprint-01/first-screen.png` |
| SPEC-002 | Estado e interação: medidor reage ao toque | PASS | `evidence/sprint-02/before-interaction.png` e `after-interaction.png` |
| SPEC-003 | Navegação entre Verificação e Detalhes | PASS | `evidence/sprint-03/screen-a.png` e `screen-b.png` |
| SPEC-004 | Nome do cômodo com validação | PASS | `evidence/sprint-04/valid-input.png` e `invalid-input.png` |
| SPEC-005 | Histórico salvo em banco local (Room) | PASS | `evidence/sprint-05/data-created.png` e `data-restored.png` |
| SPEC-006 | Leitura real do sinal Wi-Fi | PASS | `evidence/sprint-06/integration-success.png` e `integration-alternative-state.png` |
| SPEC-007 | Final quality | A executar (regressão) | `evidence/sprint-07/final-validation.md` |

**Observação sobre a SPEC-002:** na Sprint 02 o resultado da medição era sorteado. A partir da Sprint 06 ele vem do sinal real do Wi-Fi; o mecanismo de estado e a interação são os mesmos.

**Observação sobre o nome:** as SPECs 001 e 002 usam o nome antigo "Wi-Fi Mapper". O produto passou a se chamar Wiflux na Sprint 03.

## 3. Teste de regressão

Roteiro executado a partir de uma abertura limpa do app, no emulador do Android Studio. O resultado de cada passo está em [`evidence/sprint-07/final-validation.md`](evidence/sprint-07/final-validation.md).

| # | Passo | Resultado |
| --- | --- | --- |
| 1 | O app abre | A executar |
| 2 | A tela principal é utilizável | A executar |
| 3 | A navegação funciona | A executar |
| 4 | O estado e a interação funcionam | A executar |
| 5 | A validação do formulário funciona | A executar |
| 6 | Os dados persistem depois de reabrir o app | A executar |
| 7 | A integração funciona ou falha com mensagem clara | A executar |
| 8 | O botão voltar se comporta corretamente | A executar |
| 9 | Nenhum crash crítico no roteiro | A executar |

## 4. Melhorias de uso e consistência

Revisão rápida, sem redesenhar o app:

- **Nome do app:** o app aparecia como "Wifi" no aparelho e no Android Studio, enquanto a tela dizia "Wiflux". O nome "Wifi" veio do projeto novo criado na Sprint 03. Corrigido em `strings.xml` (`app_name`) e `settings.gradle.kts` (`rootProject.name`).
- Os demais itens (espaçamentos, rótulos, estados vazios e de erro) serão conferidos durante a regressão; o que não for corrigido entra nas limitações conhecidas.

## 5. Limpeza do repositório

- Não existem `.idea/`, `.gradle/`, `build/`, `.kotlin/` nem `local.properties` entre os arquivos versionados de `projects/team-03/`.
- Não há API, chave, senha ou token no projeto.
- O Gradle Wrapper e os arquivos de configuração necessários foram mantidos.

## 6. README da equipe

Criado em [`README.md`](README.md): produto, problema, público, funcionalidades, tecnologias, como compilar e executar, configuração, limitações e integrantes.

## 7. Limitações conhecidas

- O app lê só a rede Wi-Fi conectada no momento; não mostra o nome da rede (SSID).
- No emulador o sinal costuma ser forte; "Médio" e "Fraco" dependem de um aparelho real.
- O histórico guarda cômodo, status e data/hora, mas não o dBm, e mostra só as 5 últimas.
- Não há testes automatizados além dos de exemplo; a validação é manual.
- As SPECs 001 e 002 usam o nome antigo do produto.

## 8. Evidências finais

- `evidence/sprint-07/final-home.png`
- `evidence/sprint-07/final-feature.png`
- `evidence/sprint-07/final-validation.md`

## 9. Rastreabilidade dos requisitos

Ver SPEC-007, seção 8 (requisito → código → evidência).

## 10. Uso de LLM

| Item | Resposta da equipe |
| --- | --- |
| LLM/tool used | Claude (Anthropic) |
| Task supported by the LLM | Revisão das SPECs anteriores, geração do roteiro de regressão a partir delas, rascunho do README, da SPEC-007 e deste relatório |
| Main suggestion received | Executar o roteiro de 9 passos partindo de uma abertura limpa e registrar cada resultado; deixar como "A executar" o que ainda não foi testado |
| What the team changed manually | *(a equipe preenche depois de revisar os textos e executar a regressão)* |
| How the result was validated | *(a equipe preenche com o aparelho e os cenários realmente executados)* |

Nenhum print, resultado de teste, informação de aparelho ou critério foi inventado: a evidência vem de execução real.

## 11. Critérios de aceite da Sprint 07

- [ ] **AC-01** — SPEC-007 existe.
- [ ] **AC-02** — Todas as SPECs anteriores foram revisadas.
- [ ] **AC-03** — O fluxo principal funciona desde a abertura do app.
- [ ] **AC-04** — A navegação funciona.
- [ ] **AC-05** — O estado e a interação funcionam.
- [ ] **AC-06** — A validação do formulário funciona.
- [ ] **AC-07** — A persistência funciona conforme a SPEC-005.
- [ ] **AC-08** — A integração funciona ou falha com mensagem clara (SPEC-006).
- [ ] **AC-09** — Nenhum crash crítico no fluxo documentado.
- [ ] **AC-10** — A evidência final está completa.
- [ ] **AC-11** — O README da equipe está completo.
- [ ] **AC-12** — Nenhum segredo nem pasta gerada foi enviado.
- [ ] **AC-13** — Os requisitos principais são rastreáveis até o código e a evidência.
- [ ] **AC-14** — Cada integrante consegue explicar o projeto.

*(Marcar cada item só depois de validar.)*

## 12. Informações de submissão Git

- **Branch:** `team-03/sprint-07`
- **PR:** `[Sprint 07] Team 03 — Final Integration, Quality & Delivery`
- **Base:** `brenofeliix/mobile-development-2026-2`, branch `main`

## 13. Definition of Done

- [x] SPEC-007 escrita.
- [ ] Regressão executada.
- [ ] Problemas críticos corrigidos ou documentados.
- [x] README criado.
- [ ] Evidência final real e completa.
- [x] Repositório sem arquivos indevidos.
- [ ] Uso de IA documentado (falta a revisão da equipe na seção 10).
- [ ] PR final enviado até 23/11/2026.
