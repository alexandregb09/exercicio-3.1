# Service Blueprint AS-IS — Executivo
## Consulta Médica Especializada (Ambulatorial)
**Secretaria de Estado da Saúde de São Paulo (SES-SP) — Sistema Único de Saúde**
**Versão:** 1.0 | **Metodologia:** Shostack (1984) com extensões contemporâneas de Service Design

---

## Premissas metodológicas

Este blueprint adota a estrutura de camadas de Shostack com três extensões analíticas:
- **Camada emocional** acima das evidências físicas (hipótese inferida, a validar em campo)
- **Camada de atores responsáveis** entre frontstage e backstage (identifica esfera institucional)
- **Normas transversais** e **fail points** como camadas analíticas complementares

**Fronteiras da jornada:** Da percepção da necessidade de saúde até a continuidade do cuidado pós-consulta especializada.

**Legenda de evidências:**

| Código | Tipo |
| :--- | :--- |
| **D** | Documental direta — norma, manual, sistema ou documento oficial |
| **L** | Literatura e estudos de saúde pública |
| **I** | Inferência analítica — deduzida de falhas, fluxos e documentos existentes |
| **V** | Necessita validação por pesquisa de campo |

**Legenda de atores:**

| Código | Ator | Esfera |
| :--- | :--- | :--- |
| CID | Cidadão | — |
| APS-MUN | Atenção Primária Municipal (UBS/ESF/eMulti) | Municipal |
| REG-EST | Regulação Estadual — CROSS e operadores | Estadual |
| AMB-EST | Ambulatório Estadual — administração direta | Estadual |
| AMB-OSS | Ambulatório gerenciado por OSS (Lei 9.637/1998) | Estadual/Contratado |
| SUP-FED | Sistemas e suporte federal (DATASUS, RNDS, MS) | Federal |

**Legenda emocional:**

| Símbolo | Estado |
| :--- | :--- |
| 🟢 | Positivo — confiança, alívio, segurança |
| 🟡 | Neutro — expectativa, dúvida, espera |
| 🟠 | Negativo — frustração, insegurança, preocupação |
| 🔴 | Crítico — sensação de abandono, perda de controle, ruptura da confiança |

---

## Blueprint Executivo — Matriz Principal

> **Leitura:** Linhas = camadas do serviço | Colunas = macroetapas da jornada (esquerda → direita = progressão temporal)

---

### CAMADA 1 — Emoção do Cidadão *(extensão contemporânea; hipótese a validar em campo — I/L)*

| | **Macroetapa 1** Pré-acesso | **Macroetapa 2** APS / UBS | **Macroetapa 3** Regulação | **Macroetapa 4** Atendimento Especializado | **Macroetapa 5** Continuidade do Cuidado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Emoção** | 🟠 Preocupação com o problema de saúde / 🟡 Dúvida sobre onde e como buscar atendimento | 🟡 Expectativa ao entrar no sistema / 🟢 Alívio parcial se o acolhimento for adequado | 🔴 Ansiedade crescente pela espera / Sensação de "caixa preta" — sem informação sobre posição ou prazo | 🟢 Alívio ao ser atendido / Confiança no especialista / 🟡 Incerteza ao sair com pedidos sem encaminhamento | 🟠 Frustração com ausência de fluxo / 🔴 Perda de confiança no sistema ao não saber os próximos passos |

---

### CAMADA 2 — Evidências Físicas *(D para etapas 2–4; I/L para etapas 1 e 5)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Evidências Físicas** | Sites institucionais (SES-SP, gov.br) / App Meu SUS Digital / Centrais telefônicas / Informações de familiares ou ACS | Prédio físico da UBS / Cartão Nacional de Saúde (físico ou digital) / Guia de Encaminhamento impressa / Ficha de protocolo | SMS de confirmação / Chamada telefônica de número oculto / Ficha de Agendamento CROSS impressa na UBS | Prédio do AME ou Hospital / Painel eletrônico de senhas / Consultório e computador com prontuário / Receita médica / Pedidos de exames / Documento de contrarreferência | Documentos de saída (receita, pedidos de exame) / Resultado de exame (quando obtido) / Ausência de comprovante de continuidade |

---

