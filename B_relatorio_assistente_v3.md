# Relatório Técnico: Diagnóstico de Processo e Service Blueprint AS-IS
**Serviço:** Consulta Médica Especializada (Ambulatorial) — Canal Presencial  
**Escopo:** Secretaria de Estado da Saúde de São Paulo (SES-SP) no contexto do SUS  
**Abordagem:** Desenho de Serviços, Jornada do Cidadão e Modelagem Operacional  
**Versão:** 3.0 — Pós-Auditoria V2: Aprofundamento da Modelagem Operacional SES-SP

---

## Nota Metodológica de Revisão

A Versão 3.0 foi elaborada para corrigir as lacunas identificadas na Segunda Auditoria (auditoria\_v2), que concluiu: **"O principal risco remanescente é produzir um relatório juridicamente correto, porém não operacionalmente fiel à execução real da consulta médica na SES/SP."**

As adições centrais desta versão são:

1. Modelagem do papel dos **Departamentos Regionais de Saúde (DRS)** na governança regional;
2. Reconstrução do **fluxo operacional real de solicitação, regulação e disponibilização de vagas**;
3. Detalhamento do **backstage dos AMEs**: abertura/bloqueio de agendas, gestão de absenteísmo, recepção/faturamento e controle de glosas;
4. Detalhamento da **estrutura dos contratos de gestão com OSS** (metas, fiscalização, auditoria, repasse);
5. Novos **fail points operacionais** derivados do fluxo real (inconsistência cadastral, duplicidade de solicitação, absenteísmo reativo);
6. Referências a **normativos estaduais** específicos da SES-SP.

---

## 1. Caracterização do Serviço de Consulta Médica

O serviço analisado é a **Consulta Médica Especializada Ambulatorial**, prestada em caráter **presencial**, nos **Ambulatórios Médicos de Especialidades (AMEs)** e **Hospitais Estaduais** geridos pela Secretaria de Estado da Saúde de São Paulo (SES-SP) diretamente ou por meio de Contratos de Gestão com Organizações Sociais de Saúde (OSS), conforme previsto na **Lei Federal nº 9.637/1998** e no **Decreto Estadual nº 43.493/1998**.

A SES-SP não opera a Atenção Primária à Saúde (APS), que é de responsabilidade estritamente municipal. O Estado atua como principal gestor e provedor da **média e alta complexidade ambulatorial**, organizando a rede por meio dos **17 Departamentos Regionais de Saúde (DRS)**.

### 1.1 Tipos de Consultas Ofertadas

| Modalidade | Descrição | Canal de Regulação |
| :--- | :--- | :--- |
| **Primeira Consulta Especializada** | Atendimento inicial com médico especialista para diagnóstico ou definição de conduta. Exige encaminhamento da APS. | CROSS/SIRESP — Módulo Ambulatorial |
| **Consulta de Retorno** | Acompanhamento evolutivo, avaliação de exames ou ajuste farmacológico. Pode ser agendado diretamente pelo AME ou via SIRESP. | NIR do AME ou SIRESP |
| **Acompanhamento Crônico** | Atendimentos periódicos de longo prazo (pré-natal de alto risco, oncologia, cardiologia intervencionista). | SIRESP — APAC de acompanhamento |

### 1.2 Usuários e Critérios de Acesso

Os usuários são cidadãos residentes no Estado de São Paulo dependentes do SUS que possuem condição clínica que supera a capacidade resolutiva da APS municipal. O acesso às consultas de **primeira vez** é **vedado** ao paciente diretamente no AME ou Hospital — o acesso deve ser **obrigatoriamente mediado** pela Central de Regulação (CROSS/SIRESP), conforme determina a **Portaria GM/MS nº 2/2017** (Política Nacional de Regulação).

### 1.3 A Rede de Atores e Unidades

| Ator | Esfera | Papel no Serviço |
| :--- | :--- | :--- |
| UBS / ESF / eMulti | Municipal | Porta de entrada; solicita encaminhamento especializado via SIRESP |
| Operador de Regulação Municipal | Municipal | Insere e acompanha solicitações no SIRESP Ambulatorial |
| **DRS (17 regionais)** | Estadual | Supervisão regional; pactuação de vagas; arbitragem de fluxos inter-regionais; fiscalização de contratos OSS no território |
| **CROSS — Central de Regulação** | Estadual | Triagem clínica das solicitações; priorização P1 a P4; match vaga-paciente; gestão da fila estadual |
| **AME / Hospital Estadual (Adm. Direta)** | Estadual | Presta a consulta especializada; gerencia agendas; registra produção |
| **AME / Hospital gerido por OSS** | Estadual/Contratado | Mesma função, sob Contrato de Gestão com metas obrigatórias definidas pela Resolução SS-SP nº 44/2021 |
| NIR (Núcleo Interno de Regulação) | AME/Hospital | Disponibiliza vagas no SIRESP; confirma atendimentos realizados; gere encaixes |
| Setor de Faturamento e Auditoria | AME/Hospital | Codifica produção, submete BPA-I e APAC ao SIA-SUS; trata glosas |

---

## 2. O Papel Operacional dos DRS na Regulação Regional

Os Departamentos Regionais de Saúde (DRS) são estruturas desconcentradas da SES-SP com competência regional. Sua atuação no processo de consulta especializada envolve três funções operacionais centrais que a Versão 2 não detalhou:

### 2.1 Pactuação Programática de Vagas

A cada ciclo de planejamento (geralmente semestral), os DRS coordenam reuniões de **pactuação assistencial** com os municípios de sua região e com os AMEs/Hospitais do território. Nessas reuniões define-se:

- O **quantitativo de vagas** por especialidade que cada unidade deverá disponibilizar mensalmente no SIRESP;
- A **lógica de prioridade geográfica** (quais municípios têm preferência de acesso a qual AME, com base em tempo de deslocamento e porte populacional);
- O **perfil de demanda reprimida** por especialidade, identificado pelos relatórios do Módulo Indicadores do SIRESP.

Processo interno: Reunião de Pactuação → Coordenador DRS → SIRESP + registros administrativos → Portaria DRS formalizando a programação anual.

### 2.2 Arbitragem de Fluxos Inter-Regionais

Quando a demanda de um município supera a oferta dos AMEs de seu próprio DRS, o paciente pode ser encaminhado a unidade de outro DRS. A arbitragem é realizada pelo **Grupo de Trabalho de Regulação do DRS** em conjunto com a CROSS, atualizando as regras de roteamento no SIRESP para aquela especialidade e período.

