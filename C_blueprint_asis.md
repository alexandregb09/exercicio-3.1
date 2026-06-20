# Service Blueprint AS-IS — Consulta Médica Especializada (Ambulatorial)
## Secretaria de Estado da Saúde de São Paulo (SES-SP) — Sistema Único de Saúde
**Versão:** 2.0 | **Metodologia:** Shostack (1984) com extensões contemporâneas de Service Design  
**Elaborado com base em:** `B_relatorio_assistente_v3.md` | **Sessão de refinamento:** `C_grill_transcript.md`

---

## Premissas metodológicas

Este blueprint adota as **5 camadas padrão de Shostack (1984)** como estrutura principal — Evidências Físicas, Ações do Cidadão, Frontstage, Backstage e Processos de Suporte, separadas pelas Linhas de Interação, Visibilidade e Interação Interna. Após as 5 camadas padrão são apresentadas quatro **extensões analíticas** explicitamente identificadas como adições ao modelo clássico:

- **Extensão A — Emoção do Cidadão**: camada emocional acima das evidências físicas (hipótese inferida da literatura e dos fail points; a validar em campo)
- **Extensão B — Atores Responsáveis**: mapeia a esfera institucional de cada ator por macroetapa (federal, estadual, OSS, municipal)
- **Extensão C — Normas Transversais**: camada de governança que perpassa todas as macroetapas
- **Extensão D — Fail Points catalogados**: com identificação de prioridade, categoria e tipo de evidência

**Fronteiras da jornada:** Da percepção da necessidade de saúde (pré-acesso) até a tentativa de continuidade do cuidado pós-consulta especializada (pós-acesso).

**Canal analisado:** Atendimento **presencial**, modalidade **ambulatorial especializada**, com foco nos Ambulatórios Médicos de Especialidades (AMEs) e Hospitais Estaduais geridos pela SES-SP (diretamente ou via OSS).

---

### Legenda de evidências

| Código | Tipo |
| :--- | :--- |
| **D** | Documental direta — norma, manual, sistema ou documento oficial |
| **L** | Literatura e estudos de saúde pública |
| **I** | Inferência analítica — deduzida de falhas, fluxos e documentos existentes |
| **V** | Necessita validação por pesquisa de campo |

### Legenda de atores

| Código | Ator | Esfera |
| :--- | :--- | :--- |
| CID | Cidadão | — |
| APS-MUN | Atenção Primária Municipal (UBS / ESF / eMulti / Operador de Regulação) | Municipal |
| DRS | Departamento Regional de Saúde | Estadual |
| REG-EST | Regulação Estadual — CROSS, médicos reguladores e operadores SIRESP | Estadual |
| NIR | Núcleo Interno de Regulação do AME ou Hospital | Estadual / Contratado |
| AMB-EST | Ambulatório Estadual — administração direta | Estadual |
| AMB-OSS | Ambulatório gerenciado por OSS (Lei 9.637/1998) | Estadual/Contratado |
| FAT | Setor de Faturamento e Auditoria da unidade | Estadual/Contratado |
| SUP-FED | Sistemas e suporte federal (DATASUS, RNDS, MS) | Federal |

---

## Blueprint AS-IS — Matriz Principal (5 Camadas Shostack)

> **Leitura:** Linhas = camadas do serviço | Colunas = macroetapas da jornada (esquerda → direita = progressão temporal)  
> As 5 camadas abaixo correspondem à estrutura padrão de Shostack (1984). As extensões analíticas estão na seção seguinte.

---

### CAMADA 1 — Evidências Físicas *(Shostack, 1984: Physical Evidence) — D para macroetapas 2–4; I/L para 1 e 5*

| | **Macroetapa 1** Pré-acesso | **Macroetapa 2** APS / UBS | **Macroetapa 3** Regulação | **Macroetapa 4** Atendimento Especializado | **Macroetapa 5** Continuidade do Cuidado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Evidências Físicas** | Portal gov.br / App Meu SUS Digital / Centrais telefônicas 156 / Informações de familiares ou ACS / Sinalização urbana de UBS | Prédio físico da UBS (placa, sinalização interna, recepção) / Cartão Nacional de Saúde (físico ou digital) / Senha de atendimento / Ficha de triagem / Guia de Encaminhamento impressa / Ficha de protocolo de regulação | SMS de agendamento (número frequentemente não identificado) / Chamada telefônica de confirmação / Ficha de Agendamento CROSS impressa retirada na UBS / Ausência de portal cidadão de consulta de fila | Prédio do AME ou Hospital Estadual (sinalização, estacionamento, recepção) / Painel eletrônico de senhas / Senha de atendimento / Consultório e computador com prontuário visível / Receita médica carimbada / Pedidos de exames / Solicitação de APAC / Documento de contrarreferência em papel | Documentos de saída (receita, pedidos de exame, contrarreferência) / Resultado de exame (quando consegue agendar e retirar) / Ausência de comprovante de continuidade integrada |

