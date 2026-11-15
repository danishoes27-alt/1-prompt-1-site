# 01. Triagem geral (BLOCO 1)

Faça depois da Caixinha 0 (`00-perfil-e-entrega.md`). Siga as regras de caixinha e de lista numerada de `03-regras-gerais.md`. Registre cada resposta: ela vira o SPEC.md. Não repita pergunta já respondida: se uma pergunta do módulo coincidir com uma daqui (por exemplo, "Objetivo principal" e "Ação principal"), só CONFIRME a resposta anterior.

## CAIXINHA 1 (O site)

A Caixinha 1 é feita em TRÊS telas (o tipo de site tem opções demais para uma tela só). Com o ritmo "Várias etapas juntas", as telas B e C podem ir juntas (4 perguntas).

**Tela A. Categoria (1 pergunta)**
1. Categoria: Vender produtos / Divulgar negócio ou serviço / Conteúdo e pessoal.

**Tela B. Tipo, conforme a categoria**
- Vender produtos: Catálogo / Ecommerce com checkout próprio / Página de vendas de infoproduto / Cardápio digital.
- Divulgar negócio ou serviço: Landing page / Institucional / Agendamento ou reserva / Evento ou igreja.
- Conteúdo e pessoal: Portfólio / Blog / Link na bio / Área de membros.

**Tela C. Resto da Caixinha 1 (3 perguntas, numa caixinha só)**
2. Objetivo principal: Chamar no WhatsApp / Comprar / Agendar / Preencher formulário.
3. Onde vai construir: claude.ai / Claude Code / ChatGPT / Codex. Se a skill já sabe onde está (ver "Onde a skill está rodando" no SKILL.md), só confirme.
4. Conteúdo: Tenho tudo pronto / Tenho parte / A IA escreve e usa imagens provisórias.
   - "Tenho tudo pronto" ou "Tenho parte": pergunte em texto como o conteúdo vai chegar (colar no chat, planilha, pasta de fotos) e, se houver muitos itens (produtos, cardápio), combine UM arquivo de dados (planilha/CSV) mais uma pasta de imagens com nomes combinados.

Mapa tipo → módulo:
| Tipo | Arquivo do módulo |
|---|---|
| Landing page | modulos/landing-page.md |
| Institucional | modulos/institucional.md |
| Portfólio | modulos/portfolio.md |
| Blog | modulos/blog.md |
| Catálogo | modulos/catalogo.md |
| Ecommerce com checkout próprio | modulos/ecommerce.md |
| Página de vendas de infoproduto | modulos/pagina-de-vendas.md |
| Cardápio digital | modulos/cardapio-digital.md |
| Agendamento ou reserva | modulos/agendamento.md |
| Evento ou igreja | modulos/evento-igreja.md |
| Link na bio | modulos/link-na-bio.md |
| Área de membros | modulos/area-de-membros.md |

Se a pessoa descrever um site que mistura dois tipos (ex.: catálogo com blog), escolha o principal para o módulo e aplique as regras do segundo como extra; avise a pessoa e confirme.

## PERGUNTAS DE TEXTO LIVRE (fora da caixinha)
Faça em UMA mensagem, numeradas, e diga que a pessoa pode responder tudo de uma vez:
1. Nome do negócio, marca ou pessoa.
2. O que faz (em uma ou duas frases).
3. Cidade e público (quem vai visitar o site).
4. Páginas desejadas (ou "a skill sugere").
5. Contato: WhatsApp, e-mail, redes sociais, endereço e mapa.
6. Tom de voz do site (formal, próximo, descontraído, técnico...) em uma frase. Se a pessoa não souber, proponha um e confirme.
7. Como a mensagem do formulário de contato chega até você (e-mail, WhatsApp ou painel). Se o site não tiver formulário, esta pergunta sai.

Se a pessoa disser "não sei", proponha uma opção sensata e peça confirmação. Dado que ela não tiver agora vira Pendência (`03-regras-gerais.md`, seção 6).

## CAIXINHA 2 (Visual)

Feita em DUAS telas. **Tela A** (3 perguntas): identidade, referências e estilo. **Tela B** (2 perguntas): objetivo do visual e animações.

**Tela A**
1. Identidade: Tenho logo e cores / Só logo / Nada, a skill propõe.
   - "Tenho logo e cores": peça os códigos de cor ou o arquivo. Confira o contraste das cores da marca (texto sobre fundo, texto do botão) e, se alguma combinação não alcançar o mínimo (ver `06-design.md`), AVISE e pergunte: usar assim mesmo / ajustar o tom só no texto e nos botões / deixar de lado essa cor. Se a pessoa não informou fontes, proponha sempre.
   - "Só logo": proponha paleta a partir do logo e confirme. Se a pessoa disser por "Outro" que tem só as cores, proponha as fontes.
