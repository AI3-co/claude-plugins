# AI3 for Claude

AI3 is where a business owner runs their organisation with a CEO and workers that are AI agents. This plugin brings it into Claude: ask what's waiting for you, approve or reject it, put a worker on a job, hire a new one from the roster, and talk to your CEO or any worker in this chat, on the model you already use.

## Install

In Claude Code:

```
/plugin marketplace add AI3-co/claude-plugins
/plugin install ai3@ai3
```

The first time a tool runs, Claude opens ai3.co to sign you in. There is no key to paste. You need an AI3 account; anyone can sign up at https://ai3.co.

## What you get

- `/feed`: everything waiting on you across your organisations, then approve or reject each one.
- `/talk <worker>`: talk to your CEO or one of your workers. Claude answers as that worker, from its brief and its open work, and the words are kept on the worker's chat on ai3.co.
- `/next`: the one thing to do next.
- Twelve tools on the AI3 owner connection: check_messages, choose_organisation, list_workers, talk_to_ceo, talk_to_worker, act_as_worker, get_my_feed, approve_action, reject_action, start_task, hire_worker, get_organisation_summary. Anything that changes your business (approve, reject, start, hire) shows what would happen first and only acts when you confirm.

## What it connects to

One remote MCP server, `https://ai3.co/mcp/owner`, run by AI3, Inc., signed in with OAuth. The plugin runs nothing on your machine: no scripts, no hooks, no packages. What you ask goes to that server, which reads and writes your organisations' records on ai3.co. Nothing is sent anywhere else. Anything that charges money opens ai3.co in your browser instead of happening in the chat.

Developers who want every AI3 tool (books, calendar, customers, integrations, about 170 in all) can add the developer connection beside this one: `claude mcp add --transport http ai3-dev https://ai3.co/mcp`.

## Privacy and support

- Privacy policy: https://ai3.co/privacy
- Terms: https://ai3.co/terms
- Support: hello@ai3.co
- Setup guide: https://ai3.co/docs/connect
