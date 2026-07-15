# M03 Cursor Model Benchmark — Bounded Results (Public)

> **Published bounded results report. This publication presents descriptive observations from one frozen M03 benchmark schedule. It does not establish a general ranking of Cursor models, statistical superiority, or a model recommendation.**

```text
publication_status = published
external_publication_executed = true
publication_channel = github_public_repository
public_repository_name = cursor-model-benchmark-results
publication_tag = m03-bounded-results-v1.0.0
rankings_authorized = false
recommendations_authorized = false
statistical_superiority_claims_authorized = false
source_release_ready_report_sha256 = ac28f2fedf94084459ad2c46e41e62d089eb0834362853ab0cffa1bdd7b257e7
source_execution_seal_sha256 = c9528032128b54b8cc232a74a3d322cb7d9df74967b4581094657ad15a7c1d18
source_analysis_freeze_sha256 = 34637ed9c14f3d9dc3eb91609dd4729ae90b20c86a197b47ff65f9c17e91c284
source_publication_release_freeze_sha256 = 29a38efc967c5a18c7cbb0a58cedc7569dae10f3d4541d1ad150d666830055e2
display_names = resolved campaign mapping (secondary labels only)
model_table_order = alphabetical by requested slug
public_url = https://github.com/m-cahill/cursor-model-benchmark-results
published_at_utc = 2026-07-15T04:28:38Z
```

---
## 1. Executive scope statement

This document summarizes a controlled headless benchmark of four named Cursor model selections on a frozen schedule of four tasks and three repetitions (48 scored slots). First-pass acceptance was the primary metric. Timing and tool-use measures are secondary descriptive appendix fields only.

Conclusions are limited to this frozen schedule, environment freeze, and acceptance gates. This report does not authorize model recommendations, superiority claims, or any broader ranking beyond the observed schedule counts. This report was published externally as a bounded descriptive publication.

---

## 2. Methodology

```text
models = 4 (alphabetical requested slugs listed in section 5)
tasks = 4 (T01–T04)
repetitions = 3
scored slots = 48
fresh workspaces and sessions per slot
hidden evaluator boundary retained
single-shot execution
no corrective prompts
primary metric = first_pass_acceptance_rate
uncertainty = Clopper–Pearson exact binomial interval, two-sided, 95%
```

Model tables appear in alphabetical order by requested model slug.

Requested model slugs are authoritative identifiers. Resolved display names in tables are secondary labels recorded by the frozen campaign mapping; they do not imply provider endorsement or affiliation.
 No performance ordering is applied.

---

## 3. Execution integrity

```text
execution_seal_sha256    = c9528032128b54b8cc232a74a3d322cb7d9df74967b4581094657ad15a7c1d18
campaign_manifest_sha256 = b6e2a31493c2845ae30d525b75248b6995bf6e43e88cfd119becda72f998d8e7
analysis_freeze_sha256   = 34637ed9c14f3d9dc3eb91609dd4729ae90b20c86a197b47ff65f9c17e91c284
completed scored slots   = 48 / 48
inspect-incomplete-attempts = []
scored identity mismatches = 0
frozen-contract drift during scored campaign = false
```

Infrastructure accounting: scored external CLI spawns = 49; scored meaningful executions = 48; one pre-meaningful infrastructure replacement (SLOT-024 A001) did not enter the scored analysis denominator. SLOT-024 A002 is the scored row for that schedule slot.

Source: sealed campaign execution seal; analysis dataset `infrastructure_appendix`.

---

## 4. Overall descriptive result

```text
accepted = 32
eligible = 48
observed proportion = 0.666667 (66.7%)
exact 95% Clopper–Pearson interval = [0.515892, 0.796040]
denominator = 48 predeclared scored schedule slots
```

Source: `frozen M03 descriptive results` → `overall`.

---

## 5. Model-level descriptive results

Alphabetical by requested model slug. Denominator per model = 12 (4 tasks × 3 repetitions).

| Model | Accepted | Eligible | Observed proportion | Exact 95% CP interval |
| --- | ---: | ---: | ---: | --- |
| claude-opus-4-8-high<br>(Opus 4.8 300K High No Thinking) | 9 | 12 | 0.750 | [0.428142, 0.945139] |
| composer-2.5<br>(Composer 2.5) | 9 | 12 | 0.750 | [0.428142, 0.945139] |
| gpt-5.3-codex-high<br>(Codex 5.3 High) | 7 | 12 | 0.583333 | [0.276670, 0.848348] |
| gpt-5.5-high<br>(GPT-5.5 272K High) | 7 | 12 | 0.583333 | [0.276670, 0.848348] |

The observed accepted counts differed by two slots between the 9/12 and 7/12 results. The exact confidence intervals are wide and overlap. No superiority test or general model ranking was authorized.

Source: `frozen M03 descriptive results` → `by_model`.

---

## 6. Task-level results

Task-ID order. Denominator per task = 12.

| Task | Accepted | Eligible | Observed proportion | Exact 95% CP interval |
| --- | ---: | ---: | ---: | --- |
| T01 | 8 | 12 | 0.666667 | [0.348876, 0.900754] |
| T02 | 12 | 12 | 1.000 | [0.735352, 1.000] |
| T03 | 0 | 12 | 0.000 | [0.000, 0.264648] |
| T04 | 12 | 12 | 1.000 | [0.735352, 1.000] |

T02 and T04 recorded acceptance on all scheduled slots. T03 recorded no accepted scheduled slots. T01 recorded eight accepted scheduled slots.

Task composition materially affects overall model proportions because each model’s 12-slot denominator includes all four tasks.

Source: `frozen M03 descriptive results` → `by_task`.

---

## 7. Model × task cells

Each cell denominator = 3 repetitions.

