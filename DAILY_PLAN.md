# Daily AI-Assisted Learning Plan

> **Goal:** Become highly skilled at prompting AI and mastering software development, security, and system problem-solving through deliberate daily practice.

---

## 🗓️ Daily Schedule Overview

| Time Block | Duration | Activity |
|---|---|---|
| Morning Warm-Up | 15 min | Review yesterday's work + set today's goal |
| Deep Work | 60–90 min | Build / code / research a focused topic |
| AI Collaboration | 30 min | Generate, review, refine, and test with AI |
| Tool Practice | 15 min | Practice IDE tools, CLI, or workflow automation |
| Reflection & Tracking | 15 min | Log progress and update metrics |

---

## ✅ Pillar 1 — Treat AI as a Collaborative Tool

AI is a **pair programmer, not a replacement**. Use it to accelerate thinking, not to bypass it.

### Daily Habits
- [ ] Open a session with a clear goal: *"Today I want to learn/build/fix ___."*
- [ ] Ask AI to explain *why*, not just *what*: e.g., *"Explain why this approach is better than X."*
- [ ] Push back on AI output — challenge assumptions and ask for alternatives.
- [ ] Summarize what you learned in your own words after each AI session.

### Prompt Starters
```
"Act as a senior [role]. I'm a beginner learning [topic]. Explain [concept] with a simple example and one pitfall to avoid."
"I have this code. Walk me through what each part does and suggest one improvement."
"Compare approach A vs approach B for [problem]. What are the trade-offs?"
```

---

## ✅ Pillar 2 — Build Habit Loops (Generate → Review → Refine → Test)

Every learning cycle follows this loop to prevent passive consumption.

```
Generate  ──►  Review  ──►  Refine  ──►  Test
   ▲                                        │
   └────────────────────────────────────────┘
```

### The Loop in Practice
1. **Generate** — Use AI or your own knowledge to create a solution, explanation, or piece of code.
2. **Review** — Read it critically. What is unclear? What could break?
3. **Refine** — Improve it: better naming, error handling, edge cases, or clarity.
4. **Test** — Run it, break it, verify it works as expected.

### Daily Checklist
- [ ] Complete at least one full Generate → Review → Refine → Test cycle per day.
- [ ] Write down one thing you changed during *Refine* and why.
- [ ] Write down one thing you learned during *Test*.

---

## ✅ Pillar 3 — Write Prompts That Include Context and Constraints

A great prompt has four elements: **Role, Context, Task, Constraints**.

### Prompt Template
```
Role:        "Act as a [role, e.g. security engineer / Python developer]."
Context:     "I am building [what] for [who]. I'm currently [situation]."
Task:        "Help me [specific action]."
Constraints: "Keep it under [X lines / Y complexity]. Use only [language/library]. Avoid [anti-pattern]."
```

### Example (Bad vs. Good)
| ❌ Bad Prompt | ✅ Good Prompt |
|---|---|
| "Write me a login function." | "Act as a Python security engineer. I'm building a CLI tool for personal use. Write a login function that hashes passwords with bcrypt and returns a JWT token. Keep it under 30 lines and avoid storing plaintext passwords." |

### Daily Practice
- [ ] Write at least one structured prompt using the Role/Context/Task/Constraints template.
- [ ] Review the prompt after getting a response — could you have been more specific?
- [ ] Save useful prompt patterns in [`prompts/`](./prompts/) for reuse.

---

## ✅ Pillar 4 — Use the Tools Inside Your IDE and Workflow

Knowing your tools multiplies your effectiveness. Invest time learning them.

### Core Tools to Master
| Category | Tool | Learning Goal |
|---|---|---|
| Editor | VS Code / Neovim | Shortcuts, extensions, multi-cursor, refactor |
| AI Integration | GitHub Copilot / Cursor | Inline suggestions, chat, `/explain`, `/fix` |
| Version Control | Git | Branching, rebasing, bisect, stash |
| Terminal | Bash / Zsh | Scripting, pipes, aliases, process management |
| Debugging | DevTools / GDB / pdb | Breakpoints, watch expressions, call stacks |
| Security | Burp Suite / nmap | Scanning, intercepting, analysing traffic |

### Daily Practice
- [ ] Learn one new shortcut or command each day and use it at least five times.
- [ ] Use the AI chat inside your IDE (not the browser) to stay in flow.
- [ ] Automate one repetitive manual step per week using a script or tool feature.

---

## ✅ Pillar 5 — Always Verify Output with Tests and Reviews

Never ship or trust code you haven't verified — including AI-generated code.

### Verification Checklist (run every session)
- [ ] **Read the output** — does it actually do what you asked?
- [ ] **Run it** — execute the code and observe real behaviour.
- [ ] **Write a test** — even a simple assertion proves it works.
- [ ] **Edge cases** — what happens with empty input, huge input, invalid input?
- [ ] **Security check** — does this output expose credentials, allow injection, or leak data?
- [ ] **Code review** — ask AI *"What could go wrong with this code?"* before committing.

### Minimal Test Template (Python)
```python
def test_my_function():
    # Arrange
    input_value = ...
    expected = ...

    # Act
    result = my_function(input_value)

    # Assert
    assert result == expected, f"Expected {expected}, got {result}"
```

### Daily Practice
- [ ] Write at least one test for every function you create or modify today.
- [ ] Ask AI to review your code for bugs *before* you test it yourself.
- [ ] Log any bugs found during testing in [`logs/bugs.md`](./logs/bugs.md).

---

## ✅ Pillar 6 — Track Progress Using Measurable Project Outcomes

Vague effort is invisible. Measurable outcomes prove growth.

### Weekly Metrics to Track
| Metric | How to Measure |
|---|---|
| Projects completed | Count of projects pushed to GitHub |
| Concepts learned | Entries in [`logs/learning.md`](./logs/learning.md) |
| Bugs found & fixed | Entries in [`logs/bugs.md`](./logs/bugs.md) |
| Prompts refined | Saved prompts in [`prompts/`](./prompts/) |
| Tests written | Count of test files / assertions |
| Tools mastered | New shortcuts/commands logged |

### Weekly Review Template
```markdown
## Week of [DATE]

### What I built
- 

### What I learned
- 

### Biggest challenge
- 

### What I'll focus on next week
- 

### Metrics
- Projects completed:
- Concepts logged:
- Bugs fixed:
- Tests written:
```

### Daily Practice
- [ ] At the end of each session, add one line to [`logs/learning.md`](./logs/learning.md).
- [ ] At the end of each week, complete the Weekly Review Template above.
- [ ] Compare this week's metrics to last week's — are the numbers growing?

---

## 📁 Recommended Repository Structure

```
Beginning-Coding-Journey/
├── README.md               # Overview and goals
├── DAILY_PLAN.md           # This file — daily habits and templates
├── prompts/
│   └── README.md           # Saved, reusable prompt patterns
├── projects/
│   └── README.md           # Index of all projects with status
├── logs/
│   ├── learning.md         # Daily learning log
│   └── bugs.md             # Bug log — found, fixed, lesson learned
└── resources/
    └── README.md           # Curated links, books, and courses
```

---

## 🔁 End-of-Day Checklist

Before closing your editor, run through this list:

- [ ] Completed at least one full habit loop (generate → review → refine → test)
- [ ] Wrote or updated at least one test
- [ ] Logged today's learning in `logs/learning.md`
- [ ] Committed and pushed changes to GitHub
- [ ] Identified tomorrow's first task so you can start without friction

---

*"The best prompt you'll ever write is the one you refine after seeing the first answer."*
