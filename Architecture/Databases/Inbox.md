# Database Blueprints

# Inbox Database

## Purpose
Acts as the default capture point for the entire system.

The Inbox prioritizes:
- speed
- low friction
- temporary storage
- later processing

It is not intended for long-term organization.

---

# Responsibilities

The Inbox stores:
- quick tasks
- ideas
- notes
- links
- references
- temporary thoughts
- uncategorized information

---

# Core Principles

- Capture first, organize later
- Minimal required properties
- Fast entry over structure
- Temporary holding area

---

# Processing Philosophy

Inbox items should eventually be:
- converted
- moved
- linked
- archived

The Inbox should not become permanent storage.

---

# Essential Properties

| Property | Type | Purpose |
|---|---|---|
| Title | Title | Main captured content |
| Type | Select | Task / Note / Idea / Resource / Project |
| Created | Created Time | Automatic capture timestamp |
| Status | Select | Unprocessed / Processing / Processed |
| Priority | Select | Optional quick importance indicator |
| Project Reference | Relation (optional) | Temporary project linkage |
| Notes | Text | Additional quick context |

---

# Optional Future Properties

| Property | Purpose |
|---|---|
| Source | Track where capture came from |
| Tags | Temporary categorization |
| Processed Date | Track inbox clearing |
| Converted To | Link to final destination |

---

# Inbox Rules

- Inbox capture must remain extremely fast
- Avoid excessive required fields
- Inbox is temporary, not permanent storage
- Inbox should be reviewed daily

---

# Inbox Workflow

```text
Capture
→ Inbox
→ Process
→ Move to Proper System
```

---

# Possible Destinations

- Projects
- Tasks
- Notes
- Resources
- Archives

---

# Design Notes

The Inbox is one of the most critical systems in the architecture.

A high-friction Inbox breaks:
- capture flow
- trust in the system
- speed of thought recording

The Inbox should always remain lightweight.
