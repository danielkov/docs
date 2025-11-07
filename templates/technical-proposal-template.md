# Technical proposal template

> [!WARNING]
> This template is a starting point. Work with your peers to customise it for your company's needs, culture, and technical context.

---

## 💡 Product proposal

> [!NOTE]
> This section gets you buy-in before diving into implementation details. Share this with stakeholders, get feedback, iterate, and only proceed to Part 2 once you've validated the idea is worth building.

### 🎯 What are you trying to solve?

State the problem clearly, without jumping to solutions. Use concrete examples, quantify the impact, and include data or user quotes where possible.

> [!TIP]
> "Users wait an average of 8 seconds for their transaction history to load, and we're seeing 23% drop-off at this screen." is better than "Transaction history is slow."

### 🚫 What are you NOT trying to solve?

Explicitly define what's out of scope to prevent scope creep and set clear boundaries. This gives you permission to say no to feature requests that don't align with the core problem.

### 🤷‍♂️ Why should this problem be solved?

Make the case for why this deserves engineering time and resources.

**Consider:**

- Impact on users (how many, how badly)
- Impact on business (revenue, retention, conversion, costs)
- Impact on engineering (tech debt, velocity)
- Impact on compliance or risk

Show your work with numbers and data.

### ⏰ Why now?

Explain why this is the right time to solve this problem.

**Think about:**

- External deadlines (regulatory, marketing, events)
- Internal readiness (infrastructure, team capacity)
- Dependencies (what needs to ship first)
- Opportunity windows (when will this be easier/harder)

### ✅ Requirements

List non-negotiable must-haves as testable statements. These should be specific and verifiable.

> [!TIP]
> Write requirements as testable statements:
>
> - "Transaction history must load in under 2 seconds at p95"
> - "Solution must work for users on iOS 14 and above"
> - "Data must be encrypted at rest and in transit"

### 🔍 High-level solution overview

Explain your solution in terms a non-technical stakeholder can understand. No tech jargon yet.

**Rules:**

- Avoid technical terminology
- Think user-centric (what changes from their perspective)
- Anchor on outcomes, work backwards
- If possible, offer 2-3 alternative approaches with pros/cons

---

### ☑️ Checklist

> [!IMPORTANT]
> Before proceeding to **Technical specification**, verify all items below. If you can't check all boxes, don't proceed yet. Get feedback, iterate, and validate the idea first.

- [ ] Problem statement is clear and specific
- [ ] Business impact is quantified
- [ ] Non-goals are explicitly stated
- [ ] Requirements are testable
- [ ] High-level solution makes sense to a non-engineer
- [ ] I'm confident this is worth doing

---

## 🔧 Technical specification

> [!NOTE]
> This section is more dynamic and collaborative. Write the first draft, then invite stakeholders to review and improve it. The plan should evolve based on feedback and what you learn.

### 📏 Best practices and company standards (optional)

If your implementation diverges from established practices, explain how and why.

> [!IMPORTANT]
> If proposing changes to standards, include:
>
> - Outside proof of concept (case studies from other companies)
> - Prior art from adjacent domains
> - Clear reasoning for why current approach doesn't work
> - Migration path from current to proposed state

### 🔄 Prior art and alternatives considered

Document what already exists and what other approaches you evaluated.

**Include:**

- Similar solutions that exist internally or externally
- Why you can't reuse existing solutions
- Table of alternatives with pros, cons, and rejection reasons

> [!TIP]
> If you find prior art that solves your problem, attach this spec to that solution's documentation to help maintainers understand stakeholders.

### ⚙️ Technical implementation details

Now you can get into implementation details. Explain architecture, tech stack choices, and design decisions.

**Include:**

- Architecture diagrams, sequence diagrams, data flow diagrams
- The "why" behind technical decisions, not just "what"
- Performance characteristics and scalability limits
- Data models, API contracts, key interfaces (with examples)
- New infrastructure or services needed

### 🗓️ Milestones

Decompose the solution into trackable milestones and tasks.

**Consider:**

- Phases that deliver incremental value (MVP → MLP → Full Product)
- Critical path vs nice-to-haves (use MoSCoW prioritization)
- What can be parallelised vs must be sequential
- Rough sizing (developer-hours, days, weeks)
- Explicit dependencies between tasks

### 📊 Success metrics

Define how you'll measure if this worked. What are your victory conditions?

**Include:**

- Measurable outcomes (latency, error rates, conversion, costs)
- Baseline metrics before implementation (screenshots of current state)
- How you'll track metrics (dashboards, alerts, A/B tests)
- Both business and technical metrics

### ⚠️ Risk assessment, dependencies and mitigation

Be brutally honest about what could go wrong.

**List:**

- External dependencies (other teams, third-party services)
- Single points of failure in your design
- Areas with high uncertainty
- Mitigation strategies or fallback plans for each major risk
- What you don't know yet (invite help)
- Compliance, security, or data privacy concerns

### 🚀 Rollout strategy

Explain how this will be deployed safely.

**Plan for:**

- Gradual rollout (5% → 10% → 50% → 100%)
- Feature flags to decouple deploy from release
- Rollback criteria (specific conditions that trigger rollback)
- Dark launching or shadow testing
- Data migration strategy (separate from code deploys)
- Communication plan for stakeholders and customers

#### ↩️ Rollback strategy

> [!CAUTION]
> Provide step-by-step instructions for reverting changes if things go wrong. This should be clear enough that anyone on the team can execute it during an incident.

**Example:**

1. Disable feature flag X
2. Or: roll back to commit abc123 and deploy
3. Run database script Y to revert schema changes
4. Clear cache Z to remove stale data
5. Monitor metrics A, B, C to confirm rollback successful
6. Post in #incidents channel with status

### 🧪 Testing approach

Explain how you'll validate this works.

**Cover:**

- Test coverage expectations (what needs extensive vs light testing)
- Load/performance testing for high-traffic features
- Chaos engineering for critical systems
- Edge cases and failure modes (not just happy paths)
- Manual QA/exploratory testing where needed
- Security testing for sensitive features

### 📅 Timeline and milestones

Provide realistic estimates with buffer for unknowns.

**Remember:**

- Work backwards from hard deadlines
- Pad estimates (1.2x for familiar, 1.5-2x for unfamiliar territory)
- Define clear milestones with demos every two weeks
- Call out external constraints (holidays, deadlines)
- Be realistic about team capacity (6 productive hours/day)
- Update estimates as you learn more

### ❓ Open questions

List what still needs to be figured out. This section should shrink over time.

**Include:**

- Unknowns that need research or prototyping
- Decisions requiring input from specific people/teams
- Assumptions that need validation with data
- Unresolved trade-offs
- Owner and target resolution date for each question

---

### ☑️ Part 2 checklist

> [!IMPORTANT]
> Before considering this complete, verify all items below.

- [ ] Implementation aligns with company standards (or makes case for divergence)
- [ ] Technical approach includes diagrams and explains "why" behind decisions
- [ ] Work is broken down into incremental phases
- [ ] Success metrics are specific and measurable
- [ ] Risks are identified with mitigation strategies
- [ ] Rollout and rollback plans are clear and actionable
- [ ] Testing approach covers edge cases and failure modes
- [ ] Timeline is realistic with appropriate padding
- [ ] Open questions have owners and deadlines

---

## Using this template

**Collaboration tips:**

- Use a platform that supports real-time comments (Notion, Google Docs, Confluence)
- Illustrate your points with mockups, diagrams, and metrics screenshots
- Leave your ego at the door - feedback now prevents production issues later
- Guide contributors to explain "why" and suggest alternatives, not just criticize
- Be ready to defend your value proposition with numbers
