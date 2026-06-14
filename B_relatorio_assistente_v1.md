# Relatório Técnico: Diagnóstico de Processo e Service Blueprint AS-IS
**Serviço:** Consulta Médica Especializada (Ambulatorial)  
**Escopo:** Secretaria de Estado da Saúde de São Paulo (SES-SP) no contexto do SUS  
**Abordagem:** Desenho de Serviços e Jornada do Cidadão  

---

## 1. Caracterização do Serviço de Consulta Médica

No contexto da Secretaria de Estado da Saúde de São Paulo (SES-SP), o serviço de consulta médica aqui analisado foca na **Atenção Ambulatorial Especializada (AAE)**. Diferente da Atenção Primária (UBS), que é de responsabilidade estritamente municipal, o Estado atua como o principal gestor e provedor da média e alta complexidade, operando uma rede própria, conveniada e filantrópica.

### Tipos de Consultas Ofertadas
*   **Primeira Consulta Especializada:** Atendimento inicial com um médico especialista (ex: Cardiologia, Oncologia, Neurologia) para fins de diagnóstico ou definição de conduta terapêutica, derivado de um encaminhamento da atenção básica.
*   **Consulta de Retorno:** Atendimento subsequente na mesma especialidade para avaliação de exames solicitados, monitoramento da evolução clínica ou ajuste de medicamentos.
*   **Consultas de Acompanhamento Crônico:** Atendimentos periódicos de longo prazo para pacientes com patologias complexas de alta prevalência (ex: insuficiência cardíaca grave, pré-natal de alto risco).

### Usuários do Serviço
Cidadãos residentes no Estado de São Paulo que dependem do SUS e que passaram por atendimento prévio na rede de Atenção Primária à Saúde (APS) municipal, apresentando uma necessidade clínica que supera a capacidade resolutiva do médico generalista/da família.

### Unidades e Atores Envolvidos
*   **Unidades de Origem (Municípios):** Unidades Básicas de Saúde (UBS) e Estratégias de Saúde da Família (ESF), controladas pelas secretarias municipais de saúde.
*   **Unidades de Destino (SES-SP e Conveniados):** Hospitais Estaduais (Administração Direta ou via Organizações Sociais de Saúde - OSS), Ambulatórios Médicos de Especialidades (AMEs) — que concentram o maior volume de consultas especializadas do Estado —, e Hospitais Filantrópicos/Santas Casas.
*   **Complexo Regulador Estadual:** Central de Regulação de Ofertas de Serviços de Saúde (**CROSS**), que atua como a inteligência de bastidor que gerencia o fluxo de vagas.
*   **Profissionais de Saúde:** Médicos solicitantes (básica), médicos reguladores (CROSS), equipe de recepção/faturamento, e médicos especialistas (unidades de destino).

### Integração Estado-Município e Fluxo Geral
A integração baseia-se na descentralização e na regionalização do SUS. O município identifica a necessidade e insere o pedido. O Estado coordena a distribuição do recurso especializado por meio dos DRS (Departamentos Regionais de Saúde) utilizando a plataforma CROSS. O fluxo geral segue a lógica:

`[Cidadão com Sintoma] ➔ [UBS Municipal] ➔ [Encaminhamento do Médico] ➔ [Inserção no Sistema de Regulação] ➔ [Triagem CROSS] ➔ [Agendamento AME/Hospital] ➔ [Realização da Consulta Especializada] ➔ [Retorno ou Contrarreferência]`

---

## 2. Estrutura de Camadas do Service Blueprint AS-IS

Esta seção detalha o mapeamento das três linhas fundamentais do serviço que ocorrem de forma integrada em cada macroetapa da jornada.

### Macroetapa A: Acesso e Solicitação (Na UBS/Rede Municipal)

