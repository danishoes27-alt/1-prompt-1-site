# Módulo: Área de membros

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 12 (Área de membros), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

**Nota:** montar login, assinatura e vídeos protegidos por conta própria é a parte mais difícil entre todos os tipos de site. Se a pessoa não quiser fazer isso, indique o caminho com plataforma pronta (Cakto, Hotmart, Kiwify, entre outras; confira recursos e taxas atuais na web) e adapte a triagem: o site passa a ser uma página de vendas (`pagina-de-vendas.md`) que leva para a área da plataforma. Pergunte qual caminho ela prefere antes de seguir.

## CAIXINHA (Área de membros)
1. **Conteúdo:** Aulas em vídeo / Arquivos e PDFs / Comunidade ou fórum / Ferramentas ou templates.
2. **Como entra:** Cadastro livre / Só quem comprou / Convite / Assinatura.
3. **Pagamento:** Compra única / Assinatura mensal / Assinatura anual / Gratuito.
4. **Recursos (múltipla):** Progresso das aulas / Certificado / Comentários e dúvidas / Níveis de acesso.

## SEGURANÇA (vem ligada, além da base)
- Login com senha com hash, limite de tentativas, sessão segura, CSRF e verificação em duas etapas opcional, com checagem de acesso no servidor em cada rota.
- Acesso liberado só após webhook do gateway com assinatura validada, e cortado quando a assinatura vence ou há estorno.
- Vídeos e arquivos em armazenamento privado, com link assinado e de curta duração.
- Limite de dispositivos e de sessões simultâneas.
- Cada membro só vê os próprios dados.
- Recuperação de senha com token único e validade, e e-mail de confirmação no cadastro.
- Comentários e fórum com sanitização do HTML, anti-spam e moderação.
- Painel de admin com papéis, logs de acesso e backup.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Dados dos membros** (nome, e-mail, progresso, pagamento) com política de privacidade e consentimento (LGPD).
- **Assinatura com renovação clara, cancelamento fácil e política de reembolso**, com direito de arrependimento de 7 dias (CDC).
- **Termos de uso** sobre compartilhar conta e redistribuir conteúdo.
- **Direitos autorais** de material, vídeo e música.
- **Promessa de resultado e certificado:** certificado de curso livre não é diploma; avise para não induzir a erro e pergunte como quer escrever.
- **Identificação de quem vende.**
