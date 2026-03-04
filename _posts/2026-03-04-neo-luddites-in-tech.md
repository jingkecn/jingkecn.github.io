---
layout: post
title: "From Craftsman to Architect: Rethinking Software Engineering in the AI Era"
date: 2026-03-04
categories: introspection
---

- [A Crack in the Foundation](#a-crack-in-the-foundation)
- [What Tane Is Actually Saying](#what-tane-is-actually-saying)
- [The Map Is Gone. Now What?](#the-map-is-gone-now-what)
- [From Craftsman to Architect](#from-craftsman-to-architect)
- [The Skills That Survive](#the-skills-that-survive)
- [The Luddite Mirror](#the-luddite-mirror)
- [Where I Land](#where-i-land)

A Crack in the Foundation
-------------------------

Today I read [Boris Tane's post](https://boristane.com/blog/the-software-development-lifecycle-is-dead/), half-expecting another breathless "AI will replace engineers" take.
What I found was different.
He wasn't predicting the end of engineers, he was describing the end of the ***workflow*** I had quietly built my identity around.

He was right.
And that's what scared me.

I've spent years getting good at the whole craft, breaking down requirements, thinking through architecture, reviewing pull requests with care.
I was proud of that.
It felt like engineering.

Tane's argument is that most of that craft is now a relic.
That AI agents haven't just accelerated the SDLC, they've collapsed it.
Requirements, design, implementation, testing, review: all merging into a single tight loop driven by intent and iteration, not process and ceremony.

I didn't want to dismiss him.
But I also didn't want to just nod along.
Because if he's right, and I think he largely is, the question hea leaves unanswered is the one that keeps me up at night: ***what does it mean to be a software engineer in the age of AI?***

That's what this post is about.
Not a eulogy for the SDLC.
A genuine attempt to figure out what comes next.

What Tane Is Actually Saying
----------------------------

It's tempting to read Tane's post as provocation.
The SDLC is dead.
PRs are a relic.
Jira is a terrible context store.
These are fighting words in most engineering teams.

But strip a way the sharpness, and the argument is surprisingly rigorous.
His point isn't that process is bad.
It's that process was always a response to contraints, and those constraints have changed.

**The SDLC was sequential because building was expensive.**
When a feature took weeks, we had to specify everything upfront.
We froze requirements because reopening them mid-sprint cost real money.
We had separate QA phase because catching bugs late was painful.
We had release trains because deploying was risky and slow.
***The ceremony wasn't arbitrary, it was load-bearing.***

**What AI agents change is the underlying cost structure.**
When a working draft of a feature takes minutes, not weeks, the logic that justified the ceremony collapses with it.
We don't need to specify everything upfront when we can generate 10 versions and pick the best one.
We don't need separate QA phase when tests are generated alongside code.
We don't need a release train when deployment is continuous and automated.

***Then SDLC didn't die because it was wrong.***
***It died because the problem it was solving got solved in a different way.***

Thant's what makes Tane's argument hard to dismiss.
And it's what makes the follow-up question so urgent.

The Map Is Gone. Now What?
--------------------------

Tane is convincing on the diagnosis.
The SDLC is collapsing, stage by stage, and most of use are still operating as if it isn't.
But his post ends where the hard question begins.

He tells us the map is wrong.
He sketches the outline of a new one: context engineering, observability as the connective tissue, but leaves is at that.
The diagnosis is sharp.
The prescription is thin.

And that absence is uncomfortable in a specific way.
Because if we're honest, most of us have been using the SDLC as more than a workflow.
We've been using it as a definition of what is means to be a software engineer.

That definition is dissolving.
And the industry, for all its excitement about AI agents, hasn't seriously reckoned with what replaces it.

So that's the question I want to sit with here.
Not whether the SDLC is dying, I think it is.
But what we're supposed to become on the other side of that.

From Craftsman to Architect
---------------------------

For most of our careers, being a good engineer meant being good at execution.
Writing clean code.
Knowing our patterns.
Debugging with precision.
Shipping without breaking things.
The craft was in the doing, and we got better at it by doing more of it.

That's not worthless.
But it's no longer the ceiling.

When an agent can generate a complete feature in minute, with tests, error handling, edge cases, the value of execution compresses.
Not to zero, but dramatically.
What doesn't compress is judgement.
Knowing whether the feature should be built at all.
Recognizing when the agent's architecture is clever but wrong for the context.
Feeling when something technically works but misses the point entirely.

**This is the shift: from craftsman to architect.**
From being the person who builds to being the person who designs, evaluates, and takes responsibility for the outcome.

It sounds like a promotion.
In some ways it is.
But it's also genuinely harder.
Execution is legible, we either shipped it or we didn't.
Judgement is murky.
It requires taste, context, experience, and the confidence to say "this isn't right" without always being able to fully articulate why.

And here's what make it uncomfortable: judgement can't be faked.
We could fake parts of the old craft, copy Stack Overflow answer, follow a tutorial, lean on a framework.
Judgement requires that we actually understand the system, the users, the trade-offs.
***The agent raises the floor for everyone.***
***It also raises the bar for what it means to be genuinely valuable.***

The engineers who thrive won't be the ones who use agents to do less thinking.
They'll be the ones who use agents to think about harder things.

The Skills That Survive
-----------------------

So if execution compresses, what expands?
I've been thinking about this a lot, and here's where I land.

**Context engineering.**
Tane names it and points at what matters - the quality of context we give an agent is directly proportional to the quality of what it builds.
What that means practically?
It's not about writing clever prompts.
It's about understanding a problem deeply enough to frame it well, scoping it, constraining it, anticipating where an agent will go wrong.
***We can't give good context about something we don't understand.***
This skill rewards depth, not shortcuts.

**System thinking.**
When agents handle implementation, our leverage moves up the abstraction ladder.
Understanding how distributed systems fail, where bottlenecks emerge, what architectural trade-offs actually cost, this becomes more valuable, not less.
The engineer who understand ***why*** a design is good is the one who catches when an agent over-engineers or misses a constraint.

**Product taste.**
Agents optimise for what we specify.
They have no sense of what the user actually needs, no instinct for elegant simplicity.
The engineer who can say "this technically works but it's wrong" is irreplaceable.
The requires genuine product sense: understanding users, business context, and what "good" looks like beyond the spec.

**Knowing when not to trust the agent.**
This might be the most underrated skill of all.
Agents are confidently wrong in non-obvious ways.
Reading generated code critically, not line by line but architecturally, and spotting when something ***looks*** right but isn't, requires maintaining genuine technical depth.
The agent raises the floor.
It doesn't replace the judgement that comes from real understanding.

None of these are new skills exactly.
But they were previously optional layers on top of execution.
Now they're the job.

The Luddite Mirror
------------------

There's a word Tane uses almost in passing that stuck with me.
Describing engineers who cling to PR reviews in an agent-driven world, he calls it ***luddism***.

It's a provocative word.
But I think it's th right one, if we understand what the Luddites were actually about.

The Luddites weren't anti-technology.
They were skilled craftsmen who had built their identity around a specific form of work, and who fought to protect that form when the underlying economics shifted beneath them.

They weren't irrational.
They were human.
And they lost, not because machines were evil, but because they tried to protect the specific shape of their work rather than the underlying value they brought.

That's the mirror I find uncomfortable to look into.
Because I recognize the impulse.

I've caught myself defending the PR review not because I genuinely believe it's the best way to ensure quality in an agent-driven world, but because reviewing code is something I'm good at.
It's legible.
It feels like engineering.
Letting fo of it means stepping into something less defined, less certain, less easy to measure.

***That's not rigor.***
***That's identity preservation dressed up as professional standards.***

The real question isn't whether we use AI tools.
Most of us do.
The question is whether we're willing to let go of the ceremonies that no longer serve the outcomes they were designed to produce, even when those ceremonies are deeply tied to how we see ourselves as engineers.

That's harder than adopting a new tool.
It requires honesty about what we're actually protecting.

Where I Land
------------

I don't have a tidy conclusion.
That would be dishonest.

What I have is a direction.
And a few things I'm actively trying to do differently.

We're investing more in understanding the ***why*** before touching an agent.
Not writing a PRD, not estimating story points, just sitting with a problem long enough to understand it's shape, its constraints, its failure modes.
That's what good context engineering actually requires.
And it turns out that slowing down at the start makes everything that follows faster and better.

We're talking observability more seriously, not as a monitoring layer bolted on at the end, but as a design concern from the beginning.
If the feedback loop between production and the agent is the connective tissue of the new lifecycle, then designing that loop well is ont of the highest leverage things we can do.

And we're trying to stay honest about the difference between defending quality and defending comfort.
Every time we feel the urge to insist on a process, it's worth asking: is this serving the outcome, or is this serving our sense of what engineering is supposed to look like?

The Luddites lost not because they were wrong to care about their craft.
***They lost because they confused the form of their work with its value.***
We're at a similar inflection point.
The engineers who navigate it well won't be the ones who resist the shift or the ones who abandon all judgement to the agent.
They'll be the ones who carry their values (quality, responsibility, depth) into a new shape of work.

That shape is still being defined.
I find that unsettling.
I also find it, quietly, exciting.
