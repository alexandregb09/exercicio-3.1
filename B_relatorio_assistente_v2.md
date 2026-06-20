# Relatório Técnico: Diagnóstico de Processo e Service Blueprint AS-IS
**Serviço:** Consulta Médica Especializada (Ambulatorial)  
**Escopo:** Secretaria de Estado da Saúde de São Paulo (SES-SP) no contexto do SUS  
**Abordagem:** Desenho de Serviços e Jornada do Cidadão  
**Versão:** 3.0 (Consolidada pós-Auditoria Regulatória de 2026)

---

## 1. Caracterização do Serviço de Consulta Médica

No contexto da Secretaria de Estado da Saúde de São Paulo (SES-SP), o serviço de consulta médica analisado foca na **Atenção Ambulatorial Especializada (AAE)**. Enquanto a Atenção Primária à Saúde (APS) é de responsabilidade estritamente municipal, o Estado atua como o principal gestor e provedor da média e alta complexidade, operando uma rede própria, conveniada e filantrópica estruturada por meio dos Departamentos Regionais de Saúde (DRS).

### Parâmetros de Planejamento e Programação Assistencial
O planejamento da oferta e a estimativa de necessidade de consultas básicas de uma determinada região de saúde não seguem mais as diretrizes rígidas da antiga Portaria GM/MS nº 1.101/2002, a qual foi expressamente revogada pelo Artigo 7º da **Portaria GM/MS nº 1.631, de 1º de outubro de 2015**. O ordenamento federal vigente substituiu os tetos normativos fixos por parâmetros indicativos flexíveis, que devem ser ajustados localmente com base na realidade epidemiológica, demográfica e orçamentária de cada território.

Para fins de contextualização histórica e monitoramento técnico de controle interno, a meta de 1,5 consultas estabelecida na vigência do Pacto pela Saúde (instituído pela **Portaria GM/MS nº 325, de 21 de fevereiro de 2008**, Indicador 31) aplicava-se exclusivamente à média anual de consultas médicas nas *especialidades básicas* (Clínica Médica, Pediatria e Ginecologia-Obstetrícia) por habitante, e não ao universo total ou especializado do SUS. O monitoramento histórico desse indicador demonstrou melhoria progressiva na maioria das unidades da federação, comprovando a utilidade histórica das pactuações interfederativas para o fortalecimento da gestão local de saúde.

O cálculo da necessidade anual de consultas básicas ($N_c$) pode ser modelado matematicamente pela equação:
$$N_c = P \times i$$

Onde $P$ representa a população total da área de abrangência e $i$ representa o indicador de atendimento anual de consultas por habitante. Caso um município apresente uma população de 50.000 habitantes e uma produção anual real de consultas básicas ($C_e$) de 35.000 atendimentos, a taxa de cobertura real ($Co$) é obtida pela razão:
$$Co = \frac{C_e}{P}$$

Neste cenário de exemplo, a cobertura real seria de $0,7$ consultas por habitante ao ano, revelando um déficit em relação aos antigos parâmetros históricos de planejamento e auxiliando os órgãos de controle na identificação de subutilização ou subfinanciamento das equipes locais.

### Tipos de Consultas Ofertadas
*   **Primeira Consulta Especializada:** Atendimento inicial com um médico especialista (ex: Cardiologia, Oncologia, Neurologia) focado em diagnóstico ou definição de conduta terapêutica, derivado de um encaminhamento obrigatório da atenção básica municipal.
*   **Consulta de Retorno:** Atendimento subsequente na mesma especialidade e unidade para avaliação de exames solicitados, monitoramento da evolução clínica ou ajuste farmacológico.
*   **Consultas de Acompanhamento Crônico:** Atendimentos periódicos de longo prazo voltados a pacientes com patologias complexas de alta prevalência (ex: pré-natal de alto risco, oncologia).

### Usuários e Atores Envolvidos
Os usuários são cidadãos residentes no Estado de São Paulo que necessitam de cuidados de densidade tecnológica superior àquela ofertada nas Unidades Básicas de Saúde (UBS) e Estratégias de Saúde da Família (ESF) municipais. 

