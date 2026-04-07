# Framing and Motivation Patterns

How Sant'Anna frames problems, builds intuition, and motivates results in his mature writing.

---

## Pattern 1: Solution Framing, Not Problem Framing

Frame challenges as design choices, not obstacles.

**Paper: DiD Multiple Periods (v1 → JoE 2021)**
> PROBLEM-ORIENTED (v1): "in some applications there are perhaps too many group-time ATTs, potentially making the analysis of the effectiveness of the policy intervention harder"
>
> SOLUTION-ORIENTED (published): "Our framework acknowledges that in some applications there may be many group-time average treatment effects and researchers may want to aggregate them into different summary causal effect measures."

The v1 describes a problem ("too many," "harder"). The published version describes a feature ("may want to aggregate") — the same fact reframed as an opportunity.

**Paper: DiD Continuous Treatment (v1 → published)**
> PROBLEM (v1): "interpreting differences in these parameters across different values of the treatment can be particularly challenging"
>
> SOLUTION (published): "comparing these parameters across treatments is challenging because parallel trends does not rule out selection bias" + "We discuss alternative, typically stronger, assumptions that eliminate selection bias."

The published version names the mechanism (selection bias) and immediately offers the solution (stronger assumptions that eliminate it).

---

## Pattern 2: Intuition Before Math

After a technical result, add a plain-language "heuristic" summary paragraph.

**Paper: Covariate Balance (published in JAE 2022)**
After the formal minimum-distance framework, the published version adds:
> "At the practical level, one can think of the IPS as an estimation procedure that attempts to estimate the unknown finite dimensional parameters of a PS model by making the underlying entire covariate distribution of different treatment groups as close to each other as possible."

The key phrase is **"At the practical level"** — it signals a shift from formal to intuitive exposition.

**Abstract version of the same pattern:**
> "Heuristically, our proposed procedure attempts to estimate a propensity score model by making the underlying covariate distribution of different treatment groups as close to each other as possible."

The **"Heuristically,..."** opener is a reliable signal that an intuitive restatement follows.

**Paper: Staggered Rollout (published in JPE:Micro 2023)**
The published version frames the two-period case explicitly as pedagogical:
> "To develop intuition, it is instructive to first consider the special case... This special case is analogous to conducting a randomized experiment in period 2, with the outcome in period 1 serving as a pre-treatment covariate."

This grounds the full staggered design in a simple, familiar case before introducing generality.

---

## Pattern 3: RCT Analogy

When discussing observational methods, draw an explicit parallel to what randomization achieves.

**Paper: Covariate Balance (published in JAE 2022)**
> "Indeed, the balancing property of the propensity score resembles randomization: when the data come from a randomized control trial (RCT) with perfect compliance, the entire covariate distributions among different treatment groups are balanced and, therefore, all measurable, integrable functions of the covariates are indeed balanced."

This bridges the gap between what RCTs do by design and what the proposed method tries to approximate from observational data.

**Paper: Staggered Rollout (published in JPE:Micro 2023)**
The published version adds concrete empirical examples of papers justifying quasi-random timing:
> "This special case is analogous to conducting a randomized experiment in period 2..."

And cites Fadlon and Nielsen (2021), Deshpande and Li (2019), Parker et al. (2013) as examples where researchers justified this assumption.

**The Rubin Citation:**
A recurring pattern is to cite Rubin (2007, 2008) on separating design from analysis:
> "As advocated by Rubin (2007, 2008), this separation is useful as it simultaneously mimics RCTs and avoids potential data snooping problems."

---

## Pattern 4: Forward Engineering Framing

For papers critiquing TWFE and proposing alternatives, use the "forward engineering" frame.

**Paper: DiD Continuous Treatment (published version)**
> "The ideas discussed above are in the spirit of what Mogstad and Torgovitsky (2024) call forward engineering."

Forward engineering = decompose what popular estimands actually estimate → show their limitations → build alternatives that are interpretable by construction.

This positions the paper as constructive rather than merely critical. It is not just saying "TWFE is bad" but "here is how to build something better from first principles."

---

## Pattern 5: The "No-Free-Lunch" Framing

When a paper establishes impossibility or necessity results, frame them as revealing trade-offs.

**Paper: Selection and Parallel Trends (v14, working paper)**
> "We show that parallel trends holds for all selection mechanisms in this class if and only if the untreated potential outcome is constant across time up to deterministic mean shifts. This result shows that if one is not willing to restrict selection into treatment, then one needs to essentially rule out time-varying unobservables."

The "no-free-lunch" label makes the necessity result memorable and its practical implications immediately clear.

**Paper: Parallel Trends Functional Form (Econometrica 2023)**
The published version offers a "menu of options" framework:
> "Researchers who wish to point-identify the ATT should justify one of the following: (i) why treatment is randomly assigned, (ii) why the chosen functional form is correct, or (iii) a method for inferring the entire counterfactual distribution."

This transforms a negative result (you can't avoid functional form) into a constructive guide (here are your three options).

---

## Pattern 6: From Method-Centric to Purpose-Centric Description

Describe what the method *achieves for the researcher*, not what it *does technically*.

**Paper: Covariate Balance (v1 → JAE 2022)**
> METHOD-CENTRIC (v1): "estimates the propensity score by fully exploiting its covariate balancing property"
>
> PURPOSE-CENTRIC (published): "aims to maximize the covariate distribution balance among different treatment groups"

**Paper: Propensity Score Tests (v1 → JoE 2019)**
> METHOD-CENTRIC (v1): "introduces new nonparametric diagnostic tools for detecting propensity score misspecification"
>
> PURPOSE-CENTRIC (published): "proposes new nonparametric diagnostic tools to assess the asymptotic validity of different treatment effects estimators that rely on the correct specification of the propensity score"

The v1 describes the tool (detecting misspecification). The published version describes what the tool enables (assessing estimator validity) — the thing the applied researcher actually cares about.

---

## Pattern 7: The "Practitioners" Bridge

Published versions consistently add practitioner-oriented framing absent from v1 drafts.

**Paper: DiD Multiple Periods (published in JoE 2021)**
> v1: Focuses on estimation theory
>
> Published: Adds "different aggregation schemes that can be used to highlight treatment effect heterogeneity across different dimensions as well as to summarize the overall effect of participating in the treatment"

**Paper: Selection and Parallel Trends (v14)**
> v1: "providing the formal underpinnings for justifying DiD"
>
> Latest: "easy-to-implement strategies for benchmarking its components. We also provide templates for justifying DiD in applications with and without covariates."

"Easy-to-implement strategies" and "templates" are concrete deliverables. "Formal underpinnings" is abstract.

**Paper: What's Trending in DiD? (published in JoE 2023)**
Uses boxed "Recommendations" sections, practitioner checklists, and the phrase "fear not!" to reassure applied readers when discussing technical results.

---

## Pattern 8: Connecting Separate and Nonseparable Models

In papers that cover both separable and nonseparable outcome models, discuss the distinction in the body but remove it from the abstract.

**Paper: Selection and Parallel Trends**
> v1 abstract: "We provide results for both separable and nonseparable outcome models and show that this distinction has implications for the use of covariates in DiD analyses."
>
> Published abstract: [Removed — the distinction is covered in the body]

The abstract should present contributions in terms of *practical implications*, not *model classes*.
