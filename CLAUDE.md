# TryAloha Site Agent Instructions

## Scope
Work only in this repository:
`~/code/tryaloha-site`

This is the static landing site deployed to Netlify from GitHub.

## Safety rules
- Do not edit files outside this repo.
- Do not touch DNS, Namecheap, Netlify settings, Twilio, Stripe, Vapi, or Google Workspace unless Taylor explicitly asks for that exact task.
- Do not add secrets, API keys, tokens, phone credentials, or `.env` values to this repo.
- Before making changes, run `pwd`, `git status --short`, and confirm the repo root.
- After making changes, show `git diff` and wait for Taylor to approve before committing.
- Do not push to GitHub unless Taylor explicitly says to push.

## Current site type
Static HTML site.
Main files:
- `index.html`
- `privacy.html`
- `terms.html`
- `CNAME`

No build command is currently required.
Netlify publish directory is repo root: `.`

## Twilio / SMS rules
- Do not send real SMS messages unless Taylor explicitly asks for a live send in that turn.
- Do not expose, print, commit, paste, or summarize Twilio credentials.
- Prefer Twilio API Keys over the primary Account SID/Auth Token.
- Use environment variables only; never hard-code Twilio credentials.
- Any SMS test must use a clearly labeled test recipient and must show the exact message before sending.

## Autonomy model
Agents may work autonomously on reversible local work:
- inspect files
- edit files inside this repo
- run local checks
- run link audits
- create drafts
- create local scripts
- prepare implementation plans
- summarize findings
- show diffs

Agents must pause for Taylor approval before external or irreversible actions:
- pushing to GitHub
- changing Netlify settings
- changing DNS/Namecheap
- sending real SMS/MMS
- making real phone calls
- changing Twilio/Vapi/Stripe/OpenAI billing settings
- exposing, printing, or committing secrets
- deleting files unless explicitly requested

For Twilio/SMS work:
- It is okay to write code, inspect configuration names, and prepare test messages.
- It is okay to do dry-run tests that do not contact real users.
- Before any live send or call, show the exact recipient, exact message/audio behavior, expected cost/risk, and wait for approval.
