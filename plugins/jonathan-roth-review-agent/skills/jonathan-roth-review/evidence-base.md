# Evidence Base

Paper-by-paper summary of evidence supporting each rule.

## Paper Index
| # | Short Title | ArXiv | Versions | Published | Journal | Revision Magnitude |
|---|---|---|---|---|---|---|
| 01 | Logs with Zeros | 2212.06080 | 7 | Nov 2023 | QJE 2024 | Major |
| 02 | Pre-test with Caution | 1804.01208 | 2 + title change | 2022 | AER: Insights | Transformative |
| 03 | Honest Parallel Trends | -- | Multiple drafts | 2023 | REStud | Major |
| 04 | Testing Mechanisms | 2404.11739 | 3 | Forthcoming | REStud | Moderate |
| 05 | Design-Based Uncertainty | 2008.00602 | 8 | Forthcoming | JASA | Major |
| 06 | Moment Inequalities | 1909.10062 | 5 | 2023 | REStud | Major |
| 07 | Staggered Rollout | 2102.01291 | -- | 2023 | JPE:Micro | Major (co-authored with Sant'Anna) |
| 08 | Parallel Trends FF | 2010.04814 | -- | 2023 | Econometrica | Major (co-authored with Sant'Anna) |
| 09 | What's Trending | 2201.01194 | -- | 2023 | JoE | Minor (co-authored with Sant'Anna) |
| 10 | Interpreting Event-Studies | 2401.12309 | 2 | 2026 | JER | Minor |

## Key Revision Insights by Paper

### 01 -- Logs with Zeros (MOST DISTINCTIVE ROTH PAPER)
- **Title**: Question format "Logs with zeros?" is catchy and immediately frames the problem
- **Abstract**: v1 includes math notation (theta_g), technical detail -> v7 restructured around "trilemma" concept
- **Key addition**: Named impossibility result "trilemma" -- three desirable properties that can't all hold
- **Menu of alternatives**: (i) Poisson regression, (ii) calibrate margins, (iii) Lee bounds
- **7 versions** over 11 months -- extensive polish
- **Rules sourced**: Named impossibility (04-framing S2), menu of alternatives (04-framing S3), abstract compression (01-abstract S3)

### 02 -- Pre-test with Caution (MOST DRAMATIC TRANSFORMATION)
- **Title change**: "Should We Condition on the Test for Pre-trends in Difference-in-Difference Designs?" -> "Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends"
- **Abstract**: Completely rewritten. v1 is technical (walks through valid/invalid DiD cases, monotone trends). Published is high-level problem framing ("two important limitations...First...Second...")
- **Quantified survey**: "70 papers" in leading journals
- **Practical recommendations**: Dedicated Section III
- **Software**: pretrends R and Stata packages
- **Solo author**: Uses "I" throughout -- distinctive
- **Rules sourced**: Title evolution (05-revision S-Title), problem-first framing (04-framing S1), quantified surveys (04-framing S5)

### 03 -- A More Credible Approach to Parallel Trends
- **No ArXiv** but multiple draft versions exist
- **Flagship paper**: Defines the sensitivity analysis approach to parallel trends
- **Software**: HonestDiD R and Stata packages
- **"Credible" in title**: The word "credible" is a Roth signature
- **Rules sourced**: Sensitivity framing (04-framing S4), software (02-introduction S8)

### 04 -- Testing Mechanisms
- **Abstract**: v1 long and explanatory -> v3 compressed with "exploits connections" phrasing
- **Named concept**: "sharp null of full mediation"
- **Advantage framing**: "An advantage of our approach relative to existing tools... is that it does not require stringent assumptions"
- **Rules sourced**: Abstract compression (01-abstract S3), named results (04-framing S2)

### 05 -- Design-Based Uncertainty (8 VERSIONS, 5 YEARS)
- **Abstract**: v1 "Social scientists are often interested in" -> v8 "Design-based frameworks of uncertainty are frequently used" (specific field context)
- **Reframing**: v1 descriptive (SDIM, DiD, 2SLS properties) -> v8 constructive (sensitivity analysis, "rich forms of selection")
- **Practitioner bridge**: v8 adds "more closely aligns with the way empirical researchers discuss the variation in the data"
- **Rules sourced**: Throat-clearing removal (01-abstract S1), sensitivity framing (04-framing S4)

### 06 -- Inference for Linear Conditional Moment Inequalities
- **Abstract**: v1 "We consider inference based on" -> v5 "We show that moment inequalities in a wide variety of economic applications have a particular linear conditional structure"
- **Reframing**: From "we consider" (exploratory) to "we show" (definitive)
- **Software**: LinearMomentInequalities Matlab package
- **Rules sourced**: Voice confidence (03-terminology S-Active Voice)

### 07 -- Staggered Rollout (with Sant'Anna)
- **Abstract**: 170->90 words (47% reduction). "Researchers are often interested in" -> "We study"
- **Self-promotion removed**: "most precise estimates to date" cut
- **Terminology**: "(as-if) randomly assigned" -> "as-good-as randomly assigned"
- **Software**: staggered R and Stata packages
- **Note**: Roth is first author. Patterns overlap with Sant'Anna's rules but compression rate matches Roth's other papers.
- **Rules sourced**: Throat-clearing (01-abstract S1), self-promotion (01-abstract S5), terminology (03-terminology)

### 08 -- Parallel Trends Functional Form (with Sant'Anna)
- **Abstract**: 170->100 words (41% reduction). "monotonic" -> "strictly monotonic"
- **Three-option menu**: Maintained from v1 to published
- **Falsification tests**: Major addition in published version
- **Note**: Roth is first author. The "menu of options" framing is distinctively Roth.
- **Rules sourced**: Menu of alternatives (04-framing S3), falsification tests (05-revision S-Add 6)

### 09 -- What's Trending in DiD (with Sant'Anna, Bilinski, Poe)
- **Abstract**: Virtually identical v1 to published (rare)
- **Major additions**: Medicaid running example, triple differences section
- **Survey format**: Taxonomic organization (canonical model + relaxations)
- **Boxed recommendations**: Throughout each section
- **Quantified motivation**: "over 30% of NBER papers"
- **Rules sourced**: Running example (02-introduction S4), quantified surveys (04-framing S5)

### 10 -- Interpreting Event-Studies
- **Solo author**: Uses implied "I" / third person
- **Practical focus**: Provides guidance for interpreting event-study plots from new DiD methods
- **Short paper**: 2 versions, minor changes
- **Rules sourced**: Practical recommendations (04-framing S6)
