---
id: 76aa6153-518c-40b5-bb51-bfa588d8001a
title: Task management
weight: 10
lastmod: 2026-08-12T02:59:34+02:00
last_editor: Erik Hagen

---

How should tasks be managed in a collaboration where several organisations take
part, and none of them is superior to the others?

This is a discussion of what appears to be good practice, drawing on experience
from SAMT-BU. A concrete proposal for this project can be found under
[Suggestion: wider use of GitHub for task management](https://docs.samt-bu.no/en/utkast/diverse/github-oppgavestyring/).

The examples are drawn from GitHub, which SAMT-BU uses. The principles are not
tied to that platform – see the section on tools at the end.

Draft, August 2026.

## Tasks should sit where the work sits

When a task and its result live in separate places, someone has to hold them
together by hand. That is work nobody has been assigned, and it stops the week
that person has other things to do.

When they live in the same place, a task can point to a specific change, and a
change can close the task it answered. The trail then persists on its own,
without anyone maintaining it.

This is not an argument for a particular tool. It is an argument for keeping the
distance short between "what we are going to do" and "what we did".

## Cross-cutting work needs a home that belongs to no one

In any collaboration between several parties there is always work that belongs
to no single part: shared vocabulary, shared architecture, shared ways of
working.

Without a place of its own, such work ends up in one of three places. It is
labelled with an arbitrarily chosen part of the project. It is placed with the
most central party, where the others cannot see it. Or it is not written down.

All three are losses, but the last is the worst, because it leaves no trace.

## Tool choices that follow the org chart entrench the org chart

The usual warning against running two systems at once is that such arrangements
decay: one quietly wins, and the other is left holding old items nobody has
closed.

But when the split follows an organisational boundary – one group here, another
there – it does not decay. On the contrary, it is quite stable, precisely
because the two groups rarely need each other's task list day to day.

And that is where the problem lies. A stable split along an organisational
boundary recreates the very silo the collaboration was meant to break down. The
risk is not that the arrangement stops working, but that it works – and that it
renders the work on the other side invisible without anyone noticing.

This does not mean everyone must use the same tool for everything. Distributing
work internally within one organisation is a different matter from shared work.
But the shared work should sit somewhere all participants actually look.

## Two kinds of "shared" that are easily confused

When several parties are doing something similar, it is worth distinguishing two
cases:

**The same task for several parties.** One piece of work, several who benefit
from the result. A shared vocabulary is created once. Here shared ownership is
right, and the task should be labelled as cross-cutting.

**The same type of task at each party.** Parallel tasks with their own content.
A risk and privacy assessment must be carried out for each individual solution:
different data, different legal bases, different risks. They cannot be merged.

Confusing the two leads either to duplicating work that should have been done
once, or to merging assessments that had to be done separately.

For the second case, the reuse value lies in the **template**, not in the task.
A good checklist is worth more than a shared item.

## The price: notifications cannot be separated finely enough

Gathering everything in one place gives cross-cutting visibility – but removes
the ability to follow only your own part. Today's tools separate by work area,
not by label. You follow everything, or nothing.

That cuts across a distinction that matters a great deal in practice: the
difference between **responsibility** – who must act – and **interest** – who
wants to know. Responsibility is assigned and cannot be opted out of. Interest
is self-chosen and should be easy to unsubscribe from.

If the two are mixed, those responsible drown in noise, or those merely
interested receive alerts they cannot switch off. People then switch everything
off, and miss what they should have seen.

This is a real cost of shared working surfaces, and it is worth knowing about in
advance. It does not disappear by choosing a different tool.

## Tools

### What is required

For co-creation to work in a large ecosystem, across organisations and
countries, the tool must have some properties that cannot be taken for granted:

- **Open to read without an account or licence.** Anyone considering taking
  part must be able to see the work first.
- **A low threshold for contributing across organisational boundaries.** It
  must be possible to propose a change without first being enrolled somewhere
  else.
- **Durable history and provenance.** Who proposed what, when, and what became
  of it. Without this, the traceability that makes a contribution verifiable
  disappears.
- **No single participant owns the surface.** If the work sits inside one
  party's licensed environment, the others are guests there.
- **Portable.** The content must be movable to another platform without being
  rewritten.

### Git platforms

Git-based platforms are currently the only family that has all five at once, in
practical use and at scale. That is also why international standards work has
moved there: the W3C now develops specifications in open work areas on GitHub,
where anyone can comment.

SAMT-BU uses GitHub, but equivalent solutions can be built elsewhere:

- **GitLab** – the same model, and can be self-hosted. The European Commission
  runs [code.europa.eu](https://code.europa.eu/) on GitLab, managed by its Open
  Source Programme Office and open to EU institutions, developers and partner
  organisations.
- **Forgejo and Gitea** – lighter alternatives intended for self-hosting.
  Codeberg is a European non-profit service built on Forgejo.

For the public sector, the choice between hosted and self-hosted may matter for
digital sovereignty. The way of working is the same either way.

### Why not the usual project tools

Jira, Confluence, Planner and Notion are often better at distributing tasks
taken on their own. But they are built for a single organisation: read access
requires a licence, participation requires being added, and the content is hard
to take with you.

They therefore break the first three requirements above – and that is not a
setting that can be changed. They are well suited to distributing work
internally, and poorly suited as a shared surface in an ecosystem.

### The threshold is solved by a layer on top, not by switching

The objection to Git platforms is real: they were built for developers, and to
many people they are alien.

But the objection targets the interface, not the model. Editing tools exist
that sit on top and hide the machinery – this website is itself an example.
Anyone correcting a page here writes in an ordinary text editor in the browser,
and needs neither to know Git nor to have seen GitHub. At the same time, those
who prefer to can work directly against the repository as before.

That is probably the right path: keep an open and verifiable core, and lower
the threshold with layers on top – rather than choosing a closed tool because
it is easier to get started with.

## What we do not yet know

- Whether a combined board pulling items from several work areas – called a
  Project in GitHub – gives enough overview in practice, or merely becomes
  another surface nobody opens.
- How much of the value lies in the tool, and how much lies in someone actually
  keeping the overview up to date.
- Whether the threshold for taking part is lowered or raised when work moves to
  open surfaces. Openness gives visibility, but open tools are not necessarily
  easy for everyone to adopt.
