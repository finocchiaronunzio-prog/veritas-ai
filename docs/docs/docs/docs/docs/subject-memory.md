# Subject Memory & Baseline Evolution

## Core Idea

Veritas does not treat every session as isolated.

Each Subject develops an evolving behavioral profile over time.

The goal is not to determine truth, but to compare new conversations against previously observed patterns.

---

## Subject Memory

A Subject Memory stores:

- baseline confidence
- previous sessions
- recurring conversational patterns
- common response style
- average response timing
- recurring clarification points
- previous observations
- historical Veritas Index trend

---

## Baseline Evolution

The baseline is created during the first calibration phase.

After every completed session, Veritas updates the baseline.

Baseline improves when:

- more answers are collected
- response timing becomes more stable
- speech/text patterns are observed repeatedly
- recurring behaviors are identified
- previous assumptions are confirmed or corrected

---

## Continue With This Subject

When the user selects:

Continue With This Subject

Veritas should:

- skip full baseline calibration
- load the existing subject profile
- show current baseline confidence
- continue from previous observations
- suggest follow-up questions based on past sessions

---

## Start New Subject

When the user selects:

Start New Subject

Veritas should:

- create a new subject profile
- ask for a new session objective
- perform baseline calibration
- begin a new independent session history

---

## Subject Profile Fields

| Field | Description |
|---|---|
| subject_id | Unique subject identifier |
| nickname | Optional subject label |
| baseline_confidence | Current confidence score |
| sessions_count | Number of completed sessions |
| last_session_date | Last time the subject was analyzed |
| recurring_patterns | Observations repeated across sessions |
| open_questions | Topics requiring clarification |
| veritas_index_trend | Historical index evolution |

---

## Future Features

- Subject Profile Screen
- Session comparison
- Baseline drift detection
- Long-term behavioral trend analysis
- Follow-up interview generation