---

### CAMADA 2 — Ações do Cidadão *(Shostack, 1984: Customer Actions — linha de interação do usuário)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Ações do Cidadão** | Percebe sintoma ou piora → Busca informação (internet, familiares, ACS, telefone) → Decide qual porta de entrada acessar → Reúne documentos (CNS, RG, comprovante de residência) | Chega à UBS → Aguarda triagem e acolhimento → Relata sintomas ao médico generalista → Recebe encaminhamento para especialista → Aguarda confirmação de que o pedido foi inserido no sistema | Aguarda passivamente em casa por semanas ou meses → Tenta obter informação sobre posição na fila (retorno à UBS, ligação) → Atende chamada de agendamento (ou a perde) → Confirma presença ou retira ficha CROSS na UBS | Desloca-se ao município polo (frequentemente intermunicipal, com custo de transporte) → Realiza check-in na recepção → Passa por triagem de enfermagem → Realiza consulta médica especializada → Recebe receita, pedidos de exame e orientações verbais | Tenta compreender orientações recebidas → Busca onde e como agendar exames sem fluxo definido → Realiza exames (quando consegue) → Tenta obter resultado → Busca retorno ao especialista ou à UBS de origem |

---

**──────────────────────────── LINHA DE INTERAÇÃO (cidadão ↔ organização) ────────────────────────────**

---

### CAMADA 3 — Frontstage — Ações Visíveis ao Cidadão *(Shostack, 1984: Onstage Contact Person Actions)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Frontstage** | Canais digitais públicos (sites SES-SP, gov.br, Meu SUS Digital) / Centrais de orientação telefônica (156 estadual) / ACS em campo *(I/L — ausência de canal unificado de pré-acesso documentado)* | Recepcionista orienta, valida cadastro e emite senha / Enfermagem executa acolhimento e triagem (RCPG ou classificação de risco) / Médico generalista conduz consulta e emite Guia de Encaminhamento SUS / Operador insere solicitação no SIRESP e informa prazo estimado ao paciente | Recebimento de chamada telefônica (número frequentemente oculto) ou SMS informando data, hora e local / Retirada da Ficha de Agendamento CROSS na UBS de origem | Recepcionista do AME confirma identidade, verifica ficha CROSS e abre atendimento / Enfermagem executa triagem clínica (sinais vitais, anamnese sumária) / Médico especialista conduz anamnese completa, exame físico, diagnóstico e prescrição | Orientação verbal do médico especialista ao encerrar consulta / Eventual atendimento na UBS de origem para receber a contrarreferência *(I/V — depende de retorno ativo do paciente)* |

---

**──────────────────────────── LINHA DE VISIBILIDADE (visível ↔ invisível ao cidadão) ────────────────────────────**

---

