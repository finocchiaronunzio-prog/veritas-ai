# Veritas AI - Data Model v1.0

## Overview

Veritas AI is a Conversation Intelligence Platform.

The platform does not determine truth or deception.

Its purpose is to:

- Establish behavioral baselines
- Detect conversational signals
- Track consistency across sessions
- Generate intelligent follow-up questions
- Build evolving subject profiles over time

---

# User

Represents the person using Veritas.

## Fields

| Field | Type |
|---------|---------|
| user_id | UUID |
| name | String |
| email | String |
| created_at | Timestamp |

---

# Subject

Represents the person being analyzed.

A Subject can have multiple sessions.

## Fields

| Field | Type |
|---------|---------|
| subject_id | UUID |
| user_id | UUID |
| nickname | String |
| baseline_confidence | Integer |
| sessions_count | Integer |
| last_session_date | Timestamp |
| created_at | Timestamp |

## Example

Subject:
John

Baseline Confidence:
82%

Sessions:
4

---

# Session

Represents a single interview or conversation.

Each Subject can have many Sessions.

## Fields

| Field | Type |
|---------|---------|
| session_id | UUID |
| subject_id | UUID |
| objective | String |
| status | String |
| veritas_index | Integer |
| started_at | Timestamp |
| ended_at | Timestamp |

## Status Values

- Active
- Completed
- Archived

---

# Question

Represents an individual question.

## Fields

| Field | Type |
|---------|---------|
| question_id | UUID |
| session_id | UUID |
| question_text | Text |
| source | String |
| created_at | Timestamp |

## Source Values

- baseline
- ai_generated
- user_created
- follow_up

---

# Answer

Represents the response to a question.

## Fields

| Field | Type |
|---------|---------|
| answer_id | UUID |
| question_id | UUID |
| answer_text | Text |
| response_time_seconds | Number |
| answer_duration_seconds | Number |
| input_type | String |
| created_at | Timestamp |

## Input Types

- voice
- text
- mixed

---

# Observation

Represents a detected conversational event.

## Fields

| Field | Type |
|---------|---------|
| observation_id | UUID |
| session_id | UUID |
| question_id | UUID |
| type | String |
| label | String |
| confidence | Integer |
| timestamp | String |
| description | Text |

## Example Types

- Delayed Response
- Topic Avoidance
- Gaze Shift
- Hand To Face
- Voice Pattern Shift
- Timeline Inconsistency
- Increased Response Effort

---

# Baseline

Represents the evolving behavioral profile of a Subject.

This profile improves after every completed session.

## Fields

| Field | Type |
|---------|---------|
| baseline_id | UUID |
| subject_id | UUID |
| confidence | Integer |
| average_response_time | Number |
| average_answer_length | Number |
| communication_style | String |
| last_updated | Timestamp |

## Example

Communication Style:
Detailed Narrative

Average Response Time:
2.4 seconds

Baseline Confidence:
84%

---

# Report

Represents the final output of a Session.

## Fields

| Field | Type |
|---------|---------|
| report_id | UUID |
| session_id | UUID |
| veritas_index | Integer |
| summary | Text |
| key_findings | JSON |
| follow_up_questions | JSON |
| created_at | Timestamp |

---

# Relationships

User
└── Subjects

Subject
├── Baseline
└── Sessions

Session
├── Questions
├── Answers
├── Observations
└── Report

Question
└── Answer

Observation
└── Question

---

# Future Version (v2.0)

Planned Features:

- Subject Memory
- Cross-session behavioral comparison
- AI-generated dynamic interview trees
- Question effectiveness scoring
- Community-contributed questions
- Adaptive baseline evolution
- Multi-session trend analysis
