# Módulo: Landing page

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 2 (Landing page), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

## CAIXINHA (Landing page)
1. **Oferta:** Produto físico / Serviço / Infoproduto (curso, ebook) / Evento ou lançamento.
2. **Ação principal:** Chamar no WhatsApp / Formulário de captura / Link de compra / Agendar.
3. **Seções (múltipla):** Depoimentos / Perguntas frequentes / Preços / Vídeo.
4. **Prova social:** Tenho depoimentos reais / Ainda não tenho.

Se a "Ação principal" coincidir com o "Objetivo principal" da triagem geral, só confirme em vez de perguntar de novo. Se o negócio for de profissão regulamentada (saúde, advocacia etc.), colete o aviso da base (item 4 de `03-regras-gerais.md`) sobre publicidade, preços e depoimentos, e o de dado de saúde no formulário.

Dicas de estrutura: uma página, uma ação principal repetida em pontos-chave (início, meio, fim), promessa clara na primeira tela e botão com verbo de ação. Se a pessoa escolher "Infoproduto" com venda direta, sugira o módulo `pagina-de-vendas.md`, que é mais completo, e pergunte qual prefere.

## SEGURANÇA (vem ligada, além da base)
- Formulário com anti-spam (campo invisível ou captcha) e validação no servidor.
- Chave de API, webhook e senha fora do código visível (variáveis de ambiente no servidor).
- Botão de WhatsApp e links de compra apontam só para endereços https definidos pelo dono.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Consentimento e política de privacidade ligados ao formulário (LGPD).** Aviso: "Formulário que coleta nome, e-mail ou telefone precisa explicar o uso do dado e pedir aceite (LGPD)."
- **Depoimento inventado ou número de clientes sem comprovação** (propaganda enganosa, CDC). Se a pessoa marcar "Ainda não tenho" depoimentos e quiser a seção mesmo assim, colete o aviso e pergunte na Rodada, escrito assim: "Atenção: depoimento inventado pode ser enganoso e gerar problema com o Código de Defesa do Consumidor, além de derrubar a confiança no site. **Seguir assim mesmo** (usar do jeito que está) / **Ajustar** (trocar por depoimentos reais) / **Deixar de fora** (tirar essa seção)." Se a pessoa escolher "Ajustar", o prompt inclui a seção oculta até os depoimentos reais (e autorizados) chegarem; isso vira Pendência.
- **Pixel e analytics só depois do aceite de cookies** (LGPD). Pergunte se quer o aviso de cookies com aceite antes de ligar a medição.