### CAMADA 4 — Backstage — Processos Internos e Regulatórios *(Shostack, 1984: Back-stage Contact Person Actions — inclui backstage operacional das unidades e backstage regulatório CROSS/DRS)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Backstage das Unidades** (AME/Hospital e APS-MUN) | Gestão dos canais de comunicação institucionais (sites, apps, call centers) / Sem processo formalizado de orientação pré-acesso documentado *(I)* | **APS-MUN:** Avaliação da necessidade clínica / Registro em prontuário eletrônico municipal (e-SUS PEC ou similar) / Emissão da Guia de Referência SUS / Preenchimento e inserção da solicitação no SIRESP com dados clínicos e CID preliminar | **NIR do AME/Hospital:** Abertura, parametrização e bloqueio de agendas médicas no sistema interno / Oferta de vagas no SIRESP via carga periódica / Gestão de encaixes e remanejamentos / Controle de produtividade médica vs. metas contratuais / **APS-MUN:** Atualização cadastral e acionamento do paciente após liberação da vaga | **AMB-OSS/EST:** Abertura do atendimento no prontuário interno (MV/Pixeon) / Registro da evolução clínica com CID-10 e assinatura digital ICP-Brasil / Emissão de contrarreferência em papel entregue ao paciente / **FAT:** Fechamento da produção diária e faturamento BPA-I ou APAC no SIA-SUS / Auditoria de glosas e pendências / Gestão de absenteísmo (registro de faltas e remanejamento de slots) | Emissão de contrarreferência entregue manualmente ao paciente (único veículo de informação entre os níveis) / Eventual abertura de nova solicitação de regulação para exames de alta complexidade / Ausência de fluxo sistemático de acompanhamento do resultado *(I/D)* |
| **Backstage Regulatório** (CROSS/DRS) | — *(ausente nesta fase)* | **DRS:** Supervisão do quantitativo de vagas por especialidade disponíveis na região / Arbitragem de conflitos de regulação entre municípios / Pactuação mensal de oferta com os AMEs e Hospitais do território | **Núcleo central:** Médico Regulador avalia solicitação clínica e classifica prioridade P1 a P4 com base em protocolo / Match automatizado ou manual da vaga com CNS do paciente / Gestão de fila e controle de absenteísmo preventivo (lista de espera ativa para substituição de faltas) / Confirmação e atualização de status no SIRESP / **DRS:** Monitoramento de indicadores regionais de tempo de espera e produção | **NIR:** Confirma realização do atendimento e registra produção no SIRESP / Monitora cumprimento de metas contratuais (Resolução SS-SP 44/2021) / **DRS:** Consolida indicadores regionais e reporta à SES-SP / Fiscalização do contrato de gestão com as OSS | Regulação eventual de novos procedimentos diagnósticos solicitados na pós-consulta / Gestão de filas de exames especializados / **DRS:** Auditoria de produção pós-faturamento e verificação de conformidade das APACs *(D/I)* |

---

**──────────────────────────── LINHA DE INTERAÇÃO INTERNA (atores humanos ↔ sistemas tecnológicos) ────────────────────────────**

---

### CAMADA 5 — Processos de Suporte — Sistemas, Bases de Dados e Infraestrutura *(Shostack, 1984: Support Processes)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Processos de Suporte** | Portal gov.br / Meu SUS Digital (app) / CNES (localização de unidades) / e-SUS (base cadastral CNS) *(D — sistemas existentes; integração com pré-acesso é I)* | **e-SUS PEC** ou prontuário eletrônico municipal / **SIRESP — Módulo Ambulatorial** (inserção da solicitação e validação do CNS) / Base **CNS** para validação do paciente / Base **CNES** para verificação da unidade solicitante | **SIRESP — Módulo Ambulatorial** (fila de espera, match, agendamento e confirmação) / **SIRESP — Módulo Indicadores** (monitoramento de tempo de espera e produção) / Bases **CNS** e **CNES** / Sistemas de telefonia e SMS / Sistema interno do AME/Hospital para parametrização de agendas | Sistema de Gestão Hospitalar Interno (**MV** ou **Pixeon**) / **SIA-SUS** (faturamento BPA-I ou APAC) / **SIRESP** (registro de produção pelo NIR) / Infraestrutura **ICP-Brasil** (assinatura digital médica) / Sistema interno de controle de glosas e auditoria de produção | **RNDS** (Rede Nacional de Dados de Saúde — em implantação parcial) / **SIRESP** (novos pedidos de regulação para exames) / Prontuários eletrônicos fragmentados sem barramento de interoperabilidade efetivo / **SIA-SUS** (autorização de APAC para procedimentos de alta complexidade) |

---

## Extensões Analíticas

> As extensões a seguir são **adições ao modelo clássico de Shostack (1984)**, incorporando perspectivas contemporâneas de Service Design para enriquecer o diagnóstico. Não são camadas padrão da metodologia original.

---

### EXTENSÃO A — Emoção do Cidadão *(extensão contemporânea; hipótese I/L — a validar em campo)*

| | **Macroetapa 1** Pré-acesso | **Macroetapa 2** APS / UBS | **Macroetapa 3** Regulação | **Macroetapa 4** Atendimento Especializado | **Macroetapa 5** Continuidade do Cuidado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Emoção** | 🟠 Preocupação com o problema de saúde / 🟡 Dúvida sobre onde e como buscar atendimento | 🟡 Expectativa ao entrar no sistema / 🟢 Alívio parcial se o acolhimento for adequado | 🔴 Ansiedade crescente pela espera / Sensação de "caixa preta" — sem informação sobre posição ou prazo | 🟢 Alívio ao ser atendido / Confiança no especialista / 🟡 Incerteza ao sair com pedidos sem encaminhamento claro | 🟠 Frustração com ausência de fluxo / 🔴 Perda de confiança no sistema ao não saber os próximos passos |