#### Linha de Interação (Visão do Cidadão)
*   **Objetivo do Cidadão:** Conseguir uma consulta com um médico especialista para resolver um problema que o clínico geral não pôde solucionar.
*   **Ações Realizadas:** Passar em consulta na UBS local; expor os sintomas; receber a guia de encaminhamento em papel; aguardar que o setor de regulação da UBS insira o pedido e forneça informações sobre o prazo.
*   **Canais Utilizados:** Presencial (UBS).
*   **Informações Necessárias:** Cartão Nacional de Saúde (CNS), documento com foto, comprovante de residência e sintomas detalhados.
*   **Expectativas:** Sair da UBS já com o dia e horário marcados para o especialista ou com uma estimativa clara de tempo de espera.
*   **Dificuldades Percebidas:** Longo tempo de espera na fila da UBS para conseguir a primeira consulta com o clínico; falta de clareza se o encaminhamento foi realmente enviado para o Estado.

#### Linha de Visibilidade (Pontos de Contato Percebidos)
*   **O que o cidadão enxerga:** O consultório médico da UBS, o profissional médico preenchendo uma guia manual (ou digitando no prontuário eletrônico local) e o balcão de atendimento administrativo da UBS.
*   **Quem realiza a interação:** Médico generalista municipal e recepcionista/assistente administrativo da UBS.
*   **Informações fornecidas:** A indicação de que o caso requer um especialista e que "o sistema vai avaliar a vaga".
*   **Documentos/Comprovantes:** Guia de Referência/Encaminhamento do SUS (geralmente impressa ou manuscrita).
*   **Sistemas percebidos:** Prontuário eletrônico municipal (quando houver).

#### Linha de Retaguarda (Processos de Bastidor)
*   **Análise Clínica e Registro Local:** O médico atesta a necessidade baseando-se em protocolos locais ➔ Médico da UBS ➔ Prontuário Eletrônico Municipal ➔ Registro clínico impresso ou digitalizado.
*   **Faturamento Ambulatorial Local:** Processamento da consulta básica realizada para fins de SIA/SUS ➔ Faturamento da UBS ➔ Sistema de Informação Ambulatorial (SIA-SUS) ➔ BPA (Boletim de Produção Ambulatorial) gerado.
*   **Inserção na Regulação Estadual:** Digitação dos dados clínicos do encaminhamento na plataforma do Estado para regulação ➔ Operador de Regulação Municipal ➔ Plataforma CROSS ➔ Solicitação em status "Aguardando Avaliação".

---

### Macroetapa B: Regulação e Agendamento (Processamento do Estado)

#### Linha de Interação (Visão do Cidadão)
*   **Objetivo do Cidadão:** Ter a sua consulta agendada em um tempo aceitável e ser avisado com antecedência clara sobre o local.
*   **Ações Realizadas:** Aguardar passivamente em casa (por semanas ou meses); atender chamadas telefônicas de números desconhecidos ou deslocar-se até a UBS para checar se a guia "saiu".
*   **Canais Utilizados:** Telefone (ligação ou SMS) e canal presencial de busca activa.
*   **Informações Necessárias:** Dados de contato atualizados.
*   **Expectativas:** Ser avisado com antecedência razoável para organizar transporte e folga no trabalho.
*   **Dificuldades Percebidas:** Ausência total de previsibilidade (a fila é uma "caixa preta"); alteração frequente de contatos telefônicos gera perda de vagas; ligações não atendidas resultam na queda da solicitação no sistema.

#### Linha de Visibilidade (Pontos de Contato Percebidos)
*   **O que o cidadão enxerga:** Recebimento de uma ligação telefônica da UBS ou do call center da CROSS, ou uma mensagem de texto (SMS). Em alguns municípios, o cidadão precisa ir retirar o papel impresso do agendamento na UBS.
*   **Quem realiza a interação:** Agente comunitário de saúde, telefonista da regulação municipal ou SMS automatizado.
*   **Informações fornecidas:** Nome do médico, especialidade, local do atendimento (geralmente um AME ou Hospital Estadual), data, horário e documentos obrigatórios.
*   **Documentos/Comprovantes:** Ficha de Agendamento CROSS impressa.
*   **Sistemas percebidos:** Nenhum sistema direto é acessível ao cidadão (o app "Meu SUS Digital" nem sempre reflete em tempo real as agendas estaduais geridas pela CROSS).

