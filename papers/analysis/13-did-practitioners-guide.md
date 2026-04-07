# Writing Style Analysis: Difference-in-Differences Designs: A Practitioner's Guide

## Paper Info
- Authors: Andrew Baker, Brantly Callaway, Scott Cunningham, Andrew Goodman-Bacon, Pedro H. C. Sant'Anna
- ArXiv v1 date: March 17, 2025 (arXiv:2503.13323v1)
- Published: Journal of Economic Literature, 2025 (Forthcoming)

## Abstract Comparison
### v1 Abstract
"Difference-in-Differences (DiD) is arguably the most popular quasi-experimental research design. Its canonical form, with two groups and two periods, is well-understood. However, empirical practices can be ad hoc when researchers go beyond that simple case. This article provides an organizing framework for discussing different types of DiD designs and their associated DiD estimators. It discusses covariates, weights, handling multiple periods, and staggered treatments. The organizational framework, however, applies to other extensions of DiD methods as well."

### Final Abstract
"Difference-in-differences (DiD) is arguably the most popular quasi-experimental research design. Its canonical form, with two groups and two periods, is well-understood. However, empirical practices can be ad hoc when researchers go beyond that simple case. This article provides an organizing framework for discussing different types of DiD designs and their associated DiD estimators. It discusses covariates, weights, handling multiple periods, and staggered treatments. The organizational framework, however, applies to other extensions of DiD methods as well."

### Changes Analysis
The abstract is virtually identical between the two versions. The only change is capitalization:
- v1: "Difference-in-Differences (DiD)" with capital D's
- Published: "Difference-in-differences (DiD)" with lowercase "differences"

This is a trivially small change, likely reflecting journal house style preferences. The abstract was already polished at the v1 stage, which makes sense given the multi-author team and the paper's intended audience.

## Introduction Comparison
### Key Changes
The introduction is remarkably stable between v1 and the published version, with only minor editorial changes:

1. **Slight rephrasing in footnote 1**: v1 says "17% of empirical articles in economics' top 5 journals mention them"; published says "17% of empirical articles in five leading general-interest economics journals in 2018 mention DiD." The published version is more precise and avoids the informal "top 5" label.

2. **Phrasing changes for clarity**: v1 says "for whom treatment changes and another set for whom it does not"; published says "for which treatment changes and another set for which it does not" -- using "which" instead of "whom" since the referent is "set of units" not people.

3. **Literature citation update**: Minor additions and updates to references in some places, including the addition of "(Baker et al., 2025)" as a self-referencing mechanism in some contexts.

4. **Softened/qualified language**: v1 says "producing estimates that are not only misleading in their magnitudes but potentially of the wrong sign; for recent overviews, see..."; published version removes the direct citation to de Chaisemartin and D'Haultfoeuille after the initial listing and tightens the sentence.

5. **Table 1 footnote**: Published version adds "provided by the Kaiser Family Foundation (2025)" as a data source reference for Table 1's Medicaid expansion dates.

6. **Appendix material**: v1 mentions "In an appendix, we briefly discuss related DiD designs..." with slightly different wording than the published version which says essentially the same thing with minor editorial changes.

7. **Replication materials**: Published version adds "Our replication materials include data as well as R and Stata code that can serve as a template for any DiD study using these methods" and references "Table A1 includes a list of the acronyms."

## Conclusion/Discussion Comparison
### Key Changes
Both versions have a Section 6 that concludes. The conclusion discusses extensions (triple differences, distributional parameters, repeated cross-sections, non-binary treatments, etc.). The content is substantively identical between versions with only minor editorial polishing. The conclusion maintains its role as a brief summary and pointer to extensions rather than a deep discussion.

## Writing Style Patterns Observed
- **Sentence Structure**: Highly accessible, with short-to-medium length sentences. The writing is deliberately non-technical compared to Sant'Anna's solo theory papers. Sentences are structured for maximum clarity, often using a "setup, then punch" pattern.
- **Vocabulary/Terminology**: The paper deliberately uses accessible language suitable for its JEL target audience. Terms like "building blocks" are used metaphorically to make abstract concepts concrete. The "forward-engineering" vs "reverse-engineering" framing is vivid and original.
- **Framing/Motivation**: The Medicaid expansion running example is threaded throughout the paper, giving every methodological point a concrete empirical anchor. This is a sophisticated pedagogical choice.
- **Precision**: Despite being a "practitioner's guide," the paper is precise about assumptions (formally stated as Assumption NA, Assumption PT, etc.) and about what different methods do and do not identify.
- **Tone**: Conversational but authoritative. Phrases like "So, what should applied researchers do instead?" directly address the reader. The paper strikes a balance between being a textbook and a research article.
- **Conciseness**: The paper is quite long (75+ pages with references), but individual passages are concise. The writing avoids unnecessary jargon.
- **Reader Engagement**: This is the most reader-friendly paper in the set, by design. The running example, numbered assumptions, and explicit guidance ("This paper is not designed to be a comprehensive literature review; its goal is to provide guidelines for practitioners") keep the reader oriented.

## Specific Revision Examples

1. **Before (v1):** "common empirical practices have almost certainly yielded misleading results in several concrete cases (Baker, Larcker and Wang, 2022)."
   **After (published):** "common empirical practices have almost certainly yielded misleading results in several concrete cases (Baker, Larcker and Wang, 2022)."
   **Why:** This strong claim is maintained verbatim -- the authors are willing to make bold statements about the state of the empirical literature. No hedging was added despite this being a strong claim.

2. **Before (v1):** "comparisons between one set of units for whom treatment changes and another set for whom it does not"
   **After (published):** "comparisons between one set of units for which treatment changes and another set for which it does not"
   **Why:** Grammatical correction. "Set of units" is a thing, not a person, so "which" is more correct than "whom." This reflects careful copy-editing.

3. **Before (v1):** "17% of empirical articles in economics' top 5 journals mention them"
   **After (published):** "17% of empirical articles in five leading general-interest economics journals in 2018 mention DiD"
   **Why:** The published version avoids the informal ranking language "top 5" (which could be seen as subjective) and specifies "general-interest" and the year, adding precision. "Them" is replaced with "DiD" for clarity.

4. **Before (v1):** "This is a great example of a staggered treatment adoption."
   **After (published):** "This is a great example of a staggered treatment adoption."
   **Why:** This informal phrasing ("great example") is maintained in both versions, reflecting the paper's deliberately accessible tone. In a more technical paper, one might expect "This provides a canonical example of..." but the practitioner-guide framing justifies the conversational register.

5. **Before (v1):** "We aim to use publicly available and shareable data for pedagogical purposes"
   **After (published):** "We aim to use publicly available and shareable data for pedagogical purposes"
   **Why:** This meta-commentary about the paper's goals is maintained unchanged, reflecting the transparency and pedagogical intent that characterizes this paper. The phrase "pedagogical in spirit" appears in both versions to set reader expectations.
