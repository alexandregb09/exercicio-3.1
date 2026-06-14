Quero elaborar conceitualmente um Service Blueprint AS-IS da jornada “Consulta Médica na Secretaria de Estado da Saúde de São Paulo (SES-SP)”, considerando como contexto o artefato @B\_relatorio\_assistente\_v3.md  e seguindo a metodologia de Service Blueprint de Shostack, com as camadas Evidências Físicas, Ações do Cidadão, Frontstage, Backstage e Processos de Suporte, incluindo as linhas divisórias (interação, visibilidade e interação interna) e a identificação dos fail points da jornada, como gargalos, falhas de comunicação, problemas operacionais, integrações sistêmicas e dificuldades enfrentadas pelo cidadão.

Read B\_relatorio\_assistente\_v3.md (229 lines)



I've read the report. It's thorough — 8 macro-steps, 4 fail points, Shostack layers referenced throughout. Now let me drill into the design decisions.



Question 1 — Journey boundaries:



The report currently starts at "patient arrives at UBS" and ends at "patient leaves AME with prescriptions." But Shostack's methodology typically captures the full experiential arc.



Should the blueprint start earlier — at the moment the citizen perceives a health need (before ever reaching the UBS), and end later — after the patient attempts to schedule the exams ordered by the specialist?



