# Distinctive Style Markers

Signature phrases, structural conventions, and recognizable patterns unique to Pedro Sant'Anna's writing.

---

## Characteristic Phrases

These phrases appear repeatedly across published papers and serve as stylistic fingerprints.

### Transition and Emphasis Markers
| Phrase | Usage | Example Papers |
|---|---|---|
| "As so," | Transition — introduces a consequence or implication | Parallel Trends Event Study, Doubly Robust DiD |
| "To the best of our knowledge" | Before novelty claims | Treatment Effect Heterogeneity, DiD Multiple Periods |
| "It is worth stressing" / "It is worth mentioning" | Emphasis before an important but non-obvious point | Parallel Trends Event Study, Propensity Score Tests |
| "It is worth emphasizing" | Stronger emphasis variant | Staggered Rollout |

### Contribution and Framing Phrases
| Phrase | Usage |
|---|---|
| "We contribute to the [X] literature in different fronts" | Opening a contribution enumeration |
| "In summary, we contribute to the literature on different fronts" | Closing a contribution summary in the introduction |
| "transparency and objectivity in the analysis" | When citing Rubin (2007, 2008) on design/analysis separation |
| "easy-to-implement" | Describing practical tools and procedures |
| "policy evaluation tools" | Collective term for the methods proposed in a paper |

### Pedagogical Phrases (in Survey/Review Papers)
| Phrase | Usage |
|---|---|
| "fear not!" | Reassuring practitioners before a technical section |
| "In our motivating example," | Introducing the running empirical example |
| "To develop intuition, it is instructive to first consider the special case..." | Before a simplified version of the main result |

### Technical Phrases
| Phrase | Usage |
|---|---|
| "working model" / "working models" | Potentially misspecified parametric models used for estimation |
| "doubly robust for inference" (not just "for consistency") | Distinguishing the double-robustness property for asymptotic variance |
| "forward engineering" | The approach of decomposing what estimands estimate, then building alternatives |
| "causal building block" | The fundamental causal parameter underlying an aggregate estimand |

---

## Paper Architecture Evolution

### Early Career (2016)
```
Generic opening
  → Literature gap
    → Mathematical framework (math-first)
      → Asymptotic theory
        → Monte Carlo
          → Brief application
            → [No conclusion]
```

Characteristics:
- Opening: "Assessing whether a policy has any effect..."
- Passive/deferential tone: "As summarized in Heckman and Vytlacil (2007)..."
- Statistics-oriented vocabulary: Glivenko-Cantelli, Donsker class, Banach space
- Math embedded in running text
- Section titled "Motivating Examples" (statistics convention)
- Software: "R codes are available from the author" (footnote)

### Mature Style (2020+)
```
Empirical hook or direct contribution statement
  → Setup with running example
    → Enumerated contributions
      → Formal "Related Literature" subsection
        → Body with intuition-first, then formal results
          → Empirical application (woven through from introduction)
            → Software announcement
              → Conclusion / Implications for Practice
```

Characteristics:
- Opening: "This paper proposes/derives/shows..." or quantified empirical hook
- Assertive tone: "We derive necessary and sufficient conditions"
- Econometrics-centered vocabulary: ATT, parallel trends, selection bias
- Intuition before math: "At the practical level..." / "Heuristically,..."
- Section titled "Framework" or "Setup" (econometrics convention)
- Software: Named R/Stata package with GitHub URL

### Key Transition Markers Between Periods
| Feature | 2016 | 2020+ |
|---|---|---|
| Opening sentence | Generic motivation | Direct contribution |
| First equation | Page 1–2 | After intuitive setup |
| Running example | None | Threaded from introduction |
| Contribution list | None | Numbered, explicit |
| Literature section | Woven through intro | Formal subsection |
| Software | Footnote | Named package + URL |
| Conclusion | Absent or minimal | "Implications for Practice" section |
| Tone | Deferential | Authoritative |

---

## Survey/Review Paper Style

When writing a survey or synthesis paper (as in "What's Trending in DiD?"), use:

### Taxonomic Organization
Structure the paper around a "canonical model + relaxations" framework:
> "We argue that recent advances in DiD methods can be broadly classified as relaxing some components of the canonical DiD setup, with a focus on (i) multiple periods and variation in treatment timing, (ii) potential violations of parallel trends, or (iii) alternative frameworks for inference."

### Boxed Recommendations
Include "Recommendations" boxes at the end of each section with concrete, actionable guidance for practitioners. These boxes should be self-contained — a practitioner should be able to read only the boxes and get a complete guide.

### Running Example
Thread a single empirical example from the introduction through every section:
> "In our motivating example, tau_2 would be the average effect of Medicaid expansion on insurance coverage..."

### Software Tables
Include a table of statistical packages with:
- Package name
- Language (R/Stata/Python)
- GitHub or CRAN link
- Which methods from the paper each package implements

### Practitioner Checklists
Provide a checklist (as a table) of steps practitioners should follow when using the methods reviewed in the paper.

### Conversational Tone
In surveys only, a more conversational tone is appropriate. "Fear not!" and "Readers interested in X can safely skip Y" are acceptable.

---

## Acknowledgment Patterns

### Standard Elements
- Seminar and conference presentation venues (listed)
- Research assistants named
- Editor and referees thanked: "the editor and two referees for their constructive comments which have led to an improved paper"
- Funding sources

### Modern Addition (2025+)
Transparency about AI and writing tools:
> "We used Grammarly for grammar checking, Github Co-Pilot for coding assistance, and refine.ink for a final proofreading check."

### Charming Details
Occasional attribution for non-obvious contributions:
> "We thank Scott Barkowski for suggesting the title." (What's Trending in DiD?)

---

## The "Robustness vs. Efficiency" Trade-Off Label

A recurring framing device in multiple papers:

**Paper: Parallel Trends Event Study (JAERE 2021)**
The paper documents a "robustness vs. efficiency" trade-off between different parallel trends assumptions. This labeling makes the abstract trade-off concrete and memorable.

**Paper: Staggered Rollout (JPE:Micro 2023)**
The efficiency dominance result is framed as resolving this trade-off: the efficient estimator dominates without sacrificing robustness.

When a paper involves choosing between assumptions or methods, explicitly label the trade-off.

---

## Notation Conventions

| Convention | Usage |
|---|---|
| Y(0), Y(1) | Potential outcomes |
| D or T | Treatment indicator (T preferred in duration contexts to avoid confusion) |
| p(X) | Propensity score |
| ATT | Average treatment effect on the treated |
| DiD | Difference-in-differences (not DID or DnD) |
| TWFE | Two-way fixed effects |
| G | Group indicator (treatment timing group) |
| t | Time period |

Note the D → T shift in duration papers: "We changed the treatment indicator from D to T to avoid confusion with duration-related uses of D" (Treatment Effect Heterogeneity paper).
