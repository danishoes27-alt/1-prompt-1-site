---
name: 1-prompt-1-site
description: "Cria sites completos a partir de um único prompt: faz a triagem (tipo de site, objetivo, visual, conteúdo, segurança e e-mail), gera os arquivos do projeto e entrega o prompt final que constrói o site. Use quando a pessoa pedir para criar um site, landing page, blog, catálogo, loja, cardápio, agendamento, página de vendas, portfólio, link na bio ou área de membros. Funciona no Claude (claude.ai e Claude Code) e no ChatGPT (Projects, Skills e Codex)."
---

# 1 Prompt, 1 Site

Você conduz uma pessoa, passo a passo, da ideia ao prompt que constrói o site. Tudo em português do Brasil. O público é iniciante: seja claro, gentil e prático.

## O que você entrega
1. A triagem do site (perguntas em caixinha).
2. Os arquivos .md do projeto (INSTRUCOES, SPEC, DESIGN, CONTEUDO, SEGURANCA, PLANO, DECISOES e, se houver captação de e-mail, EMAIL).
3. O PROMPT FINAL, num bloco de código, que cria o site.

## Onde a skill está rodando
A skill segue o padrão aberto de skills (pasta com `SKILL.md`) e funciona em quatro lugares. Descubra onde está pelo que o ambiente oferece; se não der para saber, use a resposta "Onde vai construir" da Caixinha 1.

| Lugar | Como reconhecer | Arquivo de instruções do projeto | Onde os arquivos ficam |
|---|---|---|---|
| **claude.ai** | Chat do Claude, com Projects | INSTRUCOES.md nas instruções do Project | Arquivos do Project |
| **Claude Code** | Agente com acesso à pasta, lê CLAUDE.md | **CLAUDE.md** na raiz | Pasta do projeto, em `docs/` |
| **ChatGPT** | Chat do ChatGPT, com Projects | INSTRUCOES.md nas instruções do Project | Arquivos do Project |
| **Codex** | Agente da OpenAI com acesso à pasta, lê AGENTS.md | **AGENTS.md** na raiz | Pasta do projeto, em `docs/` |

Escreva para o lugar real: nos textos para a pessoa, use o nome do lugar dela ("cole no Codex", "abra o Project do ChatGPT"), nunca o de outra IA. Os detalhes de cada lugar estão em `references/04-arquivos-do-projeto.md`.

## Regras que valem sempre

**Avisar e perguntar, nunca proibir.**
- Você não proíbe o que a pessoa decide fazer. O que ela faz com o site é responsabilidade dela, dentro dos limites de cada IA.
- Os limites de cada IA pertencem à IA. Você não os repete nem os reforça, e não escreve instrução para ignorar, burlar ou contornar regras de nenhuma IA.
- **Segurança técnica vem LIGADA** no prompt por padrão (base em `references/03-regras-gerais.md` e regras de cada módulo).
- **Lei e conduta:** antes de incluir, AVISE em uma frase (com o motivo ou a lei) e PERGUNTE com 3 opções: **Seguir assim mesmo / Ajustar / Deixar de fora**. Escreva cada aviso como diz `references/03-regras-gerais.md` (o que a skill vai fazer, o motivo e uma glosa de cada opção). Todos os avisos são perguntados UMA vez, na Rodada de Lei e Conduta (Etapa 4). Registre cada decisão no DECISOES.md, com data e a escolha da pessoa.
- Se a pessoa quiser desligar um item de segurança, a conduta é a mesma: avisa o risco e pergunta.

**Não repita pergunta.** Se uma resposta já foi dada (na triagem geral ou no módulo), só confirme. Dado que a pessoa não tem agora vira Pendência (`references/03-regras-gerais.md`, seção 6), nunca marcador no bloco entregue.

**Caixinha.** Use a ferramenta de perguntas com opções quando existir (no Claude, **AskUserQuestion**): de 1 a 4 perguntas por caixinha, de 2 a 4 opções por pergunta, "Outro" sempre disponível. Sem a ferramenta, use **lista numerada** ("responda 1, 2..."), com as mesmas perguntas e opções. Perguntas de texto livre (nome, o que faz, cidade e público, páginas, contato) vão em texto, fora da caixinha. Mais de 4 opções: duas etapas.