### 2.3 Fiscalização e Acompanhamento Contratual

Os DRS acompanham os **Contratos de Gestão firmados entre a SES-SP e as OSS** nas unidades de seu território. Esse papel inclui:

- Análise mensal dos **relatórios de produção** submetidos pela OSS;
- Participação nas **Comissões de Acompanhamento dos Contratos** (CAC);
- Emissão de **parecer técnico** para fins de liberação de repasse financeiro.

---

## 3. Fluxo Operacional Real: Da Solicitação ao Atendimento

A Versão 2 descreveu as camadas do blueprint de forma sumária. Esta versão reconstrói o fluxo operacional com o detalhamento de cada transição de processo.

### Fase 1 — Solicitação Municipal (UBS/ESF → SIRESP)

1. **Médico da UBS** avalia o caso, define a especialidade necessária e preenche a **Guia de Referência SUS** (física ou em prontuário eletrônico municipal);
2. **Operador de Regulação Municipal** acessa o **SIRESP — Módulo Ambulatorial**, preenche os campos obrigatórios (CNS do paciente, CID-10, dados clínicos sumários, classificação de urgência preliminar) e envia a solicitação para a fila de avaliação;
3. O sistema valida o CNS do paciente contra a **base nacional do Cartão SUS** e o cadastro do CNES da unidade solicitante. Solicitações com inconsistência são **rejeitadas automaticamente**, gerando o **FP13** (inconsistência cadastral);
4. Após validação, a solicitação recebe status "Aguardando Avaliação Médica" na CROSS.

### Fase 2 — Triagem Regulatória (CROSS)

1. **Médico Regulador da CROSS** analisa a solicitação com base nos **Protocolos Clínicos de Regulação** aprovados pela SES-SP para cada especialidade;
2. Classifica a prioridade em escala **P1 (urgente/imediato) a P4 (eletivo sem urgência clínica)**, com critérios clínicos objetivos;
3. Se a solicitação for considerada incompleta ou inadequada, o médico regulador pode: (a) **devolver** ao município solicitante com justificativa para complementação, ou (b) **rebaixar** a prioridade;
4. Casos classificados como P1 são encaminhados diretamente à **regulação de urgência** da CROSS, podendo gerar vaga em Pronto Atendimento ou internação, saindo do fluxo ambulatorial padrão.

### Fase 3 — Disponibilização de Vagas (NIR dos AMEs)

1. O **Núcleo Interno de Regulação (NIR)** de cada AME/Hospital gerencia as **agendas médicas** nos sistemas internos (MV, Pixeon ou similar) e é responsável por disponibilizar vagas para a fila do SIRESP;
2. O NIR realiza periodicamente a **abertura de agenda**: define os slots disponíveis para primeiras consultas (geralmente 60–70% da agenda total) e para retornos (30–40%), conforme metas do contrato com a SES-SP;
3. **Bloqueios de agenda** ocorrem quando: médico está em férias/licença; sala de consulta indisponível (manutenção); ou evento de treinamento/auditoria. Bloqueios não antecipados no SIRESP geram vagas ociosas na fila sem aviso ao paciente (**FP15** — absenteísmo reativo);
4. **Encaixes** são slots emergenciais criados pelo NIR fora do fluxo regular, geralmente para absorver devoluções de vagas ou pacientes P1 reclassificados.

### Fase 4 — Match e Comunicação ao Paciente

1. O **Operador de Regulação da CROSS** realiza o **match** (vinculação) entre o paciente com maior prioridade/tempo de espera e a primeira vaga disponível no raio geográfico do DRS. Em casos de alta demanda, o processo é **manual e crítico**;
2. A vaga é **reservada** no SIRESP vinculada ao CNS do paciente com status "Agendado";
3. A **comunicação ao paciente** é realizada pela UBS de origem por telefone, SMS ou visita do ACS. O SIRESP gera a **Ficha de Agendamento CROSS** que o paciente deve retirar na UBS;
4. **FP06**: Se o paciente não é localizado (telefone desatualizado ou não atendido) em número definido de tentativas, a vaga é **devolvida ao pool** e o paciente retorna à posição original da fila, perdendo o agendamento sem garantia de prazo para nova chamada.

---

## 4. Backstage Detalhado dos AMEs: Processos Internos

### 4.1 Recepção, Validação Cadastral e Check-in

O processo de check-in no AME envolve as seguintes etapas de retaguarda:

- **Conferência documental:** Recepcionista confere ficha CROSS, RG, CNS físico ou Meu SUS Digital e exames anteriores solicitados. Documentação incompleta gera **atendimento condicionado** ou recusa, com orientação ao paciente para regularização;
- **Validação de cadastro:** O sistema interno (MV/Pixeon) busca o CNS no CNES/RNDS para confirmar que o paciente está vinculado ao agendamento existente no SIRESP;
- **Abertura do atendimento:** Após validação, o sistema gera a ficha de atendimento interna e o nome do paciente é inserido na **fila médica eletrônica** do consultório do especialista;
- **Registro de comparecimento:** O NIR registra o comparecimento no SIRESP, o que dispara a contabilização da vaga como "realizada" para fins de metas contratuais.

### 4.2 Gestão de Absenteísmo

A taxa de absenteísmo nas consultas especializadas na rede SES-SP situa-se historicamente entre **20% e 30%**. O protocolo de gestão de absenteísmo inclui:

| Momento | Ação | Responsável |
| :--- | :--- | :--- |
| **D-2 (2 dias antes)** | Ligação ou SMS de confirmação ao paciente | Call Center do AME / Sistema automatizado |
| **D-1 (1 dia antes)** | Segunda tentativa de confirmação; se não confirmado, slot disponibilizado em lista de espera ativa | NIR do AME |
| **D (dia da consulta)** | Falta registrada no SIRESP; slot liberado para encaixe; paciente perde prioridade temporariamente | NIR / CROSS |
| **Pós-evento** | Relatório mensal de absenteísmo por especialidade enviado ao DRS e à Comissão de Acompanhamento do Contrato | Faturamento / NIR |

A ausência de sistema automatizado de confirmação em muitos AMEs faz com que a gestão de absenteísmo seja **reativa** — a vaga só é percebida como ociosa quando o paciente não aparece, sem tempo hábil para preenchimento (**FP15**).

### 4.3 Faturamento, Glosas e Auditoria de Produção

O ciclo de faturamento no AME segue o seguinte fluxo de retaguarda:

1. **Codificação da produção:** O médico especialista registra a evolução clínica e codifica o **CID-10** no prontuário interno. O setor de faturamento converte esse registro em código de **Procedimento SUS** (TUSS/SIGTAP) para gerar o BPA-I (Boletim de Produção Ambulatorial — Individualizado) ou APAC (Autorização para Procedimentos de Alta Complexidade);
2. **Autorização prévia (APAC):** Procedimentos de alta complexidade (ex: hemodiálise, quimioterapia, órteses e próteses) exigem **APAC** com autorização prévia da SES-SP antes da realização. A APAC é solicitada pelo AME no SIRESP/SIA-SUS e aprovada pelo gestor estadual;
3. **Submissão ao SIA-SUS:** O arquivo de produção é enviado eletronicamente ao DATASUS pelo setor de faturamento até o dia **cinco de cada mês** para o mês anterior. Atrasos geram **glosa automática** pelo sistema;
4. **Glosas:** São objetivos de **auditoria posterior** pelo DRS/SES-SP. As glosas mais frequentes são: CID-10 incompatível com o procedimento realizado; APAC sem autorização prévia; prontuário sem assinatura digital ICP-Brasil; divergência entre produção faturada e produção registrada no SIRESP;
5. **Repasse financeiro:** O repasse é calculado sobre a produção **aprovada** (descontadas as glosas), liberado pelo Tesouro Estadual por meio de transferência à conta da OSS ou unidade direta.

### 4.4 Contratos de Gestão com OSS — Estrutura Completa

Os AMEs e Hospitais geridos por Organizações Sociais de Saúde operam sob **Contratos de Gestão** celebrados com a SES-SP. A estrutura desses contratos inclui:

| Componente | Descrição |
| :--- | :--- |
| **Metas quantitativas** | Número mínimo de primeiras consultas, retornos, procedimentos de média e alta complexidade por mês, definido no Anexo Técnico do contrato e atualizado pela Resolução SS-SP nº 44/2021 |
| **Indicadores de qualidade** | Taxa de absenteísmo aceitável (≤ 25%); tempo médio de espera por especialidade; índice de satisfação do usuário (quando disponível); taxa de completude do prontuário |
| **Comissão de Acompanhamento do Contrato (CAC)** | Instância paritária (SES-SP + OSS) que se reúne mensalmente para analisar relatórios de produção, avaliar cumprimento de metas e discutir ajustes |
| **Repasse financeiro** | Calculado com base na produção realizada e aprovada, com parcela fixa (custeio da estrutura) e parcela variável (produção assistencial) |
| **Fiscalização** | DRS realiza visitas técnicas periódicas; SES-SP aplica auditoria documental e amostral |
| **Penalidades e incentivos** | Descumprimento de metas pode gerar glosa contratual proporcional; superação de metas pode gerar repasse de incentivo, conforme cláusula específica |
| **Prazo e renovação** | Contratos geralmente vigentes por 2 a 5 anos, com possibilidade de renovação mediante avaliação de desempenho pela CAC e publicação de novo instrumento |

A fiscalização efetiva desses contratos pelo DRS é variável e depende da capacidade técnica da equipe regional — uma lacuna apontada em relatórios do Tribunal de Contas do Estado (TCE-SP).

---


---

# 5. Estrutura Completa do Service Blueprint AS-IS (Versão Consolidada — Adequação Metodológica)

O Service Blueprint AS-IS foi revisado conforme a metodologia de **Service Blueprint de Shostack**, considerando a jornada do cidadão como eixo central da análise.

O modelo passa a apresentar seis camadas integradas:

1. **Ações do Cidadão** — atividades realizadas pelo usuário;
2. **Linha de Interação** — momentos de contato direto entre cidadão e serviço;
3. **Frontstage (ações visíveis)** — atividades percebidas pelo cidadão;
4. **Linha de Visibilidade** — separação entre ações percebidas e internas;
5. **Backstage (ações internas)** — processos necessários para execução do serviço;
6. **Processos de Apoio/Suporte** — estruturas organizacionais, tecnológicas e administrativas que sustentam a operação.

---

# 5.1 Jornada Executiva do Cidadão — Visão Consolidada

| Momento | Ação do cidadão | Interação com o serviço | Processo interno | Principal falha |
|---|---|---|---|---|
| Descoberta | Busca orientação para atendimento | Procura a porta de entrada SUS | Organização dos canais e informações | Dificuldade de identificar o fluxo correto |
| Entrada | Procura atendimento na UBS | Consulta e encaminhamento | Avaliação clínica e registro | Espera inicial |
| Solicitação | Apresenta documentos | Inserção da solicitação | Registro e validação no sistema | Dados incompletos ou inconsistência cadastral |
| Regulação | Aguarda especialista | Recebe comunicação eventual | Avaliação CROSS e gestão da fila | Fila invisível |
| Agendamento | Confirma atendimento | Recebe data e local | Match paciente-vaga | Perda de vaga por falha de comunicação |
| Atendimento | Comparece ao AME/Hospital | Recepção e consulta | Gestão de agenda e prontuário | Falta de integração clínica |
| Continuidade | Realiza exames e acompanha tratamento | Recebe orientações | Contrarreferência e continuidade | Fragmentação do cuidado |

---

# 5.2 Camadas do Blueprint

## Camada 1 — Ações do Cidadão

O cidadão realiza:

- Busca de informação;
- Atendimento inicial na UBS;
- Entrega de documentos;
- Acompanhamento da solicitação;
- Comparecimento ao atendimento especializado;
- Recebimento de orientações e continuidade do cuidado.

## Camada 2 — Linha de Interação

Principais pontos de contato:

- Atendimento na UBS;
- Comunicação do agendamento;
- Recepção no AME;
- Consulta médica;
- Entrega de documentos pós-consulta.

## Camada 3 — Frontstage (visível ao cidadão)

| Atividade percebida | Evidência |
|---|---|
| Atendimento inicial | UBS, equipe assistencial e encaminhamento |
| Comunicação | SMS, telefone ou aviso institucional |
| Atendimento especializado | Recepção, consulta e documentos médicos |

## Camada 4 — Linha de Visibilidade

| O cidadão vê | O cidadão não vê |
|---|---|
| Recebe encaminhamento | Critérios de regulação clínica |
| Aguarda vaga | Gestão da fila no sistema |
| Recebe agendamento | Processo de seleção da vaga |
| Realiza consulta | Processos administrativos e faturamento |

## Camada 5 — Backstage

