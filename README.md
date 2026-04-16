# Data Analysis of Reported Rape Cases in India  
### Data Science Toolbox (Python Programming) — Academic Project Framework

## 1) Final Project Title Options
1. **Reported Rape Cases in India (2001–Latest Available): Trends, Reporting Limits, Legal Outcomes, and Evidence-Based Interpretation**
2. Reported Sexual Violence in India: A Data-Driven and Ethical Analysis of Trends, Reporting, and Justice Outcomes
3. Understanding Reported Rape Statistics in India: Time Trends, State Patterns, and Limits of Inference

## Strong Final Project Title (Recommended)
**Reported Rape Cases in India (2001–Latest Available): Trends, Reporting Dynamics, Legal Outcomes, and Evidence-Based Limits**

## Narrowed Research Scope (Recommended)
- Primary focus: **reported rape cases under IPC (and clearly labeled legal definitions/time changes)** using NCRB/state-level data.
- Time frame: **2001 to latest year with complete NCRB publication**.
- Units of analysis: **India (national) + states/UTs**.
- Secondary evidence (clearly separated): underreporting context (NFHS/peer-reviewed studies), victim impact literature, legal framework, and selected case studies.
- Strictly descriptive/analytical approach: **no unsupported causal claims**.

## 2) Research Objectives
1. Quantify temporal trends in reported rape cases at national and state levels.
2. Compare reporting patterns across states/UTs and across government periods descriptively.
3. Analyze justice-process indicators (chargesheeting, conviction, acquittal, pendency) where available.
4. Clarify what official data can and cannot establish about underreporting and “false cases.”
5. Integrate legal provisions and victim-impact literature in an ethically responsible, evidence-based narrative.

## 3) Research Questions
1. How have reported rape cases changed yearly (and decade-wise) in India and across states?
2. Which states show consistently high/low reported rates and how stable are rankings?
3. What do available indicators suggest about justice delivery (chargesheeting/conviction/pendency)?
4. What can reliable sources say about underreporting, and what remains unmeasurable?
5. How should trends be interpreted considering legal reforms, reporting behavior, and social factors?
6. How do trends compare across selected government periods (descriptive, not causal)?

## 4) What Data You Can Realistically Collect
- NCRB Crime in India yearly tables (state-wise and national reported rape cases; disposal/conviction metrics where available).
- Population denominators (Census/projections) for per-100,000 rates.
- Government/legal timeline data (major amendments, e.g., Criminal Law Amendment 2013).
- NFHS indicators relevant to violence disclosure/help-seeking context (survey-based, not police-recorded incidence).
- Court/justice process aggregates where publicly available from official datasets/reports.

## 5) What Data You Cannot Reliably Claim
- **Exact national underreporting percentage for rape from police records alone**: *No reliable official measure available*.
- **Daily/monthly rape counts for all years/states** from NCRB annual publications: often unavailable/inconsistent in public consolidated format.
- “True vs false case ratio” as factual truth: police “false” classification, acquittals, and closure categories are not equivalent.
- Direct causal attribution of trend changes to one government or one law without robust causal design and evidence.

## 6) Recommended Datasets and Sources
- **NCRB Crime in India** (primary official crime statistics).
- **data.gov.in** (official downloadable datasets, including NCRB-linked resources).
- **MHA / MoWCD / MoHFW** publications and dashboards.
- **NFHS** reports and unit-level documentation (for survey context).
- **India Code** (statutory legal provisions and amendments).
- Peer-reviewed literature (underreporting context, trauma, barriers to justice).

## 7) Best Variables/Columns for CSV Files
Core trend file:
- `year`, `state_ut`, `reported_rape_cases`, `population`, `rape_rate_per_100k`

Justice outcome file:
- `year`, `state_ut`, `cases_for_investigation`, `chargesheeted_cases`, `chargesheeting_rate`
- `trials_completed`, `convicted_cases`, `acquitted_cases`, `conviction_rate`
- `cases_pending_investigation`, `cases_pending_trial`