#### Linha de Retaguarda (Processos de Bastidor)
*   **Triagem e Classificação de Risco:** Avaliação da gravidade do caso relatado na guia versus os critérios do protocolo de regulação ➔ Médico Regulador da CROSS ➔ Sistema CROSS ➔ Solicitação classificada por prioridade (Vermelho/Amarelo/Verde).
*   **Parametrização e Oferta de Agendas:** Inserção das grades de horários disponíveis pelos prestadores estaduais no sistema ➔ Núcleo de Regulação Interna (NIR) do AME/Hospital ➔ Sistema de Informação de Gestão Hospitalar próprio (ex: MV, Pixeon) integrado via barramento à CROSS ➔ Vagas disponibilizadas no pool regulatório.
*   **Casamento de Oferta e Demanda (Match):** Algoritmo ou ação manual vincula o paciente com maior prioridade/tempo de espera à primeira vaga disponível no raio geográfico do DRS ➔ Operador de Regulação CROSS ➔ Sistema CROSS ➔ Vaga pré-reservada e vinculada ao CNS do paciente.
*   **Gestão de Absenteísmo Prévio:** Monitoramento de vagas recusadas ou não confirmadas para remanejamento imediato ➔ Central de Confirmação (Call Center) ➔ Sistema de telefonia/CROSS ➔ Liberação e re-agendamento de vaga em tempo recorde.

---

### Macroetapa C: Atendimento e Desfecho (Na Unidade Estadual - AME/Hospital)

#### Linha de Interação (Visão do Cidadão)
*   **Objetivo do Cidadão:** Ser atendido com dignidade, ter um diagnóstico preciso do especialista e receber orientações claras de tratamento ou exames.
*   **Ações Realizadas:** Deslocar-se até o município polo onde o AME/Hospital está localizado; fazer o check-in na recepção; aguardar a triagem de enfermagem; passar pela consulta médica; retirar receitas e pedidos de exames na saída.
*   **Canais Utilizados:** Presencial (Unidade Ambulatorial Estadual).
*   **Informações Necessárias:** Ficha de agendamento CROSS, RG, Cartão SUS e exames anteriores.
*   **Expectativas:** Atendimento pontual no horário marcado; médico focado no seu caso; sair com os exames necessários já agendados na própria unidade.
*   **Dificuldades Percebidas:** Custos e cansaço com deslocamento intermunicipal; atrasos longos na sala de espera mesmo com horário agendado; sair com o pedido de exame na mão sem saber onde realizá-lo.

#### Linha de Visibilidade (Pontos de Contato Percebidos)
*   **O que o cidadão enxerga:** Estrutura física da unidade estadual (geralmente com melhor infraestrutura de sinalização que as UBS), painel de chamada eletrônica, guichê de recepção com computadores, consultório médico, estetoscópio, computadores com prontuário.
*   **Quem realiza a interação:** Recepcionista do AME/Hospital, técnico de enfermagem (triagem de sinais vitais) e médico especialista.
*   **Informações fornecidas:** Confirmação do cadastro, triagem clínica inicial, diagnóstico médico, orientações terapêuticas.
*   **Documentos/Comprovantes:** Receita médica carimbada, guias de solicitação de exames de apoio diagnóstico, contrarreferência para a UBS.
*   **Sistemas percebidos:** Prontuário Clínico da Unidade de Destino (visível na tela do médico).

