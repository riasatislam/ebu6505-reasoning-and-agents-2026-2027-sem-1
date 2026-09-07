# Block 2 Tutorial -- Bayesian Networks, Exact Inference, Temporal Models, MDP Planning, DDNs, and POMDPs

**Block 2 Tutorial**

Semester 1, 2026–2027 · Teaching Week 4

## Session Overview

- Session objective: Consolidate the full Block 2 reasoning arc from uncertain belief to hidden-state planning using longer-form tutorial problems.
- Timing target (min): 86
- Topic anchors: bayesian network; exact inference; dynamic bayesian network; markov decision process; dynamic decision network; partially observable markov decision process
- Padlet board: <https://padlet.com/qmul/b2-tutorial-6a1s440grh9uprtn>

## Exercises

### Q1 BN Structure and Assumptions

**Prompt**

A student says, “Once I draw a Bayesian network, the hard part is over because the edges already tell me the exact probabilities.” Explain why this statement is wrong, and include one point about graph structure, one about CPTs, and one about model assumptions.

**Task details**

- Type: concept
- Mode: pair
- Time: 10 min
- Deliverable: short explanation
- Assessment focus: explain what a BN structure commits you to
- Expected length: 4 bullets

**How to submit**

Post one pair Padlet comment with four short bullets.

**Discussion in class**

Which mistake is more dangerous: a wrong edge or a wrong number?

**Why this helps**

Helps with BN explanation questions in a fresh setting.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.12-13, pp.385-460
- Poole & Mackworth (2023) 3e, Ch.9, pp.375-458

### Q2 Dependence Reasoning

**Prompt**

Decide whether the end variables are dependent or independent in these three patterns, both before and after the middle variable is observed: (1) Weather -> Picnic -> Mood, (2) ExamStress <- Deadlines -> SleepLoss, (3) Malware -> Alert <- BenignSoftware.

**Task details**

- Type: problem
- Mode: individual
- Time: 10 min
- Deliverable: dependence judgements
- Assessment focus: reason about open and blocked paths in named scenarios
- Expected length: 6 answers

**How to submit**

Post your own Padlet comment with six answers and one short reason for each pattern.

**Discussion in class**

Which pattern changed most when the middle node was observed?

**Why this helps**

Strengthens conditional-independence reasoning in a fresh setting.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.12-13, pp.385-460
- Poole & Mackworth (2023) 3e, Ch.9, pp.375-458

### Q3 Exact Inference Practice

**Prompt**

In the Alarm network, compute P(Earthquake=true | JohnCalls=true, MaryCalls=false) using enumeration. You may reuse the standard Alarm network CPT values from class. Show the two unnormalized scores and the normalization step clearly.

**Task details**

- Type: problem
- Mode: individual
- Time: 12 min
- Deliverable: worked calculation
- Assessment focus: perform enumeration with normalization on a small BN query
- Expected length: 5 lines

**How to submit**

Post your own Padlet comment with the two scores, the normalization step, and the final posterior.

**Discussion in class**

Which hidden variable contributes most to the repeated work?

**Why this helps**

Gives exact-inference practice with a different query focus.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.13, pp.412-460
- Poole & Mackworth (2023) 3e, Ch.9, pp.375-458

### Q4 Variable Elimination and Complexity

**Prompt**

A medical BN has edges Season -> Pollen, Season -> Influenza, Pollen -> HayFever, Influenza -> Fever, and both HayFever and Influenza -> Sneezing. For the query P(Influenza | Sneezing=true), propose an elimination order and explain where factor growth becomes dangerous.

**Task details**

- Type: case
- Mode: group
- Time: 11 min
- Deliverable: elimination memo
- Assessment focus: choose a sensible elimination order and explain the risk of a bad one
- Expected length: order + 3 bullets

**How to submit**

Post one group Padlet comment with the order and three bullets on factor growth.

**Discussion in class**

Which variable feels harmless but becomes expensive if eliminated too early?

**Why this helps**

Builds VE intuition on a different network structure.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.13, pp.412-460
- Poole & Mackworth (2023) 3e, Ch.9, pp.375-458

### Q5 Temporal Model Choice

**Prompt**

