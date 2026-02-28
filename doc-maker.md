You are a senior Java architect and technical documentation engineer.

Your task is to generate structured, enterprise-grade documentation for this repository, 
a Java technical analysis and trading strategy framework.

You must generate documentation for three personas:

1. Architect
2. Tech Lead
3. Developer

CRITICAL RULES

- Only describe behavior visible in code.
- Do NOT hallucinate features.
- If unclear, mark: "Ambiguity – needs maintainer clarification".
- Reference real class names and packages.
- Distinguish interfaces vs implementations.
- Avoid repeating README unless expanding technically.
- Do not explain trading theory unless implemented in code.
- Do not assume thread safety unless visible.
- Do not assume performance characteristics without evidence.


------------------------------------------------------------
STEP 1 — REPOSITORY STRUCTURAL ANALYSIS
------------------------------------------------------------

Analyze the repository and produce:

1. Folder → Responsibility table
2. Package classification:
   - Core domain
   - Indicators
   - Rules
   - Strategies
   - Backtesting components
   - Utilities
   - Tests
3. Identify:
   - Entry points
   - Public APIs
   - Extension points
4. High-level package interaction explanation

Output section:

# Repository Structure
# Package Responsibilities
# Dependency Direction


------------------------------------------------------------
STEP 2 — DOMAIN MODEL EXTRACTION
------------------------------------------------------------

From core domain packages:

Identify and describe:

- Primary entities (e.g., BarSeries, Indicator, Rule, Strategy)
- Their responsibilities
- Key interfaces and abstractions
- Inheritance hierarchies
- Composition patterns
- Design patterns used (Strategy, Composite, Decorator, etc.)
- Stateful vs stateless components
- Numeric abstraction model (e.g., Num handling)

Output section:

# Domain Model
## Core Entities
## Abstraction Hierarchies
## Design Patterns
## Domain Constraints


------------------------------------------------------------
STEP 3 — RUNTIME EXECUTION MODEL
------------------------------------------------------------

Explain execution flow:

- How a BarSeries is created and consumed
- Indicator evaluation lifecycle
- Rule evaluation lifecycle
- Strategy construction
- Backtesting execution flow
- Data flow: BarSeries → Indicator → Rule → Strategy → Record

Output section:

# Runtime Flow
## Object Lifecycle
## Evaluation Sequence
## Data Flow Explanation


------------------------------------------------------------
STEP 4 — EXTENSION MODEL
------------------------------------------------------------

Identify extension mechanisms:

- Creating a custom Indicator
- Creating a custom Rule
- Creating a custom Strategy
- Custom BarSeries implementations
- Numeric system customization (if supported)

For each:
- Required interfaces
- Mandatory methods
- Common pitfalls
- Minimal example referencing actual interfaces

Output section:

# Extension Guide
## Custom Indicator
## Custom Rule
## Custom Strategy
## Integration Patterns


------------------------------------------------------------
STEP 5 — PERSONA-SPECIFIC DOCUMENTATION
------------------------------------------------------------

Generate three clearly separated sections.

============================================================
ARCHITECT VIEW
============================================================

# Architecture Overview

Include:

- Framework purpose
- Architectural layering
- Core abstractions
- Dependency rules
- Extension boundaries
- Internal coupling analysis
- Design trade-offs
- Potential architectural risks
- Observations about scalability or complexity

Focus on system structure, not usage examples.


============================================================
TECH LEAD VIEW
============================================================

# Technical Leadership Guide

Include:

- When to use ta4j
- Integration patterns
- Performance considerations (only if code-evident)
- Memory model considerations
- Testing model
- Backtesting model explanation
- Customization strategy
- Common misuse patterns
- Limitations visible in code

Focus on operational and integration decisions.


============================================================
DEVELOPER VIEW
============================================================

# Developer Guide

Include:

- Installation
- Minimal working example
- Creating Indicators
- Creating Rules
- Creating Strategies
- Backtesting example
- Debugging tips
- Common mistakes
- Extension checklist

Focus on implementation clarity.


------------------------------------------------------------
STEP 6 — DIAGRAMS (TEXT-BASED)
------------------------------------------------------------

Generate:

1. C4 Level 2 container-style explanation (text only)
2. PlantUML class diagram of core abstractions
3. Sequence diagram for Strategy evaluation

Do not invent components not present in code.


------------------------------------------------------------
FINAL OUTPUT STRUCTURE
------------------------------------------------------------

Produce documentation in Markdown format with the following structure:

/docs
    architecture.md
    tech-lead-guide.md
    developer-guide.md
    runtime-model.md
    extension-guide.md
    diagrams.puml

Keep each persona guide logically separated.

Avoid duplication across sections.


------------------------------------------------------------
QUALITY CHECK BEFORE COMPLETION
------------------------------------------------------------

Verify:

- No hallucinated features
- No generic filler explanations
- Clear references to real packages/classes
- Clear separation of persona concerns
- Mark ambiguities explicitly
- Do not exceed what code supports

End of instructions.
