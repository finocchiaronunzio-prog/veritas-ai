# Question Engine v1.0

## Overview

The Question Engine is the core intelligence layer of Veritas AI.

Its purpose is not to determine truth or deception.

Its purpose is to:

* Generate relevant questions
* Improve conversation quality
* Explore inconsistencies
* Identify missing information
* Adapt questioning strategies over time
* Learn from previous sessions

The effectiveness of Veritas depends largely on the quality of its Question Engine.

---

# Question Sources

Questions can originate from multiple sources.

Every question should contain a source identifier.

## Supported Sources

* baseline
* objective_driven
* ai_follow_up
* community
* adaptive

---

# Baseline Questions

Baseline Questions are used during the calibration phase.

Their purpose is to establish a behavioral reference profile.

## Examples

* Tell me about your day.
* What did you do this morning?
* How has your week been?
* Describe something interesting that happened recently.
* What are your plans for tomorrow?

## Goal

Collect:

* response timing
* response length
* communication style
* narrative structure
* conversational rhythm

---

# Objective Driven Questions

Generated from the user's interview objective.

The interviewer specifies what they want to understand.

Veritas generates relevant questions.

## Example Objective

Understand whether the story is internally consistent.

## Example Questions

* Can you walk me through the timeline?
* What happened immediately before that?
* What happened immediately after that?
* Who else was present?
* How certain are you about those details?

---

# AI Follow-Up Questions

Generated dynamically during a session.

Triggered by:

* topic avoidance
* timeline inconsistency
* response delay
* missing information
* clarification opportunities

## Example

Detected Signal:

Topic Avoidance

Suggested Follow-Up:

Could you explain that part in more detail?

---

# Community Questions

Questions contributed by users.

Community questions are evaluated over time.

Each question stores:

* usage_count
* effectiveness_score
* community_rating

## Example

Question:

What information might be missing from this explanation?

Usage Count:

1240

Community Rating:

4.7 / 5

---

# Adaptive Questions

Future capability.

Veritas automatically selects questions based on previous effectiveness.

The system learns which questions produce:

* more detailed responses
* better timeline reconstruction
* higher clarification rates
* stronger consistency validation

---

# Question Effectiveness

Every question should accumulate performance metrics.

## Metrics

| Metric              | Description                                   |
| ------------------- | --------------------------------------------- |
| usage_count         | Number of times used                          |
| answer_length       | Average response length                       |
| follow_up_rate      | Frequency of additional information generated |
| clarification_rate  | Frequency of useful clarification             |
| effectiveness_score | Overall performance score                     |

---

# Question Lifecycle

Question Created
↓
Question Used
↓
Response Collected
↓
Outcome Evaluated
↓
Effectiveness Updated
↓
Future Ranking Adjusted

---

# Future Enhancements

## Dynamic Interview Trees

Questions adapt based on previous answers.

## Session-Aware Questioning

Questions consider previous sessions with the same subject.

## Subject-Specific Recommendations

Questions generated from historical behavioral patterns.

## Community Learning Network

High-performing community questions become globally available.

## Reinforcement-Based Ranking

Questions automatically rise or fall in priority according to observed effectiveness.

---

# Veritas Principle

Veritas does not search for truth.

Veritas searches for clarity.

The purpose of every question is to improve understanding, reduce ambiguity, and increase conversational insight.