A rede de prestação do serviço integra:
*   **Unidades de Origem (Municípios):** UBS e ESF geridas pelas secretarias municipais. A composição mínima da eSF exige a presença concomitante do médico e do enfermeiro em regime de 40 horas semanais. O descumprimento desse requisito de equipe mínima por mais de dois meses gera o bloqueio automático de repasses federais de custeio na plataforma e-Gestor APS do Ministério da Saúde.
*   **Equipes Multiprofissionais (eMulti):** Instituídas, estruturadas e financiadas exclusivamente pela **Portaria GM/MS nº 635, de 22 de maio de 2023** (nas modalidades Ampliada, Complementar e Estratégica), as eMulti atuam de forma integrada às eSF, Consultórios na Rua e UBS Fluviais, oferecendo atendimento interprofissional presencial e assistência remota mediada por Tecnologias de Informação e Comunicação (TIC) para ampliar a resolutividade na atenção primária.
*   **Unidades de Destino (SES-SP e Conveniados):** Ambulatórios Médicos de Especialidades (AMEs), Hospitais Estaduais (geridos por Administração Direta ou Organizações Sociais de Saúde - OSS via Contratos de Gestão baseados na Lei Federal nº 9.637/1998) e Santas Casas.
*   **Complexo Regulador:** Central de Regulação de Ofertas de Serviços de Saúde (**CROSS**), que opera os fluxos de acesso por delegação da SES-SP.

### Integração Federativa e Articulação Institucional
A articulação entre os entes federados baseia-se na descentralização e no comando único em cada esfera de governo. No nível de gestão e controle, a Secretaria de Atenção Primária à Saúde (SAPS) do Ministério da Saúde atua na formulação de políticas nacionais e financiamento da atenção primária, enquanto o Departamento Nacional de Auditoria do SUS (DenaSUS) atua estritamente como órgão de controle interno e auditoria, sem competência operacional de monitoramento ou pactuação regional direta.

Embora o planejamento assistencial foque na rede pública, existem importantes interações regulatórias entre o ecossistema de saúde suplementar (gerido pela Agência Nacional de Saúde Suplementar - ANS) e o SUS:
1.  **Ressarcimento ao SUS (Art. 32 da Lei Federal nº 9.656/1998):** Mecanismo pelo qual as operadoras de planos de saúde são obrigadas a restituir ao Fundo Nacional de Saúde os custos de consultas e atendimentos prestados a seus beneficiários dentro da rede pública.
2.  **Rede Nacional de Dados de Saúde (RNDS):** Plataforma nacional de interoperabilidade que promove o intercâmbio de dados clínicos e prontuários eletrônicos entre os setores público e privado suplementar, gerando reflexos diretos na continuidade do cuidado.

---

## 2. A Dinâmica Operacional da Regulação: CROSS e SIRESP

A regulação do acesso às consultas especializadas no Estado de São Paulo é operacionalizada pela CROSS por meio do **Sistema Informatizado de Regulação do Estado de São Paulo (SIRESP)**. O SIRESP funciona como uma plataforma unificada que integra módulos de atuação parametrizáveis e absorve os históricos de portais anteriores como Conexa, Regnet, Hospnet e Resgate.

### Estrutura Funcional e Módulos do SIRESP

| Módulo SIRESP | Função Principal | Responsabilidade Operacional | Limitação Técnica Identificada |
| :--- | :--- | :--- | :--- |
| **Ambulatorial** | Agendamento de consultas especializadas e exames de média/alta complexidade. | Central de Regulação (CROSS). | Relatórios segregados por unidade que dificultam a visualização da demanda unificada do município. |
| **Urgência** | Transferências emergenciais e vagas de UTI. | Equipe médica e administrativa da CROSS. | Dependência estrita da inserção ágil de dados clínicos pelas unidades de origem. |
| **Leitos** | Gestão de internações com e sem emissão de AIH. | Hospitais e centrais reguladoras regionais. | Falta de transparência ativa das filas de espera diretamente para os pacientes. |
| **Indicadores** | Geração de relatórios de produção e tempo de espera. | Gestores do SIRESP e Coordenadoria de Regiões de Saúde. | Dificuldade de extração consolidada para tomada de decisões municipais estratégicas. |

Na prática assistencial, o médico da UBS insere a solicitação clínica no módulo Ambulatorial do SIRESP. A equipe multiprofissional da CROSS — composta por médicos e enfermeiros reguladores — avalia a gravidade do caso sob protocolos clínicos específicos (classificação de prioridade P1 a P4) e busca a vaga adequada no pool de agendas disponibilizado pelos AMEs e hospitais. A CROSS atua como uma estrutura de inteligência e intermediação de fluxos, não possuindo ou gerenciando leitos ou agendas de forma autônoma. 