Legal/policy timeline file:
- `date`, `law_or_policy`, `description`, `expected_reporting_effect_note`

Metadata fields:
- `source_name`, `table_number`, `source_url`, `download_date`, `notes_on_definition_changes`

## 8) Python Analysis Plan (Pandas, NumPy, Matplotlib, Seaborn)
1. Ingest CSVs with strict dtypes and missing-value handling.
2. Standardize state/UT names across years.
3. Compute yearly growth (% change), CAGR, rolling averages.
4. Create per-capita rates and state comparisons.
5. Merge legal timeline markers for annotated visualizations.
6. Build reproducible plotting functions for trend/state/outcome charts.

## 9) EDA Plan
- Missingness map by variable/year/state.
- Outlier checks for abrupt jumps and definition changes.
- Distribution of state-level rates (boxplots/histograms).
- Correlation matrix only for descriptive exploration (no causal claims).
- Data dictionary and consistency audit log.

## 10) Statistical and Trend Analyses
- Year-over-year percentage increase/decrease.
- Decade-wise aggregates and relative changes.
- Rolling trend smoothing (e.g., 3-year moving average).
- Rank stability analysis by state (Spearman rank over years).
- Pre/post descriptive comparison around major legal reform years.
- Optional robust trend: segmented linear fit (clearly labeled exploratory).

## 11) Suggested Charts/Graphs
- National yearly line chart (reported cases + rate per 100k).
- State-wise heatmap (`state x year` rates).
- Top/bottom state trend faceted lines.
- YoY change bar chart (national and selected states).
- Chargesheeting/conviction/pendency trend lines.
- Government-period comparison bars with confidence/uncertainty notes.
- Annotated timeline chart with legal reform markers.

## 12) Government-Period Comparison Methodology (Descriptive Only)
1. Define periods transparently (e.g., by election/government tenure years).
2. Compute per-period averages, medians, and growth metrics.
3. Compare reported cases and rates, plus justice indicators where available.
4. Include caveats: legal changes, reporting behavior, policing variation, state-subject nature of law and order.
5. Explicitly avoid causal claims (“Period A caused X”).

## 13) Legal Punishment Section (Indian Law)
- Cover IPC provisions for rape and related offences, and relevant CrPC/procedural points.
- Include amendment timeline (especially post-2012 reforms).
- Explain sentencing ranges, aggravated categories, and statutory minimums/maximums.
- Compare legal framework with observed outcome metrics (conviction/pendency), without overclaiming.
- Source strictly from India Code and official legal texts.

## 14) Victim Perspective Section (Research Literature)
- Trauma and post-assault mental-health consequences (peer-reviewed evidence).
- Reporting barriers: stigma, fear, retaliation, institutional distrust, economic dependence.
- Access-to-justice barriers and secondary victimization risks.
- Recovery and support systems (medical, psychosocial, legal aid) with evidence.
- Language rule: empathetic, non-sensational, dignity-preserving.

## 15) Highlighted Case Studies Section
For each case:
- `case_name`, `year`, `brief_context` (non-graphic), `legal_outcome`, `sentence`, `policy_or_social_impact`, `source_references`.
- Select only widely documented cases with credible legal/reporting records.
- Do not disclose unnecessary survivor-identifying details.

## 16) Limitations and Ethical Considerations
- Reported cases ≠ true incidence.
- Underreporting is structurally significant but often not directly measurable from police data.
- Legal definitions and recording practices change over time.
- Acquittal does not imply false allegation.
- State comparability may be affected by reporting systems and access differences.
- Use survivor-respecting language and avoid sensationalism.