Atividades internas:

- Regulação CROSS;
- Gestão de vagas pelo NIR;
- Controle de agendas;
- Atualização de sistemas;
- Registro assistencial;
- Auditoria e faturamento.

## Camada 6 — Processos de Apoio/Suporte

| Processo | Função |
|---|---|
| Sistemas de informação | Sustentar registros e comunicação |
| Governança regional | Pactuação e acompanhamento territorial |
| Gestão contratual | Monitorar metas assistenciais |
| Auditoria | Garantir qualidade e conformidade |
| Infraestrutura | Viabilizar atendimento presencial |

---

# 5.3 Blueprint AS-IS Consolidado

| Etapa | Ação do cidadão | Frontstage | Backstage | Fail Point |
|---|---|---|---|---|
| Entrada | Busca atendimento | UBS orienta usuário | Avaliação clínica | FP01 / FP03 |
| Solicitação | Entrega documentos | Atendimento administrativo | Registro no sistema | FP04 / FP13 |
| Regulação | Aguarda consulta | Comunicação eventual | CROSS avalia prioridade | FP05 |
| Agendamento | Confirma consulta | SMS/ligação | Gestão de vaga | FP06 |
| Atendimento | Realiza consulta | Recepção e médico | NIR e prontuário | FP07 |
| Continuidade | Segue tratamento | Recebe orientações | Contrarreferência | FP08 / FP10 |

---


## 5. Estrutura de Camadas do Service Blueprint AS-IS

Mapeamento integrado das três linhas fundamentais do serviço em cada macroetapa da jornada, com detalhamento operacional aprofundado.

### Macroetapa A: Acesso e Solicitação (UBS/Rede Municipal)

- **Linha de Interação:** Cidadão relata sintomas, recebe guia de encaminhamento, aguarda inserção no SIRESP e informação sobre prazo estimado.
- **Linha de Visibilidade:** Médico da UBS preenchendo guia; recepcionista inserindo dados no terminal; senha de protocolo de regulação entregue ao paciente.
- **Linha de Retaguarda:**
  - Avaliação clínica da necessidade → Médico da UBS → e-SUS PEC → Registro com CID-10 preliminar.
  - Inserção da solicitação → Operador de Regulação Municipal → SIRESP Módulo Ambulatorial → Status "Aguardando Avaliação". Validação automática de CNS e CNES.
  - **FP13:** Se CNS apresentar inconsistência, solicitação é rejeitada e deve ser regularizada antes de nova tentativa.

### Macroetapa B: Regulação (CROSS e DRS)

- **Linha de Interação:** Cidadão aguarda passivamente por semanas ou meses, sem acesso a informações sobre posição ou prazo.
- **Linha de Visibilidade:** Eventual contato por telefone de número desconhecido ou SMS da UBS comunicando o agendamento.
- **Linha de Retaguarda:**
  - Triagem clínica → Médico Regulador CROSS → SIRESP → Prioridade P1 a P4 atribuída.
  - Gestão de vagas → NIR do AME → Sistema interno MV/Pixeon → Vagas abertas ou bloqueadas no SIRESP.
  - Match → Operador CROSS → SIRESP → Vaga vinculada ao CNS do paciente; status "Agendado".
  - Comunicação → APS-MUN / Call Center → Telefone ou SMS → Paciente confirmado ou vaga devolvida ao pool.
  - **FP14:** Duplicidade de solicitação para mesmo CNS e especialidade não é bloqueada pelo sistema, distorcendo a posição real na fila.
  - Supervisão regional → DRS → Relatórios SIRESP Módulo Indicadores → Pactuação ajustada quando desequilíbrio oferta/demanda é identificado.

### Macroetapa C: Atendimento (AME / Hospital Estadual)

- **Linha de Interação:** Cidadão desloca-se ao município polo, faz check-in, passa por triagem de enfermagem, realiza consulta e retira documentos.
- **Linha de Visibilidade:** Recepção com painel de senhas; consultório do especialista com computador com prontuário visível; entrega de receita, pedidos de exame e contrarreferência em papel.
- **Linha de Retaguarda:**
  - Check-in → Recepcionista → MV/Pixeon → Abertura do atendimento; comparecimento registrado no SIRESP pelo NIR.
  - Consulta → Médico Especialista → Prontuário interno → Evolução clínica com CID-10, assinatura ICP-Brasil.
  - Faturamento → Setor FAT → SIA-SUS → BPA-I ou solicitação de APAC gerada; glosas tratadas.
  - Gestão de absenteísmo → NIR → SIRESP → Faltas registradas; lista de espera ativa acionada para encaixes.
  - Fiscalização de metas → DRS/CAC → Relatório mensal → Adequação do repasse contratual.

---

## 6. Evidências Físicas do Serviço

| Etapa | Evidência | Classificação | Papel na Experiência |
| :--- | :--- | :--- | :--- |
| Pré-acesso | App Meu SUS Digital / Portal gov.br | Evidência Digital | Canal de busca de informação e localização de unidades (CNES) |
| UBS | Prédio físico com sinalização e placa institucional | Evidência Física | Percepção inicial de acolhimento e organização do serviço |
| UBS | Cartão Nacional de Saúde (físico ou digital) | Evidência Física/Digital | Chave de identidade no ecossistema SUS |
| UBS | Guia de Encaminhamento SUS / Protocolo de Regulação | Documento Gerado | Comprovante material de que o pedido foi formalizado |
| UBS | Senha de atendimento (triagem da UBS) | Evidência Física | Sinaliza organização e fila gerenciada |
| Regulação | SMS de agendamento da CROSS/UBS | Comunicação Institucional | Informa o agendamento; reduz (parcialmente) a ansiedade da espera |
| Regulação | Ficha de Agendamento CROSS impressa na UBS | Documento Gerado | Comprovante com data, hora, endereço e especialidade |
| AME | Prédio físico (fachada, sinalização, estacionamento, recepção) | Evidência Física | Sinaliza estrutura e qualidade percebida da unidade especializada |
| AME | Senha eletrônica de atendimento | Evidência Física | Transparência e controle do tempo de espera local |
| AME | Tela do prontuário eletrônico visível durante consulta | Evidência Digital | Sinaliza registro formal e sistematizado do histórico clínico |
| Pós-consulta | Receita médica carimbada e assinada | Documento Gerado | Resultado prático da consulta; autoriza dispensação de medicamentos |
| Pós-consulta | Pedido de exame (BPA ou APAC) | Documento Gerado | Orienta o próximo passo diagnóstico, mas sem fluxo integrado de agendamento |
| Pós-consulta | Contrarreferência em papel | Documento Gerado | Único veículo de comunicação entre especialista e APS — entregue ao próprio paciente |
| Pós-consulta | Ausência de comprovante de continuidade integrada | Ausência perceptível | Cidadão sai sem saber quem é responsável pelo próximo passo |