Como o sistema apresenta relatórios segregados por unidade solicitante, as gestões municipais enfrentam dificuldades para visualizar de forma consolidada a demanda reprimida total do município. Em resposta a esse obstáculo, secretarias municipais de saúde (como a de Campinas) iniciaram o desenvolvimento de ferramentas analíticas próprias para consolidar as filas de espera locais extraídas do SIRESP, permitindo identificar as demandas reprimidas por distrito de saúde, especialidade e Código Internacional de Doenças (CID).

---

## 3. Estrutura de Camadas do Service Blueprint AS-IS

Mapeamento integrado das três linhas fundamentais do serviço que ocorrem em cada macroetapa da jornada.

### Macroetapa A: Acesso e Solicitação (Na UBS/Rede Municipal)
*   **Linha de Interação (Visão do Cidadão):**
    *   *Objetivo:* Obter encaminhamento para um médico especialista.
    *   *Ações:* Consulta com clínico geral na UBS municipal, relato de sintomas, recebimento da guia de encaminhamento impressa.
    *   *Canais:* Presencial (UBS).
    *   *Informações Necessárias:* Cartão Nacional de Saúde (CNS), documento com foto, comprovante de residência.
    *   *Expectativas:* Sair da UBS com a data marcada ou com previsão transparente do tempo de espera.
    *   *Dificuldades:* Longo tempo de espera na fila da própria UBS para conseguir a consulta inicial com o médico generalista.
*   **Linha de Visibilidade (Pontos de Contato):** O cidadão visualiza o consultório médico, o profissional preenchendo a guia e o balcão administrativo da UBS. É emitida a Guia de Referência do SUS.
*   **Linha de Retaguarda (Bastidores):** 
    *   *Processo:* Avaliação da necessidade clínica $
ightarrow$ Médico da UBS $
ightarrow$ Prontuário Eletrônico Municipal $
ightarrow$ Registro clínico.
    *   *Processo:* Inserção do pedido no sistema estadual $
ightarrow$ Operador de Regulação Municipal $
ightarrow$ Plataforma SIRESP (Módulo Ambulatorial) $
ightarrow$ Solicitação em status "Aguardando Avaliação".

### Macroetapa B: Regulação e Agendamento (Processamento do Estado)
*   **Linha de Interação (Visão do Cidadão):**
    *   *Objetivo:* Ter a consulta agendada em tempo oportuno e ser avisado com clareza.
    *   *Ações:* Aguardar passivamente em sua residência; atender chamadas telefônicas ou deslocar-se à UBS para checar o andamento do pedido.
    *   *Canais:* Telefone (ligação/SMS) ou atendimento presencial na UBS.
    *   *Informações Necessárias:* Contatos telefônicos atualizados no cadastro do SUS.
    *   *Expectativas:* Ser avisado com antecedência razoável para organizar transporte e afastamento do trabalho.
    *   *Dificuldades:* Ausência de transparência sobre sua posição na fila ("caixa preta").
*   **Linha de Visibilidade (Pontos de Contato):** Recebimento de chamada telefônica ou SMS informativo. Retirada da Ficha de Agendamento CROSS impressa na UBS. O cidadão não possui acesso direto aos sistemas de regulação do Estado.
*   **Linha de Retaguarda (Bastidores):**
    *   *Processo:* Classificação de risco clínico $
ightarrow$ Médico Regulador CROSS $
ightarrow$ SIRESP $
ightarrow$ Atribuição de prioridade (P1 a P4).
    *   *Processo:* Parametrização de agendas $
ightarrow$ Núcleo de Regulação Interna (NIR) do AME/Hospital $
ightarrow$ Sistema de Informação Hospitalar Interno (ex: MV) $
ightarrow$ Vagas disponibilizadas via barramento no SIRESP.
    *   *Processo:* Vinculação de vaga (Match) $