#### Linha de Retaguarda (Processos de Bastidor)
*   **Abertura de Prontuário e Recepção:** Validação da identidade do cidadão contra a base do Cartão SUS e ativação do prontuário local ➔ Recepcionista da Unidade ➔ Prontuário Eletrônico Interno (ex: Sistema MV) ➔ Atendimento iniciado no painel médico.
*   **Registro da Evolução Clínica e Codificação:** Anotação da anamnese, hipótese diagnóstica e inserção do código CID-10 ➔ Médico Especialista ➔ Prontuário Eletrônico Interno ➔ Prontuário atualizado e assinatura digital via certificado ICP-Brasil.
*   **Faturamento de Média Complexidade:** Registro do atendimento via SIA-SUS para geração do repasse financeiro (via teto MAC ou contrato de gestão OSS) ➔ Setor de Faturamento e Auditoria da Unidade ➔ Sistema de Informação Ambulatorial (SIA-SUS) ➔ Geração do espelho da APAC ou BPA-I (Individualizado).
*   **Emissão de Contrarreferência:** Registro de orientações para que o médico da UBS prossiga com o tratamento no território original ➔ Médico Especialista ➔ Sistema de Prontuário/CROSS (se integrado) ➔ Relatório de contrarreferência emitido.

---

## 3. Evidências Físicas do Serviço

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

## 4. Normativos Aplicáveis

| Norma | Tema Relacionado | Impacto no Processo de Consulta Médica |
| :--- | :--- | :--- |
| **Constituição Federal (Art. 196 a 200)** | Direito à Saúde e Universalidade | Garante o acesso universal e igualitário às ações de saúde, proibindo a cobrança por consultas especializadas e exigindo a gratuidade integral do processo. |
| **Lei Federal nº 8.080/1990** | Organização e Princípios do SUS | Consolida os princípios de *Integralidade* (o cidadão tem direito ao especialista se a UBS não resolver) e *Regionalização* (organização em redes de atenção à saúde). |
| **Portaria de Consolidação GM/MS nº 2/2017** | Políticas Nacionais de Saúde (Regulação) | Regulamenta a Política Nacional de Regulação do SUS. Define que o acesso às consultas especializadas deve ser obrigatoriamente mediado por complexos reguladores, vedando o agendamento direto "de balcão" no hospital pelo paciente. |
| **Decreto Estadual (SP) nº 50.759/2006** | Criação da CROSS | Institui a Central de Regulação de Ofertas de Serviços de Saúde no Estado de São Paulo, unificando a gestão de vagas de ambulatórios e hospitais sob regulação médica unificada do Estado. |
| **Resolução SS-SP nº 44/2021 (e atualizações)** | Diretrizes de Contratualização de OSS | Define as metas de produção de consultas primeiras e retornos que os AMEs e Hospitais geridos por OSS devem obrigatoriamente cumprir no mês, impactando diretamente o volume de vagas injetado na CROSS. |

---

## 5. Identificação de Fail Points (Pontos de Falha)

### Falhas na Jornada do Cidadão (Perspectiva do Usuário)

#### 1. "O Silêncio da Fila de Espera" (Falta de Transparência)
*   **Etapa do Serviço:** Regulação e Agendamento.
*   **Problema:** O cidadão fica meses sem receber qualquer feedback sobre a sua posição na fila ou previsão de atendimento.
*   **Causa Provável:** Falta de integração voltada ao usuário na plataforma CROSS; ausência de um portal público de transparência de filas detalhado por especialidade regional.
*   **Impacto no Cidadão:** Ansiedade elevada, sensação de abandono pelo Estado, piora silenciosa do quadro clínico e busca por vias judiciais (judicialização da saúde).
*   **Consequência Operacional:** Sobrecarga das ouvidorias e aumento de mandados judiciais que furam a fila técnica de prioridade médica.
*   **Indicador de Monitoramento:** Tempo Médio de Espera por Especialidade (dias) e Índice de Judicialização de Consultas.

