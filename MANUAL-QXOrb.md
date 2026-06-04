---
layout: manual
title: QX Orb — Game Manual
heading: Running the QX Orb game
permalink: /manual-qx-orb.html
eyebrow: Software · QX Orb manual
description: >-
  How to start the QX Orb game on the Bloch-sphere demonstrator, plus a guide
  to the four puzzle levels and the gates each one introduces.
lede: >-
  The QX Orb game drives the physical Bloch sphere — a small motorised ball
  whose arrow points in the direction of a single qubit's state. You rotate the
  arrow by applying quantum gates, the same gates used in a real quantum circuit.
related:
  - label: "5-minute festival pitch →"
    url: "manual-outreach-5min.html"
  - label: "30-minute classroom session →"
    url: "manual-classroom-30min.html"
---

<div class="note">
  <span class="ni">&#9881;</span>
  <div>
    <h4>Under construction</h4>
    <p>This QX Orb manual is still being written &mdash; some sections may be incomplete or change. For the latest, check the repository.</p>
  </div>
</div>

This is a physical [Bloch sphere](https://en.wikipedia.org/wiki/Bloch_sphere)
demonstrator: a small motorised ball with an arrow that points in the direction
of a single qubit's state. You rotate the arrow by applying *quantum gates* —
the same gates you would use in a real quantum circuit. The outreach material
is split by session length and audience — see the linked manuals below for a
5-minute festival pitch or a 30-minute classroom session.

## Starting QX Orb

You must have Python installed on your laptop/PC. Run the following in a
terminal window:

```bash
python app.py            # normal use, with hardware connected
python app.py test       # debug mode, no hardware required
python app.py --invert-y-axis   # for left-handed Orbs (e.g. the CWI unit)
```

Then open the URL Flask prints (usually `http://127.0.0.1:5000`) in a browser.
The game is played in your browser screen.

Each level shows the gates as buttons on screen; the buttons on the controller
correspond to the gates shown in the _same colour_ (ABXY). In each level, the
goal is to flip the arrow from up to down.

| Level | Gates | Notes |
| :--- | :--- | :--- |
| 1 | H, Z |  |
| 2 | H, U | U is a 180° rotation; from either pole it rotates the sphere *halfway* to the equator, and from there back to the original pole. |
| 3 | X₉₀, Y₉₀, Z₉₀ | 90° rotations, each usable only once. |
| 4 | H, S | An elaboration of (1). |
