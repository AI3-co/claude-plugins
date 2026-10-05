---
name: feed
description: What's waiting on you across your AI3 organisations, then approve or reject each item. Use for "/feed", "what's waiting for me", "anything to approve".
---

Show the person what is waiting on them in AI3, then help them clear it.

1. Call `check_messages` on the `ai3` server. Show any message first, as written, with who sent it and from which organisation.
2. Call `get_my_feed`. If there are no items, say "Nothing is waiting on you." and stop.
3. List the items in the order given, one line each: organisation, title, and "now" when the urgency is now. Number them.
4. Ask which to approve and which to reject. For each one the person names:
   - Approve: call `approve_action` with the item's id and no `confirm`, show what would happen in one line, then call it again with `confirm: true` when the person agrees.
   - Reject: ask for the reason in a few words if they did not give one, then call `reject_action` with `reason`, the same way, preview first and `confirm: true` after.
5. Say what changed in one line per item. Never approve or reject anything the person did not name.

If the `ai3` server is not signed in, say so in one line and tell the person to run `/mcp` and choose ai3 to sign in.
