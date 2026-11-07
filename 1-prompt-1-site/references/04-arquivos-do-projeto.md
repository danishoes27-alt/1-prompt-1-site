# 04. Arquivos do projeto (.md)

No fim da triagem, depois da Rodada de Lei e Conduta e do "posso mandar os arquivos?", a skill gera estes arquivos COMPLETOS e VERSIONADOS (v1, v2...). Cada arquivo abre com o título que já é o nome dele, a versão e a data (ex.: `# SPEC.md · v1 · 26/10/2026`). Entregue cada um em bloco de código (se o arquivo tiver blocos ``` dentro, use quatro crases no bloco externo). Confira a data atual; se não souber, pergunte.

## Os arquivos

| Arquivo | O que tem |
|---|---|
| **INSTRUCOES.md** | Como a skill conversa e entrega neste projeto: as respostas da Caixinha 0 (nível, jeito, ritmo, terminal) e as 14 regras de entrega de `00-perfil-e-entrega.md`, já ajustadas. |
| **SPEC.md** | A triagem completa: tipo de site, objetivo, onde roda, conteúdo, páginas (cada uma com a faixa de seções escolhida e a lista de seções na ordem de `07b-secoes-por-tipo.md`, O/Op, e o que ficou de fora), contato, tom de voz, respostas do módulo, domínio, hospedagem, analytics, anúncios, dados do visitante, critérios de pronto. |
| **DESIGN.md** | Identidade (logo, cores com códigos e checagem de contraste, fontes), referências e o que a pessoa gostou nelas, estilo, objetivo do visual (converter ou impressionar), nível de animações, regras de `06-design.md` aplicadas. |
| **CONTEUDO.md** | Textos de cada página e seção (a IA escreve o que faltar, marcado como "rascunho para aprovar") e a lista de fotos e imagens com nome de arquivo combinado, dizendo o que é real e o que é provisório. |
| **SEGURANCA.md** | A base de segurança de `03-regras-gerais.md` mais as regras de segurança do módulo do tipo, em lista de conferência. |
| **PLANO.md** | Tarefas pequenas em ordem (uma por página ou por grupo de seções), o que já foi feito e o que falta, as pendências da pessoa e as conferências de fatos (`07-fluxo-de-construcao.md`). |
| **DECISOES.md** | Histórico de mudanças e versões, decisões de lei e conduta e decisões de segurança, cada uma com data, o aviso dado e a escolha da pessoa. |
| **EMAIL.md** | Só se houver e-mails (captação ou automáticos): ferramenta, isca, formulário, textos dos e-mails, SPF/DKIM/DMARC, regras de consentimento. |
| **CLAUDE.md** | Só para quem roda no Claude Code: fica na raiz da pasta do projeto (modelo abaixo). Não faz parte da lista de arquivos do Project do claude.ai. |

### Estrutura mínima de cada arquivo
- **INSTRUCOES.md:** perfil da pessoa (4 respostas) · como conversar · regras de entrega · "o projeto tem estes arquivos: ...".
- **SPEC.md:** resumo do site · objetivo · páginas e, para cada uma, faixa de seções e lista de seções na ordem do quadro (O/Op, o que ficou de fora) · respostas do módulo · técnico (domínio, hospedagem, analytics, anúncios, dados) · limites (o que NÃO entra) · critérios de pronto.
- **DESIGN.md:** identidade · cores e contraste · fontes · estilo · objetivo do visual · animações · referências · o que evitar.
- **CONTEUDO.md:** por página: título, textos, botões · lista de imagens (arquivo, descrição, real ou provisória) · pendências de conteúdo.
- **SEGURANCA.md:** base ligada (lista com caixas de marcar) · regras do módulo · decisões de segurança que a pessoa tomou.
- **PLANO.md:** tabela com `ID | Tarefa | Critério de aceite | Status (a fazer, fazendo, feita)` · seção "Pendências da pessoa" · seção "Conferências na web".
- **DECISOES.md:** modelo abaixo.

Modelo do DECISOES.md:

```
# DECISOES.md · v1 · 26/10/2026

## Decisões de lei e conduta
| Data | Assunto | Aviso dado | Escolha da pessoa |
|---|---|---|---|
| 26/10/2026 | Depoimentos | Depoimento inventado pode ser enganoso (CDC) | Deixar de fora |

## Decisões de segurança
| Data | Item | Risco avisado | Escolha da pessoa |
|---|---|---|---|

## Histórico de versões
- v1 (26/10/2026): triagem inicial.
```

## Se a pessoa roda no claude.ai
Oriente UMA etapa por vez (ou até 3 por mensagem em "Várias etapas juntas"), esperando "feito" a cada uma:
1. Criar um **Project** para este site. Project é um espaço do claude.ai que guarda instruções e arquivos para todas as conversas de um mesmo assunto. Projects estão disponíveis em todos os planos, inclusive no grátis, que tem limite de cinco projetos (confira o limite atual na ajuda oficial do claude.ai, quando houver pesquisa).
2. Abrir as instruções do Project e colar o texto do **INSTRUCOES.md**.
3. Anexar os outros .md (SPEC, DESIGN, CONTEUDO, SEGURANCA, PLANO, DECISOES e, se houver, EMAIL) nos arquivos do Project.
4. Abrir uma conversa nova DENTRO do Project e colar esta primeira mensagem, que a skill entrega pronta em bloco de código: "Leia os arquivos do projeto e me entregue o prompt final do site (versão atual)." A partir daí, o fluxo segue nessa conversa (um fluxo só, sem separar por área): o prompt final, os ajustes e as novas versões saem dela.
5. Avisar: **arquivos anexados não se atualizam sozinhos.** Quando algo mudar (nova decisão, novo texto, tarefa concluída), a skill reentrega o(s) .md COMPLETO(S) afetado(s) com nova versão (v2, v3), mais DECISOES.md e PLANO.md; a pessoa substitui o arquivo antigo no Project (mesmo nome de arquivo; a versão aparece no título).
Se a conversa nova dentro do Project não tiver a skill, os arquivos do Project bastam: o INSTRUCOES.md carrega as regras de entrega e os outros arquivos carregam o projeto.

## Se a pessoa roda no Claude Code
- Pasta do projeto com **CLAUDE.md na raiz** e os mesmos .md (de preferência numa subpasta `docs/`). O INSTRUCOES.md também vai para essa pasta, e o CLAUDE.md manda ler o INSTRUCOES.md no começo de cada sessão (assim o perfil da Caixinha 0 não se perde).
- **Se a skill já roda DENTRO do Claude Code**, ela grava os arquivos direto na pasta do projeto (peça permissão e mostre a lista do que vai criar). A pessoa não copia nada.
- **Se a skill roda fora** (claude.ai) e a pessoa vai usar o Claude Code: quem não usa terminal recebe UM prompt de preparação, em bloco de código, que pede ao Claude Code para criar a pasta, o CLAUDE.md e todos os arquivos, com o conteúdo de cada um já embutido no prompt. Explique em uma etapa: abrir uma pasta vazia no Claude Code e colar o prompt. Se o prompt ficar longo demais, divida em dois ou três prompts numerados.

Modelo mínimo do CLAUDE.md do site (entregue sem marcadores: troque o nome pelo real):

```
# Projeto: Nome do Site
## Leia primeiro
docs/INSTRUCOES.md (perfil da pessoa e regras de entrega) e docs/SPEC.md, DESIGN.md, CONTEUDO.md, SEGURANCA.md, PLANO.md, DECISOES.md.
## Fluxo obrigatório
1. Especificar (SPEC.md). 2. Planejar (PLANO.md). 3. Construir uma tarefa por vez. 4. Testar. 5. Revisar.
## Regras
- Segurança vem ligada (SEGURANCA.md). Lei e conduta: avisa e pergunta, registra em DECISOES.md.
- Chaves e senhas só no servidor. Nenhum dado de cartão no site.
- Atualizar PLANO.md ao terminar cada tarefa.
```

## Um fluxo só
Todo o processo (triagem, arquivos, prompt, ajustes) segue como UM fluxo, sem separar por área. No claude.ai, a triagem acontece num chat e, depois que os arquivos estão no Project, o trabalho continua na conversa de dentro do Project (passo 4). Ideias novas geram reentrega versionada.
