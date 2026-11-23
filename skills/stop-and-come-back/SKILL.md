---
name: stop-and-come-back
description: Help someone stop a task in Nami without losing it, wait on someone else, take a rest, or pick up where they left off. Use when they say they have to stop, are out of energy, are waiting for a reply, want a break, or come back and ask where they were.
---

# Stopping, waiting, resting and coming back

Stopping part-way is normal. What matters is that the place is kept, so coming back costs nothing.

## They have to stop

`nami_mark_place` keeps their place in a task: the step they were on and, if they said it, what is
still open there. Nami's board, Today and the working session say it back when they return.

- Record only what they told you. Never guess where they got to.
- If they did not say which step, ask, or leave it unmarked.
- Do not add steps, reschedule or tidy the task on the way out. Mark the place and stop.

If they say when they will come back to it, `nami_plan_day` sets that day.

## Their part is done and they are waiting

`nami_set_waiting` marks a task as waiting on someone or something: a reply, a confirmation, an
appointment slot. Give the day to check only if they chose one; Today brings the task back on that
day. When the wait is over, clear it with the same tool.

## They need a rest

1. `nami_list_recovery_activities` shows the rests they can start and whether one is already open.
   Only one rest is open at a time.
2. Offer one or two that fit how long they have. Do not push a rest they did not ask for.
3. `nami_start_recovery` when they say they are taking it.
4. `nami_finish_recovery` when they are back, with how they say it went: better, the same, worse,
   or stopped early. Ask once, plainly; accept any answer.

If they describe something of their own that helps them recover and want it kept,
`nami_add_recovery_activity` adds it beside the built-in ones. They can change or remove their own
rests; the built-in ones stay.

## They are back

1. `nami_read_energy`, since the level may have changed. If they tell you a new one, record it
   with `nami_check_in`.
2. `nami_read_today` for the one thing Today suggests now and any waits that are due.
3. If they ask where they were, `nami_list_tasks` shows the place they marked and what was still
   open there.

Start from the step they left, not from the top of the task. If the step looks too big now, offer
to split it.