### CAMADA 3 — Ações do Cidadão

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Ações do Cidadão** | Percebe sintoma ou piora de condição existente → Busca informação (internet, familiares, telefone) → Decide qual porta de entrada acessar → Reúne documentos necessários (CNS, RG, comprovante) | Chega à UBS → Aguarda triagem e acolhimento → Relata sintomas ao médico generalista → Recebe encaminhamento para especialista → Aguarda inserção do pedido no sistema | Aguarda passivamente em casa por dias ou meses → Tenta obter informação sobre posição na fila → Atende chamada de agendamento (ou a perde) → Confirma presença ou retorna à UBS para retirar ficha | Desloca-se ao município polo (frequentemente intermunicipal) → Realiza check-in na recepção → Passa por triagem de enfermagem → Realiza consulta médica especializada → Recebe receita, pedidos de exame e orientações verbais | Tenta compreender orientações recebidas → Busca onde e como agendar exames → Realiza exames (se encontrar fluxo) → Tenta obter resultado → Busca retorno ao especialista ou à UBS de origem |

---

**──────────────────────────── LINHA DE INTERAÇÃO (cidadão ↔ organização) ────────────────────────────**

---

### CAMADA 4 — Frontstage *(ações visíveis ao cidadão)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Frontstage** | Canais digitais públicos (sites, apps) disponibilizados pela SES-SP e MS / Centrais telefônicas de orientação / Agentes Comunitários de Saúde (ACS) em campo *(I/L — ausência de canal unificado documentado)* | Recepcionista orienta e realiza cadastro / Enfermagem executa acolhimento e triagem / Médico generalista conduz consulta e emite Guia de Referência | Recebimento de chamada telefônica (número frequentemente oculto) ou SMS informando data, hora e local da consulta / Retirada de Ficha de Agendamento CROSS na UBS | Recepcionista confirma presença e abre atendimento / Enfermagem executa triagem clínica / Médico especialista conduz anamnese, exame físico, diagnóstico e emite prescrição | Orientação verbal do médico especialista ao encerrar consulta / Eventual atendimento na UBS de origem para receber a contrarreferência *(I/V — depende de retorno do paciente)* |

---

### CAMADA 5 — Atores Responsáveis *(esfera institucional explícita)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Ator Responsável** | **CID** (cidadão, sem guia institucional estruturado) / **SUP-FED** (portais MS) *(I — ausência de ator municipal formalizado nesta etapa)* | **APS-MUN** — médico generalista, enfermagem, recepcionista e operador de regulação municipal | **REG-EST** — médico regulador e operadores da CROSS (análise e match) / **APS-MUN** — insere solicitação e aciona o paciente | **AMB-OSS** ou **AMB-EST** — médico especialista, enfermagem, recepcionista, setor de faturamento e NIR | **CID** (responsável pela execução dos pedidos) / **AMB-OSS/EST** (emite contrarreferência) / **APS-MUN** (médico de família, se receber a contrarreferência) / Rede executante de exames |

---

**──────────────────────────── LINHA DE VISIBILIDADE (visível ↔ invisível ao cidadão) ────────────────────────────**

---

### CAMADA 6 — Backstage Operacional *(processos internos das unidades)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Backstage Operacional** | Gestão dos canais de comunicação institucionais (sites, apps, telefones) / Sem processo formalizado de orientação pré-acesso documentado *(I)* | Avaliação da necessidade de atenção especializada / Registro clínico em prontuário eletrônico municipal / Emissão da Guia de Referência do SUS / Inserção da solicitação no SIRESP com dados clínicos do paciente | Disponibilização de vagas pelos AMEs e Hospitais via NIR (Núcleo Interno de Regulação) / Atualização de cadastros e agendas no SIRESP / Acionamento da lista de contatos do paciente para comunicação | Abertura do atendimento no prontuário interno (MV/Pixeon) / Registro da evolução clínica com CID-10 e assinatura digital ICP-Brasil / Emissão de contrarreferência em papel entregue ao paciente / Faturamento BPA-I ou APAC no SIA-SUS | Emissão de contrarreferência entregue manualmente ao paciente (único veículo de informação entre os níveis) / Eventual abertura de nova solicitação de regulação para exames / Ausência de fluxo sistemático de agendamento integrado *(I/D)* |

---

