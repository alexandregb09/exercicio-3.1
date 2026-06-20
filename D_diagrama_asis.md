# Diagrama AS-IS — Relações entre Etapas e Atores
## Consulta Médica Especializada (Ambulatorial) — SES-SP

**Metodologia:** Service Blueprint AS-IS (Shostack, 1984)
**Renderização:** Mermaid v10+ (GitHub nativo)

---

## Diagrama Geral — Etapas, Atores e Fail Points

> Lê-se da esquerda para a direita seguindo a jornada do cidadão. As camadas agrupam: **Cidadão** → **Frontstage** (visível) → **Backstage Regulatório** (invisível, CROSS) → **Processos de Suporte**. As setas sólidas são fluxos principais; as tracejadas são consultas a sistemas ou fail points.

```mermaid
flowchart LR

  subgraph CID_L["CIDADÃO"]
    direction LR
    c1([percebe\nnecessidade]) --> c2([busca\ninformação]) --> c3([vai à\nUBS]) --> c4([aguarda\nvaga]) --> c5([vai ao\nAME]) --> c6([pós-\nconsulta])
  end

  subgraph FRONT["FRONTSTAGE — visível ao cidadão"]
    direction LR
    f1["Canais SES\npré-acesso"]
    f2["Equipe APS\nAPS-MUN"]
    f3["confirmação\nagendamento"]
    f4["Médico AME\nAMB-EST / AMB-OSS"]
    f5["orientações\npós-consulta"]
  end

  subgraph BACK["BACKSTAGE REGULATÓRIO — invisível ao cidadão"]
    CROSS["CROSS · REG-EST\nanalisa · prioriza · agenda vagas"]
  end

  subgraph SUP["PROCESSOS DE SUPORTE"]
    direction LR
    SIRESP[(SIRESP)]
    SIASUS[(SIA-SUS / CNES)]
  end

  c2 --> f1
  c3 --> f2
  c4 --> f3
  c5 --> f4
  c6 --> f5

  f2 -->|encaminha| CROSS
  CROSS -->|libera vaga| f3

  f2 -.-> SIRESP
  CROSS -.-> SIRESP
  CROSS -.-> SIASUS
  f4 -.-> SIASUS

  c2 -.->|"⚠ FP01/FP02"| fp1[/porta de entrada\nerrada · info insuficiente/]
  f2 -.->|"⚠ FP03/FP04"| fp2[/encaminhamento\nincompleto/]
  CROSS -.->|"⚠ FP05/FP06"| fp3[/fila opaca ·\nfalha de agendamento/]
  f4 -.->|"⚠ FP07"| fp4[/sem histórico\nclínico integrado/]
  f5 -.->|"⚠ FP08–FP11"| fp5[/ruptura da\ncontinuidade do cuidado/]
  SIRESP -.->|"⚠ FP12"| fp6[/retrabalho\nsistêmico/]
```

---

## Diagrama 1 — Sequência de Interações entre Atores

> Lê-se da esquerda para a direita, seguindo a progressão temporal da jornada do cidadão. Os retângulos coloridos agrupam as macroetapas. As anotações ⚠ indicam fail points no ponto exato em que ocorrem.

