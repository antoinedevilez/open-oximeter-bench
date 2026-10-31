# Finger mould (v1)

Two-part 3D-printed mould used to cast the silicone finger described in
[`../finger`](../finger). A 2 mm steel rod held in the mould forms the liquid
channel inside the finger.

## Files

| File | Use |
|---|---|
| `finger_mould_left_v1.stl` | Left half, with the four pin holes (print this) |
| `finger_mould_right_v1.stl` | Right half, with the four pins (print this) |
| `finger_mould_v1.step` | Neutral CAD format, whole assembly (finger, rod, both halves) |
| `finger_mould_v1.f3d` | Autodesk Fusion source, with parameters and history |

Outer size of the closed mould: 73 × 32 × 29 mm. Silicone needed: about 9.4 mL
(volume of the finger minus its channel).

## Parameters (user parameters in Fusion, mm)

The mould uses the finger parameters (`doigt_*`, `vaisseau_*`) plus:

| Name | Value | Meaning |
|---|---|---|
| `paroi_moule` | 8 | wall thickness around the finger cavity |
| `tige_depasse` | 15 | length of rod sticking out of the base |
| `pion_diam` | 3 | diameter of the alignment pins |
| `pion_haut` | 3 | height of the pins |
| `pion_jeu` | 0.2 | radial clearance of the pin holes (hole Ø 3.4, depth 3.5) |
| `pont_epaisseur` | 4 | thickness of the bridge across the open base |
| `pont_haut` | 5 | height of the bridge above the base |

## Design choices

- **Cast upright, fingertip down.** The base of the finger stays open: it is
  both the pouring hole and the air vent, so no extra sprue is needed.
- **Parting plane through the finger axis, on the sides of the finger.** The
  thin flash left by the seam lies on the sides, away from the light path of
  the oximeter (nail to pad).
- **No draft angle.** The silicone is soft enough to be peeled out of a
  straight cavity.
- **Four pins with 0.2 mm clearance** align the two halves without forcing.
- **A bridge across the base clamps the rod on the finger axis.** Each half
  carries one half of the bridge, so the rod is gripped when the mould is
  closed. The openings left above and below the bridge are used to pour and
  to let air out. The Ø 2 mm hole is drilled again with a 2 mm drill after
  printing, so the rod slides in without play.

## Casting procedure (planned, not yet tested)

1. Print both halves with the parting face up (no supports needed).
2. Drill the bridge hole to 2 mm and check that the halves close flat.
3. Close the mould, clamp it, and push the rod through the bridge until it is
   52 mm deep in the cavity (`doigt_longueur - vaisseau_fond`), that is
   57 mm past the outer face of the bridge. Mark the rod beforehand.
4. Stand the mould base up, pour degassed silicone slowly through one opening.
5. After curing, pull the rod out, open the mould and peel the finger.

## Limitations of v1

No release-agent or degassing guidance yet, and the rod depth is set by hand.
These will be revisited after the first casting test.
