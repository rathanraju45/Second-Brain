# Tasks Database

# Purpose

Stores actionable execution items.

Tasks represent concrete work that moves projects forward.

---

# Responsibilities

Tasks are responsible for:
- execution tracking
- scheduling
- prioritization
- operational progress

Tasks primarily support projects.

---

# Core Principles

- Tasks should remain actionable
- Tasks should be execution-focused
- Tasks should avoid excessive complexity
- Tasks exist to support project completion

---

# Essential Properties

| Property | Type | Purpose |
|---|---|---|
| Name | Title | Task title |
| Status | Status | Execution state |
| Priority | Select | Importance level |
| Start Date | Date | Planned start |
| Deadline | Date | Due date |
| Completed Date | Date | Completion tracking |
| Project | Relation → Projects | Linked project |
| Area | Relation → Areas | Responsibility domain |
| Notes | Relation → Notes | Optional related knowledge |
| Archived | Checkbox | Archive state |

---

# Suggested Status Flow

```text
Backlog
→ Planned
→ In Progress
→ Blocked
→ Completed
→ Archived
```

---

# Relationships

## Projects
Tasks may belong to projects.

Projects act as execution containers.

---

## Notes
Tasks may reference:
- research
- implementation notes
- temporary thinking

---

## Areas
Tasks may belong to broader responsibility domains.

---

# Task Philosophy

Tasks should remain:
- lightweight
- actionable
- easy to process

Avoid:
- excessive metadata
- overcomplicated scoring systems
- analytics-heavy structures

---

# Dashboard Role

Tasks are one of the primary operational components of LifeOS.

Dashboard focus:
- today tasks
- focus tasks
- upcoming deadlines
- blocked work

---

# Archive Philosophy

Completed or inactive tasks may be archived.

Archived tasks:
- remain searchable
- preserve project history
- preserve execution history

---

# Design Notes

Tasks are intentionally designed as:
- execution units
- project-support systems
- low-friction operational objects

The architecture avoids turning tasks into complex management objects.
