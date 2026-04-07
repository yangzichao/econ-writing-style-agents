# Writing Style Analysis: Covariate Distribution Balance via Propensity Scores

## Paper Info
- Authors: Pedro H.C. Sant'Anna, Xiaojun Song, Qi Xu
- ArXiv v1 date: October 2, 2018 (document dated November 21, 2019)
- Published: Journal of the American Statistical Association (JASA), 2022 (final version dated November 9, 2021)

## Abstract Comparison

### v1 Abstract
"The propensity score plays an important role in causal inference with observational data. Once the propensity score is available, one can use it to estimate a variety of causal effects in a unified setting. Despite this appeal, a main practical difficulty arises because the propensity score is usually unknown, has to be estimated, and extreme propensity score estimates can lead to distorted inference procedures. To address these limitations, this article proposes to estimate the propensity score by fully exploiting its covariate balancing property. We call the resulting estimator the integrated propensity score (IPS) as it is based on integrated moment conditions. In sharp contrast with other methods that balance only some specific moments of covariates, the IPS aims to balance all functions of covariates. Further, the IPS estimator is data-driven, does not rely on tuning parameters such as bandwidths, admits an asymptotic linear representation, and is sqrt(n)-consistent and asymptotically normal. We derive the asymptotic properties of inverse probability weighted estimators for the average, distributional and quantile treatment effects based on the IPS, and illustrate their relative performance via Monte Carlo simulations and three empirical applications. An implementation of the proposed methods is provided in the new package IPS for R."

### Final Abstract
"This paper proposes new estimators for the propensity score that aim to maximize the covariate distribution balance among different treatment groups. Heuristically, our proposed procedure attempts to estimate a propensity score model by making the underlying covariate distribution of different treatment groups as close to each other as possible. Our estimators are data-driven and can be used to estimate different treatment effect parameters under different identifying assumptions, including unconfoundedness and local treatment effects. We derive the asymptotic properties of inverse probability weighted estimators for the average, distributional, and quantile treatment effects based on the proposed propensity score estimator and illustrate their finite sample performance via Monte Carlo simulations and an empirical application."

### Changes Analysis

1. **Dramatic reframing**: The v1 abstract opens with a general statement about the propensity score's importance. The final version opens directly with the contribution: "This paper proposes new estimators for the propensity score that aim to maximize the covariate distribution balance among different treatment groups." This eliminates two setup sentences and gets to the point immediately.

2. **Title change reflected**: The title itself shifted from implying a single method ("Covariate Distribution Balance via Propensity Scores") to the same, but the abstract now frames the contribution more broadly as "new estimators" (plural) rather than a single "integrated propensity score."

3. **Intuitive framing added**: The final abstract adds a heuristic description: "our proposed procedure attempts to estimate a propensity score model by making the underlying covariate distribution of different treatment groups as close to each other as possible." This is a plain-language summary of the technical contribution -- absent from the v1, which jumped straight to technical terminology.

4. **Technical details removed from abstract**: The v1 lists specific technical properties ("admits an asymptotic linear representation, and is sqrt(n)-consistent and asymptotically normal"). The final abstract drops all of this, keeping only "data-driven." This shifts the emphasis from the statistical properties of the estimator to its purpose and applicability.

5. **Scope expansion mentioned**: The final abstract notes the estimators can be used "under different identifying assumptions, including unconfoundedness and local treatment effects." The v1 abstract only mentions the unconfoundedness setting implicitly. This signals a broader scope.

6. **Empirical applications reduced**: "three empirical applications" became "an empirical application" -- the paper was likely streamlined during revision.

7. **Software mention removed**: The v1 abstract ends with "An implementation of the proposed methods is provided in the new package IPS for R." The final abstract drops this. Software references are typically not included in JASA abstracts.

8. **"IPS" branding de-emphasized**: The v1 introduces the acronym "IPS" in the abstract and positions it as the paper's main brand. The final abstract does not use the acronym at all, referring instead to "the proposed propensity score estimator." This reflects a shift from branding a specific estimator to describing a framework.

## Introduction Comparison

### Key Changes

1. **Opening restructured**: The v1 opens with a standard motivation ("Identifying and estimating the effect of a policy... is one of the main goals in applied research") followed by a paragraph on the propensity score and then a paragraph on the practical difficulties of PS estimation. The final version preserves this structure but tightens the prose throughout.

