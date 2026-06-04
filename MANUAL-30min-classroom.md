---
layout: manual
title: 30-Minute Classroom Session
heading: One ball, a 30-minute class on qubits
permalink: /manual-classroom-30min.html
eyebrow: Teach · classroom manual
description: >-
  A 30-minute hands-on Bloch-sphere session for physics and CS students —
  state vectors, Pauli matrices, unitary rotations and non-commutativity.
lede: >-
  A deeper, hands-on session for STEM students who are comfortable with
  vectors, matrices and complex numbers. The value of the Orb is to make
  geometrical rotations visible.
meta:
  - k: Time
    v: "~30 min"
  - k: Audience
    v: "Physics / CS"
  - k: Prereq
    v: "Linear algebra"
  - k: You need
    items:
      - The Orb
      - A PC running QX Orb
      - A game controller + large screen
      - A whiteboard (optional)
related:
  - label: "5-minute festival pitch →"
    url: "manual-outreach-5min.html"
  - label: "QX Orb game manual →"
    url: "manual-qx-orb.html"
---

## The session

With this audience you can drop the analogies and use the real machinery.

**① The state as a vector (≈2 min)**

> "A qubit's state is $\lvert\psi\rangle = \alpha\lvert 0\rangle + \beta\lvert 1\rangle$, with $\lvert\alpha\rvert^2 + \lvert\beta\rvert^2 = 1$. Two complex
> numbers, one normalisation, and a global phase we can't observe — that's
> **two real degrees of freedom**, which is exactly the surface of a sphere."

Write the standard parametrisation and tie each part to the Orb:

> $$\lvert\psi\rangle = \cos\tfrac{\theta}{2}\,\lvert 0\rangle + e^{i\varphi}\sin\tfrac{\theta}{2}\,\lvert 1\rangle$$
>
> - **$\theta$** = polar angle. *(Arrow up.)* $\theta = 0$ is $\lvert 0\rangle$; *(arrow down)* $\theta = \pi$ is $\lvert 1\rangle$.
> - **$\varphi$** = azimuth, the phase. *(Sweep arrow around the equator.)* These are all
>   equal superpositions — same measurement probabilities, **different phase**.
> - Measurement probability of 1 is $\sin^2(\theta/2)$: only the *latitude* matters for
>   what you'd read out; longitude is "hidden" phase information.

**② Gates as unitary rotations (≈4 min)**

> "Quantum gates are unitary operations that act on the state vector. On the Bloch sphere, every unitary is the same as a rotation in three-dimensional space. Recall that rotations are given by an axis and an angle."

Introduce the **Pauli matrices** as the generators of these rotations:

> $$\sigma_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad \sigma_y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad \sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}.$$

Each Pauli squares to the identity, $\sigma_k^2 = I$, and they anticommute. A rotation by angle $\theta$ about an axis $\mathbf{n}$ is then the matrix exponential

> $$R_{\mathbf{n}}(\theta) = \exp\!\left(-i\,\tfrac{\theta}{2}\,\mathbf{n}\cdot\boldsymbol{\sigma}\right) = \cos\tfrac{\theta}{2}\,\mathbf{I} - i\sin\tfrac{\theta}{2}\,(\mathbf{n}\cdot\boldsymbol{\sigma}).$$

This is the key formula to write on the board. It is an **interpolation** between two limits, both visible on the Orb:

> - **$\theta = 0$:** $R = \mathbf{I}$, the identity — the arrow doesn't move.
> - **$\theta = \pi$:** $R = -i\,(\mathbf{n}\cdot\boldsymbol{\sigma})$, which up to a global phase is just the Pauli itself — a full 180° flip about $\mathbf{n}$.
> - **In between:** a weighted mix of *not rotating* (the $\mathbf{I}$ term) and *fully flipping* (the $\sigma$ term), with weights $\cos(\theta/2)$ and $\sin(\theta/2)$.

Now point at the gates on the buttons and read them off this formula:

> - **X, Y, Z** — the $\theta = \pi$ endpoints: 180° rotations about the x, y, z axes; the Paulis themselves.
> - **X₉₀, Y₉₀, Z₉₀** — $\theta = \pi/2$: equal mix of I and Pauli, $R = \tfrac{1}{\sqrt{2}}(\mathbf{I} - i\sigma_k)$. Halfway between "do nothing" and "flip".
> - **H** — 180° rotation about the $(x+z)/\sqrt{2}$ axis, i.e. $\mathbf{n}\cdot\boldsymbol{\sigma} = (\sigma_x + \sigma_z)/\sqrt{2}$. That's why it swaps the z- and x-poles, sending $\lvert 0\rangle$ to $\lvert +\rangle$ on the equator.
> - **S, T** — phase gates: rotations about z by 90° and 45° (small-$\theta$ z-rotations). They move $\varphi$ only, so from the pole they do *nothing visible* — a nice puzzle moment.

**③ Hand over the controller — Levels 1 → 2 (≈3 min)**

Start **Level 1** (H, Z): get from $\lvert 0\rangle$ to $\lvert 1\rangle$. Let them discover that two
identical 180° gates cancel ($U^2 = I$ for the Paulis and H), i.e. every gate
here is its own inverse.

Then **Level 2** (H, U): now phase matters. From a pole, the phase-type gate
looks inert until you've used H to get onto the equator first. This is where
students feel the difference between *probability* and *phase*.

**④ The punchline: gates don't commute (≈3 min)**

Move to **Level 3** (90° rotations, single-use) or **Level 4** (H, S). Have one
student do **H then Z** and another do **Z then H** from the same start — the
arrow lands in different places.

> "Rotations about different axes don't commute: $R_z R_x \neq R_x R_z$. Order is
> physical. That non-commutativity is exactly what gives quantum circuits their
> structure — and, with more qubits, their power."

Close by naming what the Orb *doesn't* show: measurement (it never collapses
the arrow), and entanglement (one qubit's two real parameters are the whole
sphere — add a second qubit and there's no 3D ball any more).