| Model | T01 | T02 | T03 | T04 |
| --- | --- | --- | --- | --- |
| claude-opus-4-8-high<br>(Opus 4.8 300K High No Thinking) | 3/3 | 3/3 | 0/3 | 3/3 |
| composer-2.5<br>(Composer 2.5) | 3/3 | 3/3 | 0/3 | 3/3 |
| gpt-5.3-codex-high<br>(Codex 5.3 High) | 1/3 | 3/3 | 0/3 | 3/3 |
| gpt-5.5-high<br>(GPT-5.5 272K High) | 1/3 | 3/3 | 0/3 | 3/3 |

Exact intervals for n=3 cells are wide. A 3/3 cell still has a non-trivial lower bound gap from certainty; a 0/3 cell still has a wide upper bound.

Source: `frozen M03 descriptive results` → `by_model_task`.

---

## 8. Repetition observations

| Repetition | Accepted | Eligible | Observed proportion |
| --- | ---: | ---: | ---: |
| R1 | 10 | 16 | 0.625 |
| R2 | 10 | 16 | 0.625 |
| R3 | 12 | 16 | 0.750 |

These totals are factual schedule cuts only. No learning, improvement, or regression characterization is authorized.

Source: `frozen M03 descriptive results` → `by_repetition`.

---

## 9. T03 caveat

T03 produced no first-pass acceptances across its 12 scheduled slots. Public tests passed, while the recorded nonacceptances included hidden-test and type-check failures. The frozen task and evaluator identities remained unchanged, and the deterministic Model 0 control remained 10/10. This uniform observed result did not distinguish the four evaluated model selections on T03 and does not, by itself, establish that the task was defective, unfair, or representative of refactoring work generally.

T03 was retained because it was part of the predeclared frozen campaign. Post hoc exclusion would change the predeclared denominator.

```text
T03 eligible in overall denominator = 12 of 48
T03 eligible in each model denominator = 3 of 12
```

A future task-design review may be considered as optional post-M03 work under separate authorization.

Source: `frozen M03 descriptive results` → `t03_observed_execution_pattern`; `frozen M03 T03 assessment`.

---

## 10. Failure taxonomy

Among 16 not-accepted slots, primary failure reasons:

| Primary failure reason | Count |
| --- | ---: |
| hidden_test_failure | 12 |
| public_test_failure | 4 |

Co-occurring gate findings also recorded `type_check_failure` on 12 rows (with the T03 hidden-test nonacceptances).

By task not-accepted counts: T03 = 12; T01 = 4; T02 = 0; T04 = 0.

Source: `frozen M03 failure analysis`.

---

## 11. Timing and tool-use appendix

Correctness was primary. The following fields are secondary descriptive measures only.

Environment caveats for all timing tables:

* sandbox was disabled;
* network conditions were not independently verified;
* service load was uncontrolled;
* models used different tool-call patterns;
* the sample was small (n=48 overall; n=12 per model);
* no fastest-model or efficiency claim is authorized.

Overall medians (observed = 48/48):

| Field | Median | Min | Max |
| --- | ---: | ---: | ---: |
| wall_clock_duration_ms | 61718.5 | 16202 | 164234 |
| cli_duration_ms | 58952 | 13590 | 161340 |
| tool_call_count | 18.5 | 12 | 61 |
| files_changed_count | 10 | 3 | 14 |

Model medians for `wall_clock_duration_ms` (alphabetical; not sorted by duration):

| Model | Median wall_clock_duration_ms |
| --- | ---: |
| claude-opus-4-8-high<br>(Opus 4.8 300K High No Thinking) | 53758.0 |
| composer-2.5<br>(Composer 2.5) | 23429.0 |
| gpt-5.3-codex-high<br>(Codex 5.3 High) | 89000.0 |
| gpt-5.5-high<br>(GPT-5.5 272K High) | 104179.0 |

Source: `frozen M03 descriptive results` → `overall_timing`, `by_model[*].timing`.

---

## 12. Limitations

```text
overall denominator = 48
per-model denominator = 12
per-model × task denominator = 3
confidence interval = Clopper–Pearson exact, two-sided, 95%
```

- Three repetitions per model/task cell are limited.
- A 3/3 cell still has a wide exact interval; a 0/3 cell still has a wide upper bound.
- Overlapping intervals do not establish equivalence.
- Descriptive differences do not establish statistical significance.
- No hypothesis testing was authorized.
- Task composition (especially T03’s uniform nonacceptance) materially affects aggregate model proportions.
- Results apply only to the frozen tasks, evaluators, and environment freeze.
- Cost and GUI workflows are out of scope. Network isolation was not independently verified.
- No composite or weighted score is defined.

---

## 13. Reproducibility hashes

```text
execution_seal_sha256    = c9528032128b54b8cc232a74a3d322cb7d9df74967b4581094657ad15a7c1d18
campaign_manifest_sha256 = b6e2a31493c2845ae30d525b75248b6995bf6e43e88cfd119becda72f998d8e7
analysis_freeze_sha256   = 34637ed9c14f3d9dc3eb91609dd4729ae90b20c86a197b47ff65f9c17e91c284
dataset_content_sha256   = 6d534808ec919dc7a9476788f9f1a0e8bf41a302e35b2ebc2d7470d92a9abcd5
```

Safe governance hashes only. Hidden-test contents, golden patches, raw streams, session IDs, and request IDs are not included.

---

## 14. Nonclaims

This report does **not** claim any ranking, superiority, recommendation, efficiency ranking, cost conclusion, network-isolation proof, or broad generalization beyond the frozen schedule.

The prohibited authorized-claim catalogue is recorded in the publication nonclaims catalogue. External publication executed per M04 publication record.
