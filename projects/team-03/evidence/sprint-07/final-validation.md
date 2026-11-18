# Validação final — Wiflux (Team 03)

> **Este arquivo só deve ser preenchido com o que foi executado de verdade.** Campos entre `[ ]` ficam em branco até o teste ser feito. Não preencher com resultado suposto.

## Ambiente do teste

| Item | Informação |
| --- | --- |
| Quem executou | [ ] |
| Data do teste | [ ] |
| Dispositivo | [ ] (ex.: emulador Pixel, Android Studio) |
| Versão do Android / API | [ ] |
| Branch / commit testado | `team-03/sprint-07`, commit [ ] |
| Build (Make Project) | [ ] PASS / FAIL |
| App executa | [ ] PASS / FAIL |

## Roteiro de regressão (a partir de uma abertura limpa do app)

Antes de começar: fechar o app pelo multitarefa e abrir de novo.

| # | Passo | Resultado esperado | Resultado obtido | Observação |
| --- | --- | --- | --- | --- |
| 1 | Abrir o app | Abre na tela "Verificação de Sinal" sem travar | [ ] PASS / FAIL | |
| 2 | Tela principal | Medidor, chip "Aguardando", campo "Nome do cômodo", botão "Iniciar Verificação" e card "Últimas verificações" visíveis e legíveis | [ ] PASS / FAIL | |
| 3 | Nome válido + Wi-Fi conectado ("Sala" → Iniciar Verificação) | Aparece "Medindo sinal...", depois o dBm real e o status | [ ] PASS / FAIL | dBm obtido: [ ] |
| 4 | Nome curto ("ab") → Iniciar Verificação | Erro "Digite pelo menos 3 letras"; nada é medido nem salvo | [ ] PASS / FAIL | |
| 5 | Ver Detalhes e Voltar | Detalhes mostra o mesmo dBm; ao voltar, o nome continua no campo | [ ] PASS / FAIL | |
| 6 | Fechar o app e reabrir | O histórico continua com os registros | [ ] PASS / FAIL | |
| 7 | Desligar o Wi-Fi e medir | Mensagem vermelha clara; nada novo é salvo | [ ] PASS / FAIL | Mensagem: [ ] |
| 8 | Botão voltar do sistema | Na tela de detalhes volta para a inicial; na inicial sai do app | [ ] PASS / FAIL | |
| 9 | Crash | Nenhum fechamento inesperado em todo o roteiro | [ ] PASS / FAIL | |

## Evidências desta validação

| Arquivo | O que mostra | Origem |
| --- | --- | --- |
| `final-home.png` | Tela inicial do app | [ ] (data e quem tirou) |
| `final-feature.png` | Medição real com o histórico | [ ] (data e quem tirou) |

> Se forem reaproveitados prints de Sprints anteriores, escrever aqui de qual Sprint e de qual data eles vêm. Não dizer que foram tirados na data da regressão.

## Problemas encontrados

| Problema | Gravidade | O que foi feito (corrigido ou limitação conhecida) |
| --- | --- | --- |
| [ ] | [ ] | [ ] |

*(Se nenhum problema for encontrado, escrever "Nenhum" depois de executar o roteiro inteiro.)*

## Conclusão

[ ] Preencher só depois de executar os 9 passos.