ightarrow$ Algoritmo/Operador CROSS $
ightarrow$ SIRESP $
ightarrow$ Vaga reservada para o CNS do paciente.
    *   *Processo — Gestão de Agenda (backstage NIR):* O Núcleo Interno de Regulação (NIR) realiza a **abertura de agenda** no sistema interno (MV ou similar) e carrega vagas no SIRESP periodicamente, conforme metas contratuais. Bloqueios de agenda por férias médicas ou indisponibilidade de sala devem ser registrados com antecedência no SIRESP; quando não o são, geram vagas ociosas sem comunicação ao paciente. O NIR gerencia também **encaixes** (slots emergenciais) para absorver devoluções de vagas e casos P1 reclassificados. Fluxo: NIR parametriza agenda → sistema interno → carga no SIRESP → vagas disponíveis para match pela CROSS.

### Macroetapa C: Atendimento e Desfecho (Na Unidade Estadual - AME/Hospital)
*   **Linha de Interação (Visão do Cidadão):**
    *   *Objetivo:* Ser atendido pelo especialista, obter diagnóstico preciso e orientações terapêuticas.
    *   *Ações:* Deslocar-se até o município polo do AME/Hospital, realizar check-in na recepção, passar pela triagem de enfermagem e pela consulta médica especializada.
    *   *Canais:* Presencial (Unidade Ambulatorial Estadual).
    *   *Informações Necessárias:* Ficha de agendamento CROSS, documento de identidade, Cartão SUS e exames anteriores.
    *   *Expectativas:* Atendimento pontual e resolutivo na mesma unidade.
    *   *Dificuldades:* Custos e desgaste com o deslocamento intermunicipal; sair da consulta com pedidos de exames sem saber onde realizá-los.
*   **Linha de Visibilidade (Pontos de Contato):** Estrutura física do AME, guichê de recepção, painel eletrônico de senhas, consultório do especialista, computadores com o prontuário interno. Emissão de receita médica, solicitações de exames e contrarreferência escrita.
*   **Linha de Retaguarda (Bastidores):**
    *   *Processo:* Abertura de atendimento $
ightarrow$ Recepcionista do AME $
ightarrow$ Prontuário Eletrônico Interno (ex: MV) $
ightarrow$ Prontuário ativado na fila médica.
    *   *Processo:* Registro clínico e codificação $
ightarrow$ Médico Especialista $
ightarrow$ Prontuário Eletrônico Interno $
ightarrow$ Evolução clínica salva e assinada digitalmente com certificado ICP-Brasil (inserção de CID-10).
    *   *Processo:* Faturamento SUS $
ightarrow$ Setor de Faturamento do AME $
ightarrow$ Sistema de Informação Ambulatorial (SIA-SUS) $
ightarrow$ Geração de BPA-I ou APAC para repasse financeiro contratual (metas da Resolução SS-SP nº 44/2021).
    *   *Processo — Recepção e Faturamento (backstage):* A recepção do AME realiza **conferência documental** (ficha CROSS, RG, CNS e exames anteriores) e **validação de cadastro** no sistema interno antes de abrir o atendimento no prontuário. O NIR registra o comparecimento no SIRESP, contabilizando a vaga como "realizada" para fins de meta contratual. O setor de faturamento codifica a produção em BPA-I ou APAC para submissão ao SIA-SUS até o dia 5 do mês seguinte; **glosas** ocorrem por CID-10 incompatível, APAC sem autorização prévia ou prontuário sem assinatura digital ICP-Brasil. O repasse financeiro à unidade (ou OSS) é calculado sobre a produção aprovada descontadas as glosas.

### Estrutura dos Contratos de Gestão com OSS

Os AMEs e Hospitais Estaduais geridos por Organizações Sociais de Saúde operam sob **Contratos de Gestão** celebrados com a SES-SP (Lei Federal nº 9.637/1998; Decreto Estadual SP nº 43.493/1998). Elementos essenciais: (a) **metas quantitativas** de primeiras consultas e retornos definidas pela Resolução SS-SP nº 44/2021; (b) **indicadores de qualidade** (taxa de absenteísmo ≤ 25%, tempo médio de espera por especialidade); (c) **Comissão de Acompanhamento do Contrato (CAC)** com reuniões mensais paritárias (SES-SP + OSS); (d) **repasse financeiro** com parcela fixa (custeio da estrutura) e parcela variável (produção assistencial aprovada); (e) **fiscalização** pelos DRS com visitas técnicas periódicas e auditoria documental amostral. O descumprimento de metas gera glosa contratual proporcional; a superação pode gerar repasse de incentivo, conforme cláusula específica.

