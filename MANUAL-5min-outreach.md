---
layout: manual
title: 5-Minute Festival Outreach
heading: Outreach guide 
permalink: /manual-outreach-5min.html
eyebrow: Teach
description: >-
  A ready-to-run 5-minute Bloch-sphere script for engaging passers-by at a
  science festival, open day or booth. No prior knowledge needed, ages 12+.
lede: >-
  A ready-to-run script for engaging passers-by at a festival, open day or
  booth. No prior knowledge needed, for anyone 12+.
meta:
  - k: Time
    v: "5–15 min"
  - k: Audience
    v: "12+"
  - k: Listeners
    v: "1–15"
  - k: You need
    items:
      - The Orb
      - A PC running QX Orb
      - A game controller (recommended)
      - A large screen, so the crowd can follow along
related:
  - label: "30-minute classroom session →"
    url: "manual-classroom-30min.html"
  - label: "QX Orb game manual →"
    url: "manual-qx-orb.html"
---

## Suggested setup

Ideally, prepare a table with nearby power socket to put the Bloch Sphere on, such that it is clearly visible (also from furthe away -- it's a great eyecatcher that will lure audience to you). Additionally, have a large screen (which as many people as possible can see well -- it should be above should height). Connect a laptop running QX Orb to the screen and to the Bloch Sphere.  

For help installing QX Orb, see the [QX Orb manual](manual-qx-orb.html). Optionally, you may like to put down additional spheres with the same or other standalone games, like the [Fish Game](play.html). 

Have at least one guide who will run through the script below. A good guide is someone who explain all steps vividly and passionately, and can adjust the content to the background of the audience. 


## The script

The following is a great way to engage with almost everyone — no prior
knowledge needed.

**1. Explain the basics of the Bloch Sphere qubit**

> "This ball shows a single **qubit** — the basic piece of a quantum computer.
> The arrow on it is the qubit's *state*: it's the information stored inside.
>
> _(Hold up and show the sphere.)_ Up means **0**. Down means **1**.
> So far that's just a normal bit — on or off.
>
> But a qubit can point **anywhere on the ball**. Here, on the **equator**, it's
> perfectly in between 0 and 1. A surprising property of quantum mechanics is
> that the qubit is now both 0 and 1 at the same time — in fact, the future of
> the universe depends on both possibilities! We call this a **superposition**.
>
> *(Tilt arrow 45 degrees above the equator.)* Up here it's *more 0 than 1*.
> *(Tilt below.)* Down here, *more 1 than 0*. *(Rotate the arrow around to the
> far side of the equator.)* And this direction is a different state again.
> **Every direction the arrow can point is a valid quantum state** — a different
> piece of information. Hence, there are infinitely many possible states or
> pieces of information that can be stored!"

**2. Explain the concept of quantum gates**

> "A quantum computer **computes** by changing that information — and changing
> the information means **moving the arrow**. One specific rotation is called a
> **quantum gate**. For example, rotating the qubit 180 degrees is one gate;
> rotating it 90 degrees is another gate."

**3. Invite the audience to play**

> "Who wants to become a quantum programmer and give this a try?"
> *(Select someone from the audience and give them the controller. Give
> instructions to start **Level 1**.)*

**4. Explain the rules of the game**

> "Here's the job: the arrow **starts pointing up**, and you need to get it
> pointing **down**.
>
> You do it with the **A, B, X, Y buttons on the controller**, which have a
> matching colour with the buttons on the screen. Clicking one button executes
> the corresponding gate. Give it a try!"

**5. Narrate while they play**

Call out every move so the crowd follows what's happening.

> "That's the red button, or the Z gate. It rotates the sphere along the
> equator, just like the earth turns. But it doesn't get the arrow down…"
>
> "Hey, that's the green button, labeled 'H'. It gets the arrow down to the
> equator. We're already halfway! That's a superposition right there."
>
> "And now it's swung around to point down — **that's it, you solved it!**"
> *(Confetti, applause, the works.)*
>
> *(Pressing H twice.)* "Notice that pressing H twice brings the arrow back to
> where it started."

> **Tip for Level 1:** every gate here is a **180° rotation** (a half-turn).
> So pressing the *same* button twice just brings you straight back where you
> started! If a player gets stuck, nudge them: *"using the same button twice is
> never going to help you."*

**6. Play freely**

After solving Level 1, allow the rest of the group to try Levels 2–4 by
themselves.

---

## Audience note

- **Kids (≈8–12).** Don't get into any quantum details. Simply state that this
  is similar to a qubit and/or programming a quantum computer, and let kids
  play! Talk about "the arrow" and let them solve Level 1 by trial and error.
- **Mathematicians.** They will know the rotations on the sphere as the
  '(special) orthogonal group' SO(3). They may also recognise the
  correspondence to SU(2), the group of unitary operations/matrices. The
  unitaries are precisely the representation in which most people study quantum
  mechanics: 2×2 matrices acting on a 2-dimensional complex vector (the
  'quantum state vector').