```mermaid
sequenceDiagram
    autonumber
    participant CID as Cidadão
    participant APS as APS Municipal (UBS)
    participant SIR as SIRESP
    participant CRX as CROSS (Regulação)
    participant NIR as NIR do AME
    participant AMB as Especialista (AME)
    participant RED as Rede de Exames

    rect rgb(255, 243, 224)
        Note over CID,APS: MACROETAPA 1 — Pré-acesso (evidência I/L)
        CID->>CID: Percebe sintoma ou piora de condição
        CID-->>APS: Decide buscar atendimento
        Note over CID,APS: ⚠ FP01 porta de entrada incorreta | ⚠ FP02 informação insuficiente sobre fluxo
    end

    rect rgb(220, 235, 255)
        Note over CID,SIR: MACROETAPA 2 — APS / UBS (evidência D/I)
        CID->>APS: Apresenta CNS e documentos
        APS->>CID: Acolhimento e triagem de enfermagem
        APS->>CID: Consulta com médico generalista
        APS->>CID: Emite Guia de Encaminhamento
        APS->>SIR: Operador insere solicitação no Módulo Ambulatorial
        Note over APS,SIR: ⚠ FP03 acesso difícil à consulta inicial | ⚠ FP04 encaminhamento incompleto e recusado
    end

    rect rgb(255, 220, 220)
        Note over SIR,NIR: MACROETAPA 3 — Regulação / CROSS (evidência D)
        SIR->>CRX: Solicitação aguarda avaliação regulatória
        NIR-->>SIR: Disponibiliza vagas do AME / Hospital
        CRX->>CRX: Classifica prioridade clínica P1 a P4
        CRX->>SIR: Match — vaga vinculada ao CNS do paciente
        SIR-->>APS: Confirmação de agendamento
        APS->>CID: Comunica por telefone ou SMS
        Note over CID,CRX: ⚠ FP05 CRITICO — fila invisivel sem previsao de espera
        Note over CID,APS: ⚠ FP06 CRITICO — vaga perdida por dados desatualizados ou aviso tardio
    end

    rect rgb(220, 255, 220)
        Note over CID,AMB: MACROETAPA 4 — Atendimento Especializado (evidência D)
        CID->>AMB: Desloca-se ao polo e faz check-in
        AMB->>CID: Triagem de enfermagem
        AMB->>CID: Consulta médica especializada
        Note over AMB,CID: ⚠ FP07 CRITICO — especialista sem acesso ao historico clinico da UBS
        AMB->>NIR: Registra atendimento no SIRESP
        AMB->>CID: Entrega receita, pedidos de exame e contrareferencia em papel
    end

    rect rgb(255, 255, 210)
        Note over CID,RED: MACROETAPA 5 — Continuidade do Cuidado (evidência I/D)
        CID->>RED: Tenta agendar exames sem fluxo definido
        Note over CID,RED: ⚠ FP08 CRITICO — exame sem fluxo integrado de agendamento
        RED-->>CID: Resultado do exame (quando consegue acesso)
        RED-->>AMB: Resultado nao integrado ao prontuario interno
        Note over RED,AMB: ⚠ FP09 — resultado nao chega ao profissional
        CID-->>APS: Entrega contrareferencia em papel (unico mensageiro)
        Note over CID,APS: ⚠ FP10 — contrareferencia sem retorno digital a APS
        Note over CID,APS: ⚠ FP11 — sem responsavel definido pelo proximo passo
        Note over SIR,AMB: ⚠ FP12 — ausencia de interoperabilidade entre sistemas
    end
```

---

## Diagrama 2 — Arquitetura de Atores, Sistemas e Lacunas de Integração

> Mostra os atores por esfera institucional (federal, estadual, OSS/direta, municipal) e os sistemas que cada um opera. As setas tracejadas marcadas com `SEM INTEGRACAO` indicam conexões ausentes que são origem direta de fail points críticos.

```mermaid
graph TD
    CID(["CIDADAO"])

    subgraph MUN["Esfera Municipal — APS"]
        direction TB
        UBS["UBS / ESF / eMulti\nAPS-MUN"]
        OP["Operador de Regulacao\nMunicipal"]
        PMUN[("e-SUS PEC\nProntuario Municipal")]
    end

    subgraph EST["Esfera Estadual — SES-SP"]
        direction TB
        CROSS["CROSS\nMedico Regulador e Operadores\nREG-EST"]
        SIR[("SIRESP\nModulo Ambulatorial")]
    end

    subgraph AME_B["AME / Hospital — OSS ou Administracao Direta"]
        direction TB
        NIR["NIR\nNucleo Interno de Regulacao"]
        ESP["Medico Especialista\nAMB-OSS ou AMB-EST"]
        PINT[("Prontuario Interno\nMV ou Pixeon")]
        FAT["Faturamento SUS"]
    end

    subgraph FED["Esfera Federal — MS / DATASUS"]
        direction TB
        SIASUS[("SIA-SUS")]
        CNS[("Base CNS")]
        CNES[("CNES")]
        RNDS[("RNDS")]
    end

    GAP["SEM INTEGRACAO\nFP07 e FP12\nProntuarios nao conversam"]

    CID -->|"1 Busca atendimento"| UBS
    UBS --> OP
    UBS <--> PMUN
    OP -->|"2 Insere solicitacao"| SIR
    SIR <-->|"3 Avaliacao regulatoria"| CROSS
    NIR -->|"4 Disponibiliza vagas"| SIR
    CROSS -->|"5 Match vaga-CNS"| SIR
    SIR -->|"consulta"| CNS
    SIR -->|"consulta"| CNES
    SIR -.->|"6 Confirma agendamento"| OP
    OP -.->|"7 Telefone ou SMS"| CID
    CID -->|"8 Comparece a consulta"| ESP
    ESP <--> PINT
    ESP -->|"9 Documentos em papel"| CID
    NIR -->|"10 Registra producao"| SIR
    PINT --> FAT
    FAT -->|"11 BPA-I ou APAC"| SIASUS
    CID -.->|"12 Contrareferencia em papel FP10"| UBS
    RNDS -. "Integracao parcial em implantacao" .-> PINT
    RNDS -. "Integracao parcial em implantacao" .-> PMUN

    PMUN -.->|"deveria conectar"| GAP
    GAP -.->|"deveria conectar"| PINT

    style GAP fill:#ffcccc,stroke:#cc3333,color:#990000
    style CID fill:#e8f4fd,stroke:#2980b9
    style CROSS fill:#fef9e7,stroke:#f39c12
    style SIR fill:#fef9e7,stroke:#f39c12
    style PMUN fill:#eafaf1,stroke:#27ae60
    style PINT fill:#fdf2f8,stroke:#8e44ad
    style RNDS fill:#eaf4fb,stroke:#2980b9
```

