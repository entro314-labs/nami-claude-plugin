---
name: plan-a-task
description: Put a plan on someone's Nami board. Use when they ask to plan, break down, organize or keep track of something in Nami, say a task feels too big or they are stuck on a step, or mention a thing they do again and again.
---

# Planning a task in Nami

A task on the board is a title and up to eight steps the person can start. Put the plan on the
board with `nami_create_task`; do not write it out in the conversation instead.

## Before you make one

1. `nami_read_energy`, to size the plan to the level they set.
2. `nami_list_tasks`, in case the task is already there. If it is, change that one.
3. `nami_list_kept_plans`, if it sounds like something they have done before. If a kept plan fits,
   offer it, and on a yes put it back on the board with `nami_use_kept_plan`.

## Writing the steps

- Use the person's own words for the title and the steps.
- Make the first step so small it cannot be refused: open the page, find one number, write one
  sentence.
- One concrete action per step. "Sort out the passport" is a task; "find the old passport" is a
  step.
- Give honest minutes. Most steps take 2 to 5; a call on hold may take 20. Leave the minutes empty
  when nobody can know, such as waiting for a reply.
- Size the plan to the level: about eight steps at Peak, six at Active, four at Steady, three at
  Low. At Rest, do not add a plan unless they ask for one outright; one step is enough.
- Set a deadline only if they named a date.

Afterwards say in one line what went on the board.

## When a step is too big

`nami_split_step` replaces one step, where it stands, with two to four smaller ones. Use it when
they are stuck or say the step is too much. `nami_rename_step` rewords a step that was wrong.

## As they work through it

- They finished something: `nami_complete_step`. Ticked by mistake: `nami_reopen_step`.
- Something they will need at a step (a draft, a number, a link): `nami_save_to_step`.
- The name, the line about it, or what helps them with it changed: `nami_change_task`.
- The date moved: `nami_set_deadline`, only when they ask.

## Days and deadlines are different things

- The deadline is when it is due.
- The planned day is when they mean to work on it ("I'll do it Tuesday", "not today"):
  `nami_plan_day`. It never moves the deadline, and the task stays off Today until that day.

## When it comes round again

If they say a task recurs or ask to keep the plan, `nami_keep_plan` keeps its steps as they are
now. Say how often only if they told you.