---

## 4. Evidências Físicas e Digitais do Serviço

As evidências que materializam a prestação do serviço e moldam a percepção do usuário ao longo da jornada são classificadas na tabela abaixo:

| Etapa da Jornada | Evidência Identificada | Classificação da Evidência | Papel na Experiência do Cidadão |
| :--- | :--- | :--- | :--- |
| **Acesso/UBS** | Unidade Básica de Saúde (Prédio físico) | Evidência Física | Define a percepção inicial de acolhimento e a infraestrutura básica do SUS. |
| **Acesso/UBS** | Cartão Nacional de Saúde (Físico ou App) | Evidência Digital / Física | Chave de identidade do cidadão; garante que ele existe no ecossistema SUS. |
| **Acesso/UBS** | Guia de Encaminhamento Escrita à Mão | Documento Gerado | Elemento de segurança material de que seu pedido foi formalizado pelo clínico. |
| **Regulação** | Mensagem de Texto (SMS) da CROSS/UBS | Comunicação Institucional | Informa o agendamento; reduz a ansiedade da espera passiva. |
| **Regulação** | Ficha de Agendamento Impressa (CROSS) | Documento Gerado | Comprovante oficial contendo data, hora e endereço do especialista. |
| **Atendimento** | Painel Eletrônico de Senhas na Recepção | Evidência Física | Organiza o fluxo e sinaliza transparência no tempo de espera local. |
| **Atendimento** | Estrutura e Consultório do AME / Hospital | Evidência Física | Ambientes tipicamente mais modernos, gerando percepção de alta qualidade. |
| **Atendimento** | Tela do Prontuário Eletrônico | Evidência Digital | Sinaliza ao paciente que seu histórico médico está sendo registrado formalmente. |
| **Desfecho** | Receita Médica e Pedidos de Exames | Documento Gerado | O resultado prático da consulta; direciona os próximos passos de saúde do cidadão. |

---

## 5. Instituições Formadoras e Residências em Saúde

Os Programas de Residência Médica e de Residência Multiprofissional em Saúde constituem pilares estratégicos na rede de serviços da SES-SP. Regulados nacionalmente pela Comissão Nacional de Residência Médica (CNRM) e pela Comissão Nacional de Residência Multiprofissional em Saúde (CNRMS), esses programas promovem a formação especializada em serviço diretamente nas unidades do SUS (como Hospitais de Ensino e AMEs de base acadêmica). 

Os profissionais residentes atuam sob supervisão direta de preceptores (médicos e especialistas do quadro fixo), incrementando a capacidade instalada e a força de trabalho assistencial da rede pública. Além disso, as residências atuam como um dos principais mecanismos de fixação, atração e provimento de médicos especialistas em regiões metropolitanas e periféricas de difícil fixação, mitigando os vazios assistenciais crônicos no Estado.

---

## 6. Normativos Aplicáveis e Fundamentação Jurisprudencial

| Norma / Precedente | Tema Relacionado | Impacto no Processo de Consulta Médica |
| :--- | :--- | :--- |
| **Constituição Federal (Art. 196 a 200)** | Direito à Saúde e Universalidade | Garante o acesso universal e igualitário às ações de saúde, proibindo a cobrança por consultas especializadas e exigindo a gratuidade integral do processo. |
| **Lei Federal nº 8.080/1990** | Organização e Princípios do SUS | Consolida os princípios de *Integralidade* (o cidadão tem direito ao especialista se a UBS não resolver) e *Regionalização* (organização em redes de atenção à saúde). |
| **Portaria de Consolidação GM/MS nº 2/2017** | Políticas Nacionais de Saúde (Regulação) | Regulamenta a Política Nacional de Regulação do SUS. Define que o acesso às consultas especializadas deve ser obrigatoriamente mediado por complexos reguladores, vedando o agendamento direto "de balcão" no hospital pelo paciente. |
| **Decreto Estadual (SP) nº 56.061/2010** | Institucionalização da CROSS | Cria e organiza a Central de Regulação de Ofertas de Serviços de Saúde no Estado de São Paulo, estabelecendo o comando regulatório unificado sob gestão estadual. |
| **Portaria GM/MS nº 635/2023** | Financiamento e Diretrizes das eMulti | Regulamenta o custeio federal, as modalidades de carga horária e a atuação interprofissional de apoio à atenção básica, viabilizando a telessaúde nas consultas. |
| **Resolução SS-SP nº 44/2021** | Contratualização de OSS / Metas | Fixa as metas obrigatórias de primeiras consultas e consultas de retorno que as Organizações Sociais devem disponibilizar mensalmente no SIRESP. |
| **Jurisprudência do STF: Tema 698 de Repercussão Geral** | Intervenção Judicial e Contratos de OS | *(Precedente originado no RE nº 684.612/RJ, julgado pelo Plenário do STF)*. A tese vinculante fixa dois pontos cruciais: <br>1. Legitima a intervenção do Judiciário em políticas públicas de saúde em caso de grave deficiência do serviço, determinando que o juiz fixe as finalidades administrativas a serem atingidas e exija do Executivo a apresentação de um plano de ação estruturado.<br>2. Chancela a constitucionalidade da contratação de Organizações Sociais (OS) e OSCIPs (Lei nº 9.637/1998) como uma alternativa discricionária e válida ao concurso público para suprir de forma ágil o déficit crônico de pessoal e recursos humanos nas unidades de saúde. |

