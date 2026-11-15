# 1 Prompt, 1 Site (skill)

Skill de IA que faz a triagem do seu site (tipo de site, objetivo, visual, conteúdo, segurança e e-mail), gera os arquivos .md do projeto e entrega um único prompt final que constrói o site. Funciona no Claude (claude.ai e Claude Code) e no ChatGPT (Projects, Skills e Codex).

Faz parte do ebook "Você a 1 Prompt do Seu Site: Com Cara de Marca, Não de IA".

## Baixar

Baixe a última versão pelo link direto:

https://github.com/danishoes27-alt/1-prompt-1-site/releases/latest/download/1-prompt-1-site.zip

Todas as versões ficam na página Releases deste repositório.

## Instalar

claude.ai: abra Personalização, depois Skills, escolha enviar uma skill e selecione o arquivo 1-prompt-1-site.zip.

Claude Code: descompacte o zip dentro da pasta de skills (no Windows, %USERPROFILE%\.claude\skills). O resultado precisa ser .claude\skills\1-prompt-1-site\SKILL.md. A skill nova aparece a partir da próxima mensagem ou de uma sessão nova.

Codex (app do ChatGPT no computador, Codex CLI ou extensão de IDE): descompacte o zip na pasta de skills do usuário. O resultado precisa ser ~/.agents/skills/1-prompt-1-site/SKILL.md (no Windows, %USERPROFILE%\.agents\skills\1-prompt-1-site\SKILL.md). No projeto, o arquivo de instruções do Codex é o AGENTS.md, e a skill gera esse arquivo.

ChatGPT com Skills (planos de empresa e educação): abra Skills e envie o arquivo, se o seu plano mostrar essa opção.

ChatGPT sem Skills (Plus e Pro, por exemplo): crie um Project, anexe o SKILL.md e os arquivos da pasta references, e cole nas instruções do Project: "Siga o SKILL.md anexado do começo ao fim, lendo os arquivos de references quando ele mandar."

## Avisos

- As faixas de seções e as ordens por tipo de site são recomendação do método, não padrão oficial, e a skill não promete resultado.
- A skill avisa sobre lei e conduta e pergunta o que fazer, mas isso não é aconselhamento jurídico.

## Licença e créditos

MIT (arquivo LICENSE). A skill destila, com palavras próprias, ideias de Impeccable (Paul Bakaus, Apache 2.0) e agent-skills (Addy Osmani, MIT). Detalhes em 1-prompt-1-site/NOTICE.md.