Match each scenario to the most suitable temporal model: (1) temperature tracking with continuous noisy sensor values, (2) umbrella-and-rain style discrete hidden weather, (3) a robot with position, battery state, and sensor faults evolving together. Choose from hidden Markov model, Kalman filter, and dynamic Bayesian network, and explain why.

**Task details**

- Type: problem
- Mode: individual
- Time: 10 min
- Deliverable: model-choice explanation
- Assessment focus: choose between HMM, Kalman filter, and DBN
- Expected length: 3 labelled answers

**How to submit**

Post your own Padlet comment with three choices and one short reason each.

**Discussion in class**

Which feature most strongly forces the DBN choice?

**Why this helps**

Helps with temporal model selection under different assumptions.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.14, pp.461-499
- Poole & Mackworth (2023) 3e, Ch.9, pp.375-458

### Q6 Planning Model Choice

**Prompt**

A classmate makes these model choices: (1) “Use a partially observable Markov decision process for a one-off insurance purchase decision,” (2) “Use a decision network for a warehouse robot that moves every minute in a fully observed map,” and (3) “Use a Markov decision process for a wildfire drone when smoke hides the true fire boundary.” For each case, say whether the choice is correct. If it is wrong, replace it with a better model and give one reason.

**Task details**

- Type: exam
- Mode: individual
- Time: 10 min
- Deliverable: critique-and-correct note
- Assessment focus: diagnose wrong planning-model choices by checking repetition, observability, and uncertainty
- Expected length: 3 short corrections

**How to submit**

Post your own Padlet comment with three labelled judgements and one reason for each.

**Discussion in class**

Which mistake comes from ignoring repeated decisions, and which mistake comes from ignoring hidden state?

**Why this helps**

Strengthens planning-model discrimination through a critique-and-correct task.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.16-18
- Poole & Mackworth (2023) 3e, Ch.12, pp.517-582

### Q7 DDN and POMDP Synthesis Case

**Prompt**

Design a small incident-response pipeline for either healthcare or cybersecurity. Your design must include: a temporal belief update, one decision step, one utility consideration, one place where the true state is partly hidden, and one human oversight gate.

**Task details**

- Type: case
- Mode: group
- Time: 13 min
- Deliverable: mini workflow
- Assessment focus: connect belief, action, and human oversight in one applied pipeline
- Expected length: 6 bullets

**How to submit**

Post one group Padlet comment with six bullets covering those five required parts plus one domain-specific detail.

**Discussion in class**

Which part of the workflow carries the greatest uncertainty burden?

**Why this helps**

Helps with capstone synthesis thinking in a fresh applied scenario.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.17-18
- Poole & Mackworth (2023) 3e, Ch.12-13, pp.517-608

### Q8 Stretch Cross-Block Reflection

**Prompt**

Choose one agent setting from the module, such as healthcare assistant, cybersecurity response, or autonomous driving. Explain which Block 2 models are most useful there and which one would be overkill.

**Task details**

- Type: stretch
- Mode: pair
- Time: 10 min
- Deliverable: short reflection
- Assessment focus: connect Block 2 uncertainty tools to agent-system design choices
- Expected length: 5 bullets

**How to submit**

Post one pair Padlet comment with five bullets naming the useful models and the one that would be overkill.

**Discussion in class**

When is a more expressive uncertainty model not worth the complexity?

**Why this helps**

Helps students choose models intelligently rather than collecting jargon.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.12-18
- Poole & Mackworth (2023) 3e, Ch.9 and Ch.12-13, pp.375-608

## Submission Instructions

Use the seeded Padlet posts for Q1--Q8. Q2, Q3, Q5, and Q6 are individual. Q1 and Q8 are pair tasks. Q4 and Q7 should be one joint group comment. Start each comment with your names or group label.

## Whole-Class Debrief Prompts

- Which Block 2 model still feels the most abstract after the lecture week?
- Which tutorial problem felt closest to exam preparation without turning into an exam clone?
- Where does full observability break most clearly across the whole block?

## Exam Transfer Note (Day-Level)

This tutorial consolidates Bayesian networks, exact inference, temporal reasoning, MDP planning, DDNs, and POMDPs in an exam-preparation style across new application settings.
