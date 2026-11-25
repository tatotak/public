# Estimation

When evaluating a task, look at it from different angles to get a more complete picture. The
dimensions inform the discussion - there is no formula for combining them.

## Complexity

- Number of **components affected**
- **Logic**: input validation, business rules, processing logic, user input, special cases (affects
  maintenance)
- How intricate the change is and how it **fits within the architecture**

## Effort

- **Testing and refactoring** needed?
- Number of **people involved**?
- ~**Time** to complete? (rough guide only)

## Risk / Uncertainty

- **Clarity of requirements** (any edge cases?)
- **Likelihood of rework**
- **Importance and impact** of the systems involved

## Familiarity

- **Prior experience** with the area / system / component
- **Recency** - how long since last working with the system?
- **Knowledge gaps** (formal knowledge) and familiarity with tools
- **Similar changes** done recently?

## Dependencies

- **Coordination** needed with other teams / stakeholders?
- **Reliance** on other teams / systems / tools?
- **Feedback, approval or review** required from external parties?

## Other

- **Cutting corners**? (tech debt)
- How **careful** must the change be? (risk)
- **Handovers**

## Summary

| Pillar                 | Core question                                                               | Focus                                                                                                 |
|------------------------|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| **Complexity**         | *How intricate is the logic and how many parts of the system are affected?* | Logical and architectural intricacy: scope of components, system areas and complexity of logic        |
| **Effort**             | *How much work to implement and test?*                                      | Coding, testing and refactoring required                                                              |
| **Risk / Uncertainty** | *What unknowns or ambiguities exist? What assumptions are made?*            | Unknowns in requirements or task scope, plus edge cases or potential issues that could lead to rework |
| **Familiarity**        | *How experienced is the team with this area?*                               | Team knowledge, plus research or learning time for unfamiliar areas                                   |
| **Dependencies**       | *How reliant is this task on other teams?*                                  | Coordination and potential blockers                                                                   |

## Story points by dimension

| SP              | Complexity                                         | Effort                            | Risk / Uncertainty                            | Familiarity                                                    | Dependencies                                                    |
|-----------------|----------------------------------------------------|-----------------------------------|-----------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------|
| **1** · XS      | Small, isolated change                             | Quick and simple, minimal testing | None - clear requirements                     | Know the exact line of code                                    | None - fully independent                                        |
| **2** · S       | Straightforward, affects a few familiar components | A few hours of work               | Minimal ambiguity, low chance of bugs         | Did a similar task recently                                    | Light coordination only                                         |
| **3** · M       | Some logic changes, affects multiple components    | 1-3 days                          | Some edge cases or uncertainty                | Worked in the area before, need a light refresh                | Some external dependencies - extra coordination / communication |
| **5** · L       | Multiple modules, more complex logic               | ~1 week                           | Medium risk, unknowns need clarification      | Familiar patterns, but not recent                              | Moderate coordination needed                                    |
| **8** · XL      | System-wide or heavily integrated changes          | 1-2 weeks                         | High risk, performance or architecture impact | Limited prior exposure (do a spike)                            | Strong reliance on others                                       |
| **13** · XXL ⛔ | Major architectural change, system-wide impact     | Spans multiple sprints            | Very high risk, many unknowns                 | No prior experience, significant research needed, new patterns | Critical dependencies, high coordination overhead               |

**Notes**

- **Times in the Effort column are a rough guide only - not hour estimates.** Story points grow
  non-linearly, roughly following Fibonacci.
- **8 SP is the maximum acceptable size. 13 SP is never accepted - do a spike, then split.**