My recommendation: yes, extend both ends. The pre-UBS moment (deciding whether/how to seek care) and the post-consultation dead-end (holding exam ordwhere the most emotionally significantfriction lives — and both are currently invisible in the blueprint. Cutting the journey short understates the actual citizen experience.



Where do you draw the journey boundaries?



✻ Cooked for 26s



❯ A definição das fronteiras da jornada é um pe do \*\*Service Blueprint AS-IS\*\*, poisdetermina quais experiências, dores e processos serão considerados. Pela metodologia de \*\*Service Blueprint de Shostack\*\*, a recomendação é que o blueprintto de experiência do usuário\*\*, e não apenaso momento em que ele entra fisicamente em uma unidade de saúde.



&#x20; Portanto, para o serviço de \*\*Consulta Médica na Secretaria de Estado da Saúde de São Paulo (SES-SP)\*\*, eu definiria

&#x20; as fronteiras da jornada da seguinte forma:



&#x20; ## Limite inicial da jornada: antes da UBS (úde)



&#x20; O blueprint deve iniciar quando o cidadão \*\*aúde\*\*, antes de procurar qualquer unidade.



&#x20; Esse momento é essencial porque envolve deciciam todo o restante do serviço.



&#x20; A jornada começa com:



&#x20; Esse momento é essencial porque envolve deciciam todo o restante do serviço.



&#x20; A jornada começa com:



&#x20; \*\*1. Percepção da necessidade de cuidado\*\*



&#x20; Exemplos:



&#x20; \* cidadão percebe sintomas;

&#x20; \* recebe orientação informal;

&#x20; \* identifica piora de uma condição existente

&#x20; \* precisa acompanhar uma doença;

&#x20; \* recebe recomendação para procurar atendime



&#x20; Nesse ponto surgem perguntas importantes:



&#x20; \* O cidadão sabe onde procurar ajuda?

&#x20; \* Ele conhece a diferença entre UBS, AMA, hospital, AME ou pronto atendimento?

&#x20; \* Ele consegue identificar se precisa de atezado?

&#x20; \* Ele tem acesso a informações claras?



&#x20; ---



&#x20; ## Etapa anterior à UBS: busca e decisão de acesso



&#x20; Antes da chegada à UBS existe uma etapa frequentemente invisível:



&#x20; \*\*2. Busca por informação e escolha do caminho\*\*



&#x20; Ações do cidadão:



&#x20; \* pesquisa na internet;

&#x20; \* consulta familiares;

&#x20; \* procura informações em aplicativos ou canais oficiais;

&#x20; \* liga para serviços públicos;

&#x20; \* tenta entender como acessar um especialista.



&#x20; Evidências físicas/digitais:



&#x20; \* tenta entender como acessar um especialista.



&#x20; Evidências físicas/digitais:



&#x20; \* sites institucionais;

&#x20; \* aplicativos;

&#x20; \* telefones;

&#x20; \* orientações recebidas;

&#x20; \* documentos necessários.



&#x20; Possíveis fail points:



&#x20; \* informação fragmentada;

&#x20; \* desconhecimento do fluxo SUS;

&#x20; \* encaminhamento incorreto;

&#x20; \* deslocamento desnecessário.



&#x20; Essa etapa deve estar no blueprint porque elercepção de qualidade do serviço.



&#x20; ---



&#x20; # Fim da jornada: não deve terminar na saída



&#x20; O encerramento em:



&#x20; > "Paciente deixa o AME com prescrição e sol



&#x20; é insuficiente, porque o cidadão ainda não cdo.



&#x20; A consulta médica é apenas uma etapa dentro ver uma necessidade de saúde\*\*.



&#x20; O correto é estender o blueprint até a efeti



&#x20; ---



&#x20; ## Limite final recomendado: após a consulta



&#x20; A jornada deve continuar até:



&#x20; \*\*3. Pós-consulta e continuidade do cuidado\*



&#x20; Incluindo:



&#x20; ### Recebimento das orientações



&#x20; O cidadão precisa compreender:



&#x20; \* diagnóstico ou hipótese diagnóstica;

&#x20; \* tratamento indicado;

&#x20; \* próximos passos;

&#x20; \* necessidade de exames;

&#x20; \* retorno.



&#x20; Fail points:



&#x20; \* linguagem técnica;

&#x20; \* orientação incompleta;

&#x20; \* falta de clareza sobre responsabilidades.



&#x20; ---



&#x20; ### Agendamento dos exames solicitados



&#x20; Essa é uma etapa crítica.



&#x20; O blueprint deve mapear:



&#x20; \* quem agenda;

&#x20; \* onde agenda;

&#x20; \* se existe encaminhamento automático;

&#x20; \* se o cidadão precisa retornar à UBS;

&#x20; \* se existe fila;

&#x20; \* se há comunicação sobre disponibilidade.



&#x20; Processos de bastidor:



&#x20; \* regulação;

&#x20; \* autorização;

&#x20; \* distribuição de vagas;

&#x20; \* integração entre sistemas;

&#x20; \* gestão da oferta.



&#x20; Possíveis falhas:



&#x20; \* cidadão recebe pedido de exame, mas não sabe onde realizar;

&#x20; \* pedido perde validade;

&#x20; \* demora excessiva;

&#x20; \* ausência de vaga;

&#x20; \* falta de integração entre unidades.



&#x20; ---



&#x20; ### Realização dos exames



&#x20; A jornada só termina quando:



&#x20; \* exame é realizado;

&#x20; \* resultado está disponível;

&#x20; \* médico consegue avaliar;

&#x20; \* tratamento continua.



&#x20; ---



&#x20; # Fronteira final proposta do Service Bluepr



&#x20; Eu recomendaria representar assim:



&#x20; \*\*INÍCIO\*\*



&#x20; > Cidadão percebe uma necessidade de saúde

&#x20; > ↓

&#x20; > Busca informação e decide procurar atendim

&#x20; > ↓

&#x20; > Acessa a rede SUS

&#x20; > ↓

&#x20; > Passa pela UBS

&#x20; > ↓

&#x20; > É encaminhado para atenção especializada

&#x20; > ↓

&#x20; > Regulação/agendamento

&#x20; > ↓

&#x20; > Consulta no AME ou unidade especializada

&#x20; > ↓

&#x20; > Recebe diagnóstico/orientação/prescrição

&#x20; > ↓

&#x20; > Agenda e realiza exames solicitados

&#x20; > ↓

&#x20; > Retorna para continuidade do cuidado



&#x20; \*\*FIM\*\*



&#x20; > Cidadão consegue executar o plano de cuida



&#x20; ---



&#x20; # Justificativa metodológica



&#x20; Essa delimitação é mais adequada porque:



&#x20; 1. \*\*Captura a experiência real do cidadão\*\*



&#x20; A percepção do serviço começa antes do prime quando a necessidade é resolvida.



&#x20; 2. \*\*Revela falhas sistêmicas\*\*



&#x20; Muitos problemas não estão dentro da consult:



&#x20; \* cidadão → UBS;

&#x20; \* UBS → regulação;

&#x20; \* regulação → especialista;

&#x20; \* especialista → exames;

&#x20; \* exames → continuidade do tratamento.



&#x20; 3. \*\*Permite identificar falhas invisíveis\*\*



&#x20; Um blueprint limitado à unidade mostra apenamas não mostra:



&#x20; \* ansiedade da espera;

&#x20; \* dificuldade de acesso;

&#x20; \* perda de informação;

&#x20; \* barreiras administrativas.



&#x20; ---



&#x20; Portanto, a fronteira recomendada para o \*\*Service Blueprint AS-IS da Consulta Médica SES-SP\*\* é:



&#x20; \*\*"Da percepção da necessidade de saúde pelo cidadão até a conclusão do cuidado após a consulta especializada e

&#x20; realização dos encaminhamentos/exames necess



&#x20; Esse recorte representa melhor a jornada compontos de melhoria reais do serviço público.





Boa definição — limites claros, justificativa metodológica sólida. Isso expande o blueprint de 8 para \~13 etapas.



Pergunta 2 — Granularidade das etapas:



Com os novos limites (percepção da necessidade → realização dos exames), o blueprint pode ser estruturado em dois níveis:

&#x20;                                                                                                                 - Opção A — Macro-etapas consolidadas (\~5): Regulação / Atendimento Especializado /Pós-consulta. Mais legível, perde detalhe nas transições.                                                         - Opção B — Micro-etapas detalhadas (\~13): C coluna separada. Mais fiel à metodologiaShostack, mas pesado para apresentar em formato tabular.                                                          - Opção C — Hierarquia em dois níveis: Macrocro-etapas dentro de cada um. Padrão adotadoem blueprints institucionais complexos como os do Nesta/UK Government Design.                                     

Minha recomendação: Opção C. O serviço tem atores e sistemas demais para achatar em 5 colunas, mas 13 colunas     paralelas tornam o blueprint ilegível. A hierva a rastreabilidade metodológica semsacrificar a clareza.                                                                                             

Qual nível de granularidade você quer adotar?                                                                     

✻ Crunched for 22s                                                                                                  

❯ Para o \*\*Service Blueprint AS-IS da Consulta Médica na SES-SP\*\*, adotaria a \*\*Opção C — Hierarquia em dois níveis (macro + micro-etapas)\*\*.



&#x20; A justificativa é que esse serviço possui calexidade operacional\*\*, com múltiplos atores, níveis de atenção, sistemas e pontos de transferência de responsabilidade. Um blueprint com apenas 5 macroetapas perderia justamente os momentos onde surgem xperiência; por outro lado, 13 colunastotalmente independentes tornariam a leitura difícil para gestores e equipes.                                        

&#x20; A estrutura recomendada seria:                                                                                       

&#x20; # Nível 1 — Macroetapas (visão executiva)                                                                            

&#x20; Organizar o blueprint em 5 grandes fases:                                                                            

&#x20; | Macroetapa                                    | Objetivo                                                                    |

&#x20; | --------------------------------------------- |                                                                     ----------------------------------------------- |

&#x20; | 1. Pré-acesso e decisão do cidadão            | Identificar necessidade, buscar informação e escolher o caminho de  cuidado  |

&#x20; | 2. Entrada na Atenção Primária (APS/UBS)      | Primeiro contato, avaliação inicial e encaminhamento                        |

&#x20; | 3. Regulação e acesso à atenção especializada | Processamento do encaminhamento, fila, agendamento e acesso ao

&#x20; especialista |

&#x20; | 4. Atendimento especializado                  | Consulta médica, diagnóstico, conduta e definição do plano

&#x20; terapêutico      |

&#x20; | 5. Pós-consulta e continuidade do cuidado     | Exames, retorno, acompanhamento e conclusão do ciclo assistencial

&#x20;         |



&#x20; ---



&#x20; # Nível 2 — Microetapas dentro de cada macro



&#x20; ## 1. Pré-acesso e decisão do cidadão



&#x20; Microetapas:



&#x20; 1.1 Percepção do problema de saúde

&#x20; 1.2 Busca de informações sobre onde procurar atendimento

&#x20; 1.3 Decisão pelo serviço adequado

&#x20; 1.4 Preparação para o atendimento (documentos, deslocamento, cadastro)



&#x20; ---



&#x20; ## 2. Entrada na Atenção Primária (UBS)





&#x20; Microetapas:



&#x20; 2.1 Chegada à UBS

&#x20; 2.2 Acolhimento e triagem inicial

&#x20; 2.3 Consulta na atenção básica

&#x20; 2.4 Identificação da necessidade de especialista

&#x20; 2.5 Emissão do encaminhamento



&#x20; ---



&#x20; ## 3. Regulação e acesso à atenção especiali



&#x20; Microetapas:



&#x20; 3.1 Registro da solicitação

&#x20; 3.2 Avaliação da necessidade pela regulação

&#x20; 3.3 Inserção em fila ou disponibilidade de v

&#x20; 3.4 Agendamento da consulta especializada

&#x20; 3.5 Comunicação ao cidadão



&#x20; ---



&#x20; ## 4. Atendimento especializado



&#x20; Microetapas:



&#x20; 4.1 Chegada ao ambulatório/AME

&#x20; 4.2 Recepção e confirmação do atendimento

&#x20; 4.3 Consulta médica especializada

&#x20; 4.4 Solicitação de exames ou procedimentos

&#x20; 4.5 Orientações e definição de próximos pass



&#x20; ---



&#x20; ## 5. Pós-consulta e continuidade do cuidado



&#x20; Microetapas:



&#x20; 5.1 Entendimento das orientações recebidas

&#x20; 5.2 Tentativa de agendamento dos exames

&#x20; 5.3 Realização dos exames solicitados

&#x20; 5.4 Retorno ao especialista ou UBS

&#x20; 5.5 Continuidade do tratamento



&#x20; ---



&#x20; # Aplicação no blueprint Shostack



&#x20; A tabela principal ficaria organizada assim:



&#x20; | Macroetapa | Microetapa | Evidências físicstage | Backstage | Sistemas | Normas | FailPoints |

&#x20; | ---------- | ---------- | --------------------- | --------- | -------- | ------ |----------- |



&#x20; Dessa forma, conseguimos manter:



&#x20; \* \*\*visão estratégica\*\* para Secretarias, direção e gestores;

&#x20; \* \*\*detalhamento operacional\*\* para equipes

&#x20; \* \*\*rastreabilidade\*\* dos pontos de falha;

&#x20; \* conexão entre experiência do cidadão e ope



&#x20; Também permite futuramente criar dois produt



&#x20; 1. \*\*Blueprint executivo\*\* → somente macroet

&#x20; 2. \*\*Blueprint operacional\*\* → microetapas completas (melhoria de processos).



&#x20; Portanto, a granularidade adotada será:



&#x20; \*\*Macroetapas como estrutura principal + microetapas como unidades de análise do Service Blueprint AS-IS.\*\*





Estrutura hierárquica sólida e bem justifica



Pergunta 3 — Definição das camadas e das lin



Você mencionou as camadas clássicas de Shostes do Cidadão, Frontstage, Backstage eProcessos de Suporte. Mas a tabela que você propôs tem colunas diferentes: Frontstage | Backstage | Sistemas | Normas.



O problema específico deste serviço: a CROSS é completamente invisível ao cidadão, mas é o ator central da macroetapa

3 inteira. Em um blueprint privado clássico, do funcionário para o cliente. Aqui, oregulador estadual nunca aparece para o paciente — nem fisicamente, nem digitalmente.



Você tem três opções para tratar isso:



\- Opção A — Shostack puro: Frontstage = tudo que o cidadão vê/ouve (UBS, AME, SMS). CROSS vai inteiramente para

Backstage. A macroetapa 3 fica quase sem frote correto, mas pode parecer vazio.

\- Opção B — Adaptação institucional: Criar uma sublinha dentro do Backstage separando "Bastidores municipais" (UBS

operacional) de "Bastidores estaduais" (CROSmas não é Shostack padrão.

\- Opção C — Linha de interação interna explícita: Usar a terceira linha divisória de Shostack (interação interna) para

separar CROSS/Estado dos processos de suport). Isso resolve o problema sem deformar ametodologia.



Minha recomendação: Opção C. A linha de interação interna existe exatamente para separar atores humanos de retaguarda

dos sistemas tecnológicos de suporte — que éOSS (pessoas) vs. SIRESP/SIA-SUS (sistemas).Usar as três linhas de Shostack fielmente também torna o blueprint academicamente defensável.



Como você quer estruturar as camadas e as linhas divisórias?



✻ Crunched for 24s



❯ Para este caso, adotaria a \*\*Opção C — Linha de interação interna explícita\*\*, mantendo a lógica original de

&#x20; \*\*Shostack\*\*, mas adaptando a representação ço público de saúde.



&#x20; A razão é que o serviço de \*\*Consulta Médicao simples de balcão: ele é uma redesociotécnica, em que existem atores humanos, regras, sistemas e fluxos decisórios que não aparecem diretamente para o

&#x20; cidadão. A CROSS (Central de Regulação de Ofé um exemplo clássico de \*\*ator de backstage com forte influência na experiência\*\*, mas sem ponto de contato direto.



&#x20; A estrutura do blueprint ficaria assim:



&#x20; # Service Blueprint AS-IS — Consulta Médica SES-SP



&#x20; ## 1. Evidências Físicas (Physical Evidence)



&#x20; \*\*Tudo que o cidadão consegue perceber como evidência do serviço\*\*



&#x20; Exemplos:





&#x20; \* UBS;

&#x20; \* recepção;

&#x20; \* ambiente físico;

&#x20; \* cartão SUS;

&#x20; \* encaminhamento médico;

&#x20; \* protocolo;

&#x20; \* comprovante de agendamento;

&#x20; \* SMS/telefone de confirmação;

&#x20; \* portal/aplicativo;

&#x20; \* AME;

&#x20; \* receita;

&#x20; \* solicitação de exame;

&#x20; \* resultado de exame.



&#x20; ---



&#x20; ## 2. Linha de interação (Interaction Line)



&#x20; Representa o limite entre o cidadão e a orga



&#x20; Acima da linha:



&#x20; \*\*Cidadão\*\*



&#x20; Ações:



&#x20; \* procura atendimento;

&#x20; \* solicita consulta;

&#x20; \* entrega documentos;

&#x20; \* aguarda;

&#x20; \* recebe informações;

&#x20; \* comparece à consulta;

&#x20; \* tenta realizar exames.



&#x20; Abaixo da linha:



&#x20; \*\*Organização prestadora\*\*



&#x20; Começa o serviço visível.

&#x20; Começa o serviço visível.



&#x20; ---



&#x20; # 3. Frontstage (ações visíveis ao cidadão)



&#x20; Aqui entra apenas aquilo que o cidadão vê ou percebe.



&#x20; Exemplos:



&#x20; ## UBS



&#x20; \* recepcionista orienta;

&#x20; \* profissional acolhe;

&#x20; \* médico avalia;

&#x20; \* equipe registra encaminhamento.



&#x20; ## Agendamento



&#x20; \* cidadão recebe aviso;

&#x20; \* unidade informa data/local;

&#x20; \* atendimento confirma consulta.



&#x20; ## AME



&#x20; \* recepção atende;

&#x20; \* enfermagem realiza acolhimento;

&#x20; \* médico realiza consulta;

&#x20; \* profissional orienta sobre exames.



&#x20; A CROSS \*\*não aparece aqui\*\*.



&#x20; Isso preserva o conceito original de Shostack:



&#x20; > Frontstage é aquilo que acontece na linha de frente do serviço.



&#x20; ---



&#x20; # 4. Linha de visibilidade



&#x20; Essa linha separa:



&#x20; \*\*o que o cidadão vê\*\*

&#x20; de

&#x20; \*\*o que acontece sem ele perceber\*\*



&#x20; Aqui está o ponto crítico do serviço.



&#x20; ---



&#x20; # 5. Backstage (ações invisíveis ao cidadão)



&#x20; Dividiria em dois níveis:



&#x20; ## 5.1 Backstage operacional (unidades)



&#x20; Atividades internas próximas ao cidadão:



&#x20; \* cadastro;

&#x20; \* conferência documental;

&#x20; \* lançamento de encaminhamento;

&#x20; \* atualização de prontuário;

&#x20; \* preparação da agenda;

&#x20; \* organização da fila local.



&#x20; Atores:



&#x20; \* UBS;

&#x20; \* ambulatórios;

&#x20; \* equipes administrativas.



&#x20; ---



&#x20; ## 5.2 Backstage regulatório estadual



&#x20; Aqui entra a CROSS.



&#x20; Atividades:



&#x20; \* análise da solicitação;

&#x20; \* classificação de prioridade;

&#x20; \* regulação da demanda;

&#x20; \* gestão da oferta;

&#x20; \* direcionamento para unidade executante;

&#x20; \* controle das filas;

&#x20; \* autorização conforme critérios.



&#x20; Atores:



&#x20; \* CROSS;

&#x20; \* gestores estaduais;

&#x20; \* coordenadorias.



&#x20; Esse detalhamento evita o erro de tratar a rque a CROSS é uma capacidade institucionalhumana e decisória.



&#x20; ---



&#x20; # 6. Linha de interação interna (Internal Interaction Line)



&#x20; Esta é a adaptação mais importante.



&#x20; Ela separa:



&#x20; \*\*Backstage humano\*\*

&#x20; de

&#x20; \*\*Processos de suporte tecnológico e institucional\*\*



&#x20; Exatamente onde entram:



&#x20; ## Processos de suporte



&#x20; Sistemas:



&#x20; \* SIRESP;

&#x20; \* SIA/SUS;

&#x20; \* CNES;

&#x20; \* sistemas de regulação;

&#x20; \* prontuário eletrônico;

&#x20; \* bases cadastrais.



&#x20; Processos:



&#x20; \* integração de dados;

&#x20; \* validações automáticas;

&#x20; \* interoperabilidade;

&#x20; \* relatórios;

&#x20; \* indicadores;

&#x20; \* auditoria.



&#x20; ---



&#x20; A estrutura final ficaria:



&#x20; ```

&#x20; EVIDÊNCIAS FÍSICAS

&#x20;         │

&#x20;         │

&#x20; CIDADÃO

&#x20; (Ações do usuário)

&#x20;         │

&#x20; ──── Linha de interação ────

&#x20;         │

&#x20; FRONTSTAGE

&#x20; (aquilo que o cidadão vê)

&#x20;         │

&#x20; ──── Linha de visibilidade ────

&#x20;         │

&#x20; BACKSTAGE OPERACIONAL

&#x20; (UBS / AME / equipes)

&#x20;         │

&#x20; BACKSTAGE REGULATÓRIO

&#x20; (CROSS / gestores)

&#x20;         │

&#x20; ──── Linha de interação interna ────

&#x20;         │

&#x20; PROCESSOS DE SUPORTE

&#x20; (SIRESP / SIA-SUS / sistemas / regras)

&#x20; ```



&#x20; ---



&#x20; Minha escolha final:



&#x20; \*\*Camadas:\*\*



&#x20; 1. Evidências físicas

&#x20; 2. Ações do cidadão

&#x20; 3. Frontstage

&#x20; 4. Backstage operacional

&#x20; 5. Backstage regulatório (CROSS)

&#x20; 6. Processos de suporte



&#x20; \*\*Linhas divisórias:\*\*



&#x20; \* Linha de interação cidadão–serviço;

&#x20; \* Linha de visibilidade;

&#x20; \* Linha de interação interna.



&#x20; Isso mantém fidelidade metodológica a Shostaenta corretamente um serviço públicoregulado, onde o cidadão experimenta o resultado de decisões tomadas por atores que ele nunca vê.





Excelente. A separação entre backstage operaio é a decisão mais defensávelmetodologicamente — resolve o problema da CROSS sem forçar uma categoria que não existe no Shostack original.



Pergunta 4 — Fail points: identificação, quantidade e classificação:



O relatório atual mapeia 4 fail points, todos dentro das macroetapas 2–4 (UBS até saída do AME). Com os novos limites

da jornada, há pelo menos 3 fail points novo



\- Pré-acesso: Cidadão não sabe distinguir UB— chega no lugar errado e é redirecionado(fail point de orientação/informação).

\- Pós-consulta: Cidadão sai com pedido de ex"vaga" que fechou o Fail Point 4 originalagora se estende para um ciclo completo sem resolução.

\- Contrarreferência: A ruptura no retorno aolatório como FP4, mas termina antes de mapearo que acontece quando o paciente volta sem resultado e sem continuidade.



A questão é como classificar os fail points dentro do blueprint. Você tem três abordagens:



\- Opção A — Notação simples: Marca ⚠ na célula correspondente da tabela com descrição inline. Mais limpo, menos

analítico.

\- Opção B — Tipologia por categoria: Classifica cada fail point por tipo — falha de informação, falha de integração

sistêmica, falha de comunicação, falha operaada e priorização.

\- Opção C — Matriz de severidade: Cada fail point recebe impacto (cidadão) × frequência (operacional). Permite

priorizar intervenções TO-BE com base em evi



Minha recomendação: Opção B como estrutura bicional. Tipologia por categoria é necessáriapara análise diagnóstica; a matriz de severidade é necessária se o blueprint vai alimentar um plano de transformação

TO-BE. Se o produto final for conceitual/acate.



Quantos fail points você quer mapear e como



✻ Crunched for 26s



❯

&#x20; ───────────────────────────────────────────────────────────



Parece que a resposta ficou em branco. Você quer compartilhar sua definição sobre os fail points, ou prefere que eu

avance com a recomendação (Opção B + C) e si



✻ Cooked for 7s



❯ Para o \*\*Service Blueprint AS-IS da Consultama combinação de \*\*Opção B + Opção C\*\*, comuma adaptação: primeiro construir a \*\*tipologia diagnóstica dos fail points\*\* e, em seguida, aplicar uma \*\*matriz de

&#x20; severidade\*\* para priorização futura no dese



&#x20; Apenas marcar ⚠ na tabela seria insuficienteplexo, porque o objetivo do blueprint não éapenas localizar problemas, mas entender \*\*natureza da falha, causa sistêmica e impacto na jornada do cidadão\*\*.



&#x20; ## Quantidade recomendada



&#x20; Eu ampliaria o mapeamento de \*\*4 para aproximadamente 10–12 fail points\*\*, distribuídos ao longo de toda a jornada.



&#x20; Motivo:



&#x20; Com os novos limites (percepção da necessidade → realização dos exames/continuidade), os problemas deixam de estar

&#x20; concentrados apenas na UBS/AME e passam a apviço.



&#x20; Proposta:

&#x20; Proposta:                                                                                                            

&#x20; | ID   | Macroetapa                | Fail Point                                                                                                                |

&#x20; | ---- | ------------------------- | -------------------------------------------------------------------------------------------------------------------------- |

&#x20; | FP01 | Pré-acesso                | Cidadão não sabe qual porta de entrada utilizar (UBS, AMA, AME, pronto

&#x20; atendimento) e inicia a jornada no local ina

&#x20; | FP02 | Pré-acesso                | Informação insuficiente sobre documentos, fluxos e critérios de acesso

&#x20;                                           |

&#x20; | FP03 | APS/UBS                   | Dificuldade para conseguir avaliação inicial ou encaminhamento adequado

&#x20;                                           |

&#x20; | FP04 | APS/Regulação             | Encaminhamento incompleto ou com informações insuficientes para regulação

&#x20;                                           |

&#x20; | FP05 | Regulação                 | Tempo de espera elevado ou ausência de transparência sobre posição na fila

&#x20;                                           |

&#x20; | FP06 | Regulação/Agendamento     | Existência de vaga sem comunicação efetiva ao cidadão ou perda do agendamento

&#x20;                                           |

&#x20; | FP07 | Atendimento especializado | Consulta ocorre sem integração adequada do histórico clínico ou informações

&#x20; anteriores

&#x20; | FP08 | Pós-consulta              | Paciente recebe solicitação de exame, mas não existe fluxo claro para

&#x20; agendamento

&#x20; | FP09 | Pós-consulta              | Exame realizado, mas resultado não chega ao profissional responsável ou ao

&#x20; cidadão

&#x20; | FP10 | Contrarreferência         | Falha na comunicação entre especialista e atenção primária para continuidade do

&#x20; cuidado                                    |

&#x20; | FP11 | Continuidade              | Paciente retorna sem resultado, sem acompanhamento definido ou sem responsável

&#x20; pelo próximo passo

&#x20; | FP12 | Sistema                   | Falta de integração entre sistemas gera retrabalho, perda de informação ou

&#x20; atraso



&#x20; ---



&#x20; # Tipologia dos Fail Points (Opção B)



&#x20; Cada falha receberia uma classificação:



&#x20; | Categoria               | Descrição                        |

&#x20; | ----------------------- | ------------------------------------------------------------ |

&#x20; | Informação              | Falha de orientaento do cidadão  |



&#x20; | Categoria               | Descrição                        |

&#x20; | ----------------------- | ------------------------------------------------------------ |

&#x20; | Informação              | Falha de orientaento do cidadão  |

&#x20; | Acesso                  | Barreiras para entrar ou avançar no serviço                  |

&#x20; | Regulação               | Problemas de fil disponibilidade |

&#x20; | Comunicação             | Rupturas entre cidadão e unidades                            |

&#x20; | Integração sistêmica    | Sistemas que nãoho               |

&#x20; | Operacional             | Problemas de execução interna                                |

&#x20; | Continuidade do cuidado | Falhas após consção              |



&#x20; Exemplo:



&#x20; \*\*FP08 — Pedido de exame sem agendamento\*\*



&#x20; Categoria:



&#x20; \* Continuidade do cuidado;

&#x20; \* Comunicação;

&#x20; \* Operacional.



&#x20; ---



&#x20; # Como aparecer no Blueprint



&#x20; Na tabela principal eu não colocaria a descrir.



&#x20; Usaria:



&#x20; | Etapa        | Ação cidadão        | Front| Backstage                 | Fail Point |

&#x20; | ------------ | ------------------- | -------------------------------- | ------------------------- | ---------- |

&#x20; | Pós-consulta | Tenta agendar exame | Orien| Regulação/gestão de vagas | ⚠ FP08     |



&#x20; E criaria uma tabela complementar:



&#x20; | ID   | Falha                           | C              | Impacto    |

&#x20; | ---- | ------------------------------- | -------------- |-------------------------------- |

&#x20; | FP08 | Pedido de exame sem agendamento | Cuxo integrado | Alta espera, abandono docuidado |



&#x20; ---



&#x20; # Matriz de severidade (para fase TO-BE)



&#x20; Depois do AS-IS, aplicaria:



&#x20; \*\*Impacto no cidadão × Frequência operacional\*\*



&#x20; Exemplo:



&#x20; | Fail Point                         | Impacto | Frequência | Prioridade |

&#x20; | ---------------------------------- | ----- |

&#x20; | FP08 — exame sem agendamento       | Alto    | Alta       | Crítico    |

&#x20; | FP05 — fila sem transparência      | Alto  |

&#x20; | FP01 — porta de entrada errada     | Médio   | Média      | Moderado   |

&#x20; | FP07 — falta de integração clínica | Alto  |



&#x20; ---



&#x20; ## Estrutura final escolhida



&#x20; Portanto:



&#x20; \* \*\*Blueprint AS-IS:\*\* 10–12 fail points;

&#x20; \* \*\*Representação:\*\* ID do fail point na tabela + catálogo analítico separado;

&#x20; \* \*\*Classificação:\*\* Tipologia por categoria

&#x20; \* \*\*Priorização futura:\*\* Matriz impacto × frequência (Opção C).



&#x20; Isso mantém o blueprint metodologicamente fiel e transforma o diagnóstico em insumo para redesenho do serviço

&#x20; (TO-BE).





Framework de fail points bem construído — 12 pontos com tipologia e matriz de severidade separada da tabela principal

é a escolha certa para não poluir o blueprin



Pergunta 5 — Integração das normas jurídicas



O relatório dedica uma seção inteira a normaeto Estadual 56.061/2010, STF Tema 698, etc.). Você também incluiu uma coluna "Normas" na tabela proposta anteriormente.



