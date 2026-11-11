# Planejamento de testes E2E com IA

IA utilizada: Claude (Anthropic).

## Prompt utilizado

```
Sou estudante e preciso planejar testes E2E com Maestro para um app React
Native (Expo) chamado Crypto Alert. O app tem: lista de criptomoedas com
cotações, tela de conversão de moedas, criação de alertas de preço
(condição acima/abaixo de um valor) e lista de alertas com estado vazio.
Proponha 8 cenários de teste E2E, com: nome, objetivo, pré-condições,
passos e resultado esperado. Inclua caminhos felizes e de erro. Avise onde
você está assumindo algo sobre a interface.
```

## Resposta original da IA

1. **Abrir o app e exibir a lista de criptomoedas.** Esperado: lista com criptomoedas, preço e variação de 24h visíveis.
2. **Estado vazio da lista de alertas.** Esperado: mensagem de estado vazio e botão para criar alerta.
3. **Criar alerta de preço (condição "acima de").** Esperado: volta à lista e o alerta aparece com valor formatado.
4. **Criar alerta de preço (condição "abaixo de").** Esperado: alerta exibido com a condição correta.
5. **Validação do formulário com campos vazios (erro).** Esperado: botão bloqueado ou mensagem de erro; nenhum alerta criado.
6. **Excluir um alerta.** Esperado: alerta some e o estado vazio volta a aparecer.
7. **Conversão de moedas com valor válido.** Esperado: resultado convertido exibido.
8. **Conversão com valor inválido (erro).** Esperado: mensagem de erro e nenhum resultado.

A IA avisou que os textos e nomes de botões eram suposições a confirmar no app real.

## Cenários selecionados

Foram selecionados quatro cenários para os testes E2E:

1. Abrir o app e exibir a lista de criptomoedas.
2. Verificar o estado vazio da lista de alertas.
3. Criar um alerta de preço.
4. Verificar a validação do formulário vazio.

O cenário de exclusão de alerta foi deixado de fora do planejamento dos fluxos implementados.

## Análise crítica

- **Aproveitado:** Foram aproveitadas as sugestões da IA para testar a lista de criptomoedas, o estado vazio dos alertas, a criação de um alerta e a validação do formulário. Esses cenários representam funcionalidades importantes do aplicativo.

- **Corrigido:** Os textos e nomes dos botões sugeridos pela IA foram conferidos com o código-fonte do aplicativo. Foram utilizados os textos encontrados no projeto, como "Alerts", "New Alert", "Create Alert" e "Save Alert", em vez de considerar os nomes sugeridos pela IA como se já estivessem confirmados.

- **Descartado:** Os cenários de conversão de moedas e exclusão de alerta não foram incluídos nos quatro fluxos preparados. A conversão foi deixada de fora porque envolve valores de cotação que podem variar. A exclusão também ficou fora do escopo dos testes preparados nesta etapa.