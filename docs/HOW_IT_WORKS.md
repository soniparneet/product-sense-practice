# How it works

Product Sense Practice is a conversational instruction system. It is not an application, a trained model, an evaluation service, or a deterministic interview engine.

## The four layers

| Layer | Role |
|---|---|
| Framework | Supplies the sequence and decision points for Product Sense reasoning |
| Instruction file | Tells ChatGPT how to conduct the practice session |
| Examples | Illustrate the interaction without prescribing one correct answer |
| Evaluation | Records what was tested, what was observed, and what remains uncertain |

The GitHub repository stores public files. A ChatGPT Project is the workspace where a user uploads the instruction file and practices. Publishing this repository does not publish anyone's ChatGPT Project, chats, or uploaded sources.

## One workflow, two answering modes

Type `New` to reset the current practice state. Then choose:

- **Candidate:** ChatGPT is the candidate and demonstrates the answer. You are the interviewer.
- **Instructor:** you are the candidate. ChatGPT interviews and coaches you without taking over.

The same reasoning model supports both. Candidate mode demonstrates the decisions; Instructor mode diagnoses which decision is missing or weak.

## Seven stages, one causal chain

The instruction file moves through:

```text
frame and assumptions
→ user value and mission
→ ecosystem player
→ target segment and persona
→ journey and prioritized problem
→ solution alternatives and choice
→ V1, distribution, success, and risks
```

Stages create natural checkpoints. The AI pauses so an interviewer can redirect the case, challenge an assumption, or approve the choice. The structure can compress when the prompt already resolves a decision, but later answers should still follow from earlier ones.

## Spoken answer versus learning scaffold

Every completed Candidate stage has two distinct layers:

1. **Candidate delivery:** the natural response a candidate could say in an interview.
2. **Learning scaffold:** short cues labeled **not spoken**, followed by a reusable reasoning pattern.

The scaffold explains the purpose of the stage, the mental questions, and the decision lens. It is excluded from the answer's word count and should not appear as interview jargon.

## Divergence and convergence

The system asks for alternatives before a decision:

- meaningful user segments before choosing a target;
- multiple real problems before prioritizing one;
- the smallest credible set of distinct solution mechanisms before selecting V1.

Counts are adaptive. Two strong solutions can be enough; three is often useful; extra ideas should not be invented to fill a template. Prioritization uses only criteria that can change the decision.

## Segmentation philosophy

The release explores motivations and several useful dimensions, then synthesizes a small set of recognizable user groups. Composite segments are allowed when the combination creates a different need or product opportunity. The checks are practical:

- Is the group coherent?
- Is it distinct enough to compare?
- Does it experience a meaningfully different need?
- Would choosing it change the product direction?

The goal is not mathematical taxonomy. The persona should make the chosen segment concrete, not rescue a vague segment by introducing its defining need for the first time.

## Company fit and solution quality

For a company-specific prompt, the instructions ask whether the company's assets materially improve user value, trust, supply, context, quality, distribution, or defensibility. A branded feature is not required. A non-unique solution is valid when the company still has a credible strategic or delivery advantage.

Solutions must address the prioritized problem through genuinely different, defensible mechanisms. Novelty is secondary to user insight and credibility.

## What the commands mean

| Input | Supported behavior |
|---|---|
| `New` | Reset the practice state and ask for Candidate or Instructor mode |
| `Candidate` | AI demonstrates the answer |
| `Instructor` | User answers; AI coaches |
| `yes`, `continue`, or similar approval | Advance from a checkpoint |
| `redo` | Repeat the current stage |
| Feedback at a checkpoint | Revise the current stage before advancing |
| Explicit request for a complete/model answer | Use the supported uninterrupted-answer exception |

No additional shortcut should be treated as guaranteed unless it appears in the instruction file.

## Expected variability

Language models are nondeterministic. They can miss rules, estimate word counts imperfectly, or produce weak reasoning. This repository offers a repeatable scaffold and a way to discuss failures; it does not turn model behavior into deterministic software.