O problema: Shostack não tem uma camada de normas. Normas jurídicas não são evidência física, não são ação do cidadão,

não são ação de frontstage ou backstage — elmoldam o design do processo, não elementos do processo em si.



Você tem três opções para tratar isso:



\- Opção A — Coluna autônoma "Norma Relacionada": Mantém como está no relatório atual. Vantagem: rastreabilidade

jurídica imediata. Problema: cria uma colunace ao blueprint Shostack — é anotação, nãocamada.

\- Opção B — Embutir nas células de Processoserna um processo aparece como sub-elementodaquele processo (ex: "Classificação de risco P1–P4 \[Portaria MS 2/2017]"). Mais fiel metodologicamente, menos

rastreável.

\- Opção C — Artefato separado: O blueprint fica limpo com as 6 camadas; as normas vivem em uma tabela de referência

cruzada independente que mapeia "etapa → norentos regulatórios complexos costumam fazer.



Minha recomendação: Opção C. O blueprint já e normas aumenta a carga cognitiva semadicionar análise — ela simplesmente referencia o que já está documentado na Seção 6 do relatório. Separar normas em

tabela cruzada permite citar o Tema 698 do Se merece, sem comprimir isso numa célula.



Como você quer tratar os normativos jurídico



✻ Cogitated for 31s



❯ Para o \*\*Service Blueprint AS-IS da Consultama combinação de \*\*Opção B + Opção C\*\*, comuma adaptação: primeiro construir a \*\*tipologia diagnóstica dos fail points\*\* e, em seguida, aplicar uma \*\*matriz de

&#x20; severidade\*\* para priorização futura no dese



&#x20; Apenas marcar ⚠ na tabela seria insuficienteplexo, porque o objetivo do blueprint não éapenas localizar problemas, mas entender \*\*natureza da falha, causa sistêmica e impacto na jornada do cidadão\*\*.



&#x20; ## Quantidade recomendada



&#x20; Eu ampliaria o mapeamento de \*\*4 para aproximadamente 10–12 fail points\*\*, distribuídos ao longo de toda a jornada.



&#x20; Motivo:



&#x20; Com os novos limites (percepção da necessidade → realização dos exames/continuidade), os problemas deixam de estar

&#x20; concentrados apenas na UBS/AME e passam a apviço.



&#x20; Proposta:



&#x20; | ID   | Macroetapa                | Fail Po                                           |

&#x20; | ---- | ------------------------- | ---------------------------------------------------------------------------------------------- |

&#x20; | FP01 | Pré-acesso                | Cidadãoada utilizar (UBS, AMA, AME, prontoatendimento) e inicia a jornada no local inadequado |

&#x20; | FP02 | Pré-acesso                | Informaentos, fluxos e critérios de acesso                                           |

&#x20; | FP03 | APS/UBS                   | Dificulo inicial ou encaminhamento adequado                                           |

&#x20; | FP04 | APS/Regulação             | Encaminformações insuficientes para regulação                                           |

&#x20; | FP05 | Regulação                 | Tempo d de transparência sobre posição na fila                                           |

&#x20; | FP06 | Regulação/Agendamento     | Existênefetiva ao cidadão ou perda do agendamento                                           |

&#x20; | FP07 | Atendimento especializado | Consultuada do histórico clínico ou informaçõesanteriores                                     |

&#x20; | FP08 | Pós-consulta              | Paciente, mas não existe fluxo claro paraagendamento                                          |

&#x20; | FP09 | Pós-consulta              | Exame rchega ao profissional responsável ou aocidadão                                         |

&#x20; | FP10 | Contrarreferência         | Falha nista e atenção primária para continuidade docuidado                                    |

&#x20; | FP11 | Continuidade              | Pacient acompanhamento definido ou sem responsávelpelo próximo passo                          |

&#x20; | FP12 | Sistema                   | Falta dgera retrabalho, perda de informação ouatraso                                          |



&#x20; ---



&#x20; # Tipologia dos Fail Points (Opção B)



&#x20; Cada falha receberia uma classificação:



&#x20; | Categoria               | Descrição                                                    |

&#x20; | ----------------------- | -------------------------------- |atendimento) e inicia a jornada no local inadequado |

&#x20; | FP02 | Pré-acesso                | Informaentos, fluxos e critérios de acesso                                           |

&#x20; | FP03 | APS/UBS                   | Dificulo inicial ou encaminhamento adequado                                           |

&#x20; | FP04 | APS/Regulação             | Encaminformações insuficientes para regulação                                           |

&#x20; | FP05 | Regulação                 | Tempo d de transparência sobre posição na fila                                           |

&#x20; | FP06 | Regulação/Agendamento     | Existênefetiva ao cidadão ou perda do agendamento                                           |

&#x20; | FP07 | Atendimento especializado | Consultuada do histórico clínico ou informaçõesanteriores                                     |

&#x20; | FP08 | Pós-consulta              | Paciente, mas não existe fluxo claro paraagendamento                                          |

&#x20; | FP09 | Pós-consulta              | Exame rchega ao profissional responsável ou aocidadão                                         |

&#x20; | FP10 | Contrarreferência         | Falha nista e atenção primária para continuidade docuidado                                    |

&#x20; | FP11 | Continuidade              | Pacient acompanhamento definido ou sem responsávelpelo próximo passo                          |

&#x20; | FP12 | Sistema                   | Falta dgera retrabalho, perda de informação ouatraso                                          |



&#x20; ---



&#x20; # Tipologia dos Fail Points (Opção B)



&#x20; Cada falha receberia uma classificação:



&#x20; | Categoria               | Descrição                                                    |

&#x20; | ----------------------- | -------------------------------- |

&#x20; | Informação              | Falha de orientação, comunicação ou entendimento do cidadão  |

&#x20; | Acesso                  | Barreiras para e                 |

&#x20; | Regulação               | Problemas de fila, critérios, priorização ou disponibilidade |

&#x20; | Comunicação             | Rupturas entre c                 |

&#x20; | Integração sistêmica    | Sistemas que não conversam ou geram retrabalho               |

&#x20; | Operacional             | Problemas de exe                 |

&#x20; | Continuidade do cuidado | Falhas após consulta ou entre níveis de atenção              |



&#x20; Exemplo:



&#x20; \*\*FP08 — Pedido de exame sem agendamento\*\*



&#x20; Categoria:



&#x20; \* Continuidade do cuidado;

&#x20; \* Comunicação;

&#x20; \* Operacional.



&#x20; ---



&#x20; # Como aparecer no Blueprint



&#x20; Na tabela principal eu não colocaria a descrição completa, para não poluir.



&#x20; Usaria:



&#x20; | Etapa        | Ação cidadão        | Frontstage                       | Backstage                 | Fail Point |

&#x20; | ------------ | ------------------- | -----| ------------------------- | ---------- |

&#x20; | Pós-consulta | Tenta agendar exame | Orientação sobre próximos passos | Regulação/gestão de vagas | ⚠ FP08     |



&#x20; E criaria uma tabela complementar:



&#x20; | ID   | Falha                           | Categoria    | Causa provável              | Impacto

&#x20;    |

&#x20; | ---- | ------------------------------- | ------------ | --------------------------- |

&#x20; -------------------------------- |

&#x20; | FP08 | Pedido de exame sem agendamento | Continuidade | Ausência de fluxo integrado | Alta espera, abandono do

&#x20; cuidado |



&#x20; ---



&#x20; # Matriz de severidade (para fase TO-BE)



&#x20; Depois do AS-IS, aplicaria:



&#x20; \*\*Impacto no cidadão × Frequência operaciona



&#x20; Exemplo:



&#x20; | Fail Point                         | Impac |

&#x20; | ---------------------------------- | ------- | ---------- | ---------- |

&#x20; | FP08 — exame sem agendamento       | Alto  |

&#x20; | FP05 — fila sem transparência      | Alto    | Alta       | Crítico    |

&#x20; | FP01 — porta de entrada errada     | Médio |

&#x20; | FP07 — falta de integração clínica | Alto    | Média      | Alto       |



&#x20; ---



&#x20; ## Estrutura final escolhida



&#x20; Portanto:



&#x20; \* \*\*Blueprint AS-IS:\*\* 10–12 fail points;

&#x20; \* \*\*Representação:\*\* ID do fail point na tabarado;

&#x20; \* \*\*Classificação:\*\* Tipologia por categoria (Opção B);

&#x20; \* \*\*Priorização futura:\*\* Matriz impacto × f



&#x20; Isso mantém o blueprint metodologicamente fio em insumo para redesenho do serviço(TO-BE).



Parece que você enviou a resposta sobre fail points novamente — a questão atual era sobre como integrar os normativos

jurídicos no blueprint (Opção A: coluna autôos de Suporte, ou C: tabela cruzada separada).



Como você quer tratar as normas dentro da es



✻ Crunched for 7s



❯ Para o \*\*Service Blueprint AS-IS da Consultaa as normas como uma \*\*camada transversal degovernança\*\*, e não como uma coluna isolada dentro de cada microetapa.



&#x20; A razão é que, diferente de um processo empresarial comum, no SUS a norma não é apenas uma referência documental: ela

&#x20; \*\*define papéis, responsabilidades, critérios de decisão\*\*. Colocar uma norma em cadacélula pode deixar o blueprint pesado e repetitivo.



&#x20; Minha recomendação: \*\*abordagem híbrida\*\*, com a norma vinculada ao ponto do processo onde ela produz efeito.



&#x20; ## Estrutura proposta



&#x20; Manter o blueprint principal com as camadas de Shostack:



&#x20; 1. Evidências físicas

&#x20; 2. Ações do cidadão

&#x20; 3. Frontstage

&#x20; 4. Backstage operacional

&#x20; 5. Backstage regulatório (CROSS)

&#x20; 6. Processos de suporte



&#x20; E acrescentar uma camada transversal:



&#x20; \*\*↓ Governança normativa ↓\*\*



&#x20; ---



&#x20; Exemplo:



&#x20; | Macroetapa    | Microetapa          | Ação              | Backstage  | Fail Point | Norma aplicável                             |

&#x20; | ------------- | ------------------- | ----------------- |------------------------------ | ---------- | ------------------------------------------- |

&#x20; | Pré-acesso    | Busca de informação | Procicos orientam | Gestão de comunicação  | FP01       | Direito de acesso à saúde / organização SUS |

&#x20; | UBS           | Avaliação inicial   | Passia            | Registro e encaminhamento  | FP03       | Atenção Primária / protocolos assistenciais |

&#x20; | Regulação     | Entrada na fila     | Aguanicação       | CROSS analisa demanda  | FP05       | Política Nacional de Regulação              |

&#x20; | Especializado | Consulta AME        | Realde            | Prontuário, registro  | FP07       | Protocolos clínicos e diretrizes            |

&#x20; | Pós-consulta  | Exames              | Buscrecebida      | Fluxo desolicitação/regulação | FP08       | Normas de atenção especializada             |



&#x20; ---



&#x20; ## Classificação das normas



&#x20; Eu separaria em quatro grupos:



&#x20; ### 1. Normas estruturantes do SUS



&#x20; Definem o "porquê" e o modelo do serviço.                                                                             

&#x20; Exemplos:                                                                                                             

&#x20; \* Constituição Federal (direito à saúde);                                                                             \* Lei nº 8.080/1990;

&#x20; \* Lei nº 8.142/1990.                                                                                                  

&#x20; Afetam todo o blueprint.                                                                                              

&#x20; ---                                                                                                                   

&#x20; ### 2. Normas de organização do acesso                                                                                

&#x20; Relacionadas à entrada, filas e regulação.                                                                            

&#x20; Aplicação:                                                                                                            

&#x20; \* UBS;                                                                                                                \* encaminhamento;

&#x20; \* CROSS;                                                                                                              \* agendamento.

&#x20;                                                                                                                       Exemplos:

&#x20;                                                                                                                       \* Política Nacional de Regulação;

&#x20; \* pactuações de acesso;                                                                                               \* normas estaduais de regulação.

&#x20;                                                                                                                       ---

&#x20;                                                                                                                       ### 3. Normas assistenciais

&#x20;                                                                                                                       Relacionadas ao atendimento médico.

&#x20;                                                                                                                       Aplicação:

&#x20;                                                                                                                       \* consulta;

&#x20; \* diagnóstico;                                                                                                        \* conduta;

&#x20; \* exames;                                                                                                             \* retorno.

&#x20;                                                                                                                       Exemplos:

&#x20;                                                                                                                       \* protocolos clínicos;

&#x20; \* linhas de cuidado;                                                                                                  \* diretrizes terapêuticas.

&#x20;                                                                                                                       ---

&#x20;                                                                                                                       ### 4. Normas operacionais e de sistemas

&#x20;                                                                                                                       Relacionadas ao backstage.

&#x20;                                                                                                                       Exemplos:

&#x20;                                                                                                                       \* cadastro;

&#x20; \* registro;                                                                                                           \* faturamento SUS;

&#x20; \* sistemas de informação.                                                                                             

&#x20; Aplicação:                                                                                                            

&#x20; \* SIA/SUS;                                                                                                            \* CNES;

&#x20; \* sistemas estaduais.                                                                                                 

&#x20; ---                                                                                                                   

&#x20; ## Complemento recomendado: Matriz Norma × Processo                                                                   

&#x20; Criaria um anexo:                                                                                                     

&#x20; | Norma               | Processo impactado | Ator responsável | Efeito no serviço            |                        | ------------------- | ------------------ |-------------------- |

