You are a senior Java architect and technical documentation engineer.

Your task is to generate structured, enterprise-grade documentation 
for this repository (ta4j), a Java technical analysis and trading strategy framework.

The documentation must serve three personas:
1. Architect
2. Tech Lead
3. Developer

In addition to horizontal architecture documentation,
you MUST also produce vertical slice documentation
that traces end-to-end feature flows.

------------------------------------------------------------
GLOBAL RULES
------------------------------------------------------------

- Only describe behavior visible in code.
- Do NOT hallucinate features.
- If unclear, mark: "Ambiguity – needs maintainer clarification".
- Reference real class names and packages.
- Distinguish interfaces vs implementations.
- Avoid generic language.
- Do not assume thread safety unless visible.
- Do not assume performance characteristics without evidence.
- Do not explain financial theory unless implemented in code.

------------------------------------------------------------
STEP 1 — REPOSITORY STRUCTURE (HORIZONTAL VIEW)
------------------------------------------------------------

Analyze and produce:

1. Folder → Responsibility table
2. Package classification:
   - Core domain
   - Indicators
   - Rules
   - Strategies
   - Backtesting
   - Utilities
   - Tests
3. Identify:
   - Public APIs
   - Extension points
   - Dependency direction

Output:

# Repository Structure
# Package Responsibilities
# Dependency Direction


------------------------------------------------------------
STEP 2 — DOMAIN MODEL (HORIZONTAL ABSTRACTIONS)
------------------------------------------------------------

Extract:

- Primary entities (BarSeries, Indicator, Rule, Strategy, etc.)
- Abstraction hierarchies
- Inheritance trees
- Composition relationships
- Design patterns used
- Stateful vs stateless components
- Numeric abstraction model

Output:

# Domain Model
## Core Entities
## Abstraction Hierarchies
## Design Patterns
## Domain Constraints


------------------------------------------------------------
STEP 3 — RUNTIME FLOW
------------------------------------------------------------

Explain execution flow:

- Strategy construction
- Indicator chaining
- Rule evaluation
- Backtesting execution
- Data flow:
  BarSeries → Indicator → Rule → Strategy → TradingRecord

Output:

# Runtime Flow
## Object Lifecycle
## Evaluation Sequence
## Data Flow


------------------------------------------------------------
STEP 4 — VERTICAL SLICING DOCUMENTATION (MANDATORY)
------------------------------------------------------------

Identify 3–5 meaningful vertical slices (end-to-end flows).

Examples:
- Indicator evaluation slice
- Rule evaluation slice
- Strategy execution slice
- Backtesting slice
- Custom indicator extension slice

For each vertical slice:

1. Entry point (class/method)
2. Participating classes (ordered)
3. Interfaces involved
4. Data transformations
5. State mutations (if any)
6. Extension points inside the slice
7. Error handling behavior (if visible)
8. Test coverage references (if present)

Output:

# Vertical Slices

## Slice 1 — Indicator Evaluation
- Flow diagram (text-based)
- Participating classes
- Call chain
- Data propagation

## Slice 2 — Strategy Execution
...

Do NOT mix horizontal layering explanation here.
Focus strictly on end-to-end traversal.


------------------------------------------------------------
STEP 5 — EXTENSION MODEL
------------------------------------------------------------

Explain:

- How to create custom Indicator
- How to create custom Rule
- How to create custom Strategy
- Custom BarSeries integration
- Numeric system customization

For each:
- Required interfaces
- Mandatory methods
- Internal expectations
- Common pitfalls

Output:

# Extension Guide


------------------------------------------------------------
STEP 6 — PERSONA-SPECIFIC DOCUMENTATION
------------------------------------------------------------

============================================================
ARCHITECT VIEW
============================================================

Focus on:

- Architectural layering
- Abstraction boundaries
- Dependency direction
- Vertical slice integrity
- Coupling analysis
- Extension boundaries
- Design trade-offs
- Scalability observations
- Architectural risks

Output:
# Architecture Overview


============================================================
TECH LEAD VIEW
============================================================

Focus on:

- Integration strategy
- Backtesting workflow
- Performance considerations (code-visible only)
- Testing strategy
- Extension governance
- Safe customization patterns
- Vertical slice ownership
- Common misuse patterns
- Operational considerations

Output:
# Technical Leadership Guide


============================================================
DEVELOPER VIEW
============================================================

Focus on:

- Minimal working example
- How to build a complete vertical slice
- Creating Indicators, Rules, Strategies
- Debugging flow across slice
- Unit testing slices
- Extension checklist

Output:
# Developer Guide


------------------------------------------------------------
STEP 7 — DIAGRAMS
------------------------------------------------------------

Generate:

1. C4 Level 2 explanation (text)
2. PlantUML class diagram (core abstractions)
3. Sequence diagram for:
   - Strategy execution slice
   - Indicator evaluation slice

Do not invent components.


------------------------------------------------------------
FINAL OUTPUT STRUCTURE
------------------------------------------------------------

Produce Markdown files:

/docs
    architecture.md
    tech-lead-guide.md
    developer-guide.md
    runtime-model.md
    extension-guide.md
    vertical-slices.md
    diagrams.puml

Avoid duplication across documents.

Ensure vertical slicing section explicitly maps to runtime and domain model.

------------------------------------------------------------
QUALITY CHECK BEFORE COMPLETION
------------------------------------------------------------

Verify:

- No hallucinated functionality
- No generic filler
- Real class/package references
- Clear separation:
    Horizontal Architecture vs Vertical Slices
- Ambiguities clearly marked
- Personas properly segmented

End of instructions.
