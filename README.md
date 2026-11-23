# Nami for Claude

[Nami](https://namiai.app) is an assistant that paces itself to the energy level you set. This
plugin connects Claude to your Nami and teaches it how Nami is meant to be used: plans in steps
you can start, sized to your level; your place kept when you stop; notes, memories, rests and
calendar entries put where you will see them.

It works in Claude on the web, desktop and mobile, in Cowork, and in Claude Code.

## What's inside

- **The Nami connector** (`.mcp.json`): the remote MCP server at `https://namiai.app/api/mcp`. It
  reads your planning board, the plans you kept, your notes, your memories, Recovery, what Today
  suggests and the calendars you connected, and it can add to and change them when you ask.
- **Skills**
  - `nami` - how to work with Nami: read your level first, read before changing, and what belongs
    on the board, on the Notes page, in a memory or in your calendar.
  - `plan-a-task` - put a plan on the board in small steps, split a step that is too big, and keep
    a plan that comes round again.
  - `stop-and-come-back` - keep your place when you stop, mark a task as waiting, take a rest in
    Recovery, and pick up from the step you left.

## Use it

Install the plugin, then connect the Nami connector from the plugin's **Connectors** tab and sign
in with your Nami account. In Claude Code it connects with the plugin; run `/mcp` to sign in.

Then ask for what you need:

- "Put renewing my passport on my Nami board. I'm at Low today."
- "What does Nami say I should do next?"
- "I have to stop. I was on the form, the photo is still missing."
- "I've sent the email, mark that as waiting until Friday."
- "Remember that I work best with headphones on."

You need a Nami account. The connector works whether or not you subscribe.

## What Claude can and cannot do

- Claude asks you before each change. Reading does not ask.
- It can delete a note, a memory, or a rest you added yourself, and it asks first. It cannot
  delete tasks, your account or anything else.
- It never sets your energy level on its own. A check-in is recorded only with what you said.
- Searching your memories is off while memories are switched off in Nami.
- Nami's own "Ask before Nami writes" setting covers Nami's chat, not Claude; Claude's own
  confirmation applies here.

## Data

The plugin holds only instructions and the connector's address. It runs no code on your machine
and stores nothing. Tool calls go from Claude to Nami at `namiai.app`, signed in as you, and act
on your own data there. What Claude reads becomes part of your conversation with Claude, which
Anthropic handles under its own terms. Nothing is sent to any other service. See Nami's
[privacy policy](https://namiai.app/privacy), under "If you connect Claude".

To disconnect, remove the connector in Claude.

## Install in Claude Code

```
/plugin install nami --marketplace entro314-labs/nami-claude-plugin
```

## Support

Write to hello@namiai.app.

## License

MIT. See [LICENSE](LICENSE).
