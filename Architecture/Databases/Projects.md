# Projects Database

# Purpose

Stores active initiatives and operational goals.

Projects act as the central execution units of the system.

They connect:
- tasks
- notes
- resources
- execution workflows

---

# Responsibilities

Projects are responsible for:
- execution tracking
- progress tracking
- deadline management
- operational organization
- linking related knowledge

---

# Core Principles

- Projects drive execution
- Projects contain operational context
- Projects should remain actionable
- Projects are temporary by nature

---

# Essential Properties

| Property | Type | Purpose |
|---|---|---|
| Name | Title | Project title |
| Status | Status | Active lifecycle state |
| Priority | Select | Importance level |
| Start Date | Date | Project start |
| Deadline | Date | Expected completion |
| Progress | Number | Completion tracking |
| Tasks | Relation → Tasks | Linked execution tasks |
| Notes | Relation → Notes | Linked knowledge |
| Resources | Relation → Resources | Linked references |
| Area | Relation → Areas | Responsibility domain |

---

# Suggested Status Flow

```text
Planning
→ Active
→ On Hold
→ Completed
→ Archived
```

---

# Relationships

## Tasks
Projects may contain multiple tasks.

Tasks support project execution.

---

## Notes
Projects may reference knowledge and thinking.

Knowledge remains independent from projects.

---

## Resources
Projects may link:
- documentation
- tutorials
- external references

---

## Areas
Projects belong to broader responsibility domains.

Examples:
- Development
- Learning
- Career

---

# Progress Philosophy

Progress should remain simple.

Avoid:
- excessive KPI systems
- overly complex analytics
- formula-heavy scoring

Progress exists to support execution clarity.

---

# Dashboard Role

Projects are one of the primary dashboard elements.

The dashboard should emphasize:
- active projects
- focus projects
- deadlines
- execution status

---

# Archive Philosophy

Completed or inactive projects are archived.

Archived projects:
- remain searchable
- preserve linked knowledge
- preserve historical context

---

# Design Notes

Projects are the operational backbone of the system.

The architecture is intentionally:
- project-centric
- execution-oriented
- scalable
- modular
