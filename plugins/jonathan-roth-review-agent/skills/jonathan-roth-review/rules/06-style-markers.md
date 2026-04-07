# Distinctive Style Markers

## Characteristic Phrases

### Problem-Identification Phrases
| Phrase | Usage | Example Papers |
|---|---|---|
| "common practice" | Opening: identifying what researchers do | Pre-test, Logs |
| "hidden assumption" | Revealing what's implicit in standard approaches | Research statement, Design-Based |
| "two important limitations" / "two limitations" | Structuring the problem | Pre-test |
| "remarkably common" | Quantifying prevalence of the practice | Pre-test |

### Impossibility/Result Phrases
| Phrase | Usage |
|---|---|
| "trilemma" | Named three-way impossibility result |
| "sharp null of full mediation" | Named testable hypothesis |
| "there is no treatment effect parameter that is..." | Impossibility statement with enumerated properties |
| "it is thus impossible to construct" | Formal impossibility claim |

### Solution/Alternative Phrases
| Phrase | Usage |
|---|---|
| "several alternative approaches" | Opening a menu of options |
| "practical recommendations" | Labeling actionable guidance |
| "sensitivity analysis" | Framing robustness as formal analysis |
| "credible" / "more credible approach" | Describing improved methodology |

### Transition and Emphasis
| Phrase | Usage |
|---|---|
| "Taken together" | Synthesizing multiple results |
| "In other words" | Restating a technical result in plain language |
| "We further establish" | Introducing an additional result |
| "An advantage of our approach" | Comparing to existing methods |

## Paper Architecture

### Roth's Mature Style (2022+)
```
Question or problem identification (often in title)
  -> Common practice description with quantified survey
    -> Hidden limitations/assumptions revealed
      -> Named impossibility result (if applicable)
        -> Menu of constructive alternatives
          -> Formal results in body
            -> Empirical illustration(s)
              -> Practical recommendations
                -> Software announcement
```

### Paper Architecture Evolution

#### Early Career / Working Paper Stage (2018)
```
Question title or technical title
  → Detailed technical abstract with math notation
    → Extended background motivation
      → Technical results
        → Monte Carlo simulations
          → Brief application
```

Characteristics:
- Title: question format ("Should We Condition on the Test for Pre-trends?")
- Abstract: walks through cases step by step
- Hedging: "I analyze the properties of... conditional on having passed"
- Uses "I" naturally for solo work

#### Mature Style (2022+)
```
Question or cautionary title
  → Common practice description with quantified survey
    → Hidden limitations revealed (numbered)
      → Named impossibility result (if applicable)
        → Menu of constructive alternatives
          → Empirical illustration(s)
            → Practical recommendations section
              → Software announcement
```

Characteristics:
- Title: catchier, more directive ("Pretest with Caution" instead of "Should We Condition...")
- Abstract: high-level problem framing, no math
- Confident voice: "We establish," "We develop," "We show"
- "Related Literature" as a formal subsection
- Software packages with GitHub URLs

### Key differences from Sant'Anna:
| Dimension | Sant'Anna | Roth |
|---|---|---|
| Opening | "This paper proposes/derives..." | Common practice -> hidden problem |
| Title style | Descriptive statements | Questions or cautionary phrases |
| Core framing | Solution-first | Critique-then-construct |
| Impossibility results | "No-free-lunch" | Named "trilemma" with enumerated menu |
| Contribution style | "We contribute in different fronts" | "This paper highlights/develops/establishes" |
| Sensitivity | Efficiency results | Sensitivity analysis as philosophy |
| Tone | Authoritative | Authoritative but with pedagogical warmth |
| Solo papers | Always "we" | "I" for solo work |

## Question Titles
A distinctive Roth pattern. Several papers use question titles:
- "Logs with zeros? Some problems and solutions"
- "Should We Condition on the Test for Pre-trends?" (v1 title)
- "When Is Parallel Trends Sensitive to Functional Form?"
- "What's Trending in Difference-in-Differences?"

The question is answered in the abstract and the paper body provides the proof.

## Software Packages
Roth consistently announces software:
- HonestDiD (R + Stata) -- sensitivity analysis for parallel trends
- pretrends (R + Stata) -- pretesting diagnostics
- staggered (R + Stata) -- efficient staggered estimation
- TestMechs (R) -- testing mechanisms
- LinearMomentInequalities (Matlab) -- conditional moment inequalities

## Acknowledgment Patterns
- Detailed seminar venue lists
- Named co-editors and referees
- NSF funding acknowledged
- AI tools: Not mentioned (as of 2024 papers)

### Notation Conventions

| Convention | Usage |
|---|---|
| Y(0), Y(1) | Potential outcomes |
| D | Treatment indicator |
| Z | Instrument |
| X | Covariates |
| DiD | Difference-in-differences (not DID) |
| ATT | Average treatment effect on the treated |
| TWFE | Two-way fixed effects |
| ATE | Average treatment effect |
| LATE | Local average treatment effect |
| (i), (ii), (iii) | Numbering alternatives in menus |