**Legenda emocional:** 🟢 Positivo — confiança, alívio, segurança | 🟡 Neutro — expectativa, dúvida, espera | 🟠 Negativo — frustração, insegurança, preocupação | 🔴 Crítico — sensação de abandono, perda de controle, ruptura da confiança

---

### EXTENSÃO B — Atores Responsáveis por Macroetapa *(adaptação: esfera institucional explícita — não é camada padrão de Shostack)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Ator Responsável** | **CID** (cidadão, sem guia institucional estruturado) / **SUP-FED** (portais MS, app Meu SUS Digital) *(I — ausência de ator municipal formalizado nesta etapa)* | **APS-MUN** — médico generalista, enfermagem, recepcionista e operador de regulação municipal; apoio de **eMulti** quando disponível | **REG-EST** (médico regulador e operadores CROSS/SIRESP) / **NIR** (disponibiliza vagas no SIRESP) / **APS-MUN** (insere solicitação e comunica agendamento ao paciente) / **DRS** (supervisão e arbitragem regional de fluxos) | **AMB-OSS** ou **AMB-EST** — médico especialista, enfermagem, recepcionista, NIR e **FAT** (faturamento/auditoria) | **CID** (responsável pela execução dos pedidos) / **AMB-OSS/EST** (emite contrarreferência) / **APS-MUN** (médico de família, se receber a contrarreferência) / Rede executante de exames (laboratórios, serviços diagnósticos) |

---

### EXTENSÃO C — Normas Transversais *(camada de governança jurídico-regulatória — afeta todo o blueprint)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Normas Transversais** | **CF Art. 196–200** (direito universal à saúde) / **Lei 8.080/1990** (universalidade, integralidade e hierarquização) | **Lei 8.080/1990** (integralidade e hierarquização da rede) / **Portaria GM/MS 635/2023** (eMulti — equipes interprofissionais de apoio à APS) / **Portaria GM/MS 1.631/2015** (parâmetros de planejamento assistencial) | **Portaria GM/MS 2/2017** (Política Nacional de Regulação — acesso obrigatoriamente mediado por regulação) / **Decreto Estadual SP 56.061/2010** (criação e organização da CROSS) / **Resolução SS-SP 44/2021** (metas de primeiras consultas e retornos para OSS) | **Resolução SS-SP 44/2021** (metas contratuais das OSS) / **Lei Federal 9.637/1998** (contratos de gestão com OSS) / **STF Tema 698** (legitimidade da intervenção judicial e das OS) / **Código de Ética Médica** / **Portaria GM/MS 1.604/2023** (PNAES — Política Nacional de Atenção Especializada) | **Lei 8.080/1990** (integralidade e continuidade do cuidado) / **RNDS** (interoperabilidade público-suplementar) / **Lei 9.656/1998, Art. 32** (ressarcimento de planos ao SUS) / **Carta dos Direitos dos Usuários do SUS** (Portaria GM/MS 1.820/2009) |

---

### EXTENSÃO D — Fail Points por Macroetapa *(pontos de falha identificados — classificados por prioridade)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Fail Points** | ⚠ **FP01** — Cidadão não identifica porta de entrada correta e inicia jornada no local inadequado *(I/L)* / ⚠ **FP02** — Informação insuficiente sobre documentos, fluxos e critérios de acesso *(I/L)* | ⚠ **FP03** — Dificuldade de acesso à consulta inicial na UBS para obter encaminhamento (fila de espera prolongada) *(D/I)* / ⚠ **FP04** — Encaminhamento emitido com dados clínicos incompletos, causando recusa ou rebaixamento de prioridade pela regulação *(D)* / ⚠ **FP13** — Inconsistência cadastral (CNS desatualizado, dados divergentes) impede inserção da solicitação *(D/I)* | ⚠ **FP05** 🔴 *CRÍTICO* — Fila invisível: cidadão sem informação sobre posição ou previsão de espera *(D)* / ⚠ **FP06** 🔴 *CRÍTICO* — Vaga agendada não comunicada efetivamente: perda por dados cadastrais desatualizados, aviso tardio ou número de telefone não atendido *(D)* / ⚠ **FP14** — Duplicidade de solicitação (paciente inserido duas vezes em municípios distintos ou por diferentes unidades) distorce a fila *(I/D)* | ⚠ **FP07** 🔴 *CRÍTICO* — Médico especialista não acessa histórico clínico da UBS de origem; paciente refaz anamnese e exames em duplicidade *(D)* / ⚠ **FP15** — Gestão de absenteísmo reativa: vaga ociosa por falta do paciente não é preenchida a tempo com lista de espera ativa *(D/I)* | ⚠ **FP08** 🔴 *CRÍTICO* — Pedido de exame emitido sem fluxo integrado de agendamento; cidadão fica responsável por encontrar onde realizá-lo *(I/D)* / ⚠ **FP09** — Resultado do exame não chega ao profissional responsável nem ao cidadão *(I)* / ⚠ **FP10** — Contrarreferência não chega à UBS de origem; paciente é o único mensageiro *(D)* / ⚠ **FP11** — Ausência de responsável definido pelo próximo passo clínico *(I)* / ⚠ **FP12** — Retrabalho administrativo por ausência de interoperabilidade entre sistemas *(D)* |

