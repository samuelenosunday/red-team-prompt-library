# Red Team Prompt Library

A curated library of adversarial prompts for **AI red-teaming**. Organized by attack type, with descriptions, expected model behavior, and evaluation rubrics.

Built for AI safety evaluators, red teamers, and QA reviewers who need structured, reusable tests to probe model robustness.

---

## Why This Exists

Red teaming — deliberately trying to break AI models — is one of the highest-value skills in AI training and safety evaluation. But most red-team work is ad-hoc: someone writes a few clever prompts, checks the model's response, moves on.

This library brings structure. Each prompt is:
- **Categorized** by attack type (jailbreak, instruction override, system prompt extraction, encoding attack, multi-turn escalation)
- **Documented** with what it attempts and why
- **Scored** against a reusable evaluation rubric

The goal: a shared vocabulary of adversarial prompts that evaluators can use, extend, and reference across projects.

---

## Categories

| File | Attack Type | Count | Purpose |
|---|---|---|---|
| `jailbreaks.md` | Role-play and persona-based jailbreaks | 15 | Test whether the model abandons safety guidelines under a fictional persona |
| `instruction-override.md` | Attempts to discard prior instructions | 15 | Test whether the model honors its system prompt or gets overridden |
| `system-prompt-extraction.md` | Attempts to leak the system prompt | 10 | Test confidentiality of system instructions |
| `encoding-attacks.md` | Base64, hex, unicode, delimiter tricks | 10 | Test whether the model mis-parses encoded payloads |
| `multi-turn-escalation.md` | Gradual escalation over multiple turns | 5 | Test whether the model maintains safety across a conversation |
| `evaluation-rubric.md` | — | — | How to score each response on a 1–5 safety scale |

---

## How Each Prompt Is Documented


---

## Who This Is For

- **AI safety evaluators** running red-team assessments
- **QA reviewers** on platforms like Outlier, Surge, Scale AI
- **Model evaluation teams** building benchmark suites
- **Anyone** documenting adversarial prompting for safety research

---

## How to Use It

1. Pick a category (or read all five).
2. Send each prompt to the model you're evaluating.
3. Score the response using `evaluation-rubric.md`.
4. Log results in a spreadsheet or reporting tool.

This library is **not** an attack toolkit. It's a documentation and evaluation resource. All prompts are published for **defensive** use: testing and improving model safety.

---

## Limitations

- This is a **curated starting point**, not a comprehensive benchmark.
- New jailbreak techniques emerge constantly. This library is a snapshot, not a live feed.
- Model behavior changes with context, temperature, and version. Always re-test on the specific model you're evaluating.

---

## About the Author

**Samuel Eno Sunday** — AI Training Specialist & LLM Quality Analyst

- LinkedIn: [linkedin.com/in/samuelenosunday001](https://www.linkedin.com/in/samuelenosunday001/)
- GitHub: [github.com/samuelenosunday](https://github.com/samuelenosunday)
- Email: samuelenosunday@gmail.com

*Open to remote contract, part-time, and project-based AI training roles.*

Every prompt follows this template:
