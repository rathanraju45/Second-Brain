# Design Decisions

---

# System Identity

## Decision
The system will follow a Developer + Knowledge + Productivity hybrid architecture.

## Reason
The system is primarily intended to support:
- project execution
- learning
- research
- development workflows
- long-term knowledge building

Life management systems such as:
- fitness
- finance
- habits
- personal CRM

are intentionally postponed for future modular expansion.

---

# System Structure

## Decision
The architecture is divided into three major layers:

1. Second Brain Page
2. Databases Layer
3. LifeOS Layer

## Reason
This separation creates a clean distinction between:
- philosophy
- backend logic
- frontend operational experience

This prevents the dashboard and databases from becoming tightly coupled.

---

# Operational Model

## Decision
The system follows a project-centric workflow.

## Reason
Projects act as the primary operational units.

Tasks, notes, and resources support projects instead of existing independently.

This prevents:
- task clutter
- context switching confusion
- disconnected execution

especially when handling multiple parallel initiatives.

---

# Capture Philosophy

## Decision
The system follows an Inbox-first capture workflow by default.

## Reason
Low-friction capture is prioritized over immediate organization.

This reduces cognitive load during:
- idea capture
- task entry
- note collection
- research gathering

However, direct capture into specific databases is allowed when the destination is immediately obvious.

This preserves flexibility while maintaining structure.

---

# Knowledge Architecture

## Decision
Knowledge exists independently from projects but can reference projects when relevant.

## Reason
Some knowledge is:
- project-specific
- temporary
- execution-oriented

while other knowledge is:
- evergreen
- reusable
- independent of current work

Separating knowledge from projects improves long-term reusability.

---

# Dashboard Philosophy

## Decision
The LifeOS dashboard is execution-focused instead of analytics-focused.

## Reason
The dashboard should guide action and focus rather than display excessive metrics.

Priority is given to:
- current work
- focus
- actionable tasks
- active projects

instead of complex productivity analytics.

---

# Simplicity Principle

## Decision
Simplicity is prioritized over cleverness.

## Reason
The system must remain usable even during:
- stress
- overload
- busy project periods

Overengineering reduces long-term usability.

---

# Scalability Strategy

## Decision
The architecture must support modular expansion without redesigning the core system.

## Reason
Future systems such as:
- life management
- fitness
- finance
- habit tracking

should integrate into the existing structure cleanly.

The core architecture should remain stable as the system grows.

---

# Archive Strategy

## Decision
Archived items remain searchable within main databases.

## Reason
Historical information should remain accessible without requiring separate archive navigation.

Archived items may later receive:
- visual indicators
- archive filters
- archive views

instead of complete database separation.

---