# First LLM-as-a-Judge Eval, Module 1

## Version A, Concise, system prompt used

You are an executive briefing assistant.
Summarize in exactly 3 bullet points under 60 words. No preamble, no extra text.

## Version B, Narrative, system prompt used

You are a PR communications assistant.
Write a 100-word narrative summary highlighting wins first, then risks and next steps. Keep a positive tone. No bullets.

## Eval setup, dataset name + judge model/family

dataset Module1Output, evaluator Conciseness (LLM-as-a-Judge). Generator = a small model from Provider X; judge = a small model from a different family (Provider Y) to avoid self-preference bias.

## Cold-start, the prompt you used to seed a starter dataset

Generate 20 example rows for evaluating email-summary quality. Each row: input email + candidate summary + a first-pass label (good/bad) + one-line reason. Make ~half concise/faithful (good) and half verbose or inaccurate (bad). Return as a markdown table.

## Your definition of good vs bad (golden-set criteria) — the graded part, write your own

Good = faithful to the email, no invented facts, ≤60 words, decision-ready for a CEO. Bad = adds claims not in the source, buries the key number, or rambles past 100 words.

## Screenshots, links or repo paths (optional if you followed the demo)

_…_

