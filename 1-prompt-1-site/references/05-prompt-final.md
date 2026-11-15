# 05. Prompt final (o PROMPT GIGANTE)

É a entrega principal da skill: um único prompt que cria o site. Ele vem dentro de UM bloco de código (quatro crases se tiver ``` dentro), para a pessoa copiar de uma vez, já preenchido, sem marcadores para editar (regra 5 de entrega). Se faltar informação que só a pessoa sabe, pergunte antes; se ela não tiver agora, use a regra de Pendências (`03-regras-gerais.md`, seção 6).

## Antes de enviar
1. Os .md de `04-arquivos-do-projeto.md` JÁ foram entregues na etapa anterior. O prompt diz a mesma coisa que eles. Se os dois divergirem, vale o DECISOES.md mais recente, e o prompt manda a IA parar e perguntar quando notar divergência.
2. Resuma as ideias e decisões em lista curta ("Até agora tenho...").
3. Pergunte: **"Posso mandar o prompt final?"** Só envia depois do sim (ou de "manda", que vale para esta pergunta).
4. Versione: o primeiro é v1. Ideia nova → reenvia tudo completo como v2, v3.

## Ordem das partes do prompt (mantenha as 10 partes)

O prompt final tem 10 partes. "Seção" fica reservada para os blocos do site (hero, perguntas frequentes...).

1. **Contexto do negócio:** nome, o que faz, cidade, público, tom de voz, contato.
2. **SPEC:** tipo de site, objetivo principal, páginas e, para cada uma, a faixa de seções e a lista de seções na ordem de `07b-secoes-por-tipo.md`, respostas do módulo (cada opção marcada), domínio e hospedagem.
3. **Design:** identidade (cores com códigos, fontes), estilo, objetivo do visual (converter ou impressionar), animações, referências, regras de `06-design.md` (contraste, responsivo, textos de interface, anti-padrões a evitar).
4. **Conteúdo:** textos de cada página e de cada seção, no estilo do exemplo "bom" do tipo (`07b-secoes-por-tipo.md`); lista de fotos com nomes de arquivo e quais são provisórias; avisos de "imagem ilustrativa" quando for o caso.
5. **Segurança do tipo:** a base de `03-regras-gerais.md` mais as regras do módulo, escritas como itens a implementar e conferir.
6. **Avisos de lei já decididos:** cada decisão da Rodada de Lei e Conduta, na forma final que a pessoa escolheu (Seguir assim mesmo / Ajustar / Deixar de fora), com o texto a incluir no site (política de privacidade, aviso de cookies, termos, identificação, política de troca, etc., a partir da estrutura mínima de `03-regras-gerais.md`, marcados como modelo para revisão profissional). O que ficou de fora é dito como "não incluir".
7. **E-mail:** formulário, e-mail de boas-vindas, ferramenta, SPF/DKIM/DMARC, consentimento. Sem e-mail no projeto, mantenha a parte com a frase "Não se aplica a este site".
8. **Fluxo de construção:** o resumo de `07-fluxo-de-construcao.md` (especificar, planejar, construir aos poucos, testar, revisar, desempenho, lançar). O prompt pede para a IA mostrar o plano de tarefas e ir uma tarefa por vez.
9. **Critérios de pronto:** lista conferível (páginas existem; objetivo principal funciona; formulário valida no servidor; sem erro no console; contraste ok; celular ok; Core Web Vitals em "bom"; segurança conferida; decisões de lei aplicadas; pendências listadas; checklist go/no-go).
10. **Entrega:** depende de onde roda (abaixo).

### Tarefa 1 do prompt: tecnologia e hospedagem
Se a triagem não fechou a tecnologia e a hospedagem, a Tarefa 1 do plano é "propor e confirmar com a pessoa". Regra de escolha: site sem login, pagamento, banco ou painel → site estático (HTML, CSS e JavaScript) com serviço de formulário; site com qualquer um desses → site com servidor, escolhido na Tarefa 1, com a hospedagem que a pessoa tiver e aprovação dela antes de construir. O prompt diz isso com a recomendação já preenchida (nunca "escolha a tecnologia" solto).

### Pendências e conferências de fatos dentro do prompt
- Dado que a pessoa não tinha: arquivo de configuração único, recurso oculto até preencher, pendência listada na parte 9.
- Fato que dependia de pesquisa (preço, plano, meta de desempenho, texto de lei) e não foi conferido: vira tarefa de conferência no plano ("conferir X na fonte oficial antes de publicar").

## Final do prompt depende de onde roda

**Claude Code ou Codex** (a pessoa escolheu um agente na Caixinha 1):
- O prompt pede para criar os arquivos do site NA PASTA DO PROJETO (estrutura de pastas definida no próprio prompt), rodar o site localmente para testar e mostrar como abrir.
- Pede para criar/atualizar o arquivo de instruções (CLAUDE.md no Claude Code, AGENTS.md no Codex), os .md do projeto e manter o PLANO.md em dia.
- Se a pessoa prefere não usar terminal: o prompt diz que o agente executa tudo e que ela só precisa aprovar e abrir o endereço local que ele indicar.

**claude.ai ou ChatGPT** (a pessoa escolheu o chat):
- O prompt pede os arquivos prontos para baixar (HTML, CSS, JS e imagens provisórias), em artefato ou arquivo quando o ambiente permitir, e o **passo a passo para publicar** (hospedagem da triagem, domínio, HTTPS), uma etapa por vez.
- Se o ambiente NÃO gerar arquivo para baixar: o prompt manda entregar cada arquivo num bloco de código com o nome na primeira linha, em ordem, poucos por mensagem, e a pessoa salva cada um na pasta combinada. Imagens provisórias são geradas pelo próprio código (cores e formas) e as fotos reais a pessoa coloca numa pasta `imagens/` com os nomes do CONTEUDO.md.
- Onde o site precisa de servidor (login, pagamento, banco, painel), o chat entrega o código e as instruções, mas a pessoa precisa de uma hospedagem que rode servidor; a skill indica o caminho (ou uma plataforma pronta) e registra a escolha.

## Cuidados ao montar
- Linguagem do prompt: português do Brasil, imperativa e específica ("Crie", "Use", "Valide no servidor").
- Nada de segredo dentro do prompt (chaves, senhas): use nomes de variáveis de ambiente e explique onde a pessoa cadastra os valores.
- Preços em R$; domínio .com como padrão.
- Não inclua instruções para ignorar ou contornar regras de nenhuma IA. O prompt descreve o site e o processo; os limites de cada IA continuam sendo da IA.
- Fatos de ferramentas (planos, versões) conferidos na web quando houver pesquisa; sem pesquisa, regra 13 de entrega.
- Tamanho: o prompt pode ser longo, mas organizado em títulos e listas, sem repetir a mesma regra em partes diferentes (a parte 5 detalha a segurança; as outras só apontam para ela).

## Esqueleto do prompt (use como base e preencha tudo)

```
# PROMPT FINAL v1 · Nome do Site

Você vai construir um site completo, seguindo este documento. Trabalhe uma tarefa por vez e confira cada uma antes de seguir.

## 1. Contexto do negócio
...
## 2. SPEC
...
## 3. Design
...
## 4. Conteúdo
...
## 5. Segurança (vem ligada)
...
## 6. Lei e conduta: decisões já tomadas
...
## 7. E-mail
...
## 8. Fluxo de construção
...
## 9. Critérios de pronto
...
## 10. Entrega
(Claude Code ou Codex: criar os arquivos na pasta do projeto / claude.ai ou ChatGPT: arquivos para baixar e passo a passo para publicar)
```

(No prompt entregue, troque o nome do site e todos os "..." pelo conteúdo real. Nenhum marcador pode sobrar.)

## Depois de entregar
- Pergunte se funcionou. Se a pessoa colar um erro: correção direta, com o arquivo completo e a versão nova.
- Termine com "Ainda falta fazer: ..." (regra 8).