---

## 7. Normativos Aplicáveis (Federais e Estaduais Específicos)

| Norma | Tema Relacionado | Impacto no Processo de Consulta Médica |
| :--- | :--- | :--- |
| **Constituição Federal (Art. 196–200)** | Direito à Saúde e Universalidade | Garante acesso universal e gratuito, vedando cobrança em qualquer etapa da jornada. |
| **Lei Federal nº 8.080/1990** | Organização e Princípios do SUS | Consolida integralidade, hierarquização e regionalização; fundamenta o encaminhamento obrigatório da APS para a média complexidade. |
| **Lei Federal nº 9.637/1998** | Organizações Sociais (OS) | Autoriza a contratação de entidades privadas sem fins lucrativos para gestão de serviços públicos de saúde mediante Contrato de Gestão. |
| **Portaria GM/MS nº 2/2017** | Política Nacional de Regulação | Veda o acesso direto do paciente à consulta especializada sem mediação regulatória; organiza o fluxo CROSS. |
| **Portaria GM/MS nº 1.631/2015** | Parâmetros Assistenciais (revoga 1.101/2002) | Substituiu os tetos rígidos de consultas por parâmetros indicativos flexíveis, adequados à realidade local. |
| **Portaria GM/MS nº 635/2023** | Equipes Multiprofissionais (eMulti) | Regula custeio e modalidades das eMulti de apoio à APS; viabiliza telessaúde e aumenta resolutividade antes do encaminhamento especializado. |
| **Portaria GM/MS nº 1.604/2023** | PNAES — Política Nacional de Atenção Especializada | Define diretrizes para organização da atenção especializada ambulatorial e hospitalar no SUS, com ênfase em regionalizaçação e fluxos regulados. |
| **Portaria GM/MS nº 1.820/2009** | Carta dos Direitos dos Usuários do SUS | Garante ao usuário direito à informação sobre fila e prazo de espera, acesso ao prontuário e tratamento humanizado — base jurídica para exigir transparência no SIRESP. |
| **Decreto Estadual SP nº 56.061/2010** | Institucionalização da CROSS | Cria e organiza a Central de Regulação de Ofertas de Serviços de Saúde no Estado de São Paulo. |
| **Decreto Estadual SP nº 43.493/1998** | Organizações Sociais (SP) | Regulamenta, no âmbito estadual, a qualificação de OSS e os requisitos para celebração de Contratos de Gestão com a SES-SP. |
| **Resolução SS-SP nº 44/2021** | Contratualização OSS / Metas | Define metas mensais obrigatórias de primeiras consultas e retornos para cada AME/Hospital gerido por OSS, com impacto direto no volume de vagas disponibilizado no SIRESP. |
| **STF — Tema 698 (RE nº 684.612/RJ)** | Judicialização e OS | Legitima intervenção judicial em políticas de saúde por grave deficiência do serviço; chancela constitucionalidade das OSS como alternativa ao concurso público para provimento de pessoal. |

---

## 7.1 Interface com a Saúde Suplementar e a ANS

A Segunda Auditoria identificou como ponto parcialmente aberto a lacuna sobre "como a regulação estadual paulista trata usuários com cobertura suplementar, ressarcimento ao SUS, interoperabilidade e conflitos de fila." Esta seção endereça esse ponto.

### 7.1.1 Ressarcimento ao SUS (Art. 32, Lei nº 9.656/1998)

Quando um beneficiário de plano de saúde privado utiliza serviços da rede SUS — inclusive AMEs e Hospitais Estaduais da SES-SP —, a operadora de plano de saúde é obrigada a ressarcir o Fundo Nacional de Saúde pelo custo do atendimento. O mecanismo opera assim:

- O AME/Hospital registra o atendimento normalmente no SIA-SUS com BPA-I ou APAC;
- O DATASUS identifica, por cruzamento do CNS do paciente com a base da ANS, se o beneficiário possui cobertura suplementar ativa;
- A ANS notifica a operadora e emite a Guia de Ressarcimento ao SUS (GR-SUS);
- O ressarcimento é depositado no Fundo Nacional de Saúde, **não retornando diretamente ao AME prestador**, o que gera baixo incentivo para o registro correto da situação suplementar.

**Impacto na operação SES-SP:** O fluxo de regulação CROSS/SIRESP não distingue operacionalmente usuários com ou sem cobertura suplementar — o acesso à consulta especializada no AME é igual para ambos, desde que mediado pela regulação estadual. Não existe fila paralela ou preferência para beneficiários de plano que optam pelo SUS.

### 7.1.2 Conflito de Fila e Dupla Cobertura

Cidadãos com cobertura suplementar que utilizam o SUS para consultas especializadas (por exemplo, em especialidades não cobertas pelo plano ou em municípios sem rede credenciada do plano) entram na mesma fila regulada do SIRESP. A **Portaria GM/MS nº 1.820/2009** garante ao usuário o direito de usar o SUS independentemente de possuir cobertura suplementar. Não existe mecanismo operacional na SES-SP para redirecionar automaticamente esses usuários para a rede suplementar, uma vez que a regulação estadual não tem acesso em tempo real à base de beneficiários da ANS.

**FP Derivado:** A ausência de interoperabilidade entre a base ANS e o SIRESP impede que o médico regulador da CROSS saiba se o paciente possui cobertura suplementar que poderia absorver a demanda, potencialmente liberando vagas SUS para pacientes exclusivamente dependentes do sistema público.

### 7.1.3 Interoperabilidade RNDS entre Setores Público e Suplementar

A **Rede Nacional de Dados de Saúde (RNDS)** é a principal plataforma de interoperabilidade clínica entre os setores público e suplementar, prevista na **Lei 9.656/1998 (Art. 32 e correlatos)** e operada pelo DATASUS. Em termos práticos para os AMEs da SES-SP:

