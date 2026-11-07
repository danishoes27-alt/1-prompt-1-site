# Módulo: Cardápio digital

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 7 (Cardápio digital), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

## CAIXINHA (Cardápio digital)
1. **Tipo de negócio:** Restaurante ou lanchonete / Pizzaria / Café, doceria ou padaria / Bar ou delivery.
2. **Como o cliente pede:** Só mostra o cardápio / Pedido pelo WhatsApp / Pix / WhatsApp e Pix.
3. **Recursos (múltipla):** Categorias com fotos / Adicionais e observações (sem cebola, ponto da carne) / Horário de funcionamento / Pedido de mesa por QR code.
4. **Entrega:** Só retirada / Entrega com taxa por bairro / Consumo no local / Entrega e retirada.

Se a resposta for "Só mostra o cardápio", pule as regras de pedido e pagamento abaixo.

## SEGURANÇA (vem ligada, além da base)
- Preço, taxa de entrega e total conferidos pelo dono antes de cobrar.
- Dados do pedido escapados antes de montar a mensagem do WhatsApp.
- QR code de mesa com número da mesa validado no servidor.
- Pix com valor gerado no servidor e confirmação pelo webhook do provedor. Se for Pix estático (chave copiada), avise que a confirmação é manual (o dono confere no app do banco).
- Limite de pedidos por pessoa e anti-spam.
- Painel de admin protegido, com upload validado e backup.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Ingredientes e alergênicos informados** (dever de informação do CDC).
- **Preço claro com taxa e prazo e política de cancelamento.**
- **Foto identificada como "imagem ilustrativa"** quando não for o prato real.
- **Alvará e licença sanitária** são responsabilidade do dono; a skill avisa e não verifica.
- **Uso de nome e logo de apps de delivery** sem autorização: avise o risco e pergunte.
- **Política de privacidade e cookies.**