---

## Síntese dos Fail Points — Catálogo Executivo

| ID | Macroetapa | Descrição da Falha | Causa Provável | Impacto no Cidadão | Categoria | Prioridade TO-BE | Evidência |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| FP01 | Pré-acesso | Porta de entrada desconhecida | Ausência de canal unificado de orientação | Deslocamento desnecessário; início errado do fluxo | Informação / Acesso | Média | I/L |
| FP02 | Pré-acesso | Informação insuficiente sobre documentos e fluxos | Comunicação institucional fragmentada | Retorno à UBS por documentação incompleta | Informação | Baixa/Média | I/L |
| FP03 | APS/UBS | Dificuldade de acesso à consulta inicial na UBS | Déficit de oferta de médicos generalistas | Atraso no início do fluxo especializado | Acesso / Operacional | Alta | D/I |
| FP04 | APS/Regulação | Encaminhamento incompleto ou recusado pela regulação | Falta de treinamento do operador de regulação municipal; campos obrigatórios não preenchidos | Retrabalho e atraso adicional; paciente notificado da recusa sem saber o motivo | Operacional / Comunicação | Alta | D |
| FP05 | Regulação | **Fila invisível — sem previsão de espera para o cidadão** | Ausência de portal de transparência ativa no SIRESP para o usuário final | Ansiedade, judicialização, agravamento clínico silencioso | Regulação / Comunicação | **Crítica** | D |
| FP06 | Regulação | **Vaga perdida por falha de comunicação** | Dados cadastrais desatualizados no CNS; aviso por ligação de número oculto com antecedência insuficiente | Perda do encaminhamento; reinício do fluxo desde o início na UBS | Comunicação / Operacional | **Crítica** | D |
| FP07 | Atendimento | **Especialista sem acesso ao histórico clínico municipal** | Falta de barramento de interoperabilidade entre prontuários municipais e estaduais | Repetição de anamnese e exames; risco de conduta inadequada por falta de informação | Integração sistêmica | **Crítica** | D |
| FP08 | Pós-consulta | **Pedido de exame sem fluxo integrado de agendamento** | Ausência de pactuação contratual sobre agendamento integrado de exames na saída do AME | Cidadão sem saber onde ir; exame não realizado; perda de seguimento clínico | Continuidade / Operacional | **Crítica** | I/D |
| FP09 | Pós-consulta | Resultado de exame não chega ao profissional ou ao cidadão | Ausência de integração entre rede executante de exames e prontuário do especialista | Retorno clínico sem resultado; condutas baseadas em informações incompletas | Continuidade / Integração sistêmica | Média/Alta | I |
| FP10 | Contrarreferência | Contrarreferência sem retorno digital à APS | Fluxo de contrarreferência em papel entregue ao paciente como único mensageiro | Descontinuidade terapêutica; risco de prescrições conflitantes | Continuidade / Comunicação | Alta | D |
| FP11 | Continuidade | Ausência de responsável definido pelo próximo passo clínico | Falta de coordenação do cuidado entre APS e especialidade | Paciente "abandonado" sem saber a quem recorrer | Continuidade / Operacional | Alta | I |
| FP12 | Transversal | Retrabalho por ausência de interoperabilidade sistêmica | Sistemas municipais e estaduais sem barramento padronizado (HL7/FHIR ausente) | Duplicação de exames; perda de informação clínica; ineficiência operacional | Integração sistêmica | Média | D |
| FP13 | APS/Regulação | Inconsistência cadastral impede inserção da solicitação | CNS duplicado, desatualizado ou com dados divergentes entre municípios | Atraso no início do processo regulatório; cidadão sem saber o motivo | Dados / Operacional | Alta | D/I |
| FP14 | Regulação | Duplicidade de solicitação distorce a fila | Ausência de validação de unicidade no SIRESP por CNS e especialidade | Desperdício de vaga; distorção do tempo real de espera | Operacional / Dados | Média | I/D |
| FP15 | Atendimento | Gestão de absenteísmo reativa — slot ocioso não preenchido | Ausência de lista de espera ativa para substituição imediata de faltas | Desperdício de recurso especializado; cidadão em fila não avançado | Operacional | Alta | D/I |