## 17) Suggested Final Report Chapter Structure
1. Introduction and Motivation  
2. Scope, Definitions, and Ethics  
3. Data Sources and Data Quality  
4. Methods (EDA + Trend Analysis)  
5. National Trend Findings  
6. State-wise Comparative Findings  
7. Justice Process Outcomes  
8. Government-Period Descriptive Comparison  
9. Legal Framework and Punishment Analysis  
10. Underreporting, False-Case Misinterpretations, and Evidence Limits  
11. Victim Perspective from Literature  
12. Highlighted Case Studies  
13. Discussion, Limitations, and Responsible Interpretation  
14. Conclusion and Policy-Relevant Insights  
15. References and Appendices

## 18) Beginner-Friendly Coding Workflow in Python
1. Create project folders: `data/raw`, `data/processed`, `notebooks`, `src`, `outputs/figures`.
2. Load and inspect each dataset (`pd.read_csv`, `df.info()`, `df.head()`).
3. Clean columns and harmonize state names.
4. Build one master analysis table by year-state.
5. Compute key metrics (rates, YoY %, rolling averages).
6. Produce one chart per research question.
7. Save processed data and figures with clear filenames.
8. Write interpretation below each chart with “what we know / what we cannot claim.”
9. Compile notebook outputs into final report chapters.

## 19) Question Answerability Matrix
| Question Type | Status | Why |
|---|---|---|
| National yearly trend in reported rape cases | **Answerable** | Directly available in NCRB annual data |
| State-wise comparison of reported rates | **Answerable** | NCRB + population denominator |
| Annual increase/decrease percentages | **Answerable** | Computable from yearly totals |
| Decade-wise trend summaries | **Answerable** | Computable from annual series |
| Daily/monthly all-India long-term trends | **Partially answerable** | Not consistently available in one official longitudinal dataset |
| Exact underreporting percentage | **Not answerable (officially exact)** | No single reliable official measure from police records |
| “True vs false case ratio” | **Not answerable as stated** | Definitions differ; acquittal/closure/false classification are not equivalent |
| Effect of legal reforms on reporting | **Partially answerable** | Descriptive pre/post possible; causal proof requires stronger design |
| Government responsible for increase/decrease | **Not answerable causally** | Multiple confounders; only descriptive period comparison valid |
| Conviction/pendency pattern over time | **Partially to fully answerable** | Depends on year-wise consistency of available justice metrics |

## Realistic Dataset Plan
1. **Primary panel dataset** (`year x state_ut`): reported cases, population, rate.
2. **Justice outcome dataset** (`year x state_ut`): chargesheeting/conviction/acquittal/pendency (where available).
3. **Legal-policy timeline dataset**: key amendment/policy dates and references.
4. **Context dataset**: selected NFHS/survey indicators and metadata (kept separate from police data).

## High-Quality Project Synopsis
This project presents an evidence-based analysis of **reported rape cases in India** using official crime statistics, supported by legal texts and carefully separated survey/literature context. It quantifies national and state trends, analyzes year-over-year and decade-level changes, and examines justice-system indicators such as chargesheeting, conviction, and pendency where available. The study explicitly distinguishes recorded crime trends from true incidence and highlights underreporting as a critical but not exactly measurable factor in official records. A descriptive comparison across government periods is included with strict caution against causal attribution. The report integrates legal punishment provisions and survivor-centered literature to ensure ethically responsible interpretation. The final output is a reproducible Python-based analysis and an academically structured report emphasizing transparency, limitations, and methodological integrity.

## Step-by-Step Roadmap for Execution
1. Finalize scope, definitions, and research questions.
2. Download and catalog official datasets and legal sources.
3. Build data dictionary and source traceability sheet.
4. Clean/standardize data; document missingness and definition changes.
5. Generate core trend and state comparison metrics.
6. Perform justice outcome analysis (if data completeness permits).
7. Conduct descriptive government-period comparison with caveats.
8. Integrate legal framework analysis from India Code.
9. Add victim-perspective synthesis from peer-reviewed literature.
10. Draft case studies using credible, dignity-preserving summaries.
11. Write limitations/ethics chapter with explicit non-claim statements.
12. Finalize report, references, and reproducible notebook/code appendix.
