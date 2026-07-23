---
title: New Minor Forcing
skill_paths:
  - bidding_conventions/new_minor_forcing
primary: bidding_conventions/new_minor_forcing
level: intermediate
author: Rick Wilson
status: published
reviewed-by: self
columns: 3
---

**New Minor Forcing (NMF)** solves a common problem: after opener rebids 1NT,
responder has game-going values and a five-card major but doesn't yet know
whether opener holds three-card support. Bidding the *other* minor — the "new
minor" — is an artificial force that asks opener to describe support and shape.

## The trigger

Opener rebids **1NT** over a one-level major response — a balanced ~12–14 that
was too weak or wrong-shaped to open 1NT. Responder then bids the unbid minor:

```auction
dealer: N
columns: 2
labels: Opener, Responder
grid: off
1C   P    1S   P
1NT  P    2D =1= P
---
1. New Minor Forcing — artificial and invitational. Says nothing about diamonds.
```

With this hand, responder wants the best game: 4♠ if opener has three spades,
otherwise 3NT.

```hand
seat: S
S: A Q 9 5 4
H: K 7 3
D: A 5
C: J 8 4
```

## Opener's rebids

Opener answers the question — cheaply with 12 or 13 HCP, or with a jump with 14 HCP:

```response-box
title: Opener's rebids after 1♣–1♠–1NT–2♦!
2H/3H | Four hearts - top priority
2S/3S | Three-card spade support
2NT/3NT | Heart stopper
3D | 4 diamonds
3C | 5 clubs
Jump | With 14 HCP
```

## Putting it together

Opposite three-card support, responder drives to the major-suit game:

```auction
columns: 2
labels: Opener, Responder
grid: off
dealer: N
1C   P    1S   P
1NT  P    2D =1= P
2S =2= P    4S   P
---
1. New Minor Forcing
2. Three-card spade support, 12-13 HCP
```

## Remember

* NMF is **only** on after a **1NT rebid** by opener — not after every 1NT.

* The new minor promises **nothing** in that minor; it is pure convention.

* Responder needs at least invitational values. Weaker hands pass 1NT or sign
  off in a suit instead.
