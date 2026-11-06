# An unmodified retinal object-motion circuit localises a robot's own body

**Viraj Deshwal** · ReinforceAI

A robot derives which part of its visual field is its own body, using no markers, no CAD
model, no training, and no prior images of itself.

**[Read the paper](reinforceAI-reafference.pdf)**

---

## The problem

A moving animal receives self-caused and world-caused sensory change on the same channel,
and the fact that separates them is not in the channel. It is in the motor system. Robots
are normally handed the answer: a CAD model, fiducial markers, or forward kinematics with a
calibrated camera. Every one of those is fixed at build time, so a damaged platform, a new
tool, or a heavier payload makes the answer wrong with nothing in the system to report it.

## What was done

The object-motion-sensitive circuit characterised in salamander retina was taken with its
thirteen constants at values from the primary literature and run unmodified on a camera
bolted to the gripper of a five degree-of-freedom arm.

The camera is rigid to the hand, so while the arm sweeps the room past it the body is the
only region of the image that does not move. The circuit responds to a region that could
register change and does not while its neighbourhood does. The body emerges from the
circuit's ordinary operation.

## Three predictions, registered before measurement

| prediction | published | measured |
|---|---|---|
| the field's characteristic length is the circuit's own inhibitory pool | 1 pool | **1.006 pools** |
| the object-motion ganglion cell is silent on the body | zero | **identically zero**, three captures |
| the release time constant of the sensitisation dynamic | **2.4 s** in salamander | **2.347 s**, r² 0.96 |

The release constant was measured over 98 continuous movement offsets in a previously unseen
room under direct sun and moving shadow. Nothing in the sensitisation chain was tuned to
produce it. The single parameter the literature leaves unconstrained has since been swept
across its full admissible range: no value reaches 2.4 s, and the value used is twice as far
from the published figure as the closest one.

## Five controls, each able to end it

contrast · translation, 0 of 200 placements · order reversed · held out, 1.00 against
in-sample · four gripper apertures

## What did not transfer

The onset time constant does not reproduce. Sensitisation is published at 0.55 s and
measures 0.11 s here. The reason is reported in full: the camera runs at 30.3 fps and the
26 ms presynaptic step inside the circuit is 0.79 of one frame, so at this rate it rounds
away and the mechanism is absent. Half the circuit transfers. Half does not, for a stated
reason that predicts the conditions under which it would.

## One policy, two problems

The move-stop movement policy was fixed earlier in this programme for credit assignment, so
that one command is in flight at a time and the mapping from command to outcome has one term.
The body localisation reads the recording that policy was already producing. The policy that
maximises information gain about your own effects is the policy that localises you. Same
policy, no second mechanism.

## The claim

A published biological computation survives transplantation into an engineered sensor intact,
and a useful capability falls out of it.

## Contents

```
reinforceAI-reafference.pdf    the paper, 12 pages
```

## Citation

```bibtex
@misc{deshwal2026reafference,
  author = {Deshwal, Viraj},
  title  = {An unmodified retinal object-motion circuit localises a robot's own body},
  year   = {2026},
  note   = {ReinforceAI},
  url    = {https://github.com/ReinforceAI/reafference}
}
```

## Contact

[reinforceai.com](https://reinforceai.com) · viraj@reinforceai.com