2. **RCT connection strengthened**: The v1 mentions randomized control trials briefly. The final version draws a stronger parallel: "Indeed, the balancing property of the propensity score resembles randomization: when the data come from a randomized control trial (RCT) with perfect compliance, the entire covariate distributions among different treatment groups are balanced and, therefore, all measurable, integrable functions of the covariates are indeed balanced." This sentence crystallizes the intuition that IPS is trying to approximate what randomization does automatically.

3. **Broader scope signaled earlier**: The v1 introduction focuses exclusively on the unconfoundedness setting. The final version adds: "We emphasize that the IPS can be used under different 'research designs', including not only the unconfounded treatment assignment setup... but also the 'local treatment effect' setup, where selection into treatment is possibly endogenous but a binary instrumental variable is available." This expansion to the LATE framework is a substantive addition.

4. **"At the practical level" paragraph added**: The final version includes a new paragraph beginning "At the practical level, one can think of the IPS as an estimation procedure that attempts to estimate the unknown finite dimensional parameters of a PS model by making the underlying entire covariate distribution of different treatment groups as close to each other as possible." This provides a non-technical summary of the approach after the technical details, making the paper more accessible.

5. **Three IPS variants explicitly listed**: The final version explicitly describes three ways to characterize covariate distribution balance: "1) using the covariates' joint cumulative distribution, 2) their joint characteristic function, or 3) exploiting the Cramer-Wold theorem to focus on the cumulative distribution of the one-dimensional projections of the covariates." This structural overview was implicit but not enumerated in the v1.

6. **Related literature section formalized**: The v1 weaves literature discussion throughout the introduction. The final version adds a formal "Related literature:" subsection at the end of the introduction, providing a systematic comparison to existing work (Graham et al. 2012, Imai and Ratkovic 2014, Diaz et al. 2015, Fan et al. 2016).

7. **Rubin's design/analysis separation**: The final version adds: "As advocated by Rubin (2007, 2008), this separation is useful as it simultaneously mimics RCTs and avoids potential data snooping problems." This philosophical point about separating design from analysis was not in the v1.

8. **Zhao (2019) added**: The final version adds Zhao (2019) to the list of covariate balancing methods in the introduction, reflecting a paper that appeared after the v1.

## Conclusion/Discussion Comparison

### Key Changes

1. **Core message preserved**: Both versions conclude that the paper proposes a minimum distance framework for PS estimation that balances all functions of covariates.

2. **LATE framework acknowledged**: The final conclusion adds: "Importantly, we have shown that our framework can accommodate the empirically relevant situation under which treatment allocation is endogenous." This highlights the extension to instrumental variables, which is the main new contribution relative to the v1.

3. **Extension to multivalued treatments removed**: The v1 conclusion discusses extending to multivalued treatments (following Imbens 2000) and to the LATE setting. The final version removes the multivalued treatment discussion and integrates the LATE content into the main paper (Section 4) rather than leaving it as a future direction.

4. **Doubly robust extension**: The v1 discusses potential doubly robust extensions at length ("one can also use the minimum distance approach to estimate the outcome regression model... These extensions are currently being explored by us"). The final version retains this direction more briefly: "one can easily combine our IPS estimation procedure with such outcome regression model to form doubly-robust, locally efficient treatment effect estimators."

5. **"Currently being explored by us" removed**: The v1's forward-looking "These extensions are currently being explored by us" is replaced with "We leave the detailed discussion of such procedure for future research" -- a more standard and formal phrasing.

6. **Empirical applications reduced**: The v1 mentions "three empirical applications"; the published version has one main empirical application (401k). The v1 included applications on right heart catheterization and child soldiering that were apparently moved to supplementary material or removed.

## Writing Style Patterns Observed

- **Sentence Structure**: The v1 uses longer, more complex sentences with multiple subordinate clauses. The final version breaks these into shorter, more digestible units. For example, the v1's abstract is a single flowing paragraph; the final version is more structured with distinct conceptual beats.

- **Vocabulary/Terminology**: The most notable shift is the de-emphasis of the "IPS" brand name. The v1 consistently uses "IPS" as a proper noun ("the IPS estimator," "the IPS aims to balance"). The final version more often uses descriptive language ("the proposed propensity score estimator," "our proposed procedure"). This reflects a move toward describing what the method does rather than naming it.