---

## 7. Identificação de Fail Points (Pontos de Falha)

Os *Fail Points* representam as rupturas e gargalos críticos identificados no desenho do processo atual (AS-IS).

### Falhas na Jornada do Cidadão (Perspectiva do Usuário)

#### 1. "O Silêncio da Fila de Espera" (Falta de Transparência Ativa)
*   **Etapa do Serviço:** Regulação e Agendamento.
*   **Problema:** O cidadão aguarda por meses sem receber qualquer feedback sobre a sua posição na fila ou previsão estimada de atendimento.
*   **Causa Provável:** Ausência de um portal de transparência ativa das filas parametrizado para o usuário final dentro do SIRESP/CROSS; falta de integração de notificações automáticas ao cidadão.
*   **Impacto no Cidadão:** Elevada ansiedade, sensação de desamparo estatal, agravamento silencioso do quadro clínico e indução à judicialização individual.
*   **Consequência Operacional:** Sobrecarga dos canais de Ouvidoria da SES-SP e aumento de mandados judiciais de urgência que desorganizam os critérios técnicos de priorização médica.
*   **Indicador de Monitoramento:** Tempo Médio de Espera por Especialidade (dias) e Índice de Judicialização de Consultas.

#### 2. Agendamento com Prazo Exíguo e Defasagem Cadastral (Vaga Perdida)
*   **Etapa do Serviço:** Confirmação da Consulta.
*   **Problema:** A comunicação do agendamento ocorre com poucos dias de antecedência, frequentemente por chamadas telefônicas de números ocultos ou privados, gerando perda da vaga por não localização do paciente.
*   **Causa Provável:** Desatualização dos dados cadastrais do cidadão na base do Cartão SUS e dependência de métodos síncronos de contato (ligação telefônica tradicional), sem o uso de canais digitais assíncronos institucionais.
*   **Impacto no Cidadão:** Perda do agendamento e cancelamento da solicitação no sistema, obrigando o usuário a retornar ao início do fluxo assistencial na UBS municipal.
*   **Consequência Operacional:** Elevada taxa de ociosidade em consultórios de alta tecnologia, desperdiçando a hora de contratação do médico especialista.
*   **Indicador de Monitoramento:** Taxa de Absenteísmo em Consultas Especializadas (Média histórica da rede frequentemente situada entre 20% e 30%).

### Falhas Internas (Perspectiva Operacional e de Retaguarda)

#### 3. Fragmentação de Prontuários e Desconexão Tecnológica
*   **Etapa do Serviço:** Atendimento Médico Especializado.
*   **Problema:** O médico especialista no AME ou Hospital Estadual não tem acesso aos registros clínicos, anamnese e exames laboratoriais prévios realizados pelo paciente na UBS de origem municipal.
*   **Causa Provável:** Falta de barramentos de interoperabilidade tecnológica entre os sistemas de prontuário eletrônico municipais (e-SUS PEC ou softwares próprios) e os sistemas de gestão hospitalar das unidades estaduais (ex: MV, Pixeon).
*   **Impacto no Cidadão:** O paciente é obrigado a repetir todo o seu histórico clínico verbalmente e, frequentemente, precisa refazer exames laboratoriais básicos porque o especialista não visualiza os resultados anteriores.
*   **Consequência Operacional:** Desperdício financeiro com redundância de exames diagnósticos básicos solicitados em duplicidade e perda de tempo clínico útil na consulta especializada.
*   **Indicador de Monitoramento:** Taxa de Redundância de Exames Solicitados e Percentual de Consultas com Prontuário Interoperável.

