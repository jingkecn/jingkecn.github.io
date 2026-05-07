---
layout: post
title: "The Shape of Your Team Is the Shape of Your System"
date: 2026-05-08
categories: introspection
---

I once joined a roughly ten-person engineering team building a B2B platform for a global scientific testing company.
My first weeks were spent reading code and context.
The platform was already several separate projects.
I was assigned to two of them: different projects, different architectures, different ways of communicating internally.
Nobody explained the split.
I didn't ask yet.
What I noticed: each project had its own team, and both teams spanned the same four countries: France, Ireland, India, and Romania.
Coordinating within each team was expensive.
I was working in France. Ireland and Romania were one or two time zones away, that's manageable.
India was three and a half to four and a half hours ahead, a quick question became a ticket, a clarification became a thread that resolved tomorrow.
I was working in the constraint before I had a name for it.

- [The Constraint Has A Name](#the-constraint-has-a-name)
- [Eurofins: Accept the Law, and Work With It](#eurofins-accept-the-law-and-work-with-it)
- [MyScript: The Cost of Ignoring It](#myscript-the-cost-of-ignoring-it)
- [PERF: The Fourth Stance](#perf-the-fourth-stance)
- [The Pattern](#the-pattern)

## The Constraint Has A Name

There's a name for it.
Melvin Conway observed it in 1968:

> *"Any organization that designs a system will produce a design whose structure is a copy of the organization's communication structure."*

Fred Brooks later named it **Conway's Law** in *The Mythical Man-Month*.

Martin Fowler [synthesized](https://martinfowler.com/bliki/ConwaysLaw.html) the practitioner response into three stances:

| Stance                                | Description                                                              |
| ------------------------------------- | ------------------------------------------------------------------------ |
| **Ignore** it                         | Your architecture fights your org structure and tensions accumulate.     |
| **Accept** it                         | Align your design to how your teams actually communicate.                |
| Apply the **Inverse Conway Maneuver** | Deliberately reorganize your teams to produce the architecture you want. |

Those three stances are a useful map.
But after several different engagements with the law across a decade, I've found they're incomplete.
There is a fourth stance, and a pattern running through all four, that I haven't seen written about.

## Eurofins: Accept the Law, and Work With It

I know this because I lived it twice at [Eurofins](https://www.eurofins.com).

Partway through the engagement, the engineering department reorganized.
I moved from one team to another.
Different people, different code, different technology, but the same geography and timezone gaps, the same pattern of quick questions becoming tickets and clarifications becoming threads that resolved tomorrow.

The law didn't care that the org chart had changed.
The communication structure hadn't.

Accepting Conway's Law doesn't mean giving up.
It means starting from reality.

The response (ours, and the teams' before us) was to put the coordination work *into writing*.
Not emails.
Not tickets.
Artifacts that lived alongside the code: integration tests that proved the system boundaries worked end-to-end, specification documents that described what a feature was supposed to do in terms both engineers and the business team could read.

These weren't just good engineering practices.
They were *communication substitutes*.
A test that crosses a system boundary encodes a contract.
A specification document encodes a decision.
When your morning in France is someone's afternoon in Romania and someone else's evening in India, the written artifact is the meeting that didn't happen.

You stop relying on the conversation.
The conversation is in the artifact.

## MyScript: The Cost of Ignoring It

Earlier in my career, I spent eight years at [MyScript](https://www.myscript.com), a handwriting recognition company in Nantes.
About five engineers.
One office.
Everyone within shouting distance.

By Conway's Law, this should be fine. A small, co-located team has cheap and constant communication.
You don't need formal structures, you just talk.
The law operates through communication friction; remove the friction, and it has nothing to act on.

But cheap communication cuts both ways.

When it's easy to just ask, nothing forces you to define interfaces.
Nobody has to say "this is where your code ends and mine begins."
They just reach across.
Over time, everything reaches into everything else.
Features depend on each other's internals.
A change in one corner breaks something in a corner with no obvious relationship to it.

This is what we had, not because the team was careless, but because the organizational structure gave no signal that boundaries were needed.
Conway's Law didn't produce the coupling.
The absence of it did.

The fix was to introduce the structure the organization hadn't imposed: a redesign along domain boundaries, where each domain owned its data and its logic, and other domains could only interact through a defined interface.
It wasn't a reorganization, but it had the same effect: it changed what the team had to discuss, what a code change could touch, what "done" meant for a feature.

The org chart stayed the same.
The way the team communicated about the code changed.

## PERF: The Fourth Stance

My recent engagement was at [PERF](https://www.perf-solutions.com), an industrial software company in France.
Around ten engineers, one location, everyone in the same office.

Ten is a different number than five.
At five, informal communication covers the gaps, you notice the coupling only after it has become a problem, as we did at MyScript.
At ten, you can see it coming.
The team is large enough that "everyone talks to everyone" no longer works, but small enough that nobody has been forced yet to formalize how work is divided.
Left alone, the architecture will start to reflect whatever lines the social dynamics happen to produce: who sits near whom, who joined first, who owns what by habit.

Fowler's third stance, the Inverse Conway Maneuver, says: restructure the organization to get the architecture you want.
That's a leadership-level decision, not something a single engineer on a consulting engagement controls.
But between Accept and Inverse, there is something an engineer can do: establish the structures before the law acts, so that what the law eventually produces is what you intended.

At PERF, this looked like establishing a shared vocabulary before inconsistency could accumulate, and restoring a structural boundary that had gradually eroded.
Both were proactive.
Neither was urgent at the time.
That was the point.

This is the fourth stance.
Call it **Preempt**: impose the communication structure you want in the code and the team's working practices, before the organization's informal dynamics impose a different one.

## The Pattern

All four stances have something in common.

At MyScript, the coupling accumulated because nothing forced the team to encode its boundaries.
The fix was to encode them: in domain models, in interfaces, in written decisions.

At Eurofins, the timezone gaps made real-time communication expensive.
The fix was to encode the coordination that couldn't happen in real time: in tests, in specifications, in written contracts between system components.

At PERF, the risk was that informal dynamics would encode themselves into the architecture before anyone made a deliberate choice.
The fix was to encode the intended structure first: in a shared procedure, in refactored boundaries.

Even the Inverse Conway Maneuver follows the same logic.
Reorganizing the team is itself an act of encoding: you're writing the communication structure into the org chart, deliberately, so the system that emerges reflects what you intended.

**The pattern**: *when natural communication is unreliable or insufficient, encode the intended structure into something durable.*

Conway's Law works because software is a communication system.
Every operation is a message.
Every boundary between parts of the system is a decision about who talks to whom.
Every connection point is a written contract between parts of the system, and between the people who build and maintain them.

The shape of your team is the shape of your system because the code is the conversation.
And when you can't change who talks to whom, you can change what gets written down.