&#x20; | Lei 8.080/90        | Acesso ao cuidado  | Rede SUS         | Define direito e organização |                        | Regulação SUS       | Fila e vaga        |luxo de acesso       |

&#x20; | Protocolos clínicos | Consulta/exames    | Equipe médica    | Padroniza conduta            |                        

&#x20; ---                                                                                                                   

&#x20; ## Decisão final                                                                                                      

&#x20; Eu adotaria:                                                                                                          

&#x20; ✅ \*\*Normas como camada transversal de governança no Blueprint\*\*                                                      +

&#x20; ✅ \*\*Matriz complementar Norma × Etapa × Responsável\*\*                                                                

&#x20; Assim o blueprint continua visualmente limpo, preserva Shostack e evidencia que as falhas não são apenas              operacionais: muitas vezes são resultado de stribuídas e restrições institucionais.

&#x20;                                                                                                                       

Abordagem híbrida bem fundamentada — norma como constrangimento estrutural, não como anotação documental. Faz sentido no contexto federativo do SUS onde a norma l fazer o quê.

&#x20;                                                                                                                     Pergunta 6 — Mapeamento emocional do cidadão

&#x20;                                                                                                                     Shostack original não inclui uma camada emoccontemporâneo — em especial o padrão adotadopor organismos como UK Government Digital Service, Nesta e IDEO — frequentemente adiciona uma linha de emoção do      usuário acima das evidências físicas, mapeanm cada microetapa (frustração, alívio,ansiedade, confiança).                                                                                                

Para este serviço específico, a relevância é alta: o relatório já documenta que o cidadão experimenta "sensação de    desamparo estatal" na fila de espera e "ansincia. Isso não é decoração analítica — é dadodiagnóstico.                                                                                                          

Você tem três opções:                                                                                                 

\- Opção A — Não incluir: Mantém Shostack puro. Blueprint mais limpo, mas perde a dimensão experiencial que diferencia service design de mapeamento de processo com

\- Opção B — Linha emocional simplificada: Uma linha acima das evidências físicas com escala de valência (positivo /

neutro / negativo / crítico) por microetapa.icamente defensável como extensão do Shostack.

\- Opção C — Curva de emoção narrativa: Descreve o estado emocional dominante em cada macroetapa com justificativa (ex:

"Macroetapa 3 — Regulação: ansiedade máxima 05"). Mais analítico, menos visual.



Minha recomendação: Opção B. Uma escala de vpa é suficiente para evidenciar os picos defrustração sem transformar o blueprint em um mapa de empatia. Ela conecta diretamente os fail points à experiência vivida — e no contexto de mestrado, demonstrordagem centrada no usuário sem desviar dofoco no serviço.



Você quer incluir uma dimensão emocional no blueprint, e em que formato?



✻ Worked for 30s



❯ Para o \*\*Service Blueprint AS-IS da Consulta Médica SES-SP\*\*, eu incluiria a dimensão emocional, adotando a \*\*Opção B

&#x20; — Linha emocional simplificada\*\*.



&#x20; A justificativa é que, embora a emoção não fnal de Shostack, ela é uma extensãoconsolidada em práticas contemporâneas de \*\*Service Design\*\*, principalmente quando o objetivo é compreender

&#x20; experiência do usuário e identificar pontos



&#x20; No caso da saúde pública, essa camada tem vaadão não avalia apenas o funcionamentotécnico do serviço; ele avalia também:



&#x20; \* previsibilidade;

&#x20; \* segurança;

&#x20; \* confiança;

&#x20; \* sensação de acolhimento;

&#x20; \* percepção de abandono;

&#x20; \* clareza dos próximos passos.



&#x20; Excluir essa dimensão faria o blueprint reprracional\*\*, mas não a \*\*experiência vivida\*\*.



&#x20; ---



&#x20; ## Estrutura proposta do Blueprint com camad



&#x20; A camada ficaria posicionada acima das evidê



&#x20; ```

&#x20; EMOÇÃO DO CIDADÃO

&#x20;         │

&#x20; EVIDÊNCIAS FÍSICAS

&#x20;         │

&#x20; AÇÕES DO CIDADÃO

&#x20;         │

&#x20; ──── Linha de interação ────

&#x20;         │

&#x20; FRONTSTAGE

&#x20;         │

&#x20; ──── Linha de visibilidade ────

&#x20;         │

&#x20; BACKSTAGE OPERACIONAL

&#x20; BACKSTAGE REGULATÓRIO (CROSS)

&#x20;         │

&#x20; ──── Linha de interação interna ────

&#x20;         │

&#x20; PROCESSOS DE SUPORTE

&#x20; ```



&#x20; ---



&#x20; ## Escala emocional adotada



&#x20; Não usaria sentimentos detalhados em cada célula, pois deixaria o blueprint excessivamente subjetivo.



&#x20; Usaria uma escala simples:



&#x20; | Símbolo     | Estado emocional                                              |

&#x20; | ----------- | --------------------------------- |

&#x20; | 🟢 Positivo | confiança, alívio, segurança                                  |

&#x20; | 🟡 Neutro   | expectativa, espera, dúvida       |

&#x20; | 🟠 Negativo | frustração, insegurança, preocupação                          |

&#x20; | 🔴 Crítico  | sensação de abandono, perda iança |



&#x20; ---



&#x20; ## Exemplo aplicado à jornada



&#x20; | Microetapa                        | Emoção      |

&#x20; | --------------------------------- | --------------------------------------- |

&#x20; | Percepção da necessidade de saúde | 🟠 pre      |

&#x20; | Busca de informação               | 🟡 dúvida                               |

&#x20; | Chegada à UBS                     | 🟡 exp      |

&#x20; | Avaliação e encaminhamento        | 🟢 alívio se houver clareza             |

&#x20; | Entrada na regulação              | 🟠 ans      |

&#x20; | Espera por vaga                   | 🔴 sensação de invisibilidade/desamparo |

&#x20; | Recebimento do agendamento        | 🟢 alí      |

&#x20; | Consulta especializada            | 🟢 confiança                            |

&#x20; | Saída com pedido de exame         | 🟡 exp      |

&#x20; | Tentativa de agendar exame        | 🟠 frustração                           |

&#x20; | Sem fluxo claro para continuidade | 🔴 per      |



&#x20; ---



&#x20; ## Relação com os Fail Points



&#x20; A camada emocional não deve ser independenteos fail points.



&#x20; Exemplo:



&#x20; \*\*FP05 — Espera sem transparência na regulaç



&#x20; \* Processo: fila CROSS;

&#x20; \* Falha: ausência de informação sobre posição e prazo;

&#x20; \* Impacto operacional: aumento da espera;

&#x20; \* Emoção: 🔴 sensação de abandono.



&#x20; \*\*FP08 — Solicitação de exame sem agendamento\*\*



&#x20; \* Processo: pós-consulta;

&#x20; \* Falha: ruptura entre prescrição e execução

&#x20; \* Impacto: atraso do cuidado;

&#x20; \* Emoção: 🟠 frustração.



&#x20; ---



&#x20; ## Cuidados metodológicos



&#x20; Eu não colocaria emoções como "verdades abso



&#x20; A legenda metodológica deve indicar:



&#x20; > "A dimensão emocional representa hipótesesnferidas a partir de evidências documentais,relatos de usuários e pontos de falha identificados, devendo ser validada por pesquisa de campo."



&#x20; Isso é importante para manter rigor acadêmico.



&#x20; ---



&#x20; ## Decisão final



&#x20; Adotar:



&#x20; ✅ Camada emocional simplificada (Opção B)

&#x20; ✅ Escala de valência por microetapa

&#x20; ✅ Associação direta com fail points

&#x20; ✅ Validação posterior por entrevistas/pesqu



&#x20; Assim o blueprint continua fundamentado em Sspectiva contemporânea de \*\*experiência docidadão\*\*, adequada para um estudo de transformação de serviço público de saúde.





Escala de valência com ressalva metodológicade rigor — não trata hipótese como dado, nãoabandona a dimensão experiencial.



Pergunta 7 — Formato do artefato final:



Até agora definimos a estrutura conceitual completa. O blueprint tem 7 camadas, 2 níveis de granularidade, 12 fail

points, normas transversais e dimensão emocibre o artefato concreto que será produzido.



Duas tensões precisam ser resolvidas:



Tensão 1 — Tabela vs. diagrama visual:

\- Blueprint como tabela matricial (colunas = microetapas, linhas = camadas): leitura linear, editável em

markdown/Word/Excel, adequado para documento

\- Blueprint como diagrama visual (swimlanes horizontais, colunas verticais, setas de fluxo): padrão visual da

metodologia Shostack, mais legível para apreMiro, Figma, Lucidchart).



Tensão 2 — Documento único vs. conjunto de a

\- Documento único: Blueprint completo com todas as camadas numa tabela expandida, substituindo/expandindo a Seção 8 do

relatório atual.

\- Conjunto de artefatos: (1) Blueprint executivo — só macroetapas; (2) Blueprint operacional — microetapas completas;

(3) Catálogo de fail points; (4) Matriz de nVocê já mencionou essa possibilidade naPergunta 2.



Minha recomendação: tabela matricial como artefato principal (dado que o contexto é um relatório técnico de mestrado,

não uma apresentação executiva), complementaíticos separados — catálogo de fail points,matriz norma × processo e linha emocional. Isso produz um documento academicamente defensável sem depender de

ferramenta visual externa.



Qual é o formato do artefato que você quer p



✻ Brewed for 31s



❯ Para o \*\*Service Blueprint AS-IS da Consulta seguinte solução:



&#x20; \*\*Artefato principal: tabela matricial complcomplementares.\*\*



&#x20; Ou seja, uma combinação entre \*\*documento téentação operacional do serviço\*\*.



&#x20; Apenas um diagrama visual seria insuficienteo, porque dificultaria a rastreabilidade dasfontes, normas, fail points e responsáveis. Por outro lado, apenas uma tabela gigante com todas as dimensões poderia

&#x20; ficar difícil de comunicar.



&#x20; Portanto, a estrutura final seria:



&#x20; ---



&#x20; # Artefato 1 — Blueprint AS-IS Matricial (pr



&#x20; Formato:



&#x20; \*\*Linhas = camadas do serviço\*\*

&#x20; \*\*Colunas = microetapas da jornada\*\*



&#x20; Estrutura:



&#x20; | Camadas ↓ / Microetapas → | Percepção da necessidade | Busca informação | UBS | Encaminhamento | Regulação CROSS |  Agendamento | Consulta AME | Exames | Retorn

&#x20; | ------------------------- | ------------------------ | ---------------- | --- | -------------- | --------------- |  ----------- | ------------ | ------ | ------

&#x20; | Emoção                    | 🟠                       | 🟡               | 🟡  | 🟢             | 🔴              |  🟠          | 🟢           | 🟠     | 🟡

&#x20; | Evidências físicas        |                          |                  |     |                |                 |             |              |        |

&#x20; | Ações cidadão             |                          |                  |     |                |                 |             |              |        |

&#x20; | Frontstage                |                          |                  |     |                |                 |

&#x20;            |              |        |

&#x20; | Backstage operacional     |                          |                  |     |                |                 |

&#x20;            |              |        |

&#x20; | Backstage regulatório     |                          |                  |     |                |                 |

&#x20;            |              |        |

&#x20; | Processos de suporte      |                          |                  |     |                |                 |

&#x20;            |              |        |

&#x20; | Normas relacionadas       |                          |                  |     |                |                 |

&#x20;            |              |        |