#### 4. Ruptura da Linha de Cuidado na Contrarreferência
*   **Etapa do Serviço:** Encerramento e Continuidade do Cuidado.
*   **Problema:** Após a definição da conduta ou alta do especialista no AME/Hospital, a orientação clínica de continuidade do tratamento não chega formalmente ao conhecimento do médico de família na UBS de origem.
*   **Causa Provável:** O fluxo de contrarreferência depende de um documento em papel entregue em mãos ao próprio paciente, transformando o usuário no único mensageiro da informação clínica entre os entes federados.
*   **Impacto no Cidadão:** Descontinuidade terapêutica e risco de prescrições medicamentosas conflitantes ou incompatíveis entre os profissionais da rede.
*   **Consequência Operacional:** Retorno desnecessário de pacientes crônicos estabilizados às filas da média complexidade (hiperutilização ambulatorial), sufocando a oferta de vagas para novos casos.
*   **Indicador de Monitoramento:** Índice de Efetividade da Contrarreferência Digital (guias devolvidas eletronicamente e integradas à APS).

---

## 8. Tabela Completa do Service Blueprint AS-IS

A matriz a seguir consolida todas as camadas mapeadas do serviço, correlacionando a jornada do cidadão aos bastidores e regras de operação da Secretaria de Estado da Saúde de São Paulo.

| Etapa da Jornada | Ação do Cidadão | Ponto de Contato | Evidência Física/Digital | Processo de Bastidor | Responsável | Sistema Utilizado | Norma Relacionada | Fail Point Identificado |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Triagem na Atenção Básica** | Relata sintomas em consulta na UBS municipal. | Consultório médico da UBS de origem. | Guia de encaminhamento manual; Prontuário local. | Avaliação da necessidade de densidade tecnológica superior. | Médico Generalista Municipal. | Prontuário Eletrônico Municipal (ou e-SUS). | Art. 196 CF / Lei 8.080 (Integralidade). | Demora crônica no agendamento da consulta básica inicial na UBS. |
| **2. Solicitação da Vaga** | Entrega a guia no balcão e aguarda inserção. | Guichê administrativo/Regulação da UBS. | Protocolo de recebimento de documento impresso. | Digitação e transcrição clínica dos dados do paciente para o sistema estadual. | Operador de Regulação Municipal. | **SIRESP (Módulo Ambulatorial)** | Portaria MS 2/2017 (Regulação). | Erros de digitação e omissão de dados clínicos essenciais que causam recusa da guia. |
| **3. Triagem de Regulação** | Aguarda passivamente em sua residência. | Nenhum contato visível. | Ausente. | Avaliação clínica do pedido com base nos protocolos de priorização de risco. | Médico Regulador do Estado (CROSS). | **SIRESP** | Diretrizes Técnicas da CROSS / Portaria MS 2/2017. | **Fail Point 1:** Falta de transparência na fila; paciente sem previsão do tempo de espera. |
| **4. Casamento da Oferta** | Aguarda processamento interno da vaga. | Nenhum contato visível. | Ausente. | Vinculação automatizada ou manual da vaga disponibilizada pelo AME/Hospital ao paciente. | Operador do Complexo Regulador. | **SIRESP** | Resolução SS-SP 44/2021 (Contratos OSS). | Baixa disponibilidade de vagas especializadas injetadas pelas unidades de destino. |
| **5. Comunicação do Agendamento** | Atende o telefone ou recebe aviso por mensagem/ACS. | Chamada telefônica, SMS ou visita do ACS. | Mensagem de SMS ou Ficha CROSS impressa na UBS. | Acionamento de listas de contatos e atualização de status da vaga para "Confirmada". | Central de Atendimento Municipal / ACS. | SIRESP / Sistema de Telefonia Local. | Princípio da Eficiência Administrativa. | **Fail Point 2:** Perda da vaga devido a dados cadastrais defasados ou aviso de última hora. |
| **6. Check-In na Unidade** | Viaja até o município polo e apresenta-se no balcão. | Recepção do Ambulatório Especializado (AME/Hospital). | Painel de senhas; Documentos validados. | Conferência cadastral, abertura do atendimento no Prontuário local e ativação de faturamento. | Recepcionista da Unidade Estadual (ou OSS). | Sistema de Gestão Hospitalar Interno (ex: MV). | Regras de Faturamento Ambulatorial SUS (SIA). | Atrasos na fila da recepção misturando fluxos de especialidades distintas. |
| **7. Consulta com Especialista** | Responde à anamnese e passa por exame físico clínico. | Consultório médico da unidade estadual. | Estetoscópio; Computador com prontuário visível. | Registro da evolução clínica, preenchimento de CID-10 e emissão de laudos de cobrança. | Médico Especialista do Estado/OSS. | Sistema de Prontuário Életrônico Interno. | Código de Ética Médica / Padrões de Faturamento SUS. | **Fail Point 3:** Apagão de informações; médico não vê o histórico da UBS. |
| **8. Desfecho e Encaminhamento** | Retira documentos de saída e orientações na mesa/saída. | Balcão de atendimento pós-consulta ou mesa médica. | Receita médica; Pedidos de exames especializados; Contrarreferência. | Emissão de guias de faturamento SIA (BPA-I/APAC) e registro estatístico de produção. | Médico Especialista / Faturamento Interno. | Sistema de Prontuário / Faturamento SIA-SUS. | Pacto pela Saúde / Diretrizes de Redes de Atenção. | **Fail Point 4:** Paciente sai com pedidos de exames complexos sem saber onde e como agendá-los. |