---

## Diagrama 3 — Priorização de Fail Points por Impacto e Frequência

> Quadrante superior direito = intervencao imediata. Os quatro fail points criticos (FP05, FP06, FP07, FP08) estao concentrados nessa regiao e correspondem as quatro macrodiretrizes TO-BE do relatorio.

```mermaid
quadrantChart
    title Priorizacao de Fail Points — Impacto no Cidadao x Frequencia Operacional
    x-axis Frequencia Baixa --> Frequencia Alta
    y-axis Impacto Baixo --> Impacto Alto
    quadrant-1 Critico — intervir primeiro
    quadrant-2 Investigar — alto impacto
    quadrant-3 Baixa prioridade atual
    quadrant-4 Monitorar — alta frequencia
    FP08 Exame sem agendamento: [0.82, 0.93]
    FP05 Fila sem transparencia: [0.85, 0.90]
    FP07 Sem historico clinico: [0.73, 0.88]
    FP06 Vaga perdida: [0.78, 0.84]
    FP03 Acesso dificil UBS: [0.55, 0.78]
    FP04 Encaminhamento incompleto: [0.52, 0.74]
    FP10 Sem contrareferencia: [0.44, 0.80]
    FP11 Sem responsavel: [0.40, 0.77]
    FP09 Resultado nao integrado: [0.38, 0.72]
    FP12 Retrabalho sistemico: [0.72, 0.57]
    FP01 Porta de entrada errada: [0.67, 0.52]
    FP02 Sem informacao de acesso: [0.60, 0.46]
```

---

## Diagrama 4 — RACI Completo: Responsabilidade por Macroetapa e Ator

> **R** = Responsável pela execução | **A** = Accountable (responde pelos resultados) | **C** = Consultado (colabora com informações) | **I** = Informado (notificado do resultado)

```mermaid
%%{init: {"theme": "default"} }%%
graph LR
    subgraph RACI["RACI — Macroetapas x Atores"]
        direction TB
        H["Ator"]
        M1["ME1\nPré-acesso"]
        M2["ME2\nAPS / UBS"]
        M3["ME3\nRegulação"]
        M4["ME4\nAtendimento"]
        M5["ME5\nContinuidade"]

        CID["Cidadão (CID)"]
        APSMUN["APS-MUN\nUBS / ESF"]
        DRS["DRS\nDep. Regional"]
        CROSS["REG-EST\nCROSS"]
        NIR["NIR\nAME Interno"]
        AMB["AMB-OSS/EST\nEspecialista"]
        FAT["FAT\nFaturamento"]
        FED["SUP-FED\nFederal"]
    end

    CID -->|"R/A"| M1
    CID -->|"R"| M2
    CID -->|"I"| M3
    CID -->|"R"| M4
    CID -->|"R/A"| M5

    APSMUN -->|"I"| M1
    APSMUN -->|"R/A"| M2
    APSMUN -->|"R inserção e comunicação"| M3
    APSMUN -->|"C"| M4
    APSMUN -->|"R recebe contraref."| M5

    DRS -->|"—"| M1
    DRS -->|"C"| M2
    DRS -->|"A supervisão regional"| M3
    DRS -->|"I"| M4
    DRS -->|"A fiscalização"| M5

    CROSS -->|"—"| M1
    CROSS -->|"C"| M2
    CROSS -->|"R/A regulação e match"| M3
    CROSS -->|"I"| M4
    CROSS -->|"I"| M5

    NIR -->|"—"| M1
    NIR -->|"—"| M2
    NIR -->|"R disponibiliza vagas"| M3
    NIR -->|"R registra produção"| M4
    NIR -->|"C"| M5

    AMB -->|"—"| M1
    AMB -->|"—"| M2
    AMB -->|"I"| M3
    AMB -->|"R/A atendimento"| M4
    AMB -->|"R emite contraref."| M5

    FAT -->|"—"| M1
    FAT -->|"—"| M2
    FAT -->|"—"| M3
    FAT -->|"R faturamento e glosas"| M4
    FAT -->|"C"| M5

    FED -->|"C"| M1
    FED -->|"C"| M2
    FED -->|"C"| M3
    FED -->|"C"| M4
    FED -->|"C"| M5

    style CID fill:#e8f4fd,stroke:#2980b9
    style CROSS fill:#fef9e7,stroke:#f39c12
    style NIR fill:#fdf2f8,stroke:#8e44ad
    style DRS fill:#fff3e0,stroke:#e67e22
    style AMB fill:#eafaf1,stroke:#27ae60
    style FAT fill:#fdedec,stroke:#e74c3c
```

