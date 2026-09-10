---
name: agent-dev
description: >-
  For execution and runtime work.
---

# agent-dev

## Scope
Development of the agent's core execution loop, tool integrations, and runtime behavior.

## Guidelines
1. **Isolation**: Ensure the agent operates within its defined sandbox and respects token efficiency rules.
2. **Tooling**: When adding new tools, ensure they have strict validation and fail gracefully.
3. **Logging**: Maintain clear audit logs of all agent actions and decisions.
4. **State Management**: Ensure that the agent's state can be safely serialized and restored (using handoff/pickup patterns).

## Verification
- Test tool execution with edge cases and malformed inputs.
- Verify that the agent respects context limits and does not hallucinate commands.
