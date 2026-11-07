# 06. Design (guia para o visual do site)

Base de ideias destilada, com palavras próprias, do skill Impeccable de Paul Bakaus (Apache 2.0). Créditos no NOTICE.md. Use este arquivo para propor o visual quando a pessoa disser "a skill propõe", para preencher o DESIGN.md e para escrever a seção de design do prompt final.

## Princípio
Escolha UMA direção visual e vá até o fim. O pedido da pessoa (cores, fontes, estilo, referências) manda; só proponha algo diferente onde ela deixou em aberto. Site bonito é site com decisões claras, não com enfeites demais.

## 1. Tipografia
- **Papéis:** defina poucos papéis (título grande, título de seção, texto, legenda/rótulo, botão) e use sempre o mesmo estilo para o mesmo papel.
- **Escala:** passos de tamanho com diferença evidente entre um e outro (cada passo entre 1,2 e 1,5 vezes o anterior). Se dois níveis parecem iguais, um deles é desnecessário.
- **Texto corrido:** pelo menos 16 px (1rem), linhas de 45 a 75 caracteres, espaço entre linhas confortável (algo perto de 1,5), mais folgado em linhas largas.
- **Pareamento:** uma fonte para títulos com personalidade e uma para texto bem legível costuma bastar; uma família só também funciona. Mais de duas famílias exige motivo claro.
- **Escolha com intenção:** a fonte precisa combinar com o negócio e com o estilo escolhido. Fontes gratuitas de bibliotecas abertas, baixadas e hospedadas no próprio site (carregar de um serviço de fora envia dados do visitante a terceiros e exigiria aviso de cookies; hospedando junto do site, fica mais rápido e mais simples). Carregue só os pesos usados e use fallback parecido para o texto não pular. Confira a licença da fonte.
- **Texto claro em fundo escuro:** dê um pouco mais de espaço entre linhas e um peso a mais se a fonte ficar fina.
- Respeite o zoom e o tamanho de fonte do navegador da pessoa (use rem, não px fixo para texto).

## 2. Cor e contraste
- **Papéis de cor:** fundo, superfície elevada, texto principal, texto secundário, ação principal, destaque, bordas e estados (sucesso, aviso, erro).
- **Contraste (acessibilidade, WCAG AA):** texto normal pelo menos 4,5 para 1; texto grande, ícones e foco de teclado pelo menos 3 para 1. Confira par por par, inclusive botões, links, texto sobre imagem e estados desativados.
- **Cor não é a única pista:** erro, link e seleção também têm texto, ícone ou sublinhado.
- **Cor de ação:** o botão principal usa a cor mais forte da página, e ela não é gasta em decoração.
- **Texto em superfície colorida:** derive o tom do texto da própria cor do fundo (um tom mais claro ou mais escuro), não use cinza genérico.
- **Modo escuro:** projete as superfícies escuras (camadas com níveis de claridade diferentes), não apenas inverta as cores do modo claro. Se o site oferecer os dois temas, teste ambos. Se oferecer só um, escolha pelo cenário de uso do visitante (quem visita, onde, com que luz) e não por moda.
- **Cores da marca que não passam no contraste** (por exemplo, dourado claro como texto sobre branco): use a cor da marca em fundos, bordas e detalhes grandes, e um tom mais escuro da mesma família para texto e para o botão com texto claro. Avise a pessoa e pergunte (usar assim mesmo / ajustar só o tom do texto / deixar a cor de lado).
- Prefira definir as cores uma vez, como variáveis (tokens), e reaproveitar.

## 3. Espaçamento e ritmo visual
- Use uma escala de espaçamento fixa (múltiplos de 4: 4, 8, 12, 16, 24, 32, 48, 64, 96).
- **Agrupe por proximidade:** itens relacionados ficam juntos; grupos diferentes ficam bem separados. Mais espaço acima de um título do que abaixo dele.
- **Ritmo:** alterne trechos compactos e trechos folgados. Se tudo tem o mesmo espaço, nada se destaca.
- **Teste de apertar os olhos:** com a tela desfocada, ainda dá para ver o que é principal, o que é secundário e quais são os grupos?
- Sombras com deslocamento e desfoque suaves, só quando ajudam a mostrar camada ou clique.