&#x20; | Fail points               |                          |                  |     |                |                 |

&#x20;            |              |        |



&#x20; Esse será o "produto central" do capítulo.



&#x20; ---



&#x20; # Artefato 2 — Blueprint Executivo (macrovis



&#x20; Uma versão reduzida para gestores:



&#x20; 5 macroetapas:



&#x20; 1. Pré-acesso

&#x20; 2. Atenção Primária

&#x20; 3. Regulação e acesso especializado

&#x20; 4. Consulta especializada

&#x20; 5. Continuidade do cuidado



&#x20; Com:



&#x20; \* principais dores;

&#x20; \* principais atores;

&#x20; \* principais falhas.



&#x20; Objetivo:



&#x20; permitir leitura em poucos minutos.



&#x20; ---



&#x20; # Artefato 3 — Catálogo de Fail Points



&#x20; Documento separado.



&#x20; Estrutura:



&#x20; | ID   | Etapa        | Falha               Causa                | Impacto cidadão   |Responsável |

&#x20; | ---- | ------------ | ---------------------------------------- | ----------------- |----------- |

&#x20; | FP01 | Pré-acesso   | Porta de entrada desBaixa orientação     | Redirecionamento  |Rede SUS    |

&#x20; | FP05 | Regulação    | Falta de transparêncAusência de feedback | Ansiedade         |CROSS       |

&#x20; | FP08 | Pós-consulta | Exame sem fluxo de aRuptura do processo  | Atraso do cuidado |Rede        |



&#x20; ---



&#x20; # Artefato 4 — Matriz Norma × Processo



&#x20; Para evitar sobrecarregar o blueprint.



&#x20; | Norma               | Processo afetado | Etapa        | Ator          |

&#x20; | ------------------- | ---------------- | -|

&#x20; | Lei 8.080/90        | Acesso à saúde   | Toda jornada | SUS           |

&#x20; | Regulação SUS       | Fila/vagas       | C|

&#x20; | Protocolos clínicos | Atendimento      | AME          | Equipe médica |



&#x20; ---



&#x20; # Artefato 5 — Curva emocional



&#x20; Uma linha simples:



&#x20; ```

&#x20; Emoção



&#x20; 🟢

&#x20;     \\          /

&#x20;      \\        /

&#x20; 🟡----\\------/----

&#x20;        \\

&#x20;         \\

&#x20; 🟠       🔴

&#x20;           |

&#x20;        Regulação

&#x20; ```



&#x20; Com destaque para:



&#x20; \* maior ansiedade;

&#x20; \* maior frustração;

&#x20; \* momentos de recuperação da confiança.



&#x20; ---



&#x20; # Relação com Shostack



&#x20; O blueprint principal continua fiel:



&#x20; ```

&#x20; Evidências físicas

&#x20;         ↓

&#x20; Ações do cidadão

&#x20;         ↓

&#x20; Linha de interação

&#x20;         ↓

&#x20; Frontstage

&#x20;         ↓

&#x20; Linha de visibilidade

&#x20;         ↓

&#x20; Backstage

&#x20;         ↓

&#x20; Linha de interação interna

&#x20;         ↓

&#x20; Processos de suporte

&#x20; ```



&#x20; As extensões (emoção, normas e fail points) aparecem como camadas analíticas complementares.



&#x20; ---



&#x20; ## Decisão final



&#x20; O formato adotado será:



&#x20; ✅ \*\*Blueprint matricial como artefato principal\*\*

&#x20; ✅ \*\*Versão executiva resumida\*\*

&#x20; ✅ \*\*Catálogo de fail points separado\*\*

&#x20; ✅ \*\*Matriz norma × processo\*\*

&#x20; ✅ \*\*Linha emocional complementar\*\*



&#x20; Esse formato é mais adequado para um \*\*relatório acadêmico de mestrado\*\*, porque mantém rigor metodológico, permite

&#x20; auditoria do raciocínio e deixa o material pormação AS-IS → TO-BE.





Conjunto de artefatos bem definido — o blueprint matricial como núcleo analítico com documentos satélite é a estrutura

certa para um mestrado.



Pergunta 8 — Problema estrutural das colunas



