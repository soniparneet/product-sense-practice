# Getting started

This setup uses a ChatGPT Project to keep the practice instructions available across related chats. You do not need Git, a terminal, an API key, or Codex.

**Documentation checked:** 13 September 2026.

- The official [ChatGPT Learn guide to Projects and chats](https://learn.chatgpt.com/docs/projects) confirms that a ChatGPT Project can keep related chats, uploaded files, instructions, and sources together, and that Project instructions apply across its chats.
- The requested [OpenAI Help Center article about Projects](https://help.openai.com/en/articles/10169521-projects-in-chatgpt) could not be retrieved during packaging because its edge protection returned an access error. Use it as the primary place to check current account-specific controls and limits.
- GitHub's official [source archive guide](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives) confirms the **Code → Download ZIP** route and release archive downloads.

Interfaces and feature availability can vary by account and may change after the verification date.

## 1. Download the instructions

Recommended: open [`project_segmentation_golden_aligned.md`](../project_segmentation_golden_aligned.md) and download the file.

Whole-repository alternative:

1. Open the repository's main page on GitHub.
2. Select **Code**.
3. Select **Download ZIP**.
4. Extract the ZIP and locate `project_segmentation_golden_aligned.md`.

If a GitHub release is available, its assets should include the exact instruction file, `PROJECT_SETUP.txt`, and a reviewed starter ZIP. Do not upload the whole repository to ChatGPT; the one instruction file and activation text are sufficient.

## 2. Create a dedicated ChatGPT Project

In ChatGPT, create a Project named something recognizable, such as **Product Sense Practice**. A dedicated Project reduces conflicts with unrelated instructions and files.

If your account offers a **project-only memory** choice, prefer it for this practice Project so unrelated conversations are less likely to influence the session. Availability and labels may vary. This is a context-management choice, not a technical privacy guarantee; consult the current official OpenAI Projects guidance for your account.

## 3. Add the instruction file

Open the Project and add `project_segmentation_golden_aligned.md` to its files or sources.

The file is intentionally long. Keep it uploaded as a Project source rather than pasting the whole document into a settings field.

## 4. Activate it with short Project instructions

Open the Project's settings or instruction editor and paste the complete contents of [`PROJECT_SETUP.txt`](../PROJECT_SETUP.txt). Save the change.

The activation block tells ChatGPT to read the uploaded file in full and use it as the practice rules. It does not replace the framework with a shorter version.

## 5. Run the setup check

Start a chat inside the Project and type:

```text
New
```

Expected response:

```text
Choose mode: Candidate or Instructor?
```

This is a startup check only. It does not prove that every later answer will follow the framework perfectly.

## 6. Choose how to practice

### Learn by watching

```text
You: Candidate
AI: Candidate mode. Send the Product Sense question.
You: Design a product for people moving to a new city.
```

The AI answers one stage, separates its learning notes from the words you would say aloud, reports estimated pacing, and pauses.

### Practice by answering

```text
You: Instructor
AI: Instructor mode. Send the Product Sense question.
You: Design a product for people moving to a new city.
AI: Design a product for people moving to a new city. Go ahead.
```

You provide the answer. The AI gives focused coaching and keeps you in control of the reasoning. It supplies a model answer only when you explicitly ask for one.

## Commands and checkpoint behavior

- `New`: resets the current practice state and asks for a mode.
- `Candidate`: the AI answers; you act as interviewer.
- `Instructor`: you answer; the AI acts as interviewer and coach.
- `yes` or `continue`: advances after a checkpoint. Similar explicit approval also works.
- `redo`: repeats the current stage.
- Feedback at a checkpoint: the AI addresses that feedback before advancing unless you also ask it to continue.
- An explicit request for a complete answer, model response, or uninterrupted simulation: the AI may combine the full sequence while preserving stage order.

`New` is a practice command, not the same as opening a new ChatGPT chat. It resets the framework state but does not delete chats or files.

## Troubleshooting

### `New` does not produce the expected reply

- Confirm the filename is exactly `project_segmentation_golden_aligned.md`.
- Confirm the file appears in this Project's files or sources.
- Confirm `PROJECT_SETUP.txt` was pasted into this Project's instructions.
- Remove or disable older, conflicting Product Sense instruction files.
- Confirm the chat is inside the intended Project.

### The AI skips stages or checkpoints

Say: “Follow the uploaded instruction file's stage order and stop at the current required checkpoint.” If the behavior repeats, start a fresh chat inside the same Project and type `New`.

### Coaching appears inside the answer

Say: “Keep Candidate delivery separate from `Coaching cues — not spoken`; only the Candidate delivery should sound spoken.”

### Answers are unexpectedly long

Ask the AI to respect the stage's word guide and prioritize the consequential choice rather than expanding every framework field.

### The AI makes a questionable claim

Ask it to mark uncertain claims as assumptions or hypotheses. Product Sense practice should not invent research or market data as fact.

### An outdated duplicate keeps taking precedence

Remove old instruction copies from the ChatGPT Project, keep only `project_segmentation_golden_aligned.md`, and start a fresh chat.