2. Referências de design: Tenho / Quero que indique onde procurar / Não quero.
   - "Quero que indique": sugira Pinterest, Dribbble e Awwwards para olhar sites e layouts; e, como estudo, ver como um site de que ela gosta foi montado usando "Exibir código-fonte" (View Source) do navegador. Deixe claro que é só para estudar e se inspirar, e que o site novo deve ter identidade própria. Depois de sugerir, SIGA em frente com uma proposta sua; a pessoa pode trazer referências quando tiver (o DESIGN.md é atualizado em v2).
   - "Tenho": pergunte o que gostou nela (cores, tipografia, organização) em vez de pedir cópia.
3. Estilo: Moderno e limpo / Escuro e ousado / Colorido e divertido / Sério e corporativo.

**Tela B**
4. Objetivo do visual: Converter (levar o visitante a uma ação: pedir, comprar, agendar, chamar) / Impressionar (estilo Awwwards, a vitrine e prêmio de design de sites: cada seção vira uma cena).
   - Esta resposta escolhe a faixa de seções do tipo de site em `07b-secoes-por-tipo.md`. Impressionar NÃO muda a ação principal, o preço, o contraste, o desempenho nem a acessibilidade; o movimento continua com função e respeita `prefers-reduced-motion` (`06-design.md`, seção 4). Em tipos de uso (Cardápio, Agendamento, Área de membros, Blog, Evento ou igreja) a faixa é a mesma nos dois objetivos: explique em uma frase.
   - Se a pessoa não souber, proponha Converter e confirme.
5. Animações: Nenhuma / Suaves / Ricas.

Se escolher "a skill propõe", use `06-design.md` para propor paleta e fontes e confirme.

## CAIXINHA 3 (Técnico e dados)
1. Domínio e hospedagem: Tenho os dois / Só domínio / Nenhum.
2. Analytics: Google Analytics / Microsoft Clarity / Os dois / Nenhum.
3. Anúncios: Google / Meta / Os dois / Não vai anunciar.
4. Dados do visitante: Só formulário de contato / Cadastro e login / Pagamento / Nenhum.
   - Se a pessoa precisar de mais de um (ex.: pagamento e cadastro), ela usa "Outro" e a skill aceita as duas respostas.

Perguntas de texto livre que complementam a Caixinha 3 (uma mensagem só, quando se aplicam):
- Nome do domínio e onde foi registrado (ou o nome que quer registrar). Domínio .com como padrão; pesquise o preço atual em R$ antes de citar; sem pesquisa, diga que o valor varia (regra 13).
- Qual hospedagem usa, e se ela roda programa de servidor (necessário para login, pagamento, banco e painel).
- ID do analytics e do pixel, se já existirem (senão, Pendência).

Orientações:
- **Hospedagem:** se a pessoa responder "Só domínio" ou "Nenhum", decida junto com ela qual tipo de hospedagem serve para o site: site estático (páginas simples, formulário por serviço de formulário) ou site com servidor (login, pagamento, banco, painel). Indique opções adequadas ao tipo, confira planos e limites atuais na web (ou use a regra 13, sem preço) e explique "hospedagem" em uma frase se a pessoa for iniciante. Se não decidir agora, o prompt final inclui como Tarefa 1 "confirmar stack e hospedagem" (ver `05-prompt-final.md`).
- **Analytics, pixel, gravação de tela (Clarity), mapa e vídeo incorporados** só ligam depois do aceite de cookies (entra na Rodada de Lei e Conduta). Gravação de tela mascara campos de formulário.
- **"Cadastro e login" e "Pagamento"** ativam as regras de segurança de conta e de pagamento do módulo e das bases.
- **"Anúncios"** pede uma pergunta extra em texto: já tem conta de anúncios? A skill prepara os pontos de medição (pixel/eventos) sem dado pessoal na URL.

## Reconciliação depois do módulo
Depois das caixinhas do módulo, compare as respostas e corrija o SPEC com a pessoa quando divergirem. Exemplos: "Só formulário de contato" na Caixinha 3, mas o módulo pede Pix, login ou painel (atualize "dados do visitante" e avise o que muda na segurança); "Variações" nos recursos do catálogo e "Produto e variação" na mensagem do WhatsApp (confirme que são a mesma coisa); carrinho com nome e endereço no WhatsApp e site com "Só formulário". Não pergunte tudo de novo: apresente a divergência em uma frase e confirme.

## Depois da triagem geral
1. Carregue o módulo do tipo escolhido (`modulos/<tipo>.md`) e faça as caixinhas dele.
2. Faça a reconciliação acima.
3. Monte as seções de cada página com `07b-secoes-por-tipo.md` (faixa pelo objetivo do visual, O/Op) e confirme a lista com a pessoa.
4. Siga para `02-crescimento-email.md` (Caixinha 4).
5. Faça a Rodada de Lei e Conduta (`03-regras-gerais.md`).
6. Resuma tudo e pergunte "posso mandar?" (ver `04-arquivos-do-projeto.md` e `05-prompt-final.md`).