Você definiu \~25 microetapas (5 macro × \~5 micial tem colunas = microetapas e linhas =camadas (9 linhas: emoção, evidências, cidadão, frontstage, 2 backstages, suporte, normas, fail points).



Uma tabela 9×25 é funcionalmente ilegível em qualquer formato de documento — Word, PDF, markdown. O exemplo que você

mostrou na Pergunta 7 já usou apenas 9 colun



Você tem três maneiras de resolver isso:



\- Opção A — Blueprint por macroetapa: 5 tabefase, cada uma com \~5 colunas (microetapas).Leitura fluida, preserva todo o detalhe, mas perde a visão contínua da jornada.

\- Opção B — Blueprint condensado com células(uma coluna por macroetapa) onde cada célulacontém as microetapas como bullet points dentro dela. Visão contínua da jornada, menor fidelidade visual ao padrão

matricial.

\- Opção C — Dois blueprints complementares: Um blueprint 9×5 para visão executiva + cinco blueprints 9×5 detalhados

(um por macroetapa) para visão operacional. s — é o que o UK GDS usa em jornadascomplexas.



Minha recomendação: Opção C. Você já planejou dois produtos (executivo e operacional) desde a Pergunta 2 — a Opção C é

a materialização exata disso. O blueprint exda completa; os cinco blueprints operacionais (9×5 cada) detalham cada macroetapa sem comprometer a legibilidade.



Como você quer resolver o problema das colunas?



✻ Baked for 28s



❯ Para resolver o problema estrutural das colunas, adotaria a \*\*Opção C — dois níveis de blueprint complementares:

&#x20; executivo + cinco blueprints operacionais po



&#x20; Essa escolha é a mais coerente com tudo que \*\*jornada completa, granularidade em doisníveis, camadas de Shostack, fail points, normas e dimensão emocional\*\*.



&#x20; O problema identificado é correto: um blueprint único com \*\*9 linhas × 25 microetapas\*\* deixa de funcionar como

&#x20; artefato de comunicação. Ele vira uma matrizlegível.



&#x20; A solução será separar \*\*visão sistêmica\*\* d



&#x20; ---



&#x20; # Artefato 1 — Blueprint Executivo (visão da



&#x20; Objetivo:

&#x20; Mostrar o ciclo completo do cidadão.



&#x20; Estrutura:



&#x20; \*\*Colunas = 5 macroetapas\*\*



&#x20; | Camadas ↓ / Macroetapas → | Pré-acesso | APS/UBS | Regulação | Especialista | Continuidade |

&#x20; | ------------------------- | ---------- | ------ | ------------ |

&#x20; | Emoção                    |            |         |           |              |              |

&#x20; | Evidências físicas        |            |        |              |

&#x20; | Ações cidadão             |            |         |           |              |              |

&#x20; | Frontstage                |            |        |              |

&#x20; | Backstage operacional     |            |         |           |              |              |

&#x20; | Backstage regulatório     |            |        |              |

&#x20; | Processos suporte         |            |         |           |              |              |

&#x20; | Normas                    |            |        |              |

&#x20; | Fail points               |            |         |           |              |              |



&#x20; Dentro de cada célula entram os principais elementos resumidos.



&#x20; Exemplo:



&#x20; \*\*Regulação → Emoção\*\*



&#x20; 🔴 Ansiedade por espera e ausência de previsibilidade.



&#x20; \*\*Regulação → Backstage\*\*



&#x20; CROSS analisa demanda, prioriza e direciona oferta.



&#x20; ---



&#x20; # Artefato 2 — Cinco Blueprints Operacionais detalhados



&#x20; Cada macroetapa terá seu próprio blueprint.



&#x20; Formato:



&#x20; \*\*9 linhas × aproximadamente 5 microetapas\*\*



&#x20; ---



&#x20; ## Blueprint Operacional 1



&#x20; ## Pré-acesso e decisão do cidadão



&#x20; Microetapas:



&#x20; 1. Percepção da necessidade;

&#x20; 2. Busca de informação;

&#x20; 3. Escolha da porta de entrada;

&#x20; 4. Preparação para atendimento.



&#x20; ---



&#x20; ## Blueprint Operacional 2



&#x20; ## Atenção Primária / UBS



&#x20; Microetapas:



&#x20; 1. Chegada;

&#x20; 2. Acolhimento;

&#x20; 3. Avaliação inicial;

&#x20; 4. Encaminhamento;

&#x20; 5. Registro.



&#x20; ---



&#x20; ## Blueprint Operacional 3



&#x20; ## Regulação e acesso especializado



&#x20; Microetapas:



&#x20; 1. Entrada da solicitação;

&#x20; 2. Análise regulatória;

&#x20; 3. Gestão da fila;

&#x20; 4. Disponibilização da vaga;

&#x20; 5. Comunicação.



&#x20; Aqui a CROSS aparece com destaque.



&#x20; ---



&#x20; ## Blueprint Operacional 4



&#x20; ## Atendimento especializado



&#x20; Microetapas:



&#x20; 1. Recepção;

&#x20; 2. Consulta;

&#x20; 3. Avaliação clínica;

&#x20; 4. Prescrição/solicitação;

&#x20; 5. Orientações.



&#x20; ---



&#x20; ## Blueprint Operacional 5



&#x20; ## Pós-consulta e continuidade



&#x20; Microetapas:



&#x20; 1. Entendimento das orientações;

&#x20; 2. Agendamento dos exames;

&#x20; 3. Realização;

&#x20; 4. Resultado;

&#x20; 5. Retorno/continuidade.



&#x20; ---



&#x20; # Artefatos complementares



&#x20; Além dos blueprints:



&#x20; ## Catálogo de Fail Points



&#x20; Mantido separado:



&#x20; FP01 a FP12



&#x20; com:



&#x20; \* localização;

&#x20; \* categoria;

&#x20; \* causa;

&#x20; \* impacto;

&#x20; \* emoção associada.



&#x20; ---



&#x20; ## Matriz Norma × Processo



&#x20; Mantida como anexo.



&#x20; ---



&#x20; ## Curva emocional



&#x20; Uma visão transversal:



&#x20; Percepção → UBS → Regulação → Especialista →



&#x20; mostrando os pontos de maior tensão.



&#x20; ---



&#x20; # Resultado final do capítulo



&#x20; A estrutura ficaria:



&#x20; \*\*Capítulo: Service Blueprint AS-IS da Consu



&#x20; 1. Metodologia e premissas

&#x20; 2. Limites da jornada

&#x20; 3. Blueprint executivo

&#x20; 4. Blueprint operacional 1 — Pré-acesso

&#x20; 5. Blueprint operacional 2 — UBS

&#x20; 6. Blueprint operacional 3 — Regulação/CROSS

&#x20; 7. Blueprint operacional 4 — Especialista

&#x20; 8. Blueprint operacional 5 — Continuidade

&#x20; 9. Catálogo de fail points

&#x20; 10. Matriz normativa

&#x20; 11. Síntese dos principais pontos críticos



&#x20; ---



&#x20; Essa solução mantém:



&#x20; \* fidelidade ao método Shostack;

&#x20; \* legibilidade;

&#x20; \* rastreabilidade acadêmica;

&#x20; \* possibilidade de virar posteriormente um \*\*Service Blueprint TO-BE\*\* com melhorias priorizadas.





Estrutura bem resolvida. O capítulo de 11 sete e metodologicamente rastreável.







A estrutura atual embute os atores implicitae. Mas este serviço tem uma característicacrítica: os atores operam sob contratos e esferas de governo diferentes, e isso importa para a análise de

responsabilidade.



Exemplo do problema: na Macroetapa 4 (Consulo AME pode ser:

\- Servidor público estadual (administração direta)

\- Funcionário de uma OSS (contrato de gestão

\- Médico residente sob supervisão de preceptor



Isso afeta diretamente qual norma se aplica, quem responde por falhas e quem pode ser alvo de uma recomendação de

melhoria no TO-BE.



Você tem três opções para tratar atores:



\- Opção A — Atores implícitos nas células: Mo das células de backstage. Simples, masdificulta análise de responsabilidade.

\- Opção B — Linha dedicada "Ator Responsável, entre frontstage e backstage operacional,identificando o ator principal de cada microetapa com sua natureza jurídica (Municipal/Estadual/OSS/Federal). Adiciona

uma linha, mas torna a responsabilidade audi

\- Opção C — Legenda de atores no cabeçalho: Uma tabela prévia que define os atores e seus vínculos; no blueprint, cada

ator é citado por sigla (ex: "Med-OSS", "Regual, mais rastreável.



Minha recomendação: Opção B. A distinção Munalhe burocrático — é o núcleo da fragmentação que gera os fail points FP04, FP07 e FP10. Um blueprint que não torna isso visível obscurece a causa estrutural dos

problemas. A 10ª linha é justificada.



Como você quer identificar os atores no blue



✻ Cooked for 35s



❯ Para o \*\*Service Blueprint AS-IS da Consulta\*\*Opção B — Linha dedicada "AtorResponsável"\*\*, com um pequeno complemento da Opção C.



&#x20; A inclusão dos atores como uma camada explícita é necessária neste serviço porque a fragmentação institucional não é

&#x20; apenas uma característica administrativa: elestruturais dos \*\*fail points\*\*identificados.



&#x20; No setor público de saúde, a experiência do cidadão é resultado de uma cadeia em que participam organizações com

&#x20; diferentes vínculos:



&#x20; \* Município;

&#x20; \* Estado;

&#x20; \* prestadores contratualizados;

&#x20; \* OSS;

&#x20; \* equipes assistenciais;

&#x20; \* sistemas nacionais;

&#x20; \* regulação.



&#x20; Sem tornar esses atores visíveis, o blueprin"o processo" sem mostrar \*\*quem possuicapacidade real de decisão e intervenção\*\*.



&#x20; ---



&#x20; # Estrutura final do Blueprint com atores



&#x20; A ordem das camadas ficaria:



&#x20; ```

&#x20; EMOÇÃO DO CIDADÃO



&#x20; EVIDÊNCIAS FÍSICAS



&#x20; AÇÕES DO CIDADÃO



&#x20; ──── Linha de interação ────



&#x20; FRONTSTAGE

&#x20; (ações visíveis)



&#x20; ATORES RESPONSÁVEIS

&#x20; (quem executa / natureza institucional)



&#x20; ──── Linha de visibilidade ────



&#x20; BACKSTAGE OPERACIONAL

&#x20; (processos internos)



&#x20; BACKSTAGE REGULATÓRIO

&#x20; (CROSS / gestão estadual)



&#x20; ──── Linha de interação interna ────



&#x20; PROCESSOS DE SUPORTE

&#x20; (sistemas, bases, infraestrutura)



&#x20; NORMAS TRANSVERSAIS



&#x20; FAIL POINTS

&#x20; ```



&#x20; ---



&#x20; # Como representar os atores



&#x20; A linha não deve apenas colocar "médico", "r



&#x20; Ela deve trazer:



&#x20; \*\*Ator + esfera institucional + papel\*\*



&#x20; Exemplo:



&#x20; | Microetapa          | Ator responsável

&#x20; | ------------------- | ------------------------------ |

&#x20; | Busca de informação | Cidadão + canais SES

&#x20; | Acolhimento UBS     | Equipe APS Municipal           |

&#x20; | Encaminhamento      | Médico APS Municipal

&#x20; | Regulação           | CROSS Estadual                 |

&#x20; | Agendamento         | Unidade reguladora /

&#x20; | Consulta AME        | Médico AME (Estado/OSS)        |

&#x20; | Exames              | Rede executante SUS

&#x20; | Retorno             | APS + especialista             |



&#x20; ---



&#x20; # Classificação dos atores



&#x20; Criaria uma legenda:



&#x20; | Código  | Ator                           |

&#x20; | ------- | ------------------------------ |

&#x20; | CID     | Cidadão                        |

&#x20; | APS-MUN | Atenção Primária Municipal     |

&#x20; | REG-EST | Regulação Estadual/CROSS       |

&#x20; | AMB-EST | Ambulatório estadual           |

&#x20; | AMB-OSS | Ambulatório gerenciado por OSS |

&#x20; | MED     | Profissional médico            |

&#x20; | SUP-SUS | Sistemas e suporte SUS         |



&#x20; Assim o blueprint fica mais limpo.



&#x20; ---



&#x20; # Exemplo aplicado



&#x20; Macroetapa: Regulação



&#x20; | Camada     | Conteúdo                                        |

&#x20; | ---------- | -----------------------------

&#x20; | Cidadão    | Aguarda consulta especializada                  |

&#x20; | Frontstage | Recebe informação de agendame

&#x20; | Ator       | REG-EST / CROSS                                 |

&#x20; | Backstage  | Análise da solicitação, fila,

&#x20; | Suporte    | Sistema de regulação                            |

&#x20; | Fail Point | FP05 — espera sem transparênc



&#x20; ---



&#x20; # Benefício para análise TO-BE



&#x20; Essa camada permite responder perguntas esse



&#x20; ### "Quem pode resolver esse problema?"



&#x20; Exemplo:



&#x20; \*\*FP08 — Exame solicitado sem fluxo de agend



&#x20; Sem atores:



&#x20; > Falha no agendamento.



&#x20; Com atores:



&#x20; > Especialista AMB-OSS solicita exame → siste não possui fluxo integrado → cidadão ficaresponsável por descobrir o próximo passo.



&#x20; A intervenção muda completamente.



&#x20; ---



&#x20; # Ajuste metodológico



&#x20; Para preservar Shostack, eu não trataria "Ator Responsável" como uma nova camada de serviço, mas como uma \*\*camada

&#x20; analítica complementar\*\*.



&#x20; Assim:



&#x20; \* Camadas originais permanecem;

&#x20; \* Linha de interação e visibilidade continuam intactas;

&#x20; \* Atores tornam responsabilidade operacional



&#x20; ---



&#x20; ## Decisão final



&#x20; Adotar:



&#x20; ✅ Linha dedicada \*\*"Ator Responsável"\*\* no

&#x20; ✅ Identificação por esfera institucional (Municipal/Estadual/OSS/Federal)

&#x20; ✅ Complemento com legenda de códigos de ato

&#x20; ✅ Uso dos atores para análise dos fail points e desenho TO-BE



&#x20; Esse ajuste torna o blueprint adequado para um serviço público complexo e permite transformar o mapa de experiência

&#x20; em uma ferramenta real de governança e melho





Excelente — a camada de atores com códigos institucionais transforma o blueprint de mapa descritivo em ferramenta de

responsabilização. A distinção AMB-OSS vs AMte para o Tema 698 do STF que o relatório jácita.



Pergunta 10 — Base de evidências e validação do AS-IS:



O blueprint está conceitualmente completo na estrutura. Mas como artefato acadêmico de mestrado, ele precisa

responder: de onde vêm os dados que preenche



O relatório usa como fontes: manuais SIRESP/egulação, legislação federal e jurisprudência STF. Isso cobre bem as macroetapas 2–4 (UBS → Regulação → AME). Mas as macroetapas 1 (pré-acesso) e 5 (continuidade)

foram adicionadas ao escopo e não têm base erio.



Você tem três opções para tratar isso:



\- Opção A — Blueprint 100% documental: Todasor fontes secundárias — legislação, manuaisoperacionais, literatura de saúde pública, dados DATASUS. Explicitamente reconhece a ausência de pesquisa primária com

cidadãos. Academicamente honesto, mas limitacia vivida.

\- Opção B — Blueprint com validação parcial por pesquisa primária: Macroetapas 1 e 5 são preenchidas com base em

entrevistas ou questionários com usuários do coleta de campo que pode não estar no escopo do exercício.

\- Opção C — Blueprint inferencial com ressalses sem base documental direta são marcadascomo "inferidas a partir de fail points documentados e literatura de design de serviços". Você já usou essa lógica

para a camada emocional — pode ser estendidacamente defensável desde que a ressalva sejaclara.



Minha recomendação: Opção C para este exercício, com Opção B como próximo passo natural. Tratar as fases inferidas

como hipóteses documentadas (não afirmações mpromete o rigor — e sinaliza claramente onde está a lacuna de pesquisa, o que é exatamente o que uma banca de mestrado quer ver.



Qual é a base de evidências do seu blueprint e como você pretende tratar as fases sem cobertura documental direta?



✻ Crunched for 39s



❯ Para o \*\*Service Blueprint AS-IS da Consulta Médica SES-SP\*\*, adotaria a \*\*Opção C — Blueprint inferencial com

&#x20; ressalva metodológica explícita\*\*, complemens com evidência documental consolidada\*\*.



&#x20; Essa combinação é a mais adequada para um trdois problemas:



&#x20; 1. \*\*Excesso de afirmação sem evidência\*\* — bservados;

&#x20; 2. \*\*Redução artificial da jornada\*\* — voltar a limitar o blueprint apenas ao que tem documentação disponível.



&#x20; Como o objetivo do AS-IS é representar o funcionamento atual do serviço, a ausência de dados primários de usuários

&#x20; não deve eliminar as etapas de pré-acesso e aramente sinalizada.



&#x20; ---



&#x20; # Estratégia de evidências adotada



&#x20; Cada elemento do blueprint receberá um marca



&#x20; | Código | Tipo de evidência    | Uso                            |

&#x20; | ------ | -------------------- | ----------------------------------------------------------- |

&#x20; | D      | Documental direta    | Baseado emcumento oficial      |

&#x20; | L      | Literatura/estudos   | Baseado em pesquisas e modelos de saúde pública             |

&#x20; | I      | Inferência analítica | Deduzido aocumentos existentes |

&#x20; | V      | Validação futura     | Necessita confirmação com pesquisa de campo                 |



&#x20; ---



&#x20; # Aplicação por macroetapa



&#x20; ## Macroetapas 2, 3 e 4



&#x20; ## UBS → Regulação → Atendimento Especializado



&#x20; Base mais robusta.



&#x20; Predominância:



&#x20; \*\*D — documental\*\*



&#x20; Fontes:



&#x20; \* normas do SUS;

&#x20; \* Política Nacional de Regulação;

&#x20; \* manuais operacionais;

&#x20; \* documentos estaduais;

&#x20; \* sistemas de informação;

&#x20; \* fluxos institucionais.



&#x20; Exemplo:



&#x20; \*\*Regulação CROSS\*\*



&#x20; Atores:



&#x20; \* CROSS;

&#x20; \* unidades solicitantes;

&#x20; \* unidades executantes.



&#x20; Evidência:



&#x20; \* documental.



&#x20; ---



&#x20; # Macroetapa 1



&#x20; ## Pré-acesso



&#x20; Aqui não afirmaria:



&#x20; > "O cidadão sempre faz X"



&#x20; A redação correta seria:



&#x20; > "A etapa foi modelada como hipótese de jor acesso aos serviços de saúde, canaisinstitucionais existentes e falhas identificadas relacionadas à porta de entrada."



&#x20; Exemplo:



&#x20; \*\*Percepção da necessidade → busca de informação\*\*



&#x20; Tipo de evidência:



&#x20; I + L



&#x20; Porque:



&#x20; \* o cidadão necessariamente inicia algum processo de decisão;

&#x20; \* porém o comportamento específico precisa s



&#x20; ---



&#x20; # Macroetapa 5



&#x20; ## Pós-consulta e continuidade



&#x20; Mesma lógica.



&#x20; Não dizer:



&#x20; > "O cidadão enfrenta dificuldade para marca



&#x20; como fato universal.



&#x20; Usar:



&#x20; > "Foi identificado como ponto potencial de ndo a separação entre prescrição médica,regulação de procedimentos e execução da rede."



&#x20; Tipo:



&#x20; I + D



&#x20; Porque a existência do fluxo é documental, mas a experiência precisa de validação.



&#x20; ---



&#x20; # Como isso aparece no Blueprint



&#x20; Eu acrescentaria uma coluna complementar:



&#x20; \*\*Base de evidência\*\*



&#x20; Exemplo:



&#x20; | Microetapa          | Fail Point                      | Evidência |

&#x20; | ------------------- | --------------------

&#x20; | Busca de informação | FP01 — porta de entrada incerta | I/L       |

&#x20; | Encaminhamento      | FP04 — informação in

&#x20; | Regulação           | FP05 — espera sem transparência | D/I       |

&#x20; | Exame               | FP08 — ruptura pós-c



&#x20; ---



&#x20; # Declaração metodológica do capítulo



&#x20; Eu incluiria algo como:



&#x20; > "O Service Blueprint AS-IS foi construído l de normas, fluxos institucionais, sistemas operacionais e literatura especializada. As etapas com menor disponibilidade de evidência documental direta,

&#x20; especialmente pré-acesso e continuidade do como hipóteses analíticas inferidas a partirdas barreiras identificadas no fluxo assistencial e deverão ser validadas em pesquisa com usuários e profissionais."



&#x20; ---



&#x20; # Relação com o rigor acadêmico



&#x20; Essa abordagem fortalece o trabalho porque demonstra:



&#x20; \* consciência do limite dos dados;

&#x20; \* distinção entre fato e hipótese;

&#x20; \* capacidade analítica;

&#x20; \* identificação de lacunas de pesquisa.



&#x20; ---



&#x20; ## Decisão final



&#x20; Adotar:



&#x20; ✅ Opção C — inferencial com ressalvas explí

&#x20; ✅ Opção A — documental onde houver fonte direta

&#x20; ✅ Marcador de evidência em cada bloco do bl

&#x20; ✅ Indicação das etapas que necessitam validação futura



&#x20; Assim o blueprint permanece completo, metodologicamente defensável e pronto para evoluir para uma etapa futura de

&#x20; pesquisa de campo ou desenho TO-BE.





Marcadores de evidência por célula é a decisão certa — isso é o que diferencia análise analítica de afirmação

descuidada. A declaração metodológica no iní bem redigida.



Pergunta 11 — Conexão AS-IS → TO-BE:



O relatório já tem uma Seção 9 com 4 macrodirivadas dos 4 fail points originais. Agora oblueprint expandido tem 12 fail points. Essa expansão cria uma tensão que precisa ser resolvida:



As 4 recomendações TO-BE existentes cobrem FP05, FP06, FP07 e FP08 (regulação, agendamento, interoperabilidade,

exames). Mas ficam sem recomendação correspoP02, FP03, FP04, FP09, FP10, FP11 e FP12.



Você tem três maneiras de tratar isso:



\- Opção A — Manter o TO-BE existente sem altroduto deste exercício; o TO-BE da Seção 9permanece como está. A expansão dos fail points fica registrada no catálogo analítico sem exigir reformulação das

recomendações.

\- Opção B — Expandir o TO-BE para cobrir todos os 12 fail points: Cada fail point recebe uma ou mais recomendações de

transformação. Mais completo, mas aumenta sitrabalho.

\- Opção C — Criar um "mapa de priorização" entre fail points e recomendações TO-BE: A matriz de severidade (impacto ×

frequência) é usada para selecionar os fail nção prioritária no TO-BE — nãonecessariamente todos os 12. Os demais ficam como "lacunas identificadas para investigação futura".



Minha recomendação: Opção C. O blueprint AS-IS não precisa gerar uma recomendação para cada fail point — isso seria

over-engineering do diagnóstico. A matriz deiu faz exatamente esse trabalho de seleção:FP05 e FP08 já foram classificados como "críticos", o que justifica as recomendações existentes. Os demais entram como

achados do diagnóstico ampliado, com recomeno futura.



Como você quer estruturar a conexão entre o



✻ Brewed for 34s



❯ Para a conexão entre o \*\*Blueprint AS-IS\*\* eção C — mapa de priorização entre failpoints e recomendações TO-BE\*\*, utilizando a matriz de severidade (\*\*impacto × frequência\*\*) como mecanismo de

&#x20; decisão.



&#x20; Essa escolha mantém coerência metodológica: ica\*\* (identificar como o serviço funciona e onde falha) e o \*\*TO-BE tem função propositiva\*\* (definir onde intervir prioritariamente). Não é necessário que cada

&#x20; falha identificada gere uma recomendação de .



&#x20; A expansão de 4 para 12 fail points melhora brigar a expansão proporcional dasdiretrizes TO-BE, pois isso poderia diluir o foco estratégico.



&#x20; ---



&#x20; ## Estrutura final da conexão AS-IS → TO-BE



&#x20; O encadeamento será:



&#x20; \*\*Service Blueprint AS-IS\*\*

&#x20; ↓

&#x20; \*\*Catálogo de Fail Points (FP01–FP12)\*\*

&#x20; ↓

&#x20; \*\*Classificação da falha\*\*

&#x20; ↓

&#x20; \*\*Matriz de severidade\*\*

&#x20; (impacto no cidadão × frequência operacional

&#x20; ↓

&#x20; \*\*Priorização TO-BE\*\*



&#x20; ---



&#x20; # 1. Matriz de priorização dos Fail Points



&#x20; | ID   | Fail Point                         requência | Prioridade TO-BE |

&#x20; | ---- | ----------------------------------------------- | ---------- | ---------- | ---------------- |

&#x20; | FP01 | Cidadão não identifica porta corretlta       | Média            |

&#x20; | FP02 | Falta de orientação sobre documentos e fluxo    | Médio      | Média      | Baixa/Média      |

&#x20; | FP03 | Dificuldade no encaminhamento da APédia      | Alta             |

&#x20; | FP04 | Encaminhamento incompleto para regulação        | Alto       | Média      | Alta             |

&#x20; | FP05 | Espera sem transparência na regulaçlta       | Crítica          |

&#x20; | FP06 | Falha no agendamento da consulta                | Alto       | Alta       | Crítica          |

&#x20; | FP07 | Sistemas sem integração adequada   lta       | Crítica          |

&#x20; | FP08 | Pedido de exame sem continuidade                | Muito alto | Alta       | Crítica          |

&#x20; | FP09 | Resultado sem integração ao cuidadoédia      | Média/Alta       |

&#x20; | FP10 | Ruptura da contrarreferência                    | Alto       | Média      | Alta             |

&#x20; | FP11 | Ausência de responsável pelo próximédia      | Alta             |

&#x20; | FP12 | Retrabalho administrativo/sistêmico             | Médio      | Alta       | Média            |



&#x20; ---



&#x20; # 2. Relação com as 4 macrodiretrizes TO-BE existentes



&#x20; As recomendações atuais permanecem válidas e passam a ter uma fundamentação mais ampla:



&#x20; | Diretriz TO-BE                                                              | Fail points relacionados |

&#x20; | ---------------------------------------------- | ------------------------ |

&#x20; | \*\*1. Transparência e governança do acesso regulado\*\*                        | FP05, FP06               |

&#x20; | \*\*2. Integração e interoperabilidade dos s     | FP07, FP12               |

&#x20; | \*\*3. Coordenação da jornada pós-consulta e continuidade do cuidado\*\*        | FP08, FP09, FP11         |

&#x20; | \*\*4. Integração entre níveis de atenção e is\*\* | FP03, FP04, FP10         |



&#x20; ---



&#x20; # 3. Tratamento dos fail points não prioriza



&#x20; Os fail points não desaparecem. Eles serão r



&#x20; \*\*"Achados adicionais do diagnóstico AS-IS eturos de transformação."\*\*



&#x20; Exemplo:



&#x20; \*\*FP01 — Falha na orientação inicial\*\*



&#x20; Não necessariamente gera uma macrodiretriz nunidade futura:



&#x20; \* melhoria dos canais de informação;

&#x20; \* jornada digital do cidadão;

&#x20; \* comunicação integrada SUS.



&#x20; ---



&#x20; # 4. Inserção no relatório



&#x20; Eu criaria uma seção intermediária:



&#x20; ## "Da identificação de falhas à priorização



&#x20; Com a justificativa:



&#x20; > "A ampliação do Service Blueprint permitiufalha ao longo de toda a jornada do cidadão. Entretanto, considerando critérios de impacto, recorrência e capacidade de intervenção institucional, foram

&#x20; selecionados os pontos críticos que fundamenstas."



&#x20; ---



&#x20; # Decisão final



&#x20; Adotar:



&#x20; ✅ \*\*Opção C — mapa AS-IS → TO-BE por priori

&#x20; ✅ Manter as 4 macrodiretrizes de transformação

&#x20; ✅ Vincular cada diretriz aos fail points co

&#x20; ✅ Usar matriz impacto × frequência para justificar escolhas

&#x20; ✅ Registrar demais falhas como oportunidade



&#x20; Dessa forma, o trabalho fica mais forte acadstra capacidade de diagnóstico amplo,enquanto o TO-BE demonstra capacidade de priorização estratégica.





Alcançamos shared understanding em todas as Deixa eu consolidar o que foi resolvido.



\---

Síntese: Blueprint AS-IS da Consulta Médica SES-SP — Decisões de Design



Fronteiras da jornada: Da percepção da necessidade de saúde até a realização dos exames e continuidade do cuidado.

Estende o relatório original em ambos os ext



Granularidade: Hierarquia em dois níveis — 5, \~5 microetapas cada como unidades deanálise.



Camadas (10 no total):

Emoção do Cidadão

Evidências Físicas

Ações do Cidadão

──── Linha de interação ────

Frontstage

Atores Responsáveis (código institucional)

──── Linha de visibilidade ────

Backstage Operacional

Backstage Regulatório (CROSS)

──── Linha de interação interna ────

Processos de Suporte

Normas Transversais

Fail Points



Fail points: 12 (FP01–FP12), com tipologia pblueprint + catálogo analítico separado +matriz severidade (impacto × frequência) para priorização TO-BE.



Normas: Camada transversal de governança + matriz norma × processo como artefato complementar.



Emoção: Escala de valência simplificada (🟢🟡🟠🔴) por microetapa, com ressalva de validação futura.



Formato: 6 artefatos — blueprint executivo (9×5) + 5 blueprints operacionais (9×5 cada) + catálogo de fail points +

matriz normativa + curva emocional + mapa de



Atores: Linha dedicada com códigos instituciOSS, etc.).



Evidências: Documental (D) onde há fonte dirsalva metodológica explícita nas macroetapas1 e 5.



Conexão TO-BE: 4 macrodiretrizes existentes vinculadas aos fail points críticos pela matriz de severidade. FPs não

priorizados registrados como oportunidades f

