# System Architecture

# Core Architecture

```text
Second Brain
│
├── Philosophy Layer
├── Database Layer
├── LifeOS Layer
└── Archive Layer
```

---

# Philosophy Layer

Purpose:
- Define system philosophy
- Explain PARA/CODE concepts
- Document workflows and principles
- Serve as the entry point of the system

Contains:
- Vision
- Principles
- System Guides
- Architecture Documentation Links

---

# Database Layer

Purpose:
- Backend data storage
- Logical relationships
- Structured information management

Core Databases:

```text
Databases
│
├── Inbox
├── Projects
├── Tasks
├── Notes
├── Areas
├── Resources
└── Archives
```

---

# Database Responsibilities

## Inbox
Temporary capture point for:
- ideas
- quick tasks
- notes
- links
- uncategorized information

Acts as the default entry point into the system.

---

## Projects
Stores active initiatives with:
- goals
- progress
- deadlines
- execution context

Projects act as the central operational units.

---

## Tasks
Stores actionable execution items.

Tasks:
- may belong to projects
- may exist independently temporarily
- support project execution

---

## Notes
Stores reusable knowledge and thinking.

Notes:
- exist independently
- may reference projects
- support long-term knowledge building

---

## Areas
Stores long-term responsibilities and domains.

Examples:
- Development
- Learning
- Career

Areas provide organizational stability.

---

## Resources
Stores reference materials and external information.

Examples:
- articles
- tools
- documentation
- tutorials

---

## Archives
Stores inactive or completed items while preserving searchability.

Archives are logically separated but remain accessible.

---

# LifeOS Layer

Purpose:
- Operational interface
- Execution environment
- Focus and workflow management

Core Sections:

```text
LifeOS
│
├── Today
├── Focus
├── Projects
├── Tasks
├── Knowledge Feed
├── Calendar
└── Reviews
```

---

# Workflow Architecture

```text
Capture
→ Inbox
→ Process
→ Organize
→ Execute
→ Review
→ Archive
```

---

# Relationship Philosophy

## Projects
Projects connect to:
- Tasks
- Notes
- Resources

Projects act as operational centers.

---

## Notes
Notes remain independent but may reference:
- Projects
- Areas
- Resources

---

## Tasks
Tasks primarily support projects.

Independent tasks are allowed when necessary.

---

# Design Principles

- Low-friction capture
- Project-centric execution
- Independent knowledge management
- Backend/frontend separation
- Simplicity over complexity
- Modular scalability
