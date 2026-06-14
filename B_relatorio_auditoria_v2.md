# Segunda Auditoria — V2 do relatório Consulta Médica SES/SP versus Auditoria V1

## Escopo

Avaliação da versão V2 para verificar:

1. Se as falhas apontadas na auditoria V1 foram efetivamente corrigidas;
2. Se a V2 criou novas falhas;
3. Quais pontos permanecem abertos.

A análise não considera estilo, formatação ou organização textual.

---

# 1. Verificação das falhas da Auditoria V1

## 1.1 Portaria GM/MS nº 1.101/2002 como parâmetro vigente

**Status: CORRIGIDO.**

A V2 reconheceu corretamente que a Portaria 1.101/2002 foi revogada e substituída pela Portaria 1.631/2015.

Trecho da V2:
> "A Portaria 1.101/2002 foi revogada pela Portaria GM/MS nº 1.631..."

Avaliação:

Correção adequada. A V2 remove a interpretação de meta rígida de consultas por habitante/ano.

Ponto residual:

Ainda é necessário garantir que o relatório final não reutilize o indicador antigo como meta operacional da SES/SP.

---

## 1.2 Meta de 1,5 consultas/ano do Pacto pela Saúde

**Status: CORRIGIDO.**

A V2 identificou corretamente que a meta era referente às especialidades básicas e não ao conjunto total de consultas SUS.

Trecho:
> "A meta de 1,5 referia-se à média em consultas básicas."

Avaliação:

Correção conceitual adequada.

Ponto residual:

A versão final deve retirar completamente a associação entre essa meta e desempenho geral de acesso à consulta médica.

---

## 1.3 Uso da afirmação de média nacional de 1,7 consultas

**Status: CORRIGIDO.**

A V2 reconheceu ausência de fonte oficial suficiente.

Trecho:
> "Essa alegação carece de base empírica e deve ser retirada ou marcada como pendente."

Avaliação:

Boa correção metodológica.

---

## 1.4 Portaria 1.604/2023 e Portaria 1.820/2009

**Status: CORRIGIDO.**

A V2 separou corretamente:

- PNAES = atenção especializada;
- Carta dos Direitos dos Usuários = direitos do usuário.

Trecho:
> "A 1.604/2023 versa sobre atenção especializada e a 1.820/2009 estabelece direitos e deveres dos usuários."

Avaliação:

Falha normativa corrigida.

---

## 1.5 Papel do enfermeiro na eSF

**Status: CORRIGIDO.**

A V2 removeu a interpretação incorreta de substituição do médico pelo enfermeiro.

Avaliação:

Correção adequada.

---

## 1.6 SAPS/DenaSUS

**Status: CORRIGIDO.**

A V2 corrigiu a confusão entre órgão federal, estadual e auditoria.

Trecho:
> "Não há Secretaria Estadual de Atenção Primária no MS; existe a SAPS."

Avaliação:

Falha corrigida.

---

## 1.7 Papel da ANS

**Status: PARCIALMENTE CORRIGIDO.**

A V2 reconhece ausência de base para afirmar integração operacional ANS-SUS.

Entretanto:

Permanece uma lacuna sobre como a regulação estadual paulista trata usuários com cobertura suplementar, ressarcimento ao SUS, interoperabilidade e conflitos de fila.

A correção eliminou o erro, mas não aprofundou a operação real.

---

## 1.8 Contratos de Gestão com OS

**Status: CORRIGIDO.**

A distinção entre Lei 8.080/90 e Lei 9.637/98 foi adequadamente feita.

Avaliação:

Correção jurídica suficiente.

---

# 2. Novas falhas introduzidas pela V2

## 2.1 V2 audita normas, mas ainda não reconstrói a operação SES/SP

**Falha nova relevante.**

A V2 concentra-se em corrigir legislação, mas não demonstra que o fluxo operacional real da Secretaria de Estado da Saúde de São Paulo foi validado.

Faltam evidências sobre:

- como a consulta é solicitada;
- quem regula;
- como a vaga é disponibilizada;
- regras internas dos AMEs;
- papel das DRS;
- integração municipal-estadual.

Para um Service Blueprint AS-IS, isso permanece insuficiente.

---

## 2.2 Ausência de auditoria dos sistemas operacionais reais

A V2 menciona correções normativas, mas não valida sistemas usados na prática.

Pontos não demonstrados:

- CROSS/SIRESP;
- sistemas municipais;
- prontuário eletrônico;
- agendas contratualizadas;
- relatórios de produção.

Risco:

O relatório pode continuar correto juridicamente, porém fraco operacionalmente.

---

## 2.3 Backstage ainda subdimensionado

A V2 melhora conceitos, mas não detalha atividades invisíveis:

- abertura e bloqueio de agendas;
- pactuação de vagas;
- glosas;
- auditoria de produção;
- controle contratual;
- gestão de absenteísmo;
- remanejamento de oferta.

Esses pontos são essenciais para blueprint.

---

# 3. Pontos ainda abertos

## 3.1 Fail points incompletos

Continuam pouco explorados:

- perda de vaga por ausência do paciente;
- falha de comunicação entre município e estado;
- encaminhamento inadequado;
- fila sem transparência ao cidadão;
- inconsistência cadastral;
- duplicidade de solicitação;
- falta de contrarreferência.

---

## 3.2 Evidências físicas insuficientes

Ainda faltam elementos observáveis do serviço:

- protocolo de agendamento;
- mensagens SMS/app;
- comprovantes;
- formulários;
- telas dos sistemas;
- documentos entregues ao usuário.

---

## 3.3 Normativos estaduais específicos ausentes

A V2 melhora normas federais, mas ainda precisa aprofundar normas de São Paulo:

- regulamentações SES/SP;
- contratos de gestão estaduais;
- regras CROSS;
- protocolos estaduais de regulação;
- pactuações regionais.

---

# Conclusão da Segunda Auditoria

A V2 corrigiu a maior parte das falhas factuais e normativas identificadas na auditoria V1.

Resultado:

- Correções normativas: **atendidas**;
- Erros factuais principais: **corrigidos**;
- Inferências frágeis: **reduzidas**;
- Modelagem operacional SES/SP: **ainda insuficiente**;
- Service Blueprint AS-IS: **ainda incompleto**.

O principal risco remanescente é produzir um relatório juridicamente correto, porém não operacionalmente fiel à execução real da consulta médica na SES/SP.
