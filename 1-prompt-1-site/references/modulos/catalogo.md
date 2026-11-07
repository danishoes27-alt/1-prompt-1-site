# Módulo: Catálogo

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 1 (Catálogo), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

Quem quer pagamento com carrinho e checkout próprio dentro do site deve ir para `ecommerce.md`. Aqui, o cliente escolhe os produtos e conversa com o dono (WhatsApp) ou segue para um link de pagamento.

## CAIXINHA A (Produtos)
1. **Tipo de produto:** Físico (roupa, acessório, eletrônico) / Alimentos / Serviços / Imóveis ou veículos.
2. **Quantidade:** Até 20 / De 20 a 100 / Mais de 100.
3. **Como atualiza:** Peço pra IA alterar / Por planilha ou arquivo / Painel de admin com login.
4. **Recursos (múltipla):** Busca e filtro por categoria / Preço visível / Variações (cor, tamanho) / Destaques e promoções.

## CAIXINHA B (Contato e pedido)
1. **Como o cliente fala com você:** WhatsApp com mensagem pronta do produto / Link de pagamento / Os dois / Só mostra os produtos.
2. **Seleção:** Botão em cada produto / Carrinho com vários itens e uma mensagem só / Sem carrinho.
3. **O que vai na mensagem (múltipla):** Produto e variação / Lista de itens e total / Nome e endereço / Observações.
4. **Entrega:** Retirada / Entrega local com taxa / Correios / Combino pelo WhatsApp.

Se a resposta for "Só mostra os produtos", pule as perguntas 2 a 4 da Caixinha B e as regras de pedido abaixo.

## COMO OS PRODUTOS ENTRAM NO SITE
- Os produtos ficam em UM arquivo de dados (planilha CSV ou JSON) mais uma pasta de imagens com nomes combinados (ex.: `produtos.csv` e `imagens/blusa-linho-azul.jpg`). Em "Peço pra IA alterar", a pessoa manda a mudança em texto e a skill reentrega o arquivo de dados COMPLETO (v2, v3). Em "Por planilha ou arquivo", a pessoa edita a planilha e a IA converte. Em "Painel de admin com login", aplique também as regras de segurança de painel.
- Confirme que "Variações" (cor, tamanho) nos recursos é a mesma coisa que "Produto e variação" na mensagem do WhatsApp (reconciliação, ver `01-triagem-geral.md`).
- **Cupom** (quando a pessoa tiver escolhido cupom como isca na Caixinha 4): no catálogo sem checkout, o cupom vai no e-mail e o dono confere e aplica ao confirmar o pedido; o site diz isso com clareza.
- **Pedido por WhatsApp:** o visitante envia a mensagem por conta própria (o site só monta o texto). Dados do pedido não vão em endereço de página nem em ferramenta de medição; gravação de tela (Clarity) mascara campos de nome e endereço.

## SEGURANÇA (vem ligada, além da base)
- Painel de admin (só quando escolhido): senha com hash, limite de tentativas, sessão segura.
- Upload de imagem validado (tipo e tamanho) e sem metadados (só quando houver painel ou upload).
- Proteção contra injeção nos campos e na busca (quando houver servidor ou banco).
- Backup (quando houver banco ou painel).
- Anti-spam nos formulários (em site estático, por serviço de formulário).

**Regras de pedido (entram só quando a pessoa escolher pedir pelo site):**
- O preço que aparece no navegador pode ser alterado por quem visita; por isso o pedido é só uma SOLICITAÇÃO e o dono confirma o valor antes de cobrar.
- Nome, endereço e observações são escapados antes de montar a mensagem do WhatsApp.
- Link de pagamento gerado no servidor, com chave secreta fora do navegador; pagamento confirmado só pelo webhook com assinatura validada; o site não guarda dado de cartão.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Preço, promoção, frete e prazo claros** (CDC) e política de troca e devolução.
- **Direito de arrependimento de 7 dias** nas compras feitas fora da loja física, inclusive por WhatsApp (art. 49 do CDC). Confira o texto exato na web antes de afirmar detalhes.
- **Identificação de quem vende:** nome ou razão social, CNPJ ou CPF, endereço, contato.
- **Fotos e marcas de fornecedor ou terceiros** (direitos autorais e de marca).
- **Alegações do produto** ("original", "garantia", "natural") e produto regulado (Anvisa, Anatel).
- **Dados do cliente pelo WhatsApp:** política de privacidade e cookies.
- **Nota fiscal** depende do enquadramento (MEI, ME); a skill avisa e indica conversar com o contador.
