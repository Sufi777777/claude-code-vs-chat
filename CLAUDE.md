# Claude Code vs Claude Chat — Project Notes

## Project
Static single-page site comparing Claude Code and Claude Chat.
Live: https://claude-code-vs-chat-liart.vercel.app/
GitHub: https://github.com/Sufi777777/claude-code-vs-chat

## Stack
Pure HTML + CSS (no build step, no JS). Single `index.html`. Deploy via Vercel GitHub integration.

## Environment Notes (Windows)
- `node`, `npm`, `vercel`, `gh` are NOT in the bash shell PATH — use PowerShell with refreshed PATH:
  `powershell.exe -ExecutionPolicy Bypass -Command '$env:PATH = [System.Environment]::GetEnvironmentVariable("PATH","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("PATH","User"); <command>'`
- Node.js install: `winget install OpenJS.NodeJS.LTS`
- `gh` CLI install: `winget` — auth uses stored git credentials automatically
- Git CRLF warnings on Windows are expected, not errors

## Vercel Deployment
- Vercel CLI needs interactive browser login — cannot be automated in Claude shell
- To create a new project: import from GitHub at vercel.com/new
- After linking: every `git push origin main` auto-deploys via GitHub integration
- Vercel MCP `deploy_to_vercel` tool only returns instructions, not an actual deployment
