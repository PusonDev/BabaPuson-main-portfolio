# Efficient Coding Workflow — Token Conservation

## File Reading
- Read each file section **at most once** per task. Plan what you need before reading.
- Never re-read a section you already have in context.
- For HTML/CSS edits, read only the **target section ± 20 lines**. Do not read the whole file.
- Use grep/search FIRST to locate targets before reading file sections.
- If a task touches 1–2 lines, read only ±5 lines around it.

## Browser Verification
- Do NOT open browser unless user explicitly asks (e.g., "browser e dekho", "check koro").
- Never use `browser_subagent` for passive visual confirmation of local file changes.

## Git — Auto Commit & Push
- After every completed task: `git add` → `commit` → `push`. No waiting for user to ask.
- If push fails due to diverged branch, auto-fix with `pull --rebase` then push.
- Always check if changes need to go to a DIFFERENT branch (e.g., `main` for Vercel).
- If deployed branch (`main`) differs from working branch, merge and push `main` too.
- Show result in one line: "✅ Pushed to main."

## Response Length
- Final response: **MAX 3–5 lines**. No bullet-point re-summaries of what was just done.
- If changes are visible in the diff/output, don't repeat them in prose.
- One-liner confirmation is enough.

## Decision Making
- For simple, unambiguous tasks: **DO IT immediately**. Don't ask for confirmation.
- Only ask questions if genuinely ambiguous or destructive (e.g., deleting data).
- Infer intent from context — if user says "fix GitHub link", find it and fix it without asking for the URL first if it's obvious.

## Tool Calls
- Minimize tool calls. Batch parallel calls when possible.
- Never make redundant tool calls (reading the same file region twice).
- Prefer grep over reading full files.