- **Framing/Motivation**: The v1 frames the contribution as solving a specific problem (PS estimation via integrated moment conditions). The final version frames it as achieving a goal (maximizing covariate distribution balance). This is a shift from method-centric to purpose-centric framing, making the paper more accessible to applied researchers.

- **Precision**: The mathematical framework became more polished. Lemma 2.1 in the final version formalizes the covariate balancing property that was stated informally in equation (1) of the v1. The shift from equation numbering to formal lemmas increases mathematical rigor.

- **Tone**: The v1 has a more technical, methods-paper tone. The final version, while still technical, includes more heuristic explanations and intuitive summaries. The addition of "At the practical level..." and "Heuristically..." paragraphs reflects an effort to communicate with a broader audience.

- **Conciseness**: The paper maintained the same page count (34 pages each) but redistributed content. The three empirical applications were condensed to one, while the LATE extension was expanded from a brief discussion to a full section (Section 4).

- **Reader Engagement**: The final version is substantially more reader-friendly. It adds intuitive summaries after technical results, provides explicit enumeration of the three IPS variants, and includes a formal "Related literature" section that helps readers orient the contribution within the field.

## Specific Revision Examples

### Example 1: Abstract opening
**v1**: "The propensity score plays an important role in causal inference with observational data. Once the propensity score is available, one can use it to estimate a variety of causal effects in a unified setting. Despite this appeal, a main practical difficulty arises because the propensity score is usually unknown..."
**Final**: "This paper proposes new estimators for the propensity score that aim to maximize the covariate distribution balance among different treatment groups."
**Analysis**: Three sentences of setup compressed into one declarative statement. The v1 follows a "general background -> problem -> our solution" template; the final version skips straight to the solution. This is a textbook example of eliminating throat-clearing in academic writing.

### Example 2: RCT connection
**v1**: "alternative procedures that closer resemble randomization have been proposed"
**Final**: "Indeed, the balancing property of the propensity score resembles randomization: when the data come from a randomized control trial (RCT) with perfect compliance, the entire covariate distributions among different treatment groups are balanced and, therefore, all measurable, integrable functions of the covariates are indeed balanced."
**Analysis**: What was a vague allusion ("closer resemble randomization") became a precise, illuminating analogy. The final version explains exactly how PS balancing relates to what RCTs achieve by design. This kind of precise intuitive explanation is a hallmark of Sant'Anna's mature writing style.

### Example 3: Covariate balancing property formalization
**v1**: The covariate balancing property is introduced informally in equation (1): "E[D/p(X;beta_0) f(X)] = E[(1-D)/(1-p(X;beta_0)) f(X)] = E[f(X)]"
**Final**: Formalized as Lemma 2.1 with a proper statement: "Let p(X;beta) be a parametric model for the unknown propensity score. Then, if the model is correctly specified, for all measurable and integrable function f(X)..."
**Analysis**: Elevating a key equation to a formal Lemma signals its importance and makes it easier to reference. The addition of explicit conditions ("if the model is correctly specified") improves mathematical precision. This reflects the journal's higher standards for formal mathematical presentation.

### Example 4: Identification discussion
**v1**: "as emphasized by Dominguez and Lobato (2004), the global identification condition for beta_0 can fail when one adopts the generalized method of moment approach, and only attempts to balance finitely many covariate moments."
**Final**: "as emphasized by Dominguez and Lobato (2004), the global identification condition for beta_0 can fail when one adopts the generalized method of moment approach that only attempts to balance finitely many covariate moments. In these cases, one must be careful justifying inference procedures as classical tools such as Taylor expansions are harder to justify."
**Analysis**: The final version adds a sentence explaining the practical consequence of the identification failure. Rather than just citing the theoretical problem, the revised text explains why it matters for applied work. This reflects increased attention to helping readers understand the implications of technical results.

### Example 5: Software and practical implementation
**v1 abstract**: "An implementation of the proposed methods is provided in the new package IPS for R."
**Final introduction**: "In fact, our proposed method is easy to use as currently implemented in the new package IPS for R, available at https://github.com/pedrohcgs/IPS."
**Analysis**: The software reference moved from the abstract (where it stands out as promotional) to the introduction (where it serves as practical information). The addition of the specific GitHub URL makes the package more accessible. This reflects a broader trend in econometrics toward providing implementation details while keeping the abstract focused on intellectual contributions.
