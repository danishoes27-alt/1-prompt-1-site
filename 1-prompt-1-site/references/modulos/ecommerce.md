# Módulo: Ecommerce (checkout próprio)

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 3 (E-commerce), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

Este módulo envolve pagamento, banco de dados e login. Conforme a Caixinha 0, explique em uma frase cada termo novo: "gateway" (serviço que cobra o cliente por você), "webhook" (aviso automático do gateway dizendo que o pagamento foi aprovado) e "sandbox" (ambiente de teste sem dinheiro de verdade). Quem escolheu "Técnico, sem explicar o básico" não precisa dessas frases.

Antes das caixinhas, faça UMA pergunta de duas opções (não é pergunta de lei): "Loja própria dá mais trabalho do que um catálogo com WhatsApp. Seguir com loja própria / Trocar para catálogo com WhatsApp". Se a pessoa trocar, mude para `catalogo.md`.

## CAIXINHA A (Venda)
1. **Tipo de produto:** Físico / Digital (download) / Serviço ou assinatura / Misto.
2. **Meios de pagamento (múltipla):** Pix / Cartão / Boleto / Parcelamento.
3. **Gateway:** Mercado Pago / Stripe / Asaas ou Efí / Ainda não escolhi, a skill indica.
   - "Ainda não escolhi, a skill indica": pesquise na web taxas, planos e meios aceitos atuais antes de citar. Sem pesquisa, siga a regra 13 de `00-perfil-e-entrega.md` (critérios e 2 ou 3 nomes conhecidos, sem taxa, "confira no site oficial"). Depois da indicação, pergunte qual a pessoa escolhe (mini-caixinha de 1 pergunta); se ela ainda não decidir, o plano registra "gateway a escolher" como Pendência e o prompt isola o pagamento atrás de uma camada trocável.
   - "Parcelamento" significa cartão em parcelas: pergunte em texto o máximo de parcelas.
4. **Entrega:** Correios ou transportadora (com cálculo de frete) / Entrega local / Retirada / Digital, sem frete.

## CAIXINHA B (Operação)
1. **Conta do cliente:** Compra sem cadastro / Com cadastro e login / Os dois.
2. **Estoque e pedidos (múltipla):** Controle de estoque / Painel de pedidos / Rastreio de entrega.
3. **E-mails automáticos (múltipla):** Confirmação de pedido / Pagamento aprovado / Envio / Carrinho abandonado.
4. **Promoções:** Cupom de desconto / Frete grátis acima de um valor / Os dois / Nenhum.

Os e-mails automáticos usam a ferramenta da Caixinha 4 (`02-crescimento-email.md`); não repita a pergunta de ferramenta, e na Caixinha 4 não pergunte de novo os e-mails já escolhidos aqui (inclusive "Carrinho abandonado").

Pergunte em texto os valores das promoções escolhidas: percentual ou valor do cupom e regras de uso; valor mínimo para frete grátis. Se a pessoa não tiver, vira Pendência.

## SEGURANÇA (vem ligada, além da base)
- O site não toca em dado de cartão: usa o checkout ou os campos hospedados do gateway.
- Pagamento confirmado só pelo webhook, com assinatura validada.
- Preço e total calculados no servidor (o navegador não decide o valor).
- Chaves secretas só no servidor, com ambiente de teste (sandbox) separado do de produção.
- Proteção contra pedido duplicado e trava de estoque no momento do pagamento.
- Login do cliente: senha com hash, limite de tentativas, sessão segura e CSRF; cada cliente só vê os próprios pedidos.
- Admin protegido, com verificação em duas etapas quando possível.
- Limite de tentativas no checkout e nos cupons.
- Logs sem dado de cartão.
- Backup do banco.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Direito de arrependimento de 7 dias** (CDC) e política de troca e devolução.
- **Dados obrigatórios da loja:** razão social ou nome, CNPJ ou CPF, endereço, contato, preço total com frete e prazos (decreto do e-commerce, 7.962/2013).
- **Política de privacidade, cookies e termos de uso** (LGPD).
- **Nota fiscal** depende do enquadramento (MEI, ME); indique conversar com o contador.
- **Alegação do produto** e produto regulado.
- **Fotos e textos de fornecedor** (direitos autorais).
- **Confirme o texto exato das leis na web antes de afirmar.**
