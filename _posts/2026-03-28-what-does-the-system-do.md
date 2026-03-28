---
layout: post
title: "The ATM Screen vs. the Backend"
date: 2026-03-28
categories: introspection
---

- [What Does the System Do?](#what-does-the-system-do)
- [The ATM Screen and the Backend](#the-atm-screen-and-the-backend)
- [Why We Default to the Backend](#why-we-default-to-the-backend)
- [Finding the ATM Screen Together](#finding-the-atm-screen-together)
- [The ATM Screen First, Always](#the-atm-screen-first-always)

## What Does the System Do?

There's a situation I keep encountering.

Back to a time when I just joined a feature team, brought in to help move things forward after they hit a wall.
We sat down to discuss the system.
I asked: "What does the system do?"
I got the answer with how it was implemented, the classes, the services, the data flow through the code.
I asked again, same answer, different details.
Again, still implementation.

We were both frustrated.
They had deep knowledge of the system and couldn't understand why I wasn't getting it.
I needed to understand the behavior before I could reason about the code, and I couldn't make them see why that distinction mattered.
The discussion went in circles.
Nothing moved.

As a new member of the team, I felt like I had walked up to an ATM and asked "What can I do here?" and someone had opened the backend instead.

## The ATM Screen and the Backend

When we walk up to an ATM, we see a screen.
It tells us what we can do: check our balance, withdraw cash, transfer funds.
We don't see the authentication services, the ledger updates, the fraud detection algorithms running behind it.
We don't need to.
The screen is the contract between us and the system: what goes in, what comes out.

The contract has a name in software: the interface.
And behind every interface is an implementation: the backend, the wiring, the mechanics that make the contract work.

Both layers are real.
Both matter.
But they answer different questions:

- The ATM screen answers: *what does the system do?*
- The backend answers: *how does the system work?*

In that meeting room, my teammates were fluent in the backend.
They knew every service, every API call, every edge case in the data flow.
But when I asked "what does the system do?", I was asking for the ATM screen, and they kept showing me the backend.

Neither of us was wrong.
We were just answering at different layers.
And until we found a shared layer to stand on, the conversation couldn't move.

## Why We Default to the Backend

It's not a flaw.
It's a reflex.

Engineers spend most of their time in the backend: reading code, debugging services, tracing data flows.
That's where the work lives.
That's where the precision matters.
When someone asks "how does this work?", the backend is the honest answer.
It's the most complete, most accurate description of the system we have.

So when someone asks "what does the system do?", we answer the same way.
Not because we're being difficult.
Because the backend is the layer we trust.
The interface feels like a simplification: a lossy summary of something we know in full detail.

But that instinct, however natural, has a cost.
The ATM screen isn't a dumbed-down version of the backend.
It's a different kind of knowledge entirely.
It describes intent, not mechanism. It answers the question a new team member, a stakeholder, or a product owner actually needs to move forward.

When we skip the ATM screen and go straight to the backend, we're not being more rigorous. We're just answering a different question than the one that was asked.

## Finding the ATM Screen Together

After the discussion went in circles long enough, I suggested we draw a sequence diagram: the user roles, the system components, the core use cases walked through step by step.

Something shifted.
Instead of explaining how services called each other, we started describing what a user could do, and what the system would do in response.
The backend knowledge was still there, informing every step.
But it was now expressed at the interface layer: behavior, not mechanism.

The diagram became our ATM screen.
A shared surface that both of us could read, regardless of how deeply we each knew the backend behind it.

The discussion unblocked.
Not because we had learned something new about the system, but because we had found the right layer to talk about it.

## The ATM Screen First, Always

Back to that meeting room.

The feature team wasn't wrong to know the backend deeply.
That knowledge is what makes a system run.
But deep backend knowledge, expressed only in backend language, doesn't travel, not to a new team member, not to a stakeholder, not to anyone who needs to understand what the system does before they can reason about how to change it.

This is the mindset shift I'm still learning.
Before we explain how a system works, we should be able to explain what it does.
Not as a simplification.
Not as a dumbed-down summary.
But as a different, equally valid layer of knowledge, the one that makes everything else legible.

In system design, we've always known this.
Requirements before architecture.
Interface before implementation.
The ATM screen before the backend.

The sequence diagram wasn't a workaround.
It was the right starting point, the one we should have found at the beginning of the conversation.

Start with the ATM screen.
The backend will still be there when we need it.