---

## Curva Emocional da Jornada

```
Estado
emocional
   │
🟢 │                         ●─────●
   │                        /       \
🟡 │    ●        ●─────●  /         \         ●
   │   / \      /         /           \       / \
🟠 │  ●   \    /         /             \     /   ●
   │        \  /         /               \   /
🔴 │         ●          /                 ●─●
   │                   /             (FP08-12, FP15)
   └─────────────────────────────────────────────────▶
       Pré-   UBS    Regulação  Especialista  Continuidade
      acesso                                
      (FP01-02) (FP03-04,  (FP05-06,  (FP07,FP15)  (FP08-12)
                FP13)      FP14)

Pico crítico 1: Regulação — espera sem informação (FP05, FP06)
Momento de recuperação: Chegada ao especialista — alívio após longa espera
Pico crítico 2: Continuidade — ruptura pós-consulta e ausência de responsável pelo cuidado (FP08-12)
```

---

## RACI — Matriz de Responsabilidade por Macroetapa

> **R** = Responsável pela execução | **A** = Accountable (responde pelos resultados) | **C** = Consultado | **I** = Informado

| Ator | Macroetapa 1 Pré-acesso | Macroetapa 2 APS / UBS | Macroetapa 3 Regulação | Macroetapa 4 Atendimento | Macroetapa 5 Continuidade |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **CID — Cidadão** | R/A | R | I | R | R/A |
| **APS-MUN** | I | R/A | R (inserção/comunicação) | C | R (recebe contrarreferência) |
| **DRS** | — | C | A (supervisão regional) | I | A (fiscalização contratual) |
| **REG-EST (CROSS)** | — | C | R/A (regulação, match) | I | I |
| **NIR** | — | — | R (disponibiliza vagas) | R (registra produção) | C |
| **AMB-OSS / AMB-EST** | — | — | I | R/A | R (emite contrarreferência) |
| **FAT** | — | — | — | R (faturamento, glosas) | C |
| **SUP-FED** | C | C | C | C | C |

---

## Mapa de Priorização AS-IS → TO-BE

| Diretriz Estratégica TO-BE | Fail Points Relacionados | Prioridade |
| :--- | :--- | :--- |
| **1. Transparência ativa do acesso regulado** (portal cidadão integrado ao Meu SUS Digital com posição na fila e tempo estimado por especialidade e DRS) | FP05, FP06, FP14 | 🔴 Crítica |
| **2. Integração e interoperabilidade dos sistemas de informação** (barramento HL7/FHIR conectando e-SUS PEC aos sistemas AME/Hospital via RNDS) | FP07, FP12, FP13 | 🔴 Crítica |
| **3. Coordenação da jornada pós-consulta** (agendamento de exames na saída do AME; resultado integrado ao prontuário do especialista e da APS) | FP08, FP09, FP11 | 🔴 Crítica |
| **4. Integração entre níveis de atenção** (contrarreferência digital; responsabilização pelo cuidado longitudinal; gestão ativa de absenteísmo) | FP03, FP04, FP10, FP15 | 🟠 Alta |
| **5. Qualificação da pré-entrada** (canal único de orientação pré-acesso; atualização cadastral proativa no CNS) | FP01, FP02 | 🟡 Média |

---

*Declaração metodológica: O Service Blueprint AS-IS foi construído a partir de análise documental de normas, fluxos institucionais, sistemas operacionais e literatura especializada sobre jornada do paciente no SUS. A estrutura principal segue as 5 camadas padrão de Shostack (1984). As 4 extensões analíticas incorporam perspectivas contemporâneas de Service Design e são claramente identificadas como adições ao modelo clássico. As macroetapas 1 (Pré-acesso) e 5 (Continuidade do Cuidado) foram representadas como hipóteses analíticas inferidas a partir das barreiras identificadas no fluxo assistencial e deverão ser validadas em pesquisa com usuários e profissionais de saúde. Os marcadores D, L, I e V indicam o tipo de evidência subjacente a cada elemento do blueprint.*
