# Block 1 Tutorial -- Reinforcement Learning, Knowledge Graphs, MCP, Multi-Agent Systems, and Coding Agents

**Block 1 Tutorial**

Semester 1, 2026–2027 · Teaching Week 3

## Session Overview

- Session objective: Consolidate the whole of Block 1 with longer-form problems that strengthen exam-style reasoning and applied understanding.
- Timing target (min): 86
- Topic anchors: reinforcement learning; knowledge representation; knowledge graph; mcp; a2a; coding agent; prompt injection
- Padlet board: <https://padlet.com/qmul/b3-tutorial-uqe9wb7pw5cpxo20>

## Exercises

### Q1 RL Intuition and Credit Assignment

**Prompt**

A student says, “Reinforcement learning is easy because the agent can just wait for the final reward and then know exactly what to do next time.” Explain why this is not true. Use the idea of delayed reward and credit assignment, and include one everyday example.

**Task details**

- Type: concept
- Mode: pair
- Time: 10 min
- Deliverable: short explanation
- Assessment focus: connect delayed feedback to credit-assignment difficulty
- Expected length: 4 bullets

**How to submit**

Post one pair Padlet comment with four short bullets and one example.

**Discussion in class**

Which part of the action sequence is hardest to assign credit to?

**Why this helps**

Helps with short explanation questions on delayed reward and why RL is hard.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.22, pp.789-822
- Poole & Mackworth (2023) 3e, Ch.13, pp.583-608

### Q2 RL Update and Interpretation

**Prompt**

In a delivery task, the agent is in state s4, takes action Wait, receives reward -1, and moves to s5. Suppose Q(s4,Wait)=2.5, max_a Q(s5,a)=4.0, alpha=0.4, and gamma=0.8. Compute the updated Q-value and explain in one sentence whether the new experience improved or worsened the old estimate.

**Task details**

- Type: problem
- Mode: individual
- Time: 11 min
- Deliverable: worked update
- Assessment focus: compute and interpret one Q-learning update
- Expected length: 5 lines

**How to submit**

Post your own Padlet comment with the substitution, the target, the final Q-value, and the interpretation sentence.

**Discussion in class**

Which term in the update carries the long-run estimate?

**Why this helps**

Good practice for RL calculations without reusing the exam numbers.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.22, pp.789-822
- Poole & Mackworth (2023) 3e, Ch.13, pp.583-608

### Q3 Knowledge Representation with IDs

**Prompt**

A campus assistant must answer: Which room hosts EBU6505 today, who teaches it, and how can a student contact the lecturer? Write seven triples using stable IDs, and make sure one of your triples stores a contact channel correctly.

**Task details**

- Type: problem
- Mode: individual
- Time: 10 min
- Deliverable: triple set
- Assessment focus: write stable triples with entities, relations, and attributes
- Expected length: 7 triples

**How to submit**

Post your own Padlet comment with seven triples and clear IDs.

**Discussion in class**

Which information is better stored as an attribute than as a linked entity?

**Why this helps**

Consolidates triple design and ID choices.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.10, pp.314-343
- Poole & Mackworth (2023) 3e, Ch.16, pp.701-730

### Q4 Graph Path, Provenance, and Context

**Prompt**

Your graph says Module_EBU6505 taughtBy Dr_Riasat_Islam, Dr_Riasat_Islam officeRoom TB_3_335, and a newer notice says officeRoom temporaryRoom QM_4_201 for this week only. Explain how the assistant should answer a student asking “Where can I find the lecturer today?” Include the graph path, the role of provenance, and what should go into the final context packet.

**Task details**

- Type: case
- Mode: group
- Time: 12 min
- Deliverable: reasoning path with trust note
- Assessment focus: use a graph path and explain what provenance changes
- Expected length: 1 path + 2 trust notes

**How to submit**

Post one group Padlet comment with the path, the answer policy, and two notes on provenance or evidence selection.

**Discussion in class**

Why is the newer fact not enough on its own without provenance?

**Why this helps**

Helps with graph reasoning and evidence-quality questions.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.10, pp.314-343
- Poole & Mackworth (2023) 3e, Ch.16-17, pp.701-766