### CAMADA 7 — Backstage Regulatório — CROSS *(processamento estadual invisível ao cidadão)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Backstage Regulatório (CROSS)** | — *(ausente nesta fase)* | — *(ausente; solicitação ainda não foi inserida)* | **Núcleo central da macroetapa:** Avaliação clínica da solicitação pelo médico regulador / Classificação de prioridade (P1 a P4) por protocolo / Match automatizado ou manual de vaga disponível com CNS do paciente / Confirmação e atualização de status no SIRESP | NIR do AME/Hospital confirma realização do atendimento e registra produção no SIRESP / Monitoramento de metas contratuais (Resolução SS-SP 44/2021) | Regulação eventual de novos procedimentos diagnósticos solicitados na pós-consulta / Gestão de filas de exames especializados *(D/I)* |

---

**──────────────────────────── LINHA DE INTERAÇÃO INTERNA (atores humanos ↔ sistemas tecnológicos) ────────────────────────────**

---

### CAMADA 8 — Processos de Suporte *(sistemas, bases de dados e infraestrutura tecnológica)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Processos de Suporte** | Portal gov.br / Meu SUS Digital (app) / CNES (localização de unidades) / e-SUS (base cadastral CNS) *(D — sistemas existentes; integração com pré-acesso é I)* | **e-SUS PEC** ou prontuário eletrônico municipal / **SIRESP — Módulo Ambulatorial** (inserção da solicitação) / Base CNS para validação do paciente | **SIRESP — Módulo Ambulatorial** (fila, match, agendamento) / Bases **CNS** e **CNES** / Sistemas de telefonia e SMS / Módulo de Indicadores SIRESP (monitoramento) | Sistema de gestão hospitalar interno (**MV** ou **Pixeon**) / **SIA-SUS** (faturamento BPA-I/APAC) / **SIRESP** (registro de produção pelo NIR) / Infraestrutura **ICP-Brasil** (assinatura digital médica) | **RNDS** (Rede Nacional de Dados de Saúde — se a integração estiver ativa) / **SIRESP** (novos pedidos de regulação) / Prontuários eletrônicos fragmentados sem barramento de interoperabilidade / **SIA-SUS** (autorização de APAC para procedimentos de alta complexidade) |

---

### CAMADA 9 — Normas Transversais *(camada de governança — afeta todo o blueprint)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Normas Transversais** | **CF Art. 196–200** (direito universal à saúde) / **Lei 8.080/1990** (universalidade e acesso à rede SUS) | **Lei 8.080/1990** (integralidade e hierarquização) / **Portaria GM/MS 635/2023** (eMulti — equipes interprofissionais de apoio à APS) | **Portaria GM/MS 2/2017** (Política Nacional de Regulação — acesso obrigatoriamente mediado por regulação) / **Decreto Estadual SP 56.061/2010** (criação e organização da CROSS) / **Resolução SS-SP 44/2021** (metas de primeiras consultas e retornos para OSS) | **Resolução SS-SP 44/2021** (metas contratuais das OSS) / **Lei Federal 9.637/1998** (contratos de gestão com OSS) / **STF Tema 698** (legitimidade da intervenção judicial e das OS na saúde) / **Código de Ética Médica** | **Lei 8.080/1990** (integralidade e continuidade do cuidado) / **RNDS** (interoperabilidade entre setores público e suplementar) / **Lei 9.656/1998, Art. 32** (ressarcimento de planos ao SUS) |

---

### CAMADA 10 — Fail Points *(pontos de falha identificados)*

| | **Macroetapa 1** | **Macroetapa 2** | **Macroetapa 3** | **Macroetapa 4** | **Macroetapa 5** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Fail Points** | ⚠ **FP01** — Cidadão não identifica porta de entrada correta e inicia jornada no local inadequado *(I/L)* / ⚠ **FP02** — Informação insuficiente sobre documentos, fluxos e critérios de acesso *(I/L)* | ⚠ **FP03** — Dificuldade de acesso à consulta inicial na UBS para obter encaminhamento *(D/I)* / ⚠ **FP04** — Encaminhamento emitido com informações clínicas incompletas, causando recusa pela regulação *(D)* | ⚠ **FP05** 🔴 *CRÍTICO* — Espera sem transparência: cidadão sem informação sobre posição na fila ou previsão de atendimento *(D)* / ⚠ **FP06** 🔴 *CRÍTICO* — Vaga agendada não comunicada efetivamente; perda por dados cadastrais desatualizados ou aviso de última hora *(D)* | ⚠ **FP07** 🔴 *CRÍTICO* — Médico especialista não acessa histórico clínico da UBS de origem; paciente refaz anamnese e exames em duplicidade *(D)* | ⚠ **FP08** 🔴 *CRÍTICO* — Pedido de exame emitido sem fluxo claro de agendamento; cidadão fica responsável por encontrar o caminho *(I/D)* / ⚠ **FP09** — Resultado do exame não chega ao profissional responsável nem ao cidadão *(I)* / ⚠ **FP10** — Contrarreferência não chega à UBS de origem; paciente é o único mensageiro entre os níveis *(D)* / ⚠ **FP11** — Paciente retorna ao sistema sem responsável definido pelo próximo passo *(I)* / ⚠ **FP12** — Falta de integração sistêmica gera retrabalho administrativo e perda de informação clínica *(D)* |

