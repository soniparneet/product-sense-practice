# The build story

## The problem

Product Sense interviews test more than feature ideas. A candidate must frame an ambiguous prompt, choose a user, uncover and prioritize a problem, compare credible solutions, and define a coherent first version—while explaining enough for an interviewer to follow the judgment.

Static frameworks can show the boxes, and polished answers can show the destination. Neither automatically creates a repeatable practice experience. This project set out to connect the two: a conversational system that demonstrates strong reasoning and teaches the learner how to reproduce it.

## The initial approach

The project began with Ben Erez's Product Sense guide and linked template, published by Lenny's Newsletter. Those sources provided the structural backbone: assumptions, motivation and mission, ecosystem, segmentation, journey and problems, solution choices, and V1 risks.

Three article worked examples—Claude Projects, Meta gardening, and Netflix podcasts—were organized locally as “golden references.” Here, golden means a worked example used to understand the desired standard. It does not mean that its segment, problem, or feature is the only correct answer. Those article-derived files are not redistributed in this repository.

The first interaction model added `New`, Candidate, and Instructor flows, stage checkpoints, pacing guidance, and visible decisions. Candidate mode let the AI demonstrate; Instructor mode put the user in the candidate seat.

## What testing revealed

Local evaluation compared generated Candidate responses with the reasoning quality of the references and checked broader prompts spanning consumer, product-improvement, marketplace, creator, and B2B contexts. Separate synthetic cases examined whether Instructor mode could diagnose premature solutioning, weak segmentation or prioritization, broken user-to-solution logic, shallow framework recital, and poor pacing.

The evidence was useful but limited: mostly single model samples, qualitative model-assisted review, no separately generated baseline for the broader prompt set, and repeated use of the gardening question during development.

The largest product lesson was that answer quality and learning quality are different. A reasoning-focused revision produced polished answers but hid too much of the method. Learners could see a good response without easily recalling why each stage existed.

## The changes

The project separated two layers. Candidate delivery stays natural and interview-ready. After the decision, compact coaching bullets name the stage goal, mental questions, and prioritization lens, followed by a reusable pattern marked **not spoken**. Instructor mode uses the same language to diagnose the learner's answer.

Other changes made the framework adaptive rather than mechanical:

- fixed branch counts became small, meaningful comparison sets;
- problem and solution options had to diverge before convergence;
- company advantages had to improve the product thesis rather than decorate it;
- V1 gained a compact success test where useful;
- pacing favored consequential target, problem, and solution choices.

## Segmentation: the useful reversals

Segmentation produced the clearest example of why iteration needs reversals.

| Observed issue | Change tried | What we learned |
|---|---|---|
| Labels mixed experience, behavior, and social motivation | Require one dominant axis | Consistency improved, but a single axis sometimes hid combinations that materially changed the need |
| Composite groups risked becoming arbitrary | Require an organizing logic and peer archetypes | Comparability improved, but the rule could constrain useful real-world segments and become framework theater |
| Personas introduced the most important constraint too late | Add a persona inheritance/consistency test | A selected segment should already imply the core need; a persona should add texture, not redefine it |
| Clean taxonomies and arbitrary composites both failed | Explore motivations and useful dimensions, synthesize a few meaningful segments, then test need and product consequence | Product decisions—not theoretical exclusivity—are the right quality bar |

The current release therefore avoids both “always use one axis” and “combine anything that sounds specific.” It asks whether each final segment is recognizable, different in need, and consequential enough to change the likely product.

## What we learned

1. A framework becomes teachable when the learner can see the decision, not merely the heading.
2. Divergence matters only when alternatives create real trade-offs.
3. Company fit is strongest when it changes the experience or delivery advantage.
4. Personas should test and embody segmentation, not smuggle in a new target.
5. A model-generated PASS or numerical score is evidence from one review process, not independent validation.

## The current limits

The retained records do not establish statistical reliability, hiring outcomes, or measured learning gains. The golden material covers Candidate answers, not Instructor behavior. Broader prompts used during iteration are development examples rather than a fresh held-out benchmark. Model interfaces and behavior can change.

Future work could include repeated trials across models, blinded human review, fresh held-out prompts, and usability studies measuring whether learners can reproduce the method without the file.

## Packaging the current version

The public package keeps one unmistakable instruction file: `project_segmentation_golden_aligned.md`. It adds no-code setup, focused illustrations, honest evaluation notes, attribution, and maintenance guidance. Older variants, raw local evaluation files, paid/article-derived reference reconstructions, spreadsheets, and private transcripts remain outside the public package.

The contribution is the operational adaptation: translating a credited framework into a staged Candidate/Instructor learning experience, testing where the rules became rigid, and documenting the resulting trade-offs. It is not a claim to own or certify the underlying Product Sense methodology.