### Q5 MCP Workflow Check

**Prompt**

A student proposes this MCP workflow: tool call -> user intent parse -> response synthesis -> capability discovery -> audit log -> evidence return. Rewrite it into a sensible order and explain two mistakes in the original version.

**Task details**

- Type: problem
- Mode: individual
- Time: 10 min
- Deliverable: corrected workflow
- Assessment focus: understand the parts and ordering of an MCP interaction
- Expected length: 6 steps + 2 fixes

**How to submit**

Post your own Padlet comment with the corrected order and two explained mistakes.

**Discussion in class**

Which mistake is most dangerous for safety?

**Why this helps**

Consolidates MCP flow understanding in a fresh scenario.

**References**

- https://modelcontextprotocol.io/specification/
- Russell & Norvig (2021) AIMA 4e, Ch.10, pp.314-343

### Q6 Multi-Agent and A2A Design

**Prompt**

Design a student-support workflow with a coordinator agent, retrieval agent, policy-check agent, and message-draft agent. Include one A2A handoff to an external scholarship-information agent and one trust check before the answer is accepted.

**Task details**

- Type: case
- Mode: group
- Time: 12 min
- Deliverable: orchestration sketch
- Assessment focus: design a trustworthy multi-agent workflow with one A2A handoff
- Expected length: 5 bullets

**How to submit**

Post one group Padlet comment with the role order, the handoff point, and the trust check.

**Discussion in class**

Which agent should never be allowed to act without evidence from another component?

**Why this helps**

Builds confidence for architecture and handoff questions in a new scenario.

**References**

- https://a2a-protocol.org/dev/
- doi:10.1016/j.cosrev.2026.100902

### Q7 Coding-Agent Safety Review

**Prompt**

A coding agent is asked to modify a grading script in a live course repository. Explain what context it must collect first, one risk from repository text, one risk from tool use, and one human checkpoint that should not be skipped.

**Task details**

- Type: exam
- Mode: pair
- Time: 11 min
- Deliverable: risk-focused response
- Assessment focus: explain a safe coding-agent workflow with controls
- Expected length: 180-220 words

**How to submit**

Post one pair Padlet comment with a clear structure covering context, two risks, and the checkpoint.

**Discussion in class**

Which repository risk is easiest for students to underestimate?

**Why this helps**

Consolidates coding-agent governance and safety without duplicating the exam pull-request question.

**References**

- https://openai.com/codex/
- https://docs.anthropic.com/en/docs/claude-code/overview
- https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/

### Q8 Stretch Synthesis

**Prompt**

Propose a small university assistant architecture that uses structured knowledge, one graph-backed retrieval step, one MCP tool interaction, and one safety rule for any coding or tool-using agent component.

**Task details**

- Type: stretch
- Mode: group
- Time: 10 min
- Deliverable: short architecture proposal
- Assessment focus: combine Block 1 ideas into one system design
- Expected length: 6 bullets

**How to submit**

Post one group Padlet comment with six bullets describing the architecture.

**Discussion in class**

Which Block 1 idea gives the biggest practical benefit in your design?

**Why this helps**

Helps students synthesise Block 1 without mirroring any single exam question.

**References**

- Russell & Norvig (2021) AIMA 4e, Ch.10, pp.314-343 and Ch.22, pp.789-822
- Poole & Mackworth (2023) 3e, Ch.13, pp.583-608 and Ch.16-17, pp.701-766
- https://modelcontextprotocol.io/specification/

## Submission Instructions

Use the seeded Padlet posts for Q1--Q8. Q2, Q3, and Q5 are individual. Q1 and Q7 are pair tasks. Q4, Q6, and Q8 should be one joint group comment. Start each comment with your names or group label.

## Whole-Class Debrief Prompts

- Which Block 1 idea still feels the least intuitive?
- Which exercise was closest to “exam thinking” without being an exam copy?
- Where do safety and structure interact most strongly across the whole block?

## Exam Transfer Note (Day-Level)

This tutorial consolidates RL, structured knowledge, graphs, MCP, A2A, and coding-agent safety in a way that supports exam preparation across fresh scenarios.
