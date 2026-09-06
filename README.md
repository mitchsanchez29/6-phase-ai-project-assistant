# 6-phase-ai-project-assistant
A structured AI project orchestration framework that guides projects through six phases: Think, Design, Build, Validate, Launch, and Improve.

## Overview

The 6-Phase AI Project Assistant is a framework for managing projects with multiple AI tools.

Instead of asking one AI to handle an entire project, each phase has a specific purpose, role, output, and validation gate.

The goal is to make AI-assisted projects more structured, consistent, traceable, and easier to manage.

## The 6 Phases

| Phase | Name     | Purpose                                   | Primary AI           |
| ----- | -------- | ----------------------------------------- | -------------------- |
| 1     | THINK    | Define and understand the project         | ChatGPT              |
| 2     | DESIGN   | Create the system and technical blueprint | Claude               |
| 3     | BUILD    | Implement the approved design             | Codex / Claude       |
| 4     | VALIDATE | Test and verify the product               | Claude               |
| 5     | LAUNCH   | Prepare and deploy the product            | AI + Tools           |
| 6     | IMPROVE  | Monitor, learn, and continuously improve  | AI Project Assistant |

## Core Workflow

```text
IDEA
  ↓
THINK
  ↓
GATE 1
  ↓
DESIGN
  ↓
GATE 2
  ↓
BUILD
  ↓
GATE 3
  ↓
VALIDATE
  ↓
GATE 4
  ↓
LAUNCH
  ↓
GATE 5
  ↓
IMPROVE
  ↓
NEXT ITERATION
```

## Core Principles

### 1. One Project State

Every project maintains a single source of truth containing its current state, requirements, decisions, tasks, risks, issues, artifacts, validation results, and history.

### 2. Specialized AI Roles

Each AI tool is assigned a specific role instead of asking every AI to perform the entire project.

### 3. Structured Handoffs

Every phase produces a handoff package containing the information required by the next phase.

### 4. Validation Gates

A project cannot automatically move to the next phase until the required gate has been passed.

### 5. Traceability

Requirements, decisions, tasks, issues, and validation results should be connected so that project changes can be tracked.

### 6. Human Oversight

The AI Project Assistant supports decision-making and orchestration. Final project decisions remain under human control.

## Project State

The Project State is the central record of a project's current condition.

It will contain:

```text
Identity
Objective
Scope
Phase
Requirements
Decisions
Tasks
Risks
Issues
Artifacts
Handoff
Validation
Versions
Changelog
```

## Phase Outputs

### Phase 1 — THINK

Produces:

* Project Brief
* Requirements
* MVP Definition
* Risks
* Open Questions
* Decisions

### Phase 2 — DESIGN

Produces:

* System Architecture
* User Flow
* Data Model
* UI/UX Specification
* Technical Specification
* Integration Specification
* Security Considerations

### Phase 3 — BUILD

Produces:

* Source Code
* Components
* Integrations
* Tests
* Build Documentation
* Build Log

### Phase 4 — VALIDATE

Produces:

* Test Plan
* Test Results
* Bug Reports
* Security Review
* UX Review
* Validation Report

### Phase 5 — LAUNCH

Produces:

* Deployment Guide
* Production Checklist
* User Documentation
* Backup Plan
* Launch Report

### Phase 6 — IMPROVE

Produces:

* Feedback Analysis
* Improvement Backlog
* Prioritized Tasks
* New Requirements
* Version Updates
* Future Roadmap

## Phase Gate Principle

Every phase follows this rule:

```text
Required Input
     ↓
AI Work
     ↓
Required Output
     ↓
Validation
     ↓
Gate
     ↓
Next Phase
```

Possible gate results:

```text
PASS
PASS WITH WARNINGS
FAIL
BLOCKED
```

## Handoff Principle

The next AI should not need to reconstruct the entire project from previous conversations.

Instead, each phase generates a structured handoff containing:

* Project context
* Completed work
* Approved requirements
* Decisions
* Constraints
* Open questions
* Current tasks
* Known risks
* Required next actions

## Planned Architecture

```text
                    PROJECT ASSISTANT
                           |
             +-------------+-------------+
             |                           |
       PROJECT STATE                 PHASE ENGINE
             |                           |
             +-------------+-------------+
                           |
                      AI ROUTER
                           |
          +----------------+----------------+
          |                |                |
       ChatGPT           Claude           Codex
          |                |                |
        THINK           DESIGN           BUILD
                           |
                        VALIDATE
                           |
                         LAUNCH
                           |
                        IMPROVE
```

## Repository Structure

The planned repository structure is:

```text
6-phase-ai-project-assistant/
│
├── README.md
│
├── framework/
│   ├── phases/
│   ├── gates/
│   ├── handoffs/
│   └── schemas/
│
├── agents/
│   ├── think/
│   ├── design/
│   ├── build/
│   ├── validate/
│   ├── launch/
│   └── improve/
│
├── project-state/
│
├── templates/
│
├── docs/
│
└── src/
```

## Development Roadmap

### Version 0.1 — Framework Definition

* [x] Define 6 phases
* [x] Define phase responsibilities
* [x] Define Project State concept
* [ ] Define Project State schema
* [ ] Define Handoff schema
* [ ] Define Phase Gates
* [ ] Define AI Agent Instructions

### Version 0.2 — Framework MVP

* [ ] Create project templates
* [ ] Create phase prompts
* [ ] Create handoff templates
* [ ] Create gate definitions
* [ ] Create basic project controller

### Version 0.3 — AI Integration

* [ ] AI routing
* [ ] Context generation
* [ ] Automated handoffs
* [ ] Project State updates
* [ ] Validation workflow

### Version 1.0 — Working AI Project Assistant

* [ ] Complete six-phase workflow
* [ ] Project dashboard
* [ ] Automated project state
* [ ] AI agent integration
* [ ] Validation and gate system
* [ ] Documentation
* [ ] Real-world project testing

## First Test Project

The first real-world project used to test this framework will be **XYMONY**.

The goal is to use the framework to identify weaknesses in the workflow and improve the system before expanding it.

## Status

**Current Phase:** Framework Development

**Version:** 0.1.0

**Status:** In Development

---

## Vision

The long-term goal is to create an AI-assisted project operating system where multiple AI tools can work together through a structured process while maintaining shared project context, clear responsibilities, controlled handoffs, and measurable validation.