| Dimensão | Situação Atual | Impacto |
| :--- | :--- | :--- |
| Integração AME → RNDS | Em implantação parcial; não universalizada nos AMEs paulistas | Especialista no AME não acessa histórico de plano de saúde do paciente |
| Integração Plano → RNDS | Obrigatória para operadoras acima de 100 mil beneficiários (RN ANS 452/2020) | Dados suplementares disponíveis na RNDS mas não acessados pelos sistemas AME |
| Resultado prático | Cidadão com plano de saúde repete exames no SUS que já fez no plano | Duplicação de custos para o sistema; atraso diagnóstico |

A universalização da RNDS nos AMEs estaduais é condição necessária tanto para resolver o FP07 (ausência de histórico clínico da UBS) quanto para eliminar a duplicação de exames com a rede suplementar.

---

## 8. Identificação de Fail Points

### Falhas na Jornada do Cidadão

#### FP01 — Porta de Entrada Desconhecida
- **Etapa:** Pré-acesso.
- **Problema:** Cidadão não sabe identificar a porta de entrada correta (UBS vs. UPA vs. Pronto-Socorro) para obter encaminhamento à consulta especializada.
- **Causa Provável:** Ausência de canal único de orientação pré-acesso; comunicação institucional fragmentada entre SES-SP, municípios e governo federal.
- **Impacto no Cidadão:** Deslocamento desnecessário; início equivocado do fluxo; potencial negativa de atendimento no local errado.
- **Consequência Operacional:** Superlotação de prontos-socorros com demandas que deveriam iniciar na UBS.
- **Indicador:** Taxa de encaminhamentos gerados fora da APS / Percentual de primeiras consultas sem referência da UBS.

#### FP02 — Informação Insuficiente sobre Documentos e Fluxo
- **Etapa:** Pré-acesso.
- **Problema:** Cidadão não sabe quais documentos trazer à UBS ou ao AME, nem o que esperar do processo de regulação.
- **Causa Provável:** Ausência de roteiro de orientação padronizado entregue na UBS ao ser gerado o encaminhamento.
- **Impacto:** Múltiplos retornos à UBS por documentação incompleta; frustração e desistência.
- **Indicador:** Percentual de atendimentos cancelados por documentação incompleta.

#### FP03 — Dificuldade de Acesso à Consulta Inicial na UBS
- **Etapa:** APS/UBS.
- **Problema:** Antes de chegar ao especialista, o cidadão precisa conseguir consulta com o médico generalista na UBS — o que pode levar dias ou semanas, dependendo da disponibilidade local.
- **Causa Provável:** Déficit de médicos generalistas em algumas regiões; concentração do deficit nas periferias urbanas e municípios de pequeno porte.
- **Impacto:** Atraso no início do fluxo especializado; agravamento clínico antes mesmo de chegar à regulação.
- **Indicador:** Tempo médio de espera para consulta básica na UBS por município.

#### FP04 — Encaminhamento Incompleto ou Recusado pela Regulação
- **Etapa:** APS → Regulação.
- **Problema:** A solicitação inserida no SIRESP pelo operador municipal é rejeitada ou rebaixada de prioridade por dados clínicos insuficientes (CID-10 ausente, anamnese sumária sem critérios de urgência, campos obrigatórios em branco).
- **Causa Provável:** Falta de treinamento contínuo dos operadores de regulação municipal; ausência de validação obrigatória de campos no sistema antes do envio.
- **Impacto:** Retrabalho e atraso adicional; paciente notificado de recusa sem saber o motivo ou o prazo para correção.
- **Indicador:** Taxa de solicitações devolvidas por irregularidade técnica / Percentual de rejeições por especialidade.

#### FP05 — Fila Invisível: Cidadão Sem Informação Sobre Posição ou Prazo de Espera (CRÍTICO)
- **Etapa:** Regulação.
- **Problema:** O cidadão aguarda meses sem qualquer informação sobre sua posição na fila do SIRESP ou o tempo estimado de atendimento.
- **Causa Provável:** Ausência de módulo de transparência ativa no SIRESP voltado ao usuário final; o sistema é interno e acessível apenas por operadores credenciados.
- **Impacto:** Ansiedade severa; agravamento clínico silencioso; busca por atalhos (judicialização, UPAs, emergências).
- **Consequência Operacional:** Aumento de mandados judiciais que furam a ordem técnica de prioridade médica; sobrecarga das ouvidorias.
- **Indicador:** Tempo Médio de Espera por Especialidade (dias); Índice de Judicialização de Consultas por 100 mil hab.

#### FP06 — Vaga Perdida por Falha de Comunicação ou Dado Cadastral Desatualizado (CRÍTICO)
- **Etapa:** Confirmação do Agendamento.
- **Problema:** A comunicação do agendamento ocorre com poucos dias de antecedência, por chamadas de número oculto ou SMS sem interatividade. Paciente não localizado perde a vaga e retorna à fila original.
- **Causa Provável:** Cadastro do CNS desatualizado (especialmente telefone); dependência de ligação síncrona sem confirmação digital assíncrona.
- **Impacto:** Perda de encaminhamento; reinício do processo desde a UBS; agravamento clínico.
- **Consequência Operacional:** Taxa de absenteísmo 20–30%; slots ociosos em AMEs de alta complexidade; desperdício financeiro.
- **Indicador:** Taxa de Absenteísmo em Consultas Especializadas; Percentual de vagas devolvidas por não-localização do paciente.

### Falhas Internas (Perspectiva Operacional e de Retaguarda)

#### FP07 — Especialista Sem Acesso ao Histórico Clínico da UBS (CRÍTICO)
- **Etapa:** Atendimento Especializado.
- **Problema:** O médico especialista no AME ou Hospital Estadual não visualiza os registros clínicos, exames anteriores e anamnese realizados na UBS municipal.
- **Causa Provável:** Falta de barramento de interoperabilidade entre sistemas municipais (e-SUS PEC) e sistemas estaduais (MV/Pixeon). A RNDS ainda está em implantação parcial e não cobre a maioria dos municípios paulistas.
- **Impacto:** Paciente repete toda a história clínica verbalmente; refaz exames laboratoriais desnecessariamente; risco de decisão clínica inadequada por falta de contexto.
- **Consequência Operacional:** Duplicação de custos com exames diagnósticos; perda de produtividade do especialista.
- **Indicador:** Percentual de consultas com prontuário interoperável / Taxa de redundância de exames.