---

### Tabela RACI — Leitura Rápida

| Ator | ME1 Pré-acesso | ME2 APS / UBS | ME3 Regulação | ME4 Atendimento | ME5 Continuidade |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Cidadão (CID)** | **R/A** | **R** | I | **R** | **R/A** |
| **APS-MUN** | I | **R/A** | R (inserção/comunicação) | C | R (contrarreferência) |
| **DRS** | — | C | **A** (supervisão) | I | **A** (fiscalização) |
| **REG-EST (CROSS)** | — | C | **R/A** (regulação) | I | I |
| **NIR** | — | — | R (vagas) | R (produção) | C |
| **AMB-OSS / AMB-EST** | — | — | I | **R/A** (consulta) | R (contrarreferência) |
| **FAT** | — | — | — | R (faturamento) | C |
| **SUP-FED** | C | C | C | C | C |

> Fail points críticos concentram-se onde a **accountability (A) está ausente ou mal definida**: ME5 (continuidade) tem o cidadão como único R/A efetivo, revelando uma lacuna estrutural de governança.

---

## Legenda dos Diagramas

### Atores e esferas institucionais

| Código | Ator | Esfera |
| :--- | :--- | :--- |
| CID | Cidadão | — |
| APS-MUN | UBS / ESF / eMulti / Operador de Regulação Municipal | Municipal |
| REG-EST | CROSS — médico regulador e operadores | Estadual |
| NIR | Núcleo Interno de Regulação do AME ou Hospital | Estadual / Contratado |
| AMB-OSS | Especialista em AME gerido por OSS (Lei 9.637/1998) | Contratado |
| AMB-EST | Especialista em unidade de administração direta | Estadual |
| SUP-FED | DATASUS / RNDS / bases federais de saúde | Federal |

### Fail points — referência rápida

| ID | Macroetapa | Descrição resumida | Prioridade |
| :--- | :--- | :--- | :--- |
| FP01 | Pré-acesso | Porta de entrada incorreta | Média |
| FP02 | Pré-acesso | Sem informação sobre fluxo e documentos | Baixa/Média |
| FP03 | APS/UBS | Acesso difícil à consulta inicial na UBS | Alta |
| FP04 | APS/Regulação | Encaminhamento incompleto; recusado pela regulação | Alta |
| FP05 | Regulação | **Fila invisível — sem previsão de espera** | **Crítica** |
| FP06 | Regulação | **Vaga perdida por falha de comunicação** | **Crítica** |
| FP07 | Atendimento | **Especialista sem histórico clínico da UBS** | **Crítica** |
| FP08 | Pós-consulta | **Exame sem fluxo integrado de agendamento** | **Crítica** |
| FP09 | Pós-consulta | Resultado do exame não chega ao profissional | Média/Alta |
| FP10 | Contrarreferência | Contrarreferência sem retorno digital à APS | Alta |
| FP11 | Continuidade | Sem responsável definido pelo próximo passo | Alta |
| FP12 | Transversal | Retrabalho por ausência de interoperabilidade | Média |