---

## 9. Diretrizes Estratégicas para Transformação do Cuidado (TO-BE)

Com base no diagnóstico técnico estruturado no blueprint AS-IS, são recomendadas quatro macroações de transformação para a modernização do serviço público da SES-SP:

1.  **Transparência Ativa via Portal Integrado:** Viabilizar uma interface de consulta cidadã (integrada ao Poupatempo Digital ou ao aplicativo Meu SUS Digital) para que o usuário acompanhe o status de sua solicitação no SIRESP, visualizando de forma clara a classificação de prioridade de seu protocolo e o tempo médio estimado de espera regional para aquela especialidade.
2.  **Mensageria Interativa Omnichannel:** Substituir progressivamente as chamadas telefônicas manuais de números ocultos por sistemas automatizados interativos de mensageria assíncrona (como WhatsApp corporativo verificado e SMS integrados), permitindo ao cidadão confirmar, cancelar ou solicitar o reagendamento imediato da consulta de forma autônoma.
3.  **Barramento de Interoperabilidade em Saúde (HL7 / FHIR):** Estabelecer um barramento de dados clínico estadual estruturado sob padrões abertos internacionais (HL7/FHIR) para conectar os prontuários eletrônicos municipais das UBS aos prontuários hospitalares da rede própria e das OSS (AMEs), assegurando que o especialista acesse o histórico clínico territorial e eliminando a redundância de exames diagnósticos.
4.  **Agendamento Qualificado na Saída (Cuidado Resolutivo):** Pactuar contratualmente com as OSS gestoras de AMEs que nenhum paciente saia da consulta com solicitações de exames diagnósticos de alta complexidade sem o agendamento prévio e efetivado destes exames na própria estrutura física do ambulatório ou em sua rede de apoio regional direta, impedindo a devolução burocrática do cidadão às centrais municipais.

---
**Fontes e Referências Documentais Utilizadas:**
*   Secretaria de Estado da Saúde de São Paulo (SES-SP) - Manuais e Diretrizes de Operação do SIRESP e CROSS.
*   Ministério da Saúde - Política Nacional de Regulação do SUS e Banco de Dados do DATASUS.
*   Supremo Tribunal Federal (STF) - Acórdão e Tese Vinculante do Tema 698 de Repercussão Geral (RE nº 684.612/RJ).
*   Legislação Federal Aplicável: Leis Orgânicas da Saúde (Leis nº 8.080/1990 e nº 8.142/1990), Lei das Organizações Sociais (Lei nº 9.637/1998) e Lei dos Planos de Saúde (Lei nº 9.656/1998).