#### FP08 — Pedido de Exame Sem Fluxo Integrado de Agendamento (CRÍTICO)
- **Etapa:** Pós-consulta.
- **Problema:** Paciente sai do AME com solicitação de exame em mãos, sem saber onde realizá-lo, qual serviço aceita a APAC ou o BPA, ou como entrar na fila de exames regulados.
- **Causa Provável:** Ausência de pactuação contratual obrigatória de agendamento integrado de exames na saída do AME; responsabilidade pelo encaminhamento ao exame não está atribuída a nenhum ator.
- **Impacto:** Exame não realizado; seguimento clínico interrompido; retorno desnecessário ao especialista sem resultado.
- **Indicador:** Percentual de APACs solicitadas que resultam em procedimento realizado em até 30 dias.

#### FP09 — Resultado de Exame Não Chega ao Profissional ou ao Cidadão
- **Etapa:** Pós-consulta.
- **Problema:** O resultado do exame realizado na rede executante (laboratório, radiologia) não é integrado ao prontuário do especialista no AME nem ao prontuário da UBS.
- **Causa Provável:** Ausência de integração sistêmica entre rede executante de exames e sistemas de prontuário estaduais/municipais; resultado entregue apenas em papel ao paciente.
- **Impacto:** Retorno clínico prejudicado; decisão médica sem informação diagnóstica atualizada.
- **Indicador:** Percentual de exames com resultado integrado ao prontuário do solicitante.

#### FP10 — Contrarreferência Sem Retorno Digital à APS
- **Etapa:** Encerramento e Continuidade do Cuidado.
- **Problema:** Após a consulta, a orientação clínica de continuidade não chega formalmente ao médico de família na UBS de origem. O documento é entregue em papel ao paciente, que assume o papel de mensageiro do sistema.
- **Causa Provável:** Ausência de fluxo digital de contrarreferência integrado entre o AME e o prontuário eletrônico municipal; falta de responsabilização institucional pelo ato de comunicar.
- **Impacto:** Descontinuidade terapêutica; risco de prescrições conflitantes ou duplicadas.
- **Consequência Operacional:** Retorno desnecessário de pacientes crônicos à fila da média complexidade, sufocando oferta de vagas para novos casos.
- **Indicador:** Índice de Efetividade da Contrarreferência Digital (documentos devolvidos eletronicamente).

#### FP13 — Inconsistência Cadastral Impede a Solicitação
- **Etapa:** APS → Regulação.
- **Problema:** CNS desatualizado, duplicado ou com dados divergentes entre municípios impede que a solicitação seja aceita pelo SIRESP na validação automática.
- **Causa Provável:** Base do CNS com atualização fragmentada; migração incompleta de registros entre sistemas municipais; ausência de processo sistemático de higienização cadastral.
- **Impacto:** Atraso no início do processo regulatório; cidadão sem saber que a solicitação foi rejeitada.
- **Indicador:** Taxa de solicitações rejeitadas por inconsistência de CNS.

#### FP14 — Duplicidade de Solicitação Distorce a Fila
- **Etapa:** Regulação.
- **Problema:** O mesmo paciente pode ter solicitações duplicadas inseridas por unidades distintas (ex: o cidadão foi a dois municípios diferentes para o mesmo encaminhamento), distorcendo sua posição real na fila.
- **Causa Provável:** Ausência de validação de unicidade de solicitação por CNS+especialidade no SIRESP; paciente não informa que já tem solicitação ativa.
- **Impacto Operacional:** Distorção do tempo médio real de espera; aproveitamento duplo de vaga (se não detectado).
- **Indicador:** Taxa de duplicidades detectadas e canceladas no SIRESP por período.

#### FP15 — Gestão de Absenteísmo Reativa: Slot Ocioso Não Preenchido a Tempo
- **Etapa:** Atendimento.
- **Problema:** A falta do paciente só é percebida quando ele não aparece no horário. Sem lista de espera ativa com candidatos confirmados para encaixe imediato, o slot fica ocioso.
- **Causa Provável:** Ausência de sistema automatizado de confirmação e lista de espera ativa em muitos AMEs; processo de confirmação manual e dependente de call center insuficientemente dimensionado.
- **Impacto Operacional:** Taxa de ociosidade adicional de 5–15% sobre a taxa base de absenteísmo; custo do especialista contratado sem produção.
- **Indicador:** Taxa de slots ociosos por não-preenchimento de falta no dia / Percentual de encaixes realizados vs. faltas registradas.

---

## 9. Tabela Completa do Service Blueprint AS-IS (V3)

