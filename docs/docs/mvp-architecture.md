# Veritas AI MVP Architecture v1.0

## Purpose

This document defines the minimum functionality required to transform Veritas from a prototype into a usable MVP.

The goal is not to build the final product.

The goal is to create the smallest version that delivers real value to early users.

---

# MVP Definition

An MVP user should be able to:

1. Create a subject.
2. Define an interview objective.
3. Conduct an interview session.
4. Receive AI-generated questions.
5. Receive a final report.
6. Continue interviewing the same subject later.

If these six actions work, Veritas provides meaningful value.

---

# Core Architecture

User
↓
Subject
↓
Session
↓
Question Engine
↓
Observations
↓
Report

---

# MVP Module 1

## Subject Management

Purpose:

Store and retrieve subjects.

### Required Fields

* subject_id
* nickname
* baseline_confidence
* sessions_count
* last_session_date

### Required Actions

* Create Subject
* View Subject
* Continue Subject
* Start New Subject

---

# MVP Module 2

## Session Management

Purpose:

Store interviews.

### Required Fields

* session_id
* subject_id
* objective
* status
* started_at
* completed_at

### Status

* Active
* Completed

---

# MVP Module 3

## Baseline Engine

Purpose:

Create an initial behavioral profile.

### MVP Version

Simple.

Use 5 baseline questions.

Examples:

* Tell me about your day.
* What did you do this morning?
* Describe something interesting that happened recently.
* How was your week?
* What are your plans tomorrow?

### Output

* baseline_confidence
* communication_style
* average_response_length

---

# MVP Module 4

## Question Engine

Purpose:

Generate interview questions.

### Input

* interview objective
* previous answers
* previous observations

### Output

* current question
* recommended follow-up

### MVP Version

Use predefined question templates.

No adaptive learning required.

---

# MVP Module 5

## Observation Engine

Purpose:

Store notable conversational events.

### Examples

* Delayed Response
* Topic Avoidance
* Missing Detail
* Timeline Clarification Needed

### MVP Version

Manual or AI-generated observations.

No advanced behavioral analysis required.

---

# MVP Module 6

## Veritas Scoring Engine

Purpose:

Generate a session score.

### Components

Narrative Consistency
30%

Information Completeness
20%

Behavioral Stability
20%

Clarification Quality
15%

Conversational Engagement
15%

### Output

Veritas Index

0-100

---

# MVP Module 7

## Report Generator

Purpose:

Create final interview report.

### Sections

* Veritas Index
* Key Findings
* Conversation Signals
* Narrative Reconstruction
* Recommended Follow-Up Questions

---

# MVP Module 8

## Subject Continuity

Purpose:

Allow multiple sessions with the same subject.

### Workflow

Subject
↓
Session 1
↓
Session 2
↓
Session 3

Baseline improves over time.

---

# Not Included In MVP

The following features are intentionally excluded.

* Emotion Detection
* Lie Detection
* Truth Scoring
* Adaptive Learning
* Community Questions
* Voice Biometrics
* Multi-user Collaboration
* Predictive Analytics

These belong to future releases.

---

# MVP Success Criteria

The MVP is successful if users can:

* Create a subject
* Run a session
* Receive useful questions
* Receive a useful report
* Continue the same subject over time

Without requiring advanced AI infrastructure.

---

# Guiding Principle

Do not build everything.

Build the smallest version that proves users find value in Veritas.
