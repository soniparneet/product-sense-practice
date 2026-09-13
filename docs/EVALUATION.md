# Evaluation notes

Evaluation served two separate product goals. It was designed to improve the instruction system, not to estimate a candidate's chance of being hired or certify equivalence to any employer's process.

## Goal 1: answer quality

The review looked for:

- useful framing and assumptions;
- user and company motivation that affected later choices;
- meaningful targeting and segmentation;
- explicit segment, problem, and solution prioritization;
- a coherent user journey and root problem;
- credible alternatives before convergence;
- a scoped V1 linked to the chosen problem;
- mission → user → problem → solution coherence;
- natural interview communication and pacing.

## Goal 2: learning quality

A separate review asked whether a learner could see and reuse the method:

- Is the stage's purpose clear?
- Are the decision criteria visible?
- Is there a compact, memorable pattern?
- Can the lesson transfer to another question?
- Is coaching concise?
- Is **not spoken** guidance clearly separated from Candidate delivery?

## Evidence used during development

### Reference examples

Three worked examples from the source article were reconstructed locally for Claude Projects, Meta gardening, and Netflix podcasts. They were used as quality references, not answer keys. The review rewarded coherent alternatives rather than matching the same feature or persona.

These article-derived files are excluded from this public repository because attribution alone does not establish redistribution permission. The primary source is [Ben Erez's guide in Lenny's Newsletter](https://www.lennysnewsletter.com/p/the-definitive-guide-to-mastering).

### Candidate tests recorded as executed

The retained local evaluation report describes:

- three generated benchmark answers compared semantically with the worked references;
- eight broader prompts across consumer design, product improvement, marketplace/platform, creator, and B2B archetypes;
- a staged Meta-gardening comparison of an older learning-oriented file and a reasoning-optimized file;
- targeted checks for company differentiation, bounded solution divergence, and segmentation behavior.

The report contains model-assisted 1–5 judgments and dimension scorecards. Those numbers were useful for comparing instruction revisions within the project, but they were not produced by an independent evaluator and should not be treated as validated benchmarks.

### Instructor tests recorded as executed

Because the source worked examples cover Candidate answers rather than coaching, Instructor behavior used synthetic failure cases:

1. jumping directly to an AI feature;
2. weak demographic segmentation;
3. unexplained problem prioritization;
4. a solution disconnected from the selected problem;
5. shallow framework recital;
6. overlong setup that endangered solution time.

The retained review says Instructor mode identified the central issue, taught a reusable principle, and used targeted pushback without imposing a canonical answer. No independent human study was retained.

## What was designed versus what is retained

| Evidence type | Status | Public interpretation |
|---|---|---|
| Golden-reference comparison method | Designed and used locally | Quality calibration, not exact-answer matching |
| Three Candidate benchmark generations | Reported as executed | Raw transcripts are not included in the public package |
| Eight broader prompt checks | Reported as executed | Development examples, not a fresh held-out test set |
| Six Instructor failure cases | Reported as executed | Synthetic coaching checks, not a golden dataset |
| Baseline run for every broader prompt | Not retained | No clean before/after generalization claim |
| Repeated trials across models/seeds | Not run | Reliability and variance are unknown |
| Independent expert scoring | Not run | Ratings remain subjective and model-assisted |
| Human learning or usability study | Not run | Learning gains are a design hypothesis |

## Version caveat

The retained evaluation report primarily describes `project.md` and earlier targeted refinements. The designated public release, `project_segmentation_golden_aligned.md`, is a later local variant that reverses an overly rigid single-axis segmentation rule. File comparisons support the documented design evolution, but a fresh full benchmark suite for the exact release checksum was not retained. It would be misleading to carry earlier PASS labels forward as independent proof of the release.

The designated file's SHA-256 at the start of packaging was `1216da0a4d0b6f8e663ebf82bfcdfe0bf800d07d92447e3dd43c93d72cfb5e20`. Publication checks compare against this value to ensure the instruction content was not changed during documentation work.

## Qualitative findings

The available review supports several practical observations:

- separating Candidate delivery from coaching restored framework visibility without adding spoken time;
- adaptive branch counts reduced padded solution sets;
- explicit trade-offs improved target, problem, and solution choices;
- a company-substitution check discouraged decorative company name-dropping;
- segmentation required multiple revisions because both unstructured composites and rigid taxonomies could weaken the product decision;
- the causal chain was a useful regression check across stages.

These are observations from the development process, not statistically proven effects.

## Current limitations

- Most recorded runs are single samples from a generative model.
- The same gardening case appears repeatedly during tuning.
- The broader questions are development examples, not untouched holdouts.
- Baseline generalization outputs were not generated and retained consistently.
- Scores and PASS judgments were produced within the same model-assisted workflow that revised the instructions.
- The exact release file does not have a retained full-suite rerun.
- Speaking times are estimates based on word count and 130 words per minute.
- ChatGPT can still skip rules or reason poorly.

## Useful next evaluations

Without turning this into an expensive benchmark program, the next credible steps would be:

1. run repeated samples on fresh prompts not used during development;
2. retain anonymized outputs and the exact file checksum;
3. use blinded human reviewers for answer and coaching quality;
4. test whether learners can reproduce the framework without looking at the cues;
5. document failures, not only successful examples.

## Publication smoke test

On 13 September 2026, three fresh read-only Codex executions loaded the exact release file and checked its startup contract:

- `New` returned exactly `Choose mode: Candidate or Instructor?`;
- selecting Candidate returned exactly `Candidate mode. Send the Product Sense question.`;
- a fresh pet-owner prompt produced Stage 0 only, separated coaching as **not spoken**, included a pacing estimate, and stopped at the breakpoint.

This verifies instruction-following in that execution path. A live ChatGPT Project setup and UI walkthrough were **not run**, so account-specific upload, settings, and memory controls remain dependent on the current ChatGPT interface.