| Etapa da Jornada | Ação do Cidadão | Ponto de Contato | Evidência Física/Digital | Processo de Bastidor | Responsável | Sistema Utilizado | Norma Relacionada | Fail Points |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **0. Pré-acesso** | Busca informação sobre onde buscar atendimento. | Portal gov.br / App Meu SUS / ACS | Site SES-SP; app Meu SUS Digital; sinalização urbana de UBS. | Gestão de canais digitais e call centers institucionais; sem processo formalizado de orientação pré-acesso. | SUP-FED / CID | Portal gov.br / CNES / Meu SUS Digital | CF Art. 196; Lei 8.080 (universalidade) | FP01 (porta errada); FP02 (info insuficiente) |
| **1. Triagem na APS** | Relata sintomas ao médico generalista na UBS. | Consultório médico da UBS de origem. | Guia de encaminhamento; ficha de triagem; Cartão SUS. | Avaliação clínica; registro no prontuário eletrônico municipal; emissão da Guia de Referência SUS com CID-10. | Médico Generalista Municipal (APS-MUN) | e-SUS PEC / Prontuário Municipal | Lei 8.080 (integralidade); Portaria 635/2023 (eMulti) | FP03 (fila UBS); FP04 (encaminhamento incompleto) |
| **2. Solicitação e Inserção no SIRESP** | Entrega guia no balcão administrativo da UBS. | Guichê de regulação da UBS. | Protocolo de recebimento; ficha de protocolo de regulação entregue ao paciente. | Inserção da solicitação no SIRESP Módulo Ambulatorial; validação automática do CNS e CNES; status "Aguardando Avaliação". | Operador de Regulação Municipal (APS-MUN) | **SIRESP — Módulo Ambulatorial** | Portaria GM/MS 2/2017 (Regulação) | FP04 (dados incompletos → recusa); FP13 (CNS inconsistente → rejeição automática) |
| **3. Triagem Regulatória CROSS** | Aguarda passivamente em casa. | Nenhum contato visível. | Ausente. | Médico Regulador avalia caso e classifica prioridade P1 a P4; devolve ao município se dados insuficientes. | Médico Regulador (REG-EST / CROSS) | **SIRESP** | Diretrizes Técnicas CROSS; Portaria GM/MS 2/2017 | **FP05** CRÍTICO (fila invisível); FP14 (duplicidade) |
| **4. Disponibilização de Vagas (NIR)** | Aguarda processamento interno. | Nenhum contato visível. | Ausente. | NIR abre/parametriza agenda no sistema interno; carrega vagas no SIRESP; gerencia bloqueios, encaixes e absenteísmo preventivo. | NIR do AME/Hospital (AMB-OSS / AMB-EST) | Sistema Interno (MV/Pixeon) + SIRESP | Resolução SS-SP 44/2021 (metas OSS) | FP15 (absenteísmo reativo sem lista espera ativa) |
| **5. Match e Comunicação do Agendamento** | Atende telefone ou recebe SMS; confirma presença ou retira ficha CROSS na UBS. | Chamada telefônica; SMS; visita do ACS. | Ficha de Agendamento CROSS impressa na UBS. | Match vaga-paciente pelo operador CROSS; atualização de status no SIRESP; acionamento da UBS para comunicar o paciente. | REG-EST / APS-MUN / DRS (supervisão) | SIRESP / Telefonia / SMS | Princípio da Eficiência Administrativa | **FP06** CRÍTICO (vaga perdida) |
| **6. Check-in na Unidade Especializada** | Desloca-se ao polo; apresenta-se na recepção com ficha CROSS e documentos. | Recepção do AME/Hospital. | Painel de senhas; senha de atendimento; documentos validados. | Conferência documental; validação de CNS; abertura de atendimento no prontuário interno; registro de comparecimento no SIRESP pelo NIR. | Recepcionista (AMB-OSS/AMB-EST); NIR | MV ou Pixeon; SIRESP | Regras de Faturamento SIA-SUS | Atraso na triagem da recepção; erro cadastral no check-in |
| **7. Consulta com Especialista** | Passa por triagem de enfermagem; relata histórico ao especialista; realiza exame físico; recebe diagnóstico. | Consultório médico da unidade estadual. | Tela do prontuário interno; estetoscópio; resultados impressos de exames anteriores. | Registro de evolução clínica; CID-10; assinatura digital ICP-Brasil; emissão de receita e pedidos de exame; solicitação de APAC se necessário. | Médico Especialista (AMB-OSS/AMB-EST); FAT | Prontuário Interno (MV/Pixeon); SIA-SUS | Código de Ética Médica; Portaria 1.604/2023 (PNAES) | **FP07** CRÍTICO (sem histórico clínico da UBS) |
| **8. Desfecho e Continuidade do Cuidado** | Retira receita, pedidos de exame e contrarreferência; tenta agendar exames sem fluxo definido. | Balcão pós-consulta ou mesa médica. | Receita carimbada; pedido de exame (BPA/APAC); contrarreferência em papel entregue ao paciente. | Faturamento BPA-I ou APAC no SIA-SUS; tratamento de glosas; emissão de contrarreferência em papel. Paciente é o único mensageiro entre os níveis. | Médico Especialista; FAT; APS-MUN (se receber a contrarreferência) | SIA-SUS; SIRESP (novos pedidos); Prontuário Interno | Lei 8.080 (continuidade); Portaria 1.820/2009 (Carta de Direitos) | **FP08** CRÍTICO (sem fluxo de exames); FP09 (resultado não integrado); FP10 (contrarreferência não chega à APS); FP11 (sem responsável definido); FP12 (retrabalho sistêmico) |

---

## 10. Diretrizes Estratégicas para Transformação (TO-BE)

Com base no diagnóstico operacional aprofundado desta V3:

1. **Portal Cidadão de Transparência Regulatória:** Interface pública integrada ao app Meu SUS Digital que permita ao usuário consultar a posição de sua solicitação no SIRESP, a classificação de prioridade atribuída pelo médico regulador e o tempo médio de espera estimado para sua especialidade e DRS — abordando FP05, FP06 e FP14.

2. **Sistema Nacional de Confirmação e Lista de Espera Ativa:** Substituição das chamadas de número oculto por sistema omnichannel (WhatsApp institucional, SMS interativo, e-mail) com confirmação digital e lista de espera ativa para preenchimento imediato de faltas — abordando FP06 e FP15.

3. **Barramento de Interoperabilidade HL7/FHIR (via RNDS):** Priorização da conexão de todos os AMEs e Hospitais Estaduais paulistas à Rede Nacional de Dados de Saúde (RNDS) com os prontuários eletrônicos municipais, eliminando a fragmentação de informações clínicas — abordando FP07 e FP12.

4. **Agendamento Integrado de Exames na Saída do AME:** Inclusão como meta contratual obrigatória nas OSS que nenhum paciente saia do AME com pedido de exame sem agendamento efetivado na própria unidade ou na rede de apoio regional direta — abordando FP08 e FP09.

5. **Contrarreferência Digital Obrigatória:** Implementação de contrarreferência eletrônica integrada ao SIRESP e ao prontuário municipal, com prazo máximo de envio de 48h após a consulta — abordando FP10 e FP11.

6. **Higienização Cadastral Proativa do CNS:** Programa sistemático de atualização e validação do Cartão Nacional de Saúde junto aos municípios, integrado ao processo de inserção de solicitações no SIRESP — abordando FP13.

---

**Fontes e Referências Documentais:**

- Secretaria de Estado da Saúde de São Paulo (SES-SP) — Manuais e Diretrizes Operacionais da CROSS e do SIRESP; Resoluções internas.
- Ministério da Saúde — Política Nacional de Regulação do SUS; Banco de Dados do DATASUS; Portaria GM/MS nº 1.604/2023 (PNAES).
- Tribunal de Contas do Estado de São Paulo (TCE-SP) — Relatórios de Fiscalização de Contratos de Gestão com OSS na Saúde.
- Supremo Tribunal Federal (STF) — Acórdão do Tema 698 de Repercussão Geral (RE nº 684.612/RJ).
- Legislação Federal: Lei nº 8.080/1990; Lei nº 8.142/1990; Lei nº 9.637/1998; Portaria GM/MS nº 2/2017; Portaria GM/MS nº 1.631/2015; Portaria GM/MS nº 1.820/2009; Portaria GM/MS nº 635/2023.
- Legislação Estadual: Decreto Estadual SP nº 56.061/2010; Decreto Estadual SP nº 43.493/1998; Resolução SS-SP nº 44/2021.
- Literatura especializada: estudos sobre jornada do paciente no SUS, fragmentação de prontuários e absenteísmo em atenção especializada ambulatorial.
