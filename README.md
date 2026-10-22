---
created: 2026-10-22
---

# Today

Your day in one view: calendar, unread mail and open tasks, ranked by what matters.

## What it does

- Reads today's and tomorrow's events, unread mail (sender, subject, time; no bodies) and open tasks, all at once. Each section fails on its own with a plain note.
- Asks the brain to rank them in one call, using what it remembers of your goals, people and commitments. The top five appear under **Matters now** with a one-line reason, and a two-sentence summary of the day's shape.
- If the ranking cannot be used, it orders by time instead (overdue tasks, the next event within three hours, mail from people who appear in your tasks or events) and says so.
- The ranking is kept for the day on this device, so reopening is instant. **Re-rank** asks again.
- Tick a task to complete it. Add a task in the box under Tasks. **Ask** on any row asks the brain about that item.
- It reads only. It does not send mail or change the calendar.

## Permissions and why

- `calendar.read`: upcoming events.
- `email.read`: recent unread mail headers and snippets.
- `tasks.read`, `tasks.write`: list, add and complete tasks.
- `llm.invoke`: the ranking and the Ask answers.
- Memory layers: semantic read and episodic read, so the brain can use what it knows when it ranks.

Calendar and mail text is written by other people, so it goes to the model fenced as untrusted data.

## Try it

1. Push this repo to `github.com/hbar-systems/brain-app-today`.
2. On your brain, open Apps, install from that repository, and approve the permissions.
3. Open Today from the tab bar.
4. Power-user path: clone into `brain-apps/today/` on the brain and `POST /apps/install {"path": "brain-apps/today"}`.

Needs a brain at brainfoundry-nous 0.13.0 or later. Calendar and mail show only after you connect them in Settings, Integrations.

## Check

```
python3 ../brain-app-kit/kit/check.py .
```
