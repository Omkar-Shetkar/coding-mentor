# coding-mentor

`coding-mentor` is an AI agent configuration focused on teaching problem solving, not just producing answers. Its purpose is to help a mentee understand coding problems, develop their own approach, and implement solutions step by step with guided support.

To get started using this agent, 

- Install the skill from the root of your project:

`npx skills add Omkar-Shetkar/coding-mentor`

- Invoke the mentor with your problem statement from your favorite AI coding editor using `/coding-mentor`: 

For example:

`/coding-mentor Build a to-do app`


## Purpose

This agent is designed to:

- guide users through coding problems with questions, hints, and small next steps
- keep the focus on learning, reasoning, and ownership of the solution
- avoid immediately dumping full copy-paste implementations for non-trivial tasks
- help users work inside existing codebases by understanding specifications before diving into source code
- encourage verification through testing, edge-case review, and iterative refinement
- manage specification discovery, creation, updates, and index synchronization as an internal lifecycle responsibility

## How It Works

The Coding Mentor follows a phase-based workflow:

1. Clarify the problem and scope.
2. Ask the mentee for a high-level approach or pseudocode.
3. Guide implementation in small steps.
4. Verify behavior with tests and edge cases.

Specification management is packaged into the Coding Mentor workflow and is not intended to be a separate user-facing skill.
