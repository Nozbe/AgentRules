# AgentRules

A set of rules for working with AI agents in Nozbe over a local MCP connection.

[Nozbe](https://nozbe.com) is a task and project management app for teams. AI agents can join a Nozbe team, work on tasks and talk with people in comments. Read more about AI agents in Nozbe at [nozbe.com/ai](https://nozbe.com/ai).

## Files

- [`nozbe.md`](nozbe.md): the rules for how an AI agent works in Nozbe — which team and project it works in, how it handles tasks and comments, and how it collaborates with people.
- [`setup.md`](setup.md): a prompt for the initial setup of a repository. It checks the Nozbe connection, asks for the team, the director, the agent and the project, and adds them and the rules to the repository's CLAUDE.md. It can also set up a check every 15 minutes, so the agent picks up delegated tasks on its own.

Each file has a Polish version, [`nozbe.pl.md`](nozbe.pl.md) and [`setup.pl.md`](setup.pl.md), translated automatically from the English one.

## How to work with a teammate in Nozbe who is an… AI agent?

1. [Get a free Nozbe account (or Premium — knock yourself out!)](https://nozbe.com/). Nozbe is free with no time limit for up to 3 projects and 3 people on the team (agents included!), with unlimited tasks, so you don't need to pay anything to start.
2. Once you've got your account, invite the AI agent to your team. Go to "Members", hit "+" to "Invite new member to your space" and use another email address you can access, so you can confirm and set up your agent's account. Open your agent's account in a different browser session to set it up. Give it a name and optionally an avatar (why not?). You can use [`agent.png`](agent.png) from this repository.
3. Get the [Nozbe desktop app](https://nozbe.com/download) for Windows or Mac and install it.
4. Log in to your agent's account on the desktop app. Not yours. Your agent's!
5. Go to "Settings" → "Integrations" → "MCP" and enable the local MCP connection.
6. Copy the `claude mcp add …` command that Nozbe shows there. Then open Claude Code in the folder (new or existing) where you want to work with the agent and paste the command into the chat. Claude will run it and add the Nozbe connection. Start a new chat afterwards so Claude picks it up.
7. In that new chat, paste the prompt from [`setup.md`](setup.md) to set up your agent.
8. From now on, you can work with your agent directly through Nozbe: delegate tasks to it and talk in comments. Good luck!

Any questions? Contact me, the author of this repo: [Michael Sliwinski, CEO of Nozbe](https://michael.team/).

## Improvements?

Ideas for improving the setup? Better rules of engagement? Pull requests are welcome!
