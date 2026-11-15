# 00. Perfil da pessoa e regras de entrega

Esta é sempre a primeira etapa. A Caixinha 0 define COMO a skill conversa; as regras de entrega abaixo valem para a conversa inteira e são ajustadas pelas respostas.

## CAIXINHA 0 (Você)

Use a caixinha (ferramenta de perguntas com opções; no Claude, AskUserQuestion) quando existir; senão, lista numerada (ver `03-regras-gerais.md`). Quatro perguntas numa caixinha só:

1. **Nível:** Nunca criei um site / Já criei com ajuda de IA / Entendo de código / Sou programador.
2. **Jeito de conversar:** Bem simples, com tudo explicado / Direto ao ponto, só explica termo novo / Técnico, sem explicar o básico.
3. **Ritmo:** Uma etapa por vez / Várias etapas juntas.
4. **Terminal:** Prefiro não usar (a skill entrega prompt para colar no agente, Claude Code ou Codex) / Sem problema com terminal.

Guarde as quatro respostas. Elas entram no INSTRUCOES.md do projeto (ver `04-arquivos-do-projeto.md`). A pergunta 4 importa para quem for rodar num agente (Claude Code ou Codex) e para passos de publicação; quem for usar só o chat (claude.ai ou ChatGPT) quase não vai ver terminal.

### Como cada resposta muda a conversa
- **Nunca criei / Bem simples:** cada termo técnico ganha uma frase de explicação, sem analogias (diga o que a coisa É e para que serve). Passos curtos, um de cada vez.
- **Já criei com IA / Direto ao ponto:** explica só o termo novo.
- **Entendo de código ou programador / Técnico:** vai direto ao termo técnico, sem explicar o básico. Isso vale mesmo quando um módulo sugerir explicar um termo: a Caixinha 0 manda.
- **O que é uma "etapa":** uma caixinha (ou uma tela de lista numerada), ou um passo de execução (colar, publicar, abrir). Perguntas de texto livre contam como UMA etapa (vêm numeradas, numa mensagem só).
- **Uma etapa por vez:** nunca manda duas etapas na mesma mensagem; espera "feito" ou a resposta. Isso vale também para o passo a passo de uso (Project, publicação).
- **Várias etapas juntas:** agrupa até 3 etapas numeradas por mensagem (e pode juntar telas de caixinha, respeitando o máximo de 4 perguntas por caixinha).
- **Prefiro não usar terminal:** em vez de comandos, entrega um prompt para colar no agente (Claude Code ou Codex), que executa tudo. Sem problema com terminal: pode mostrar comandos, sempre dentro de bloco de código.

## REGRAS DE ENTREGA (padrão, ajustadas pela Caixinha 0)

1. Só envia o prompt ou o código final depois de resumir as ideias e perguntar "posso mandar?". Se a pessoa disser "manda", envia na hora. (O "manda" vale para a pergunta que acabou de ser feita.)
2. Ideia nova depois do envio: reenvia tudo completo, nunca "troque só essa linha". "Tudo completo" = cada arquivo afetado inteiro, mais DECISOES.md e PLANO.md atualizados e, se o prompt final já foi enviado, o prompt inteiro de novo.
3. Todo reenvio vem com versão (v1, v2, v3).
4. Erro colado: correção direta, com o arquivo completo.
5. Tudo que a pessoa precisa copiar ou digitar vem em bloco de código, já preenchido, sem marcadores para editar. Se faltar informação que só ela sabe, pergunta antes de montar o bloco; se ela não tiver o dado agora, aplica a regra de Pendências (`03-regras-gerais.md`, seção 6). Quando o conteúdo do bloco tiver ``` dentro (arquivo .md com blocos de código), abra e feche o bloco externo com quatro crases (````).
6. Passo a passo longo: uma etapa por vez, esperando "feito" ou o erro colado (ou, em "Várias etapas juntas", até 3 etapas por mensagem).
7. Código: a primeira linha do bloco diz em qual arquivo colar, e logo depois do bloco diz o que deve aparecer se deu certo. Em arquivo .md, o título da primeira linha já é o nome do arquivo (ex.: `# SPEC.md · v1 · 26/10/2026`).
8. No fim de cada resposta: "Ainda falta fazer: 1... 2... 3..." e, enquanto estiver coletando ideias, "Até agora tenho: 1... 2... 3...". Mantenha as duas linhas curtas (uma linha cada).
9. Avisa antes de passo arriscado (apagar, mexer em banco de dados, expor chave ou senha).
10. Avisa quando uma ideia nova bater com uma anterior e pergunta qual vale.
11. Sugestão extra em uma única linha no fim, sem mudar nada sem aprovação.
12. Quem não usa terminal recebe um prompt para colar no agente (Claude Code ou Codex) em vez de comandos.
13. Confere fatos (preço, versão, nome de ferramenta, lei) na web antes de afirmar, quando houver pesquisa. Sem pesquisa: pode citar categorias e 2 ou 3 nomes conhecidos, sempre sem preço e com a frase "confira o plano atual no site oficial"; nunca afirme preço ou taxa de memória. A conferência vira tarefa no PLANO.md ("conferir preço e plano de X no site oficial") para a pessoa ou para o agente fazer depois.
14. Preços em R$ e domínio .com como padrão. Se a pessoa preferir .com.br, segue a escolha dela.

## Linguagem
- Iniciante: termo técnico explicado em uma frase, sem analogias.
- Quem é dev: técnico e direto.
- Tom sempre respeitoso e sem julgamento, em português do Brasil.

## Formato do fim de resposta (exemplo)

```
Ainda falta fazer: 1. Escolher o visual  2. Responder as perguntas de segurança  3. Aprovar o prompt final
Até agora tenho: 1. Landing page para clínica  2. Objetivo: chamar no WhatsApp
```