#### 2. Agendamento com Prazo Exíguo e Perda de Contato (Vaga Perdida)
*   **Etapa do Serviço:** Confirmação da Consulta.
*   **Problema:** Chamadas telefônicas da regulação ocorrem em cima da hora, de números privados ou desconhecidos, fazendo com que o paciente perca a oportunidade por não atender ou não conseguir dispensa no trabalho a tempo.
*   **Causa Provável:** Cadastro desatualizado no Cartão SUS/CROSS e ausência de canais modernos e assíncronos de comunicação (como WhatsApp institucional estruturado).
*   **Impacto no Cidadão:** Perda do encaminhamento, obrigando-o a retornar ao início da jornada (UBS) para reiniciar todo o processo.
*   **Consequência Operacional:** Vagas ociosas geradas em cima da hora em ambulatórios de alta tecnologia, desperdiçando o recurso do especialista remunerado.
*   **Indicador de Monitoramento:** Taxa de Absenteísmo nas Consultas Especializadas.

### Falhas Internas (Perspectiva Operacional e de Retaguarda)

#### 3. Prontuários Fragmentados e "Apagão" de Informação Clínica
*   **Etapa do Serviço:** Atendimento Médico Especializado.
*   **Problema:** O médico especialista no AME ou Hospital Estadual não tem acesso aos registros médicos da UBS municipal (onde os exames iniciais e sintomas foram registrados) e vice-versa.
*   **Causa Provável:** Desconexão tecnológica crônica entre os sistemas de prontuário eletrônico municipais e os sistemas estaduais das unidades de destino, sem barramento de interoperabilidade efetivo.
*   **Impacto no Cidadão:** O paciente precisa repetir toda a sua história clínica; frequentemente precisa refazer exames laboratoriais simples porque os resultados da UBS não estão disponíveis no sistema do AME.
*   **Consequência Operacional:** Duplicação de custos com exames diagnósticos repetidos desnecessariamente e perda de produtividade do médico especialista, que gasta tempo caçando informações.
*   **Indicador de Monitoramento:** Percentual de Consultas com Prontuário Integrado / Taxa de Redundância de Exames Solicitados.

#### 4. Barreira na Contrarreferência (Ruptura na Linha de Cuidado)
*   **Etapa do Serviço:** Encerramento e Continuidade do Cuidado.
*   **Problema:** Após a consulta, o paciente recebe alta do especialista para continuar o tratamento na UBS, mas a informação da conduta nunca chega formalmente ao médico de família da ponta.
*   **Causa Provável:** A guia de contrarreferência é entregue impressa ao paciente para que ele leve fisicamente à UBS, confiando a ele o papel de mensageiro do sistema de saúde.
*   **Impacto no Cidadão:** Descontinuidade do tratamento, prescrição de medicamentos incompatíveis por falta de comunicação entre os médicos.
*   **Consequência Operacional:** Hiperutilização do sistema especializado por pacientes que poderiam ser manejados na atenção primária se houvesse suporte matricial e matriciamento de equipes.
*   **Indicador de Monitoramento:** Índice de Efetividade da Contrarreferência.

---

## 6. Tabela Completa do Service Blueprint AS-IS

