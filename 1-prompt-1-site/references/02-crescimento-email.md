# 02. E-mail do site (CAIXINHA 4)

Faça depois do módulo do tipo de site, para qualquer tipo. Esta etapa decide DOIS assuntos: (1) captar e-mails de visitantes (newsletter, promoções) e (2) a ferramenta que ENVIA qualquer e-mail do site (boas-vindas, confirmação de pedido, lembrete de agendamento, resposta de formulário).

## Antes de perguntar: o que já foi respondido?
- Se o módulo já definiu e-mails automáticos (ex.: Ecommerce, "E-mails automáticos"; Agendamento, "Lembrete"), NÃO pergunte de novo a pergunta 4 sobre esses e-mails: considere-os escolhidos e só acrescente os que faltarem.
- Se a pergunta 1 for "Não" (não captar e-mails) e o site NÃO envia nenhum e-mail automático, pule o resto e não crie o EMAIL.md.
- Se a pergunta 1 for "Não" mas o site envia e-mails automáticos ou entrega mensagens de formulário por e-mail, faça só a pergunta 3 (ferramenta) e crie o EMAIL.md com o que couber.
- Se a pergunta 1 for "Só e-mails de confirmação (pedido, cadastro)", pule a pergunta 2 (isca): não há inscrição para atrair.

## CAIXINHA 4 (E-mail)
1. **Captar e-mails:** Newsletter / Avisos de novidade e promoção / Só e-mails de confirmação (pedido, cadastro) / Não.
2. **Isca para inscrição:** Cupom de desconto / PDF ou material grátis / Nenhuma.
3. **Ferramenta de envio:** Já uso uma / Quero uma grátis / A skill indica.
   - "Já uso uma": pergunte em texto qual é (nome) e se tem plano que suporte automação. Se ela não souber o nome, trate como "A skill indica".
   - "Quero uma grátis": entre as indicadas, só as que têm plano gratuito.
   - "A skill indica": pesquise na web os planos atuais antes de citar nomes, limites e preços (em R$ quando houver). Sem pesquisa, siga a regra 13 de `00-perfil-e-entrega.md` (nomes conhecidos, sem preço, "confira o plano atual no site oficial") e transforme a conferência em tarefa no PLANO.md. Depois de indicar 2 ou 3, pergunte qual a pessoa escolhe; se ela ainda não decidir, o EMAIL.md registra "ferramenta a escolher" e o texto do e-mail fica pronto sem depender de nome. Explique "ferramenta de envio" em uma frase se a pessoa for iniciante (Caixinha 0).
4. **E-mails prontos (múltipla):** Boas-vindas / Primeira newsletter / Carrinho abandonado (só Ecommerce) / Nenhum.
   - Fora do Ecommerce, mostre só: Boas-vindas / Primeira newsletter / Nenhum.
   - No Ecommerce, "Carrinho abandonado" só aparece aqui se NÃO foi escolhido no módulo.

## O que a skill gera
- O **formulário de inscrição** (com campo de consentimento claro e link para a política de privacidade).
- O **e-mail de boas-vindas** pronto (assunto, texto, link de descadastro).
- Os outros e-mails escolhidos (na pergunta 4 ou no módulo).
- **Cupom como isca:** a pessoa informa o código e a regra (valor, validade, limite de uso). Em loja com checkout próprio, o cupom é cadastrado no checkout. Em catálogo com WhatsApp ou site sem checkout, o cupom vai no e-mail de boas-vindas e o dono confere e aplica no pedido; o texto diz isso com clareza.
- Quando houver e-mails (captação ou automáticos), entra o arquivo **EMAIL.md** no projeto (ver `04-arquivos-do-projeto.md`): ferramenta escolhida, isca, textos dos e-mails, regras de envio e checklist de domínio.

## SEGURANÇA (vem ligada)
- Formulário de inscrição com anti-spam, limite de envio e validação no servidor (em site estático, por serviço de formulário ou função de servidor; ver `03-regras-gerais.md`).
- Chave de API da ferramenta de e-mail só no servidor, nunca no código visível.
- Instruções de **SPF, DKIM e DMARC** para o domínio, passo a passo (explique em uma frase que são registros que provam que o e-mail veio mesmo do seu domínio e ajudam a não cair no spam). Entregue o passo a passo conforme onde o domínio está registrado. Se a pessoa ainda não tem domínio, deixe como tarefa para depois do registro (PLANO.md).
- Confirmação de e-mail (dupla confirmação) como opção recomendada, para evitar cadastros falsos.
- Descadastro funcionando de verdade (quem saiu da lista deixa de receber).

## LEI (avisa e pergunta, na Rodada de Lei e Conduta)
Use as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), escritas como em `03-regras-gerais.md`, e registre no DECISOES.md.
- **Consentimento claro (opt-in)** e **link de descadastro em todo e-mail**. Aviso: "Mandar e-mail para quem não pediu pode ser tratado como spam e ferir a LGPD; o ideal é a pessoa marcar que aceita receber. A skill vai deixar o aceite obrigatório no formulário."
- **Política de privacidade ligada ao formulário** (LGPD). Junte com o aviso de privacidade da base (um só).
- **Comprar ou importar lista de terceiros** tem risco legal e de entrega (e-mails caem no spam, a ferramenta pode suspender a conta). Se a pessoa mencionar isso, avise o motivo e pergunte como quer seguir.
- Cupom ou material grátis como isca: o que foi prometido tem de ser entregue (CDC), e as regras do cupom (validade, limite) ficam claras no formulário.

## Ligação com os módulos
Blog (newsletter), Link na bio (captura de e-mail), Landing page (formulário de captura), Ecommerce (e-mails de pedido) e Agendamento (lembretes) usam esta caixinha. Não repita a pergunta se ela já foi respondida dentro do módulo.
