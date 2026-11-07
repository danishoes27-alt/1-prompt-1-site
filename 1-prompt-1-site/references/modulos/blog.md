# Módulo: Blog

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 10 (Blog), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

## CAIXINHA (Blog)
1. **Assunto:** Pessoal ou lifestyle / Negócio ou marca / Notícias e opinião / Tutoriais e educação.
2. **Quem publica:** Só eu / Eu e mais pessoas / Convidados enviam artigos.
3. **Como publica:** Peço pra IA publicar / Painel de admin com editor / Escrevo em arquivos Markdown.
4. **Recursos (múltipla):** Categorias e tags / Busca / Comentários / Newsletter (ligada à Caixinha 4, em `02-crescimento-email.md`).

Explique "Markdown" e "painel de admin" em uma frase para iniciante. Sem painel (IA publica ou arquivos Markdown), as regras de painel abaixo não se aplicam; entram só quando houver painel, login, comentários ou envio de artigos.

## SEGURANÇA (vem ligada, além da base)
- Painel de admin com senha com hash, limite de tentativas, sessão segura e verificação em duas etapas quando possível.
- Rota de login fora do menu público.
- Permissões por papel (autor, editor, administrador).
- Sanitização do HTML do editor (contra XSS).
- Proteção contra injeção na busca.
- CSRF (token em formulários que alteram dados).
- Upload validado por tipo e tamanho, imagens sem metadados.
- Comentários com anti-spam, limite por pessoa e moderação.
- Rascunhos e versões dos artigos.
- Backup do banco e das imagens.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Direitos autorais** de texto, imagem, fonte e vídeo de terceiros.
- **Publicidade e parceria paga** identificadas (CONAR e CDC).
- **Responsabilidade por comentário ofensivo ou ilegal:** termos de uso e canal de denúncia.
- **Conteúdo de saúde, finanças e direito:** sem promessa de resultado e com aviso de que não substitui profissional.
- **Consentimento para newsletter e analytics** (LGPD).
