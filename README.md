# AI Agent Capability & Boundary Evaluation Prompt

A standardized, multi-dimensional prompt designed to quickly evaluate, benchmark, and audit new AI agents, LLMs, coding assistants, and autonomous systems.

---

## 📋 The Benchmark Prompt

> **Tip**: Copy and paste the prompt block below directly into any new AI agent at the start of a conversation to establish clear capabilities and operational boundaries.

```markdown
Give me a quick capability overview:

1. **Inputs/outputs**: What formats can you take in and produce (text, files, images, audio, code, etc.)?
2. **Internet access**: Can you browse or search live, and what are the limits (blocked sites, rate limits, no real-time data, etc.)?
3. **Strengths**: What tasks do you handle best?
4. **Weaknesses**: What tasks are you noticeably worse at, or should I avoid relying on you for?
5. **Common misconceptions**: What do people typically assume you can do that you actually can't?
6. **Hidden complexity**: What's something you could build or do fairly easily that most people would assume is way harder than it is?

Keep it concrete. I'd rather have specific examples than general claims.
```

---

## 🎯 Purpose & Why This Works

When working with new AI models or autonomous agents, getting past marketing claims to understand real-world behavior usually requires hours of trial and error. 

This prompt cuts through fluff by pressing the agent on:
* **Modality Boundaries**: Exactly what formats it can read and generate.
* **Environmental Access**: Live web capabilities vs. offline knowledge limits.
* **Self-Awareness & Constraints**: Real weaknesses vs. generic disclaimers.
* **Surprise Capabilities**: Tasks where the agent punches above its weight.

---

## 🔍 Detailed Question Breakdown

| # | Focus Area | What You Are Probing | Red Flags in Answers |
|---|---|---|---|
| **1** | **Inputs & Outputs** | File system, image, audio, vision, tool calls, export formats | Vague answers like "I can handle text and code" without specifying file types. |
| **2** | **Internet Access** | Real-time search capability, domain restrictions, rate limits | Claiming live internet access when operating strictly on pre-training data. |
| **3** | **Core Strengths** | Task domains where the agent excels (e.g. refactoring, debugging, synthesis) | Broad claims ("I can do everything") without naming specific niches. |
| **4** | **Known Weaknesses** | Failure modes, context degradation, high-error domains | Only giving canned disclaimers rather than specific technical limits. |
| **5** | **Common Misconceptions** | Overestimated features (e.g., persistent memory across sessions, true real-time execution) | Confusing user expectations with actual system architecture. |
| **6** | **Hidden Complexity** | Counter-intuitive strengths (e.g. multi-step AST transforms, complex regex synthesis) | Generic answers that mirror standard user expectations. |

---

## 📊 Evaluation Rubric

When evaluating an agent's response, look for the following quality indicators:

- **Specificity**: Does the agent give concrete examples (e.g., *"I can parse JSON up to 10MB and output SVG diagrams"*) rather than vague statements?
- **Honesty**: Does the agent acknowledge real architectural limitations (e.g., execution sandboxes, context window cutoffs, context leaks)?
- **Tool Awareness**: Does the agent explicitly mention its tool bindings (e.g. shell access, file read/write, browser invocation)?

---

## 📄 Raw Prompt File

If you need to fetch the prompt programmatically or via CLI:
* Raw file: [PROMPT.md](PROMPT.md)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE). Feel free to share, adapt, and incorporate into your own evaluation pipelines.