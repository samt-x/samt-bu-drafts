---
id: 76aa6153-518c-40b5-bb51-bfa588d8001a
title: Task management
weight: 10
lastmod: 2026-08-12T03:55:58+02:00
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

### Git-based platforms

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

### Traditional project tools

By traditional project tools we mean Jira, Confluence, Planner, Notion and the
like. They manage *tasks about* the work – who does what, by when, and how far
along it is. The work itself, meaning the document or the model or the code,
sits somewhere else.

That is no weakness in itself. Taken on their own, they are often better at
distributing tasks than a Git platform is. But they are built for a single
organisation, and that brings three limitations:

1. Read access requires a licence.
2. Participation requires an administrator to add you.
3. The content is hard to take with you.

**OpenProject is an exception to the last two.** It is a web-based project
management tool under GPL-3.0, developed in Germany and explicitly aimed at
public administration. It can be self-hosted or run in an EU-based cloud, it
meets WCAG 2.1, and it is used by the European Commission among others. If the
licence is free and you run it yourself, both the licence requirement and the
lock-in disappear.

**But the limitation that matters most remains.** None of these tools has forks
or pull requests – OpenProject included. To contribute, an administrator must
create an account for you on that installation. An outsider cannot propose a
change.

The wording here is easy to be misled by. OpenProject has an *integration* with
GitHub and GitLab, and it is a useful one: a pull request can be linked to a
task, and the task can close by itself when the change is accepted. But the
pull request is created and lives in GitHub or GitLab. OpenProject displays it.
The tool's own documentation is explicit that repositories are not hosted
there – you can read and download files, but need a Git client to change
anything.

The dividing line is therefore not between open and closed source. It runs
between tools that assume participants have already been enrolled, and tools
where a stranger can propose a specific change without first becoming a member
of anything.

Traditional project tools are consequently well suited to distributing work
internally – and OpenProject is a genuine option for those who want that on
open, European terms. As a shared surface in an ecosystem they all fall short,
and that is not a setting that can be changed.

### The two families in combination

The families do not exclude one another, and this is probably where the
practical solution lies.

A project tool and a Git platform can be combined so that each does what it is
good at: planning, progress and portfolio overview in the project tool – open
participation, proposals and history on the Git platform. The link between them
means a task shows the status of the actual change, and closes when the change
is accepted.

The outsider then needs no account in the project tool. They contribute on the
open surface, and the contribution still becomes visible in the planning. The
requirements neither family meets on its own are met by the pair.

What matters is not whether the work is split across two tools, but whether the
two are connected. A split without a connection is precisely what renders the
work on the other side invisible, as described in the section on the org chart.
The connection does not remove the split, but makes the boundary permeable.

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

## Challenges – and where the solutions lie

None of these is a reason to refrain. They are things worth knowing about in
advance, and for each of them there is a known direction.

### One board quickly becomes another surface nobody opens

**The challenge.** Gathering everything in one place can produce a list so long
that it offers no overview, only a bad conscience.

**The direction.** Separate two levels, as Altinn does – with GitHub as the
tool at both:

- **Portfolio level.** Few items, coarse resolution. Answers "how are the four
  pilots doing".
- **Project level.** Many items, fine resolution. Answers "what do I do next".

The mistake is to mix them on one board. It then becomes too detailed for
someone seeking an overview, and too coarse for someone doing the work. Two
boards at different resolutions cover both needs, without the item having to
exist in two places.

### Notifications cannot be tailored

**The challenge.** As described above: you follow a work area, not a label.

**The direction.** Stop solving it with notifications. Notifications are *push*
– they come to you, and can only be switched on or off. Overview is *pull* –
you seek it out when you need it.

A personal cross-cutting view – "what is assigned to me", "what has changed in
what I follow" – covers most of the need without a single email. Such queries
across work areas already exist in the tools.

It is also reasonable to expect assistants to be a real help here: receiving
"this has happened since last time that concerns you" as a summary, rather than
twenty notifications to sort through yourself. Fine-grained notification
control would then no longer determine whether you keep up.

### Someone has to keep the overview up to date

**The challenge.** A board that is wrong is worse than no board, because people
trust it for a while before they stop.

**The direction.** Derive status from the work rather than maintaining it. If
an item closes by itself when the change it concerns is accepted, the board is
up to date without anyone having done anything. That is also why the link
between task and change is worth prioritising.

### The threshold for those who do not code

**The challenge.** Git platforms are alien to many.

**The direction.** Add a layer rather than switching – see the section on
tools. This applies to the task side as much as to the content: a board can be
used through a simpler interface without the core changing.

---

All of this remains to be tried out in practice in SAMT-BU. The directions
above are drawn from others who have done it, not yet from our own experience.
