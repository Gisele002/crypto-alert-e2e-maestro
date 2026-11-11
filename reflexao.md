# Reflexão: GenIA-E2ETest

## 1. Qual problema a abordagem GenIA-E2ETest procura resolver?

Testar software manualmente demora e é fácil errar. As ferramentas de IA que geram testes costumam focar em testes unitários e deixam de lado os testes end-to-end (E2E), que validam o fluxo completo do usuário, da entrada de dados até a resposta final do sistema. O GenIA-E2ETest tenta resolver isso gerando scripts E2E executáveis a partir de descrições em linguagem natural, diminuindo o esforço manual.

## 2. Como a IA generativa pode ajudar na criação de testes E2E?

A IA pode transformar uma descrição simples, como "o usuário abre o app e cria um alerta de preço", em um rascunho de script. Ela também ajuda a levantar cenários que eu talvez não lembrasse, como casos de erro, e acelera o trabalho repetitivo. Isso facilita o início para quem ainda não domina a ferramenta de testes.

## 3. Quais limitações ou riscos existem ao usar testes gerados por IA?

O próprio artigo aponta sensibilidade a navegação que depende de contexto e a conteúdo dinâmico. Outros riscos: a IA pode inventar botões, textos ou telas que não existem no app, escrever verificações fracas (que passam sempre) e dar uma falsa sensação de que o app está bem coberto.

## 4. Por que um teste gerado por IA ainda precisa de revisão humana?

Porque a IA não enxerga o aplicativo real. Só uma pessoa consegue conferir se os seletores existem, se o resultado esperado faz sentido para o negócio e se o teste realmente falharia quando houvesse um bug. No artigo, mesmo com bons resultados, ainda foi necessária uma média de cerca de 10% de modificação manual nos scripts.

## 5. Como o Maestro pode ser usado para validar um fluxo sugerido por uma IA?

Eu transformo a sugestão da IA em um arquivo YAML e executo no emulador com `maestro test`. Se um texto ou botão não existir, o teste quebra e eu sei exatamente onde corrigir. Com o `maestro studio` consigo inspecionar a tela real e ajustar os seletores. Assim, a sugestão da IA vira um teste confiável só depois de ser validada na prática.
