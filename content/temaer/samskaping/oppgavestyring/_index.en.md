---
id: 76aa6153-518c-40b5-bb51-bfa588d8001a
title: Task management
weight: 10
lastmod: 2026-08-12T01:56:58+02:00
last_editor: Erik Hagen

---

Draft, August 2026. Written as a basis for discussion, not as a recommendation.

## The situation today

The project manages tasks in two places at once:

- **The core team uses MS Planner**, which is readily available in the
  Microsoft environment participants use day to day.
- **The pilots use GitHub issues** in a shared repository, `Oppgaver`, where
  each item is labelled with the pilot it belongs to.

`Oppgaver` was created for pilot 1 in February 2026 and has since grown into
the role of a shared backlog. In August 2026 it holds 62 items – 6 labelled
pilot 1, 14 pilot 2 and 24 pilot 3. Pilot 4 has been given a label, but has not
started using it.

## The question

Would GitHub Projects have been a better choice than Planner – and if so, what
is it that actually makes them better?

The argument is not that GitHub is a better task tool. Planner is probably
easier for someone who does not code. The argument is that the tasks would then
sit *in the same place as the work*: the documentation, the suggestions and the
decisions. An item could point to a specific change, and a change could close
an item.

The counter-argument is just as real: the tool has to suit the people who will
use it. A task system nobody opens is worthless, however well connected it is
to everything else. This is not a question of which tool is best, but of where
the threshold should sit – and for whom.

## The split is stable, and that is precisely the problem

Parallel task systems are usually described as a temporary state – "for now we
use both" – and are then never decided, merely left in place. The usual
objection is that such arrangements decay: one system quietly wins, and the
other is left holding old items nobody has closed, yet looking alive enough
that people half trust them.

This split is of a different kind. It does not follow two competing tools, but
an organisational boundary: the core team on one side, the pilots on the other.
Splits like that do not decay. On the contrary, they are quite stable, precisely
because the two groups rarely need each other's task list day to day.

That is where the problem lies. A stable split along an organisational boundary
recreates the very silo the project exists to break down. The risk is not that
the arrangement stops working, but that it works – and that it renders the work
on the other side invisible without anyone noticing. The pattern is worth
recognising beyond this project too: **tool choices that follow the org chart
entrench the org chart.**

## Shared backlog, or one per pilot?

The pilots have their own repositories for content, but share a backlog. That
may look inconsistent, and at the same time it provides something valuable: you
discover that several pilots are working on the same thing.

There is a distinction here that is easy to get wrong:

- **The same task for several pilots** – one piece of work, several
  beneficiaries. Shared vocabulary, overall architecture, methodology and ways
  of working.
- **The same type of task in each pilot** – parallel instances with their own
  content. Risk and privacy assessments must be done per pilot: different data,
  different legal bases, different risks. They cannot be merged.

The first type argues for a `Cross-cutting` label. The second argues for shared
**templates**, not shared items – the reuse value lies in the checklist, not in
the task.

The price of a shared backlog is that notifications cannot be separated per
pilot. GitHub has no subscription by label; you follow everything or nothing.
This is the same distinction between *responsibility* and *interest* that
applies elsewhere in the project, and here it cannot be solved with the current
tools.

## Why this is a deliverable, not just housekeeping

An ecosystem consists of actors that are not subordinate to one another. No one
can impose a tool on the others, nor a way of working. The question of how
shared work is coordinated without shared line management is therefore a
general problem, not an internal detail – and the experience gained here is
something others can use.

## Open questions

- Should tasks sit in the pilots' own repositories, with an organisation-level
  project board pulling items from several repositories? That would give both a
  local link between item and change, and a cross-cutting overview.
- What does it take for a change of tool not to simply move the work to a place
  where fewer people see it?
- How should tasks that concern several pilots be labelled – and who owns them?
