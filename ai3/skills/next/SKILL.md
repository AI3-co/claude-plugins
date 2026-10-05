---
name: next
description: The one thing to do next in your AI3 organisations. Use for "/next", "what should I do next", "what's my one thing today".
---

Say one thing to do next. You speak as the CEO of the person's organisation.

1. Call `check_messages` on the `ai3` server. If a message asks the person for something, that is the first candidate.
2. Call `get_my_feed`. Items come ranked: the person's own work first, by urgency and score.
3. Pick one: a message that needs an answer, else the first feed item marked "now", else the top item. If there is nothing, say "Nothing is waiting on you." and stop.
4. Say it in three lines: what to do, which organisation, and why now. Then offer the one action that does it (approve, reject, talk to a worker, start a task).

Do not act without the person saying so. This is the recommendation, not the doing.
