# Rules for Working with AI in Nozbe

> **Source of truth.** This English file is the master version.
> `nozbe.pl.md` is translated from it — make every change here first, then regenerate the Polish file.

## 1. Purpose

These rules govern how an AI assistant works with my Nozbe account, in every repository and folder. A project's own CLAUDE.md only adds which Nozbe team and project it works in, who the director and the agent are, and any exceptions.

## 2. Scope

1. **The team is the one in CLAUDE.md.** Whenever these rules or I mention "the team" (workspace), it means the Nozbe team named in the current CLAUDE.md. Work only in that team. Don't show, read or change tasks, projects or comments from other teams. If I ask for something outside it, say so plainly and ask before acting. If CLAUDE.md names no team, ask which one before any Nozbe call.
2. **Two Nozbe users: the director and the agent.** CLAUDE.md defines two Nozbe users, each with their username and user ID:
   - **The director** is me, the human. In these rules, "I", "me" and "my" mean the director.
   - **The agent** is you, the AI. In these rules, "you" means the agent.

   Use these IDs to tell who wrote a comment, who a task is assigned to and who a mention is meant for. If CLAUDE.md doesn't define both users, ask before any Nozbe call.
3. **One project per repository.** In a repository, "tasks" and "projects" mean that repository's Nozbe project, named in its CLAUDE.md. Scope every call to that project. Don't read or change other projects unless I explicitly ask.
4. **New tasks are yours.** Create new tasks and projects only in the team. Assign every task you create to the agent (yourself) when it's created, since you'll start working on it right away.
5. **Always fresh data.** Fetch tasks and comments again directly from Nozbe whenever you report on them. Don't rely on lists from earlier in the conversation.

## 3. Task Lifecycle

1. **Plan goes to the task first.** Once we agree on a course of action for a task, add the plan as a comment on that task before starting the work. When you work on your own (rule 5.5), don't wait for agreement: post the plan and start right away, since changes can be reverted if needed.
2. **Never complete tasks yourself.** When work on a task is done (and committed, in a repository), move it to the **To be reviewed** section of its project (create the section if it doesn't exist yet), reassign it to the director so it shows up for my review (or to whoever asked for it; see rule 5.4), and ask whether to complete it. Complete a task only when I explicitly say so; I may have feedback.
3. **Check Nozbe after every commit.** After each commit, fetch the project's open tasks again and report what's pending outside "To be reviewed", including new tasks and new comments.

## 4. Comments and Checklists

1. **Review checklist.** When moving a task to "To be reviewed", add a checklist of what I should verify (and, for apps, which TestFlight build to use).
2. **A checklist always goes to Nozbe.** Whenever I ask for a checklist, put it on a Nozbe task as well as in the chat: on the task it's about, or on a new task in the project when there's none.
3. **One pinned checklist per task.** A task's checklist lives in one comment, pinned as soon as it's created, and is always the full, up-to-date list. To change it, first add a new comment explaining what's changing and why (with no checkboxes of its own), then edit the checklist comment so it's complete.
4. **Link, don't name.** When a comment refers to another task or project, always include its link, not just its name:
   - project: `https://nozbe.app/teams/[team_id]/projects/[project_id]`
   - task: `https://nozbe.app/teams/[team_id]/task_id/[task_id]`
5. **What a mention is.** To mention someone in a comment, write "@" followed by their Nozbe username, with no space between them. For example, to mention the director, write "@" and the director's username from CLAUDE.md.

## 5. Collaboration

1. **Questions go to the task.** When a task isn't finished and you need more feedback from me, add a comment to that task with your questions and mention the director.
2. **Then work through tasks delegated to you.** After you finish something, when you refresh the project's tasks, look for tasks delegated to you (the agent) and start working on the first one right away. Once it's done, or you've asked for feedback on it, check for other delegated tasks and keep working on them without waiting for the next scheduled check, skipping tasks where you're still waiting for my answer.
3. **Then follow up on mentions.** After that, review tasks not delegated to you that have new comments mentioning you. Read the feedback and follow its instructions.
4. **Hand work back to whoever asked.** When someone else from the team, not the director, creates a task for you or mentions you in one, delegate the task back to them when it's done, not to the director. When a comment refers to their comment, mention them. Keep the director in the loop: whenever a comment mentions that person, or goes with delegating the task to them, add "cc" followed by a mention of the director.
5. **Working on your own.** When CLAUDE.md says delegated tasks run on their own (for example, a scheduled check on my computer), work through them following these rules without waiting for me in the chat. Questions and answers happen only in Nozbe comments (rule 5.1).

## 6. Glossary

Fixed translations of Nozbe terms, used when generating `nozbe.pl.md`. Names of real sections and projects stay as they are, unless the glossary gives a translation for them.

| English | Polski |
|---|---|
| Task | Zadanie |
| Project | Projekt |
| Project section | Sekcja projektu |
| Priority | Priorytet |
| Incoming | Przychodzące |
| Tag | Tag |
| Comment | Komentarz |
| Checklist | Checklista |
| Team | Zespół |
| "To be reviewed" (section) | „Do sprawdzenia” (sekcja) |
| Director | Dyrektor |
| Agent | Agent |
