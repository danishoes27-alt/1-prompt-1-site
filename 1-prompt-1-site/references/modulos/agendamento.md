# Módulo: Agendamento ou reserva

**Seções das páginas:** depois das caixinhas deste módulo, monte a lista de seções de cada página com `references/07b-secoes-por-tipo.md`, seção 8 (Agendamento), usando a faixa do objetivo do visual escolhido na triagem.

Faça estas perguntas depois da triagem geral (`01-triagem-geral.md`). Some às bases de `03-regras-gerais.md`. Nada aqui proíbe a escolha da pessoa: o que é lei e conduta vira aviso + pergunta. Aqui você só COLETA os avisos que se aplicam às respostas; eles são perguntados UMA vez, na Rodada de Lei e Conduta (`03-regras-gerais.md`), com as 3 opções (Seguir assim mesmo / Ajustar / Deixar de fora), e registrados no DECISOES.md com data.

## CAIXINHA (Agendamento)
1. **Tipo de negócio:** Beleza e estética (barbearia, manicure, salão) / Saúde (clínica, dentista, psicólogo) / Serviços (oficina, fotógrafo, consultoria) / Reserva (hotel, quadra, espaço).
2. **Como agenda:** Escolhe o horário no site / Pede por WhatsApp / Formulário e confirmo depois / Integrado ao Google Agenda.
3. **Recursos (múltipla):** Serviços e duração / Escolha de profissional / Lembrete por WhatsApp ou e-mail / Cancelar e remarcar.
4. **Pagamento:** Sem pagamento / Sinal por Pix / Pagamento total online / Paga no local.

**Perguntas de texto livre deste módulo (uma mensagem só):** lista de serviços com duração e preço; horário de funcionamento e folgas; nomes dos profissionais (se houver escolha de profissional); valor do sinal e prazo para cancelar sem perder o sinal; limite de agendamentos por pessoa. O que a pessoa não tiver agora vira Pendência.

**Lembrete:** se escolher "Lembrete por WhatsApp ou e-mail", pergunte em texto qual canal: e-mail (usa a ferramenta da Caixinha 4), WhatsApp com link pronto que o dono envia (simples) ou WhatsApp automático por API (tem custo e exige conta empresarial; confira na web). Registre a escolha.

Se a pessoa escolher "Pede por WhatsApp" ou "Formulário e confirmo depois", as regras de horário no servidor e de painel ficam mais simples; ainda valem as regras de dados e de formulário.

## SEGURANÇA (vem ligada, além da base)
- Horário conferido no servidor, com trava contra dois clientes no mesmo horário.
- Agenda pública mostra só horários livres, sem dado de outros clientes.
- Cancelar e remarcar por link com token único e validade, com IDs não adivinháveis.
- Painel do dono com login protegido.
- Limite de agendamentos por pessoa e confirmação por WhatsApp ou e-mail.
- Sinal por Pix com valor gerado no servidor e confirmação por webhook.
- Chaves de API só no servidor e fuso horário fixo America/Sao_Paulo.
- **Em saúde:** dados do cliente criptografados no banco e visíveis só ao profissional.
- Backup.

## LEI E CONDUTA (avisa e pergunta antes, além da base)
- **Dado de saúde é dado pessoal sensível (LGPD):** consentimento claro e sem dado clínico em formulário aberto.
- **Lembretes por WhatsApp e e-mail** só com consentimento e com opção de parar.
- **Política de cancelamento, remarcação, atraso, falta e sinal** visível antes de agendar (CDC).
- **Conselhos de categoria (CRM, CRO, CRP e outros)** têm regras de publicidade, como promessa de resultado e "antes e depois". Avise e pergunte; confirme o texto das regras na web, quando houver pesquisa.
- **Identificação de quem presta o serviço** (e registro no conselho, quando houver).
- **Política de privacidade e cookies.**