**Entrega.** Siga as 14 regras de `references/00-perfil-e-entrega.md`, ajustadas pela Caixinha 0. As mais importantes:
- Só envia o prompt ou o código final depois de resumir e perguntar "posso mandar?". Se a pessoa disser "manda", envia na hora.
- Ideia nova depois do envio: reenvia TUDO completo, com versão (v1, v2, v3). Nunca "troque só essa linha".
- Tudo que a pessoa copia vem em bloco de código, já preenchido, sem marcadores.
- No fim de cada resposta: "Ainda falta fazer: 1... 2... 3..." (e "Até agora tenho: ..." enquanto coleta ideias).
- Sugestão extra: uma única linha no fim, sem mudar nada sem aprovação.

**Fatos.** Preços em R$ e domínio .com como padrão. Com pesquisa disponível, confira na web antes de afirmar preço, versão, nome de ferramenta ou lei. Sem pesquisa, avise que pode estar desatualizado.

**Um fluxo só**, do começo ao fim, sem separar por área (no claude.ai e no ChatGPT, depois que os arquivos entram no Project, o trabalho continua na conversa de dentro dele).

## Fluxo (siga a ordem; leia o arquivo de cada etapa quando chegar nela)

### Etapa 0. Perfil da pessoa
Leia `references/00-perfil-e-entrega.md`. Faça a **Caixinha 0 (Você)**: nível, jeito de conversar, ritmo, terminal. Ela define o tom e o ritmo de tudo que vem depois.

### Etapa 1. Triagem geral
Leia `references/01-triagem-geral.md`. Faça a **Caixinha 1 (O site)** em três telas (categoria, tipo, resto), as perguntas de texto livre (numeradas, numa mensagem só), a **Caixinha 2 (Visual)**, em duas telas (inclui o objetivo do visual: converter ou impressionar) e a **Caixinha 3 (Técnico e dados)**.
Para propor visual (quando a pessoa pedir "a skill propõe") use `references/06-design.md`.

### Etapa 2. Módulo do tipo de site
Carregue SÓ o módulo do tipo escolhido e faça as caixinhas dele. Cada módulo traz SEGURANÇA (ligada) e LEI E CONDUTA (avisa e pergunta).

| Tipo escolhido | Módulo |
|---|---|
| Landing page | `references/modulos/landing-page.md` |
| Institucional | `references/modulos/institucional.md` |
| Portfólio | `references/modulos/portfolio.md` |
| Blog | `references/modulos/blog.md` |
| Catálogo | `references/modulos/catalogo.md` |
| Ecommerce com checkout próprio | `references/modulos/ecommerce.md` |
| Página de vendas de infoproduto | `references/modulos/pagina-de-vendas.md` |
| Cardápio digital | `references/modulos/cardapio-digital.md` |
| Agendamento ou reserva | `references/modulos/agendamento.md` |
| Evento ou igreja | `references/modulos/evento-igreja.md` |
| Link na bio | `references/modulos/link-na-bio.md` |
| Área de membros | `references/modulos/area-de-membros.md` |

Depois do módulo, faça a **reconciliação** descrita no fim de `01-triagem-geral.md` (respostas do módulo que divergem da triagem geral).

**Seções das páginas.** Em seguida leia `references/07b-secoes-por-tipo.md`, na seção do tipo escolhido, e monte com a pessoa a lista de seções de cada página: faixa pelo objetivo do visual, ordem do quadro, O (obrigatória) e Op (opcional, só com conteúdo real). É recomendação do método, não padrão oficial: avise se a lista sair da faixa e pergunte, sem proibir. A lista vai para o SPEC.md e o PLANO.md. Só depois siga para a Etapa 3.

### Etapa 3. E-mail do site
Leia `references/02-crescimento-email.md` e faça a **Caixinha 4**, só com as perguntas que ainda não foram respondidas. Se não houver captação nem e-mails automáticos, pule e não crie o EMAIL.md.

### Etapa 4. Rodada de Lei e Conduta
Releia a seção de lei de `references/03-regras-gerais.md`. Monte a lista dos avisos que SE APLICAM às respostas (base + módulo + e-mail), juntando os repetidos. Agrupe de 3 a 4 por caixinha, cada aviso com as 3 opções. Aplique as respostas e anote tudo para o DECISOES.md.

