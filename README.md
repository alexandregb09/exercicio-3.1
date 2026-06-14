# Exercício 3.1 — Service Blueprint AS-IS de um Serviço Público

**Aluno:** *Alexandre Garcia Bezerra*
**Disciplina:** IDP-TD 2026
**Serviço escolhido:** Consulta medicas na Secretaria de Estado de Saúde de SP

\---

## Índice dos entregáveis

### Parte A — Meta-prompt

* [A\_meta\_prompt.md](A_meta_prompt.md) — meta-prompt usado para iniciar a deep research que subsidia o blueprint AS-IS

### Parte B — Deep research adversarial (v1 → audit\_v1 → v2 → audit\_v2 → v3)

* [B\_relatorio\_assistente\_v1.md](B_relatorio_assistente_v1.md) — pesquisa original do assistente 1 (como o serviço opera hoje)
* [B\_relatorio\_auditoria\_v1.md](B_relatorio_auditoria_v1.md) — auditoria da v1 pelo assistente 2
* [B\_relatorio\_assistente\_v2.md](B_relatorio_assistente_v2.md) — revisão do assistente 1 após audit\_v1
* [B\_relatorio\_auditoria\_v2.md](B_relatorio_auditoria_v2.md) — segunda auditoria (sobre a v2) pelo assistente 2
* [B\_relatorio\_assistente\_v3.md](B_relatorio_assistente_v3.md) — versão final do assistente 1 após audit\_v2

### Parte C — Service Blueprint AS-IS via `/grill-me`

* [C\_grill\_transcript.md](C_grill_transcript.md) — transcript integral da sessão `/grill-me`
* [C\_blueprint\_asis.md](C_blueprint_asis.md) — Service Blueprint **AS-IS** elaborado conceitualmente (camadas + linhas + fail points)

### Parte D — Diagrama

* [D\_diagrama\_asis.md](D_diagrama_asis.md) — diagrama da jornada a partir dos itens da Parte C (mermaid)

\---

## Configuração do autograder

* Marcador presente: [`.autograde-exercise`](.autograde-exercise) (conteúdo: `3.1`)

Para validar localmente:

```bash
autograde validar 3.1
```