## 4. Movimento com propósito
- Cada animação precisa de um motivo: mostrar que algo mudou, guiar o olhar, dar retorno a um clique. Se não tem motivo, não entra.
- **Nível escolhido na triagem:** Nenhuma = sem animação além de estados de foco e hover. Suaves = entradas discretas, transições curtas (150 a 300 ms). Ricas = um momento marcante bem feito (por exemplo, a entrada da primeira tela) mais transições coerentes, sem espalhar efeitos por tudo.
- Curva de movimento que desacelera no final (ease-out). Animar de preferência opacidade e deslocamento (leves para o navegador).
- **Respeite "reduzir movimento":** com `prefers-reduced-motion`, desligue ou simplifique as animações.
- Evite o que pisca, o que bloqueia a leitura e o que atrasa o botão principal.

## 5. Responsivo
- Projete primeiro para o celular (a maior parte dos visitantes), depois amplie.
- Pontos de quebra pelo conteúdo, não por aparelho. Teste larguras estreita (360 px), média (768 px) e larga (1280 px).
- Alvos de toque com pelo menos 44 px; botão principal alcançável com o polegar.
- Imagens com tamanhos definidos (evita pulos na tela), carregamento preguiçoso fora da primeira tela e formatos modernos.
- Sem rolagem horizontal. Menu que vira botão no celular, com foco e teclado funcionando.
- A ordem do código acompanha a ordem visual (leitores de tela e tecla Tab).

## 6. Textos de interface
- **Botões** dizem a ação: "Chamar no WhatsApp", "Reservar horário", "Enviar pedido". Evite "Clique aqui", "Enviar" solto.
- **Erros** dizem o que aconteceu e como resolver: "O e-mail parece incompleto. Confira se tem @ e o final .com".
- **Estados vazios** explicam o que viria ali e o que fazer: "Nenhum produto nesta categoria ainda. Veja todos os produtos".
- **Carregando e sucesso:** avise que está acontecendo algo e confirme quando terminou ("Mensagem enviada! Respondemos em até 1 dia útil").
- Formulários: rótulo visível em cada campo, só os campos necessários, mensagens de erro perto do campo.
- Voz do site na primeira pessoa do negócio ou do profissional, em português do Brasil, sem jargão.

## 7. Anti-padrões (evite, a menos que a pessoa peça)
Isto é uma lista de armadilhas comuns, não uma proibição: se a pessoa quiser, a skill avisa o efeito e segue a escolha dela.
1. **Fontes saturadas:** Arial, Inter e a fonte padrão do sistema como voz do site. Prefira uma fonte escolhida com intenção.
2. **Texto cinza sobre fundo colorido:** perde contraste e fica sujo. Use um tom derivado da cor do fundo.
3. **Cartões dentro de cartões:** caixas aninhadas pesam o visual e confundem a hierarquia. Agrupe por espaço.
4. **Animação de bounce ou elástica:** efeito datado que distrai. Use movimento que desacelera suavemente.
5. Página inteira feita de cartões iguais com ícone, título e texto: parece modelo pronto. Varie a estrutura conforme o conteúdo.
6. Texto com degradê como destaque: destaque com peso ou tamanho.
7. Barra colorida grossa na lateral de cartões e alertas.
8. Emoji ou símbolo no lugar de ícones: use um conjunto de ícones consistente (mesma espessura e estilo) ou SVG próprio.
9. Vidro fosco e desfoque como enfeite sem função.
10. Uma pequena frase em letras miúdas acima de cada título como regra fixa, e numeração de seções sem necessidade.
11. Janela flutuante (modal) para algo que cabia na própria página.
12. Texto sobre imagem sem checar contraste; foto de banco genérica sem relação com o negócio.

## 8. Itens que costumam ser esquecidos (checklist de acabamento)
- Estados de passar o mouse, foco de teclado, desativado, carregando, erro e vazio, em todo botão e campo.
- Cor da seleção de texto, cursor, barra de rolagem e anel de foco combinando com a paleta.
- Textos reais no lugar de "Lorem ipsum"; imagens com texto alternativo.
- Favicon, título e descrição da página, imagem de compartilhamento.
- Páginas de erro 404 com o mesmo visual.

## Como preencher o DESIGN.md com isto
Registre: identidade (logo, cores com códigos, fontes), estilo (as 4 opções da triagem), papéis tipográficos e escala, papéis de cor e tema (claro/escuro), espaçamento, nível de animação e o que evitar. Se houver referências, anote o que a pessoa gostou em cada uma, sem pedir cópia.