---

## Síntese dos Fail Points — Catálogo Executivo

| ID | Macroetapa | Descrição da Falha | Categoria | Prioridade TO-BE | Evidência |
| :--- | :--- | :--- | :--- | :--- | :--- |
| FP01 | Pré-acesso | Porta de entrada desconhecida pelo cidadão | Informação / Acesso | Média | I/L |
| FP02 | Pré-acesso | Informação insuficiente sobre documentos e fluxos | Informação | Baixa/Média | I/L |
| FP03 | APS/UBS | Dificuldade de acesso à consulta inicial na UBS | Acesso / Operacional | Alta | D/I |
| FP04 | APS/Regulação | Encaminhamento incompleto ou recusado pela regulação | Operacional / Comunicação | Alta | D |
| FP05 | Regulação | Fila sem transparência — cidadão sem previsão de espera | Regulação / Comunicação | **Crítica** | D |
| FP06 | Regulação | Vaga perdida por falha de comunicação ou dados desatualizados | Comunicação / Operacional | **Crítica** | D |
| FP07 | Atendimento | Médico especialista sem acesso ao histórico clínico municipal | Integração sistêmica | **Crítica** | D |
| FP08 | Pós-consulta | Pedido de exame sem fluxo integrado de agendamento | Continuidade / Operacional | **Crítica** | I/D |
| FP09 | Pós-consulta | Resultado de exame não chega ao profissional ou ao cidadão | Continuidade / Integração sistêmica | Média/Alta | I |
| FP10 | Contrarreferência | Informação clínica do especialista não retorna à UBS | Continuidade / Comunicação | Alta | D |
| FP11 | Continuidade | Ausência de responsável definido pelo próximo passo | Continuidade / Operacional | Alta | I |
| FP12 | Transversal | Retrabalho por ausência de interoperabilidade entre sistemas | Integração sistêmica | Média | D |

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
   │                   /             (FP08-12)
   └─────────────────────────────────────────────────▶
       Pré-   UBS    Regulação  Especialista  Continuidade
      acesso                                
      (FP01-02) (FP03-04) (FP05-06)  (FP07)     (FP08-12)

Picos críticos: Regulação (espera sem informação) e Continuidade (ruptura pós-consulta)
Momento de recuperação: Chegada ao especialista (alívio após longa espera)
```

---

## Mapa de Priorização AS-IS → TO-BE

| Diretriz Estratégica TO-BE | Fail Points Relacionados | Prioridade |
| :--- | :--- | :--- |
| **1. Transparência ativa do acesso regulado** (portal cidadão integrado ao Meu SUS Digital com posição na fila e tempo estimado) | FP05, FP06 | 🔴 Crítica |
| **2. Integração e interoperabilidade dos sistemas de informação** (barramento HL7/FHIR conectando e-SUS PEC aos sistemas AME/Hospital) | FP07, FP12 | 🔴 Crítica |
| **3. Coordenação da jornada pós-consulta** (agendamento de exames na saída do AME; resultado integrado ao prontuário) | FP08, FP09, FP11 | 🔴 Crítica |
| **4. Integração entre níveis de atenção** (contrarreferência digital; responsabilização pelo cuidado longitudinal) | FP03, FP04, FP10 | 🟠 Alta |
| *Oportunidades para ciclos futuros* | FP01, FP02 | 🟡 Média |

---

*Declaração metodológica: O Service Blueprint AS-IS foi construído a partir de análise documental de normas, fluxos institucionais, sistemas operacionais e literatura especializada. As macroetapas 1 (Pré-acesso) e 5 (Continuidade do Cuidado) foram representadas como hipóteses analíticas inferidas a partir das barreiras identificadas no fluxo assistencial e deverão ser validadas em pesquisa com usuários e profissionais de saúde. Os marcadores D, L, I e V indicam o tipo de evidência subjacente a cada elemento.*