| Etapa da Jornada | Ação do Cidadão | Ponto de Contato | Evidência Física/Digital | Processo de Bastidor | Responsável | Sistema Utilizado | Norma Relacionada | Fail Point Identificado |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Triagem na Atenção Básica** | Relata sintomas em consulta na UBS municipal. | Consultório médico da UBS de origem. | Guia de encaminhamento manual; Prontuário local. | Avaliação da necessidade de densidade tecnológica superior. | Médico Generalista Municipal. | Prontuário Eletrônico Municipal (ou e-SUS). | Art. 196 CF / Lei 8.080 (Integralidade). | Demora crônica no agendamento da consulta básica inicial na UBS. |
| **2. Solicitação da Vaga** | Entrega a guia no balcão e aguarda inserção. | Guichê administrativo/Regulação da UBS. | Protocolo de recebimento de documento impresso. | Digitação e transcrição clínica dos dados do paciente para o sistema estadual. | Operador de Regulação Municipal. | **Plataforma CROSS** | Portaria MS 2/2017 (Regulação). | Erros de digitação e omissão de dados clínicos essenciais que causam recusa da guia. |
| **3. Triagem de Regulação** | Aguarda passivamente em sua residência. | Nenhum contato visível. | Ausente. | Avaliação clínica do pedido com base nos protocolos de priorização de risco. | Médico Regulador do Estado (CROSS). | **Plataforma CROSS** | Diretrizes Técnicas da CROSS / Portaria MS 2/2017. | **Fail Point 1:** Falta de transparência na fila; paciente sem previsão do tempo de espera. |
| **4. Casamento da Oferta** | Aguarda processamento interno da vaga. | Nenhum contato visível. | Ausente. | Vinculação automatizada ou manual da vaga disponibilizada pelo AME/Hospital ao paciente. | Operador do Complexo Regulador. | **Plataforma CROSS** | Resolução SS-SP 44/2021 (Contratos OSS). | Baixa disponibilidade de vagas especializadas injetadas pelas unidades de destino. |
| **5. Comunicação do Agendamento** | Atende o telefone ou recebe aviso por mensagem/ACS. | Chamada telefônica, SMS ou visita do ACS. | Mensagem de SMS ou Ficha CROSS impressa na UBS. | Acionamento de listas de contatos e atualização de status da vaga para "Confirmada". | Central de Atendimento Municipal / ACS. | CROSS / Sistema de Telefonia Local. | Princípio da Eficiência Administrativa. | **Fail Point 2:** Perda da vaga devido a dados cadastrais defasados ou aviso de última hora. |
| **6. Check-In na Unidade** | Viaja até o município polo e apresenta-se no balcão. | Recepção do Ambulatório Especializado (AME/Hospital). | Painel de senhas; Documentos validados. | Conferência cadastral, abertura do atendimento no Prontuário local e ativação de faturamento. | Recepcionista da Unidade Estadual (ou OSS). | Sistema de Gestão Hospitalar Interno (ex: MV). | Regras de Faturamento Ambulatorial SUS (SIA). | Atrasos na fila da recepção misturando fluxos de especialidades distintas. |
| **7. Consulta com Especialista** | Responde à anamnese e passa por exame físico clínico. | Consultório médico da unidade estadual. | Estetoscópio; Computador com prontuário visível. | Registro da evolução clínica, preenchimento de CID-10 e emissão de laudos de cobrança. | Médico Especialista do Estado/OSS. | Sistema de Prontuário Eletrônico Interno. | Código de Ética Médica / Padrões de Faturamento SUS. | **Fail Point 3:** Apagão de informações; médico não vê o histórico da UBS. |
| **8. Desfecho e Encaminhamento** | Retira documentos de saída e orientações na mesa/saída. | Balcão de atendimento pós-consulta ou mesa médica. | Receita médica; Pedidos de exames especializados; Contrarreferência. | Emissão de guias de faturamento SIA (BPA-I/APAC) e registro estatístico de produção. | Médico Especialista / Faturamento Interno. | Sistema de Prontuário / Faturamento SIA-SUS. | Pacto pela Saúde / Diretrizes de Redes de Atenção. | **Fail Point 4:** Paciente sai com pedidos de exames complexos sem saber onde e como agendá-los. |

---

## 7. Diretrizes Estratégicas para Transformação do Serviço

1. **Transparência Ativa da Fila:** Desenvolvimento de interface de consulta para o cidadão (via portal Poupatempo Digital).
2. **Plataforma Omnichannel de Confirmação:** Substituição progressiva de chamadas frias por sistemas de mensageria automatizada interativa.
3. **Barramento de Interoperabilidade em Saúde:** Implementação de um barramento de dados clínico estadual baseado no padrão HL7 / FHIR.
4. **Agendamento Integrado de Exames Correlatos:** O cidadão que necessita de exames recomendados deve sair da unidade com estes exames já agendados.

---
**Fontes e Referências Documentais Ospeciais:**
* Secretaria de Estado da Saúde de São Paulo (SES-SP) - Diretrizes CROSS
* Ministério da Saúde - Política Nacional de Regulação do SUS
* Legislação Federal do SUS (Leis 8.080/90 e 8.142/90)