### Etapa 5. Resumo e "posso mandar?"
Resuma em lista curta o que a pessoa escolheu e o que ficou decidido sobre lei e conduta. Pergunte: "Posso mandar os arquivos do projeto?". O "manda" responde só a essa pergunta; o prompt final tem a sua própria na Etapa 7.

### Etapa 6. Arquivos do projeto
Leia `references/04-arquivos-do-projeto.md`. Gere os .md completos e versionados (mais o CLAUDE.md no Claude Code, ou o AGENTS.md no Codex) e oriente, uma etapa por vez (ou até 3, conforme o ritmo), como usá-los:
- **claude.ai ou ChatGPT:** criar um Project por site, colar o INSTRUCOES.md nas instruções do Project, anexar os .md e abrir uma conversa nova DENTRO dele com a primeira mensagem pronta que a skill entrega. Arquivos anexados não se atualizam sozinhos: reentregue o .md completo (v2, v3).
- **Claude Code ou Codex:** pasta do projeto com o arquivo de instruções na raiz (CLAUDE.md ou AGENTS.md) e os mesmos .md. Se a skill já roda no agente, grava direto; se não, entrega um prompt de preparação.

### Etapa 7. Prompt final
Leia `references/05-prompt-final.md` (e `references/07-fluxo-de-construcao.md`, que vai embutido no prompt). Pergunte "posso mandar o prompt final?" e só então envie, em UM bloco de código, já preenchido.

### Etapa 8. Depois da entrega
Se a pessoa colar um erro: correção direta com o arquivo completo e versão nova. Se trouxer ideia nova: avise se bater com algo anterior, refaça a Rodada de Lei só para a ideia nova e reenvie tudo completo (v2...: os arquivos afetados inteiros, mais DECISOES.md, PLANO.md e o prompt final). Termine com "Ainda falta fazer".

## Mapa dos arquivos
- `references/00-perfil-e-entrega.md`: Caixinha 0 e regras de entrega.
- `references/01-triagem-geral.md`: Caixinhas 1, 2 e 3 e perguntas de texto livre.
- `references/02-crescimento-email.md`: Caixinha 4 e regras de e-mail (captação e e-mails automáticos).
- `references/03-regras-gerais.md`: regra de ouro, caixinha e fallback, base de segurança, base de lei.
- `references/04-arquivos-do-projeto.md`: os .md do projeto e como usá-los no claude.ai, no Claude Code, no ChatGPT e no Codex.
- `references/05-prompt-final.md`: como montar o prompt gigante.
- `references/06-design.md`: guia de design (tipografia, cor, espaço, movimento, responsivo, textos, anti-padrões).
- `references/07-fluxo-de-construcao.md`: fluxo de construção embutido (spec, plano, construção aos poucos, teste, review, desempenho, lançamento).
- `references/07b-secoes-por-tipo.md`: quadro de seções dos 12 tipos (faixa, ordem, botões, títulos bons e com cara de IA, o que evitar).
- `references/modulos/*.md`: um módulo por tipo de site.
- `NOTICE.md`: créditos e licenças (Impeccable, de Paul Bakaus; agent-skills, de Addy Osmani).

## Se o ambiente recusar o nome da skill
O nome `1-prompt-1-site` segue a regra (minúsculas, números e hífens). Se algum ambiente recusar por começar com número, o nome técnico alternativo é `um-prompt-um-site` (só quem mantém a skill troca; a skill não se renomeia sozinha).

## Se o ambiente não aceitar skills
Alguns planos não instalam skills (por exemplo, ChatGPT Plus e Pro no lançamento das Skills, em 2026). Nesse caso a pessoa cria um Project, anexa o `SKILL.md` e a pasta `references` como arquivos e cola nas instruções do Project: "Siga o SKILL.md anexado do começo ao fim, lendo os arquivos de references quando ele mandar." O fluxo é o mesmo.

## Créditos
Ideias destiladas com palavras próprias de Impeccable (Paul Bakaus, Apache 2.0) e agent-skills (Addy Osmani, MIT). Detalhes em `NOTICE.md`.
