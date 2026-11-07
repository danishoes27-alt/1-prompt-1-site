# 03. Regras gerais

Valem para todo site, de qualquer tipo. Os módulos em `modulos/` somam regras específicas por cima destas.

## 1. Regra de ouro: AVISAR E PERGUNTAR, NUNCA PROIBIR

- A skill não proíbe o que a pessoa decide fazer. O que a pessoa faz com o site é responsabilidade dela, dentro dos limites de cada IA.
- Limites de cada IA pertencem à IA. A skill não os repete, não os reforça e não traz instrução para ignorar, burlar ou contornar regras de nenhuma IA.
- Segurança técnica vem LIGADA no prompt por padrão (seção 3).
- Lei e conduta: antes de incluir qualquer item que mexa com isso, a skill AVISA em uma frase (com o motivo ou a lei) e PERGUNTA numa caixinha com 3 opções:
  1. Seguir assim mesmo
  2. Ajustar
  3. Deixar de fora
- Toda decisão sobre lei e conduta é registrada no arquivo DECISOES.md, com data e a escolha da pessoa.

### Como escrever cada aviso (para as 3 opções fazerem sentido)
Escreva o aviso como uma frase que diz o que a skill vai fazer, mais o motivo, e depois explique as três opções com uma glosa curta entre parênteses. Exemplos:

- Item que a skill inclui (política de privacidade): "A skill vai incluir uma política de privacidade e um aviso de cookies, porque o site coleta dados (LGPD). **Seguir assim mesmo** (incluir como está) / **Ajustar** (você me diz o que mudar) / **Deixar de fora** (não incluir)."
- Item que a pessoa pediu e tem risco (depoimento sem comprovação): "Atenção: depoimento inventado pode ser enganoso e gerar problema com o Código de Defesa do Consumidor, além de derrubar a confiança no site. **Seguir assim mesmo** (usar do jeito que está) / **Ajustar** (trocar por depoimentos reais) / **Deixar de fora** (tirar essa seção)."
- Item de segurança que a pessoa quer desligar (limite de tentativas no login): "Sem limite de tentativas, alguém pode tentar milhares de senhas até acertar. **Seguir assim mesmo** (desligar mesmo assim) / **Ajustar** (por exemplo, desligar só no ambiente de teste) / **Deixar de fora** (manter ligado)."

Como aplicar as respostas:
- **Seguir assim mesmo:** o item entra no prompt na forma descrita pelo aviso; registra a escolha.
- **Ajustar:** pergunta em texto o que muda e reescreve o item.
- **Deixar de fora:** o item sai do prompt (o prompt diz "não incluir") e registra.

Se a pessoa pedir para DESLIGAR um item de segurança, a conduta é a mesma (avisa o risco e pergunta). A decisão vai para a seção "Decisões de segurança" do DECISOES.md.

### Rodada de Lei e Conduta (UMA vez, no fim da triagem)
- Todos os avisos de lei e conduta são perguntados nesta rodada, uma única vez cada. Os módulos e as caixinhas só COLETAM os avisos que se aplicam; não pergunte na hora, para não perguntar duas vezes.
- Monte a lista só com os avisos que SE APLICAM às respostas da pessoa.
- **Junte avisos repetidos:** privacidade, cookies, identificação de quem vende e direitos autorais aparecem na base, no módulo e no e-mail; vire um aviso só por tema.
- Agrupe de 3 a 4 avisos por caixinha, cada um com as 3 opções. Se sobrarem 1 ou 2, vão numa caixinha menor.
- Ideia nova depois do envio: refaça a Rodada só para a ideia nova.
- Em lista numerada, cada aviso ocupa um bloco de 3 linhas (a, b, c), como na seção 2.

## 2. Caixinha de múltipla escolha

- Use a ferramenta **AskUserQuestion** (a caixinha) quando ela existir: de 1 a 4 perguntas por caixinha, de 2 a 4 opções por pergunta, e a opção "Outro" (texto livre) sempre disponível. Se a pessoa usar "Outro" para dizer algo que não está nas opções (por exemplo "só hospedagem", "só as cores"), trate a resposta normalmente.
- Quando a ferramenta não existir (por exemplo, em alguns ambientes do claude.ai), use **lista numerada**: as PERGUNTAS são numeradas (1, 2, 3...) e as OPÇÕES têm letras (a, b, c, d), com as mesmas perguntas e as mesmas opções. A pessoa responde assim: "1b, 2a, 3c". Para marcar várias opções numa pergunta de múltipla escolha: "3acd" (ou "3 todas"). Texto livre vale no lugar de uma letra (equivale a "Outro").
- Perguntas de texto livre (nome do negócio, o que faz, cidade e público, páginas, contato) são feitas em texto, fora da caixinha, numeradas numa mensagem só; a pessoa pode responder tudo de uma vez.
- Quando uma pergunta tiver mais de 4 opções, divida em duas etapas (primeiro um grupo, depois a escolha dentro do grupo).

Exemplo de lista numerada:

```
Caixinha 0 · Você
1. Qual é o seu nível?
   a) Nunca criei um site
   b) Já criei com ajuda de IA
   c) Entendo de código
   d) Sou programador
2. Como prefere a conversa?
   a) Bem simples, com tudo explicado
   b) Direto ao ponto, só explica termo novo
   c) Técnico, sem explicar o básico
(ou escreva outra resposta)
Responda assim: 1b, 2a
```

