# Semantic IOUs

> A lightweight, human-centered way to track and manage technical debt — without breaking your flow.

---

## Why Semantic IOUs?

We all want to write clean, well-designed software. Principles like those John Ousterhout shares in *A Philosophy of Software Design* — clarity, simplicity, modularity — are goals we deeply believe in.

**But real life is messy.**

Tight deadlines, shifting priorities, and unexpected problems often leave us with less-than-ideal code. We don't always have the time to refactor immediately, even if we know something could (and should) be improved.

**Semantic IOUs** was created to bridge that gap: a practical, low-friction way to recognize, record, and eventually resolve technical debt — without sacrificing delivery.

This is a **proposal** in its early stage (**v0.0.1**) and is open to contribution. Ideas are welcome to expand keywords, refine categories, and build tools around this shared need.

---

## What is a Semantic IOU?

A **Semantic IOU** is a lightweight annotation directly in your code, marking an area that needs improvement. Each IOU carries enough semantic meaning to:

- Make the debt visible and trackable.
- Prioritize it later based on risk and impact.
- Keep your momentum today.

You don't have to stop and fix everything right now. But you won't lose sight of it either.

---

## Two Ways to Register an IOU

### 1. Quick Notation (Keywords)

When you spot something to improve, mark it fast:

```javascript
// IOU (keyword): short description
```

Example:

```javascript
// IOU (elephant): This class is too large and should be broken down.
```

#### Official keywords and their mapping:

| Keyword | Meaning | Category | Impact | Urgency |
|:--|:--|:--|:--|:--|
| elephant | Component too large or monolithic | structure | low | low |
| mess | Disorganized, hard-to-follow code | readability | medium | medium |
| iceberg | Small change hiding major complexity | structure | high | medium |
| rust | Obsolete or outdated code | error | medium | low |
| stair | Known workaround or risky bug | error | high | high |
| blackbox | Unclear or undocumented logic | structure | high | high |
| fragile | Code that easily breaks with changes | error | high | medium |
| quicksand | Critical zone that traps changes | structure | critical | high |

These mappings allow for later analysis, prioritization, or transformation into structured IOUs.

> Contributions are welcome to expand this keyword list in the future.

---

### 2. Extended Notation (Detailed)

When you have more time or the problem is critical, you can be more explicit:

```javascript
// IOU[category][impact][urgency]: short description
```

Example:

```javascript
// IOU[structure][high][high]: Separate business logic from presentation layer.
```

#### Default categories (expandable):
- `structure`
- `optimization`
- `readability`
- `performance`
- `security`
- `error`
- `other`

#### Impact levels:
- `low`, `medium`, `high`, `critical`

#### Urgency levels:
- `low`, `medium`, `high`

> Detailed annotations allow teams to prioritize debt resolution across modules and releases.

---

## Workflow Summary

1. **Spot** an issue while coding.
2. **Register** an IOU (quick or extended).
3. **Keep coding** — don't lose momentum.
4. **Review IOUs periodically** to prioritize and tackle improvements.
5. **Refactor and close IOUs** as part of your continuous improvement process.

---

## Why It Matters

- **IOU vs DEBT:** We use the term `IOU` instead of `DEBT` to emphasize a more human and constructive tone. It's not about guilt — it's about acknowledging areas for growth, with the intent to resolve them. An IOU is a promise, not a failure.

- **AI collaboration:** Because Semantic IOUs are structured and semantically meaningful, they open the door for **AI-assisted refactoring and improvement suggestions**. Future tools (or even LLMs) can parse IOUs, interpret their context, and propose or generate targeted improvements automatically.

- **Not a tool — a convention:** Semantic IOUs is not a static analyzer or platform like SonarQube. It's a **developer-friendly convention**, embedded in your workflow, that works alongside tools like Sonar. While Sonar finds syntax or logic issues automatically, IOUs capture what only humans can see: architectural shortcuts, intentions, and areas for design improvement.

- **IOU vs DEBT:** We use the term `IOU` instead of `DEBT` to emphasize a more human and constructive tone. It's not about guilt — it's about acknowledging areas for growth, with the intent to resolve them. An IOU is a promise, not a failure.

- **AI collaboration:** Because Semantic IOUs are structured and semantically meaningful, they open the door for **AI-assisted refactoring and improvement suggestions**. Future tools (or even LLMs) can parse IOUs, interpret their context, and propose or generate targeted improvements automatically.

- **Technical debt is inevitable** — but unmanaged debt is dangerous.
- **Context matters** — marking debt while it's fresh is far better than trying to remember later.
- **Better team communication** — IOUs create a shared, visible language for debt.
- **Scalable quality** — work pragmatically today, without abandoning software design principles tomorrow.

Semantic IOUs help you be both **realistic** and **responsible**.

---

## Future Ideas

- IOU scanner scripts (Node.js, Bash)
- Visual dashboards of project debt
- GitHub Actions to detect or monitor IOUs in PRs
- Debt aging tracking
- Suggested prioritization algorithms
- IDE snippet packs

---

## License

MIT License.

---

## Author & Contributions

Semantic IOUs was conceptualized as a pragmatic bridge between software design ideals and real-world delivery needs.

This is an open and evolving project. **Feel free to fork, suggest improvements, open issues, or submit PRs.**

---

> "First make it work. Then make it right. Then make it fast." — Classic engineering wisdom

Semantic IOUs help you remember: **"Make it right" isn't something you forget — it's something you honor in time.**
