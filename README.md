# Product Sense Practice

**Learn the framework. See it demonstrated. Practice one stage at a time.**

Product Sense Practice turns a Markdown instruction file into a structured interview-practice partner inside ChatGPT. Watch the AI demonstrate an answer, or answer yourself while it acts as an interviewer and coach. The experience separates interview delivery from learning notes, so you can understand both the answer and the reasoning behind it.

A `.md` file is Markdown: a readable text file. The recommended ChatGPT setup requires no coding knowledge, Git, terminal, API key, or Codex.

**Start here:**

- [Download the recommended instruction file](https://github.com/soniparneet/product-sense-practice/releases/download/v1.0.0/project_segmentation_golden_aligned.md)
- [Follow the setup guide](docs/GETTING_STARTED.md)
- [See a Candidate example](examples/candidate-example.md)
- [Read the build story](docs/BUILD_STORY.md)

## What you can do with it

| Mode | Who answers? | What the AI does | Useful for |
|---|---|---|---|
| Candidate | The AI | Demonstrates an answer one stage at a time, with separate learning notes | Learning the method |
| Instructor | You | Asks follow-ups and coaches your reasoning without taking over | Practicing independently |

**Candidate mode means the AI is the candidate. Instructor mode means you are the candidate.**

`New` starts or resets the practice flow; it is not a third answering mode.

The instruction file retains its original heading, “Stripe Product Sense Practice,” because the project began as a focused interview-practice configuration. The current rules support company-specific and company-neutral Product Sense questions. This is an independent project, not an official Stripe tool.

## Start here — no coding required

1. Download [`project_segmentation_golden_aligned.md`](https://github.com/soniparneet/product-sense-practice/releases/download/v1.0.0/project_segmentation_golden_aligned.md). Alternatively, download the whole repository from GitHub using **Code → Download ZIP**, then extract it.
2. In ChatGPT, create a dedicated Project—for example, **Product Sense Practice**.
3. Add `project_segmentation_golden_aligned.md` to the Project's files or sources.
4. Open the Project's settings and paste the short activation text from [`PROJECT_SETUP.txt`](PROJECT_SETUP.txt) into Project instructions. The long Markdown file remains uploaded; the short text activates it rather than replacing it.
5. Start a chat inside that Project and type `New`.
6. Choose `Candidate` or `Instructor`, then send a Product Sense question.

Setup check:

```text
You: New
AI: Choose mode: Candidate or Instructor?
```

This verifies startup behavior only, not the quality of a complete answer. If it fails, check the uploaded filename, the Project instructions, whether an older instruction file conflicts, and whether the chat is inside the intended Project. See [Getting started](docs/GETTING_STARTED.md) for detailed guidance and current documentation links.

## Your first practice session

Opening a fresh chat is useful for a fresh question. Typing `New` resets the practice state inside the conversation; it does not delete chats or uploaded files.

```text
You: New
AI: Choose mode: Candidate or Instructor?
```

To learn by example:

```text
You: Candidate
AI: Candidate mode. Send the Product Sense question.
You: Design a product for people moving to a new city.
```

The AI answers Stage 0, shows the separate learning scaffold and pacing estimate, then waits. Reply `yes` or `continue` at a checkpoint. Give feedback to revise the current stage, or type `redo` to repeat it.

To practice your own reasoning:

```text
You: Instructor
AI: Instructor mode. Send the Product Sense question.
You: Design a product for people moving to a new city.
AI: Design a product for people moving to a new city. Go ahead.
```

You answer first. The AI identifies the current stage, gives at most two high-value coaching points, and asks a targeted follow-up without supplying the solution. If you explicitly request a model answer or rewrite, the instructions allow it to respond directly.

## How a session works

The interview uses seven conversational stages within a 35-minute working window:

| Stage | Decision | Budget |
|---|---|---:|
| 0 | Frame the prompt and set useful assumptions | 3 min |
| 1 | Explain user value, company fit, and mission | 4 min |
| 2A | Map the ecosystem and select a player | 2 min |
| 2B | Segment, prioritize a target, and make it concrete | 7 min |
| 3 | Trace the journey and prioritize a problem | 9 min |
| 4A | Compare credible solution mechanisms and choose one | 6 min |
| 4B | Scope V1, distribution, success, risks, and mitigations | 4 min |

The 35 minutes includes speaking, thinking, clarifications, feedback, and interviewer interaction. Speaking-time estimates use 130 words per minute as a practical approximation; they are not a stopwatch or a guarantee of live timing accuracy.

Each completed Candidate stage visibly separates:

1. the answer you could say aloud;
2. a one-sentence **Decision**;
3. **Coaching cues — not spoken**;
4. a memorable **Reusable framework pattern**;
5. estimated pacing;
6. a checkpoint before the next stage.

The flow is disciplined but adaptive. A tightly scoped prompt can compress ecosystem work; a marketplace may need more attention to supply and trust; a B2B prompt may use a concrete role and workflow instead of a fictional biography.

## Why we built it this way

A polished sample answer is useful but easy to consume passively. This system treats answer quality and learning quality as equal goals.

- **Staged interaction** exposes one consequential decision at a time.
- **Visible choices** make “why A instead of B?” part of targeting, problems, and solutions.
- **Separate coaching** teaches the reusable move without making the spoken answer sound robotic.
- **Bounded exploration** creates real alternatives without requiring exactly three ideas or an implausible moonshot.
- **Instructor ownership** uses targeted questions and principles before offering a model answer.
- **Causal coherence** keeps mission → user → problem → solution → V1 connected.

## How it was developed and evaluated

The reasoning backbone comes from Ben Erez's Product Sense guide and linked template, published by Lenny's Newsletter. The project creator translated that framework into an interactive workflow, then iterated against three article-derived worked examples, broader practice prompts, and synthetic Instructor cases.

Those worked examples served as “golden references”: examples of the desired reasoning quality, not unique correct answers. The article-derived files are intentionally not redistributed here. Local evaluation records include model-generated samples and qualitative, model-assisted ratings; they are not independent validation, hiring probabilities, or statistical proof.

Later iterations restored explicit teaching cues after a reasoning-focused rewrite made the method harder to learn. Segmentation rules were also revised after both single-axis and peer-archetype approaches proved too constraining. Read the evidence and caveats in [Evaluation](docs/EVALUATION.md) and the narrative in [The build story](docs/BUILD_STORY.md).

## Limits, privacy, credits, and contribution

AI responses vary by model, conversation context, and product behavior. The instructions improve structure and coaching but cannot guarantee correct facts, complete compliance, interview outcomes, or employer-specific calibration. Treat unsupported market judgments as hypotheses.

Keep confidential work material, private interview questions, customer data, and personal information out of public issues and examples. Uploading this file to your own ChatGPT Project does not publish or share that Project, its chats, or its files through this GitHub repository. The instruction file's memory-isolation rule is behavioral guidance, not a technical privacy guarantee.

The framework foundation is credited to Ben Erez and Lenny's Newsletter; the adaptation is by [soniparneet](https://github.com/soniparneet), with drafting and implementation assistance from ChatGPT and Codex. See [Credits](CREDITS.md) for precise attribution and the independent-project disclaimer.

**License status:** no reuse license has been selected yet. The repository must not be described as open source or as granting unrestricted reuse until the owner adds one.

Found a repeatable failure? [Contribute a sanitized example](CONTRIBUTING.md) with the question, mode, stage, expected behavior, and actual behavior. Reproducible reasoning failures are more useful than feature wish lists.