## 3. BASE DE SEGURANÇA (de todo site, vem LIGADA)

1. HTTPS em todo o site.
2. Cabeçalhos de segurança (CSP e X-Frame-Options, entre outros) configurados na hospedagem ou no servidor.
3. Chaves, senhas, tokens e webhooks só no servidor (variáveis de ambiente), fora do código visível no navegador e fora do repositório.
4. Formulários com anti-spam, limite de envio e validação no servidor (validar só no navegador não protege). Em site estático, sem servidor próprio, o formulário usa um serviço de formulário ou uma função de servidor que faça essa validação; se não houver nenhum dos dois, avise a pessoa e pergunte como seguir (por exemplo, trocar o formulário por um botão de WhatsApp).
5. Links externos com `rel="noopener"` (e `noreferrer` quando couber).
6. Imagens otimizadas e sem metadados (EXIF e localização).
7. E-mail do dono não escrito cru na página (usa formulário, função de servidor ou serviço de formulário).
8. Backup quando houver banco de dados ou painel de edição.
9. Fontes e scripts hospedados no próprio site sempre que possível (evita enviar dados do visitante a terceiros e acelera a página).

Regra de condição: item que depende de painel, banco, upload ou servidor só entra quando o site tiver aquilo.

## 4. BASE DE LEI E CONDUTA (a skill SEMPRE pergunta antes, na Rodada)

1. **Política de privacidade e aviso de cookies.** A política entra quando o site coletar qualquer dado (formulário, e-mail, cadastro, WhatsApp com dados). O aviso de cookies, com consentimento ANTES de ligar, entra quando houver recurso de terceiros: analytics, pixel de anúncio, gravação de tela ou mapa de calor (como o Clarity), mapa incorporado, vídeo incorporado, fontes ou scripts de fora (LGPD). Site sem nada disso não precisa de aviso de cookies: diga isso e pergunte se a pessoa quer mesmo assim. Gravação de tela, quando houver, deve mascarar campos de formulário.
2. **Direitos autorais** de fotos, fontes e textos de terceiros.
3. **Identificação de quem vende ou presta serviço** quando houver venda (nome ou razão social, CNPJ ou CPF, endereço, contato).
4. **Profissão regulamentada** (saúde, advocacia, contabilidade, engenharia e outras): os conselhos de categoria têm regras próprias sobre publicidade, preços, depoimentos e "antes e depois"; dado de saúde é dado pessoal sensível (LGPD). Se o negócio for dessa área, avise e pergunte, e confira as regras do conselho na web.

Confira o texto exato das leis na web antes de afirmar detalhes (quando houver pesquisa). A skill orienta; não substitui advogado nem contador, e diz isso em uma frase quando o assunto for jurídico.

### Estrutura mínima dos textos legais (modelo, não substitui revisão profissional)
Quando a pessoa escolher incluir, a skill escreve o texto com estes tópicos e avisa que é um modelo para revisão de um profissional:
- **Política de privacidade:** quem é o responsável e como contatar; quais dados são coletados; para que servem; base legal; com quem são compartilhados (ferramentas de e-mail, pagamento, analytics); cookies; por quanto tempo ficam guardados; direitos da pessoa (acessar, corrigir, apagar, entre outros, conforme a LGPD); data da última atualização.
- **Aviso de cookies:** o que é usado, para quê, botões "Aceitar" e "Recusar" com o mesmo destaque, link para a política.
- **Termos de uso:** o que o site oferece, regras de uso, responsabilidades, contato e foro.
- **Política de troca, devolução e cancelamento:** prazo, como pedir, quem paga o frete, como o dinheiro volta, direito de arrependimento quando couber.

## 5. Quando algo estiver fora do que a skill cobre

A skill avisa o que muda na segurança e indica o caminho (por exemplo: plataforma pronta, serviço de terceiros, ou profissional da área). Não deixa o item sumir em silêncio: registra no DECISOES.md.

## 6. Pendências: dado que a pessoa ainda não tem (ou não quer digitar no chat)

Os blocos entregues não têm marcadores para editar. Quando faltar um dado (CNPJ, endereço, número de registro no conselho, ID do analytics, depoimentos autorizados, fotos reais):
1. Pergunte primeiro. Se a pessoa não tiver agora ou preferir não digitar no chat, o dado vai para UM arquivo de configuração do site (nome sugerido: `config-do-site`, com todos os valores em um só lugar) que ela preenche depois, e a seção ou o recurso que depende dele fica oculto até o preenchimento.
2. Registre cada pendência numa seção "Pendências da pessoa" do PLANO.md, dizendo o que falta, onde preencher e o que aparece quando preencher.
3. Segredos (chaves, senhas) nunca vão no chat nem no prompt: o prompt só cita o nome da variável de ambiente.

## 7. Como os módulos usam este arquivo
Cada arquivo em `modulos/` tem: caixinha(s) de triagem, SEGURANÇA (vem ligada, além da base) e LEI E CONDUTA (avisa e pergunta antes, além da base). Se um item do módulo repetir a base, vale uma vez só.
