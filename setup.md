# Setting Up a Repository for Working with Nozbe

> **Source of truth.** This English file is the master version.
> `setup.pl.md` is translated from it — make every change here first, then regenerate the Polish file.

Use this prompt in a repository once Nozbe is connected over MCP. It checks Nozbe, asks me for what's missing and writes the result to the repository's CLAUDE.md, so that `nozbe.md` knows which team, people and project to use.

## Steps

1. **Check the connection.** Confirm that you can reach Nozbe and see which account is signed in. If you can't, stop and tell me to connect Nozbe over MCP first.
2. **Agent.** The MCP connection must use the agent's account, not the director's. Show me the signed-in account and ask whether it's the agent. If it isn't, tell me to log out of the Nozbe desktop app, log in as the agent and refresh the MCP connection, then check again. Once I confirm the agent is signed in, take the agent's username and user ID from that account.
3. **Team.** List the teams (workspaces) the agent belongs to and ask which one this repository works in. If there's only one, ask me to confirm it.
4. **Director.** List the other members of that team and ask which one is me, the director.

   For both people, note their Nozbe username (the one written after "@" in a mention) and user ID in that team. If a username isn't shown, ask me for it.
5. **Project.** Find the repository's name (the name of its folder). Look in the team for a project with the same name.
   - If there is one, ask me to confirm it's the project for this repository.
   - If there isn't, propose creating it. Once I agree, create a project with the repository's name in the team, visible to the entire team.
6. **Write CLAUDE.md.** Show me what you'll add, then add it to the repository's CLAUDE.md once I agree (create the file if it doesn't exist):

   ```markdown
   ## Nozbe

   - Team: [team name] (ID: [team_id])
   - Director: @[username] (ID: [user_id])
   - Agent: @[username] (ID: [user_id])
   - Project: [project name] (https://nozbe.app/teams/[team_id]/projects/[project_id])
   ```
7. **Rules.** Once the Nozbe setup is done, ask me how to add the rules, `nozbe.md` from https://github.com/Nozbe/AgentRules:
   - **Copy them.** Fetch `nozbe.md` from the repository and paste its contents into CLAUDE.md.
   - **Reference them.** Add `@nozbe.md` to CLAUDE.md. I'll copy `nozbe.md` into the repository myself.
8. **Scheduled check.** Ask me whether tasks delegated to the agent should run on their own (nozbe.md rule 5.5). If I say yes:
   - Create a scheduled task in Claude on this computer named "[project name]: work on tasks delegated to the agent", running every 15 minutes, with the prompt below. Fill in the repository's full path.
   - Add this line to the Nozbe section of CLAUDE.md:

     ```markdown
     - **Scheduled check:** every 15 minutes on the director's computer (nozbe.md rule 5.5).
     ```
   - Tell me that the check only runs while this computer is on and Claude is open.

   The scheduled task's prompt:

   ```markdown
   You are the agent for this repository: [repository path]. Nobody is watching this session: never stop to ask questions in chat. Questions go to Nozbe comments.

   1. **One run at a time.** If `running.lock` in this task's folder exists and is less than 3 hours old, end the run. Otherwise write the current time into it, and delete it at the end of the run, also when you stop early or something fails.
   2. **Load the rules.** Work only in the repository. Read its CLAUDE.md and `nozbe.md` in full and follow them. If it's a git repository, run `git pull` first. If Nozbe can't be reached, end the run.
   3. **Find work.** Fetch the project's open tasks delegated to the agent, with their comments. Skip tasks where you're still waiting for an answer. If there are none, follow up on new mentions of the agent (nozbe.md rule 5.3). If there's nothing at all, end the run quietly, with no comments and no changes.
   4. **Work on a task.** Follow nozbe.md, rules 3.1 to 3.2 and section 4: post the plan and start, ask questions in comments, do the work and commit it, then move the task to "To be reviewed" with a review checklist, and hand it back.
   5. **Keep going.** After each task, fetch the tasks again and start on the next one right away (nozbe.md rule 5.2).
   6. **Finish.** End with a short summary: the tasks you worked on, the commits, and the tasks waiting for answers.
   ```
9. **Confirm.** Tell me what you've set up.
