# Sleeve mould (v1)

3D-printed mould used to cast the thin pigmented silicone sleeves ("skins")
that slide over the tip of the finger phantom described in
[`../finger`](../finger). Each sleeve stands for one skin tone; the oximeter
clips onto the sleeve as it would onto a patient's finger.

## Files

| File | Use |
|---|---|
| `sleeve_mould_core_v1.stl` | Core: a rigid copy of the finger with a locating bar (print this) |
| `sleeve_mould_left_v1.stl` | Left half of the shell, with pin holes (print this) |
| `sleeve_mould_right_v1.stl` | Right half of the shell, with pins (print this) |
| `sleeve_mould_v1.step` | Neutral CAD format, whole assembly (core and both shell halves) |
| `sleeve_mould_v1.f3d` | Autodesk Fusion source, with parameters and history |

Shell: 39 × 34 × 31 mm. Silicone per sleeve: about 1.5 mL.

## Parameters (user parameters in Fusion, mm)

The mould uses the finger parameters (`doigt_*`, `bout_rayon`) and the pin
parameters of the finger mould (`paroi_moule`, `pion_*`), plus:

| Name | Value | Meaning |
|---|---|---|
| `manchon_epaisseur` | 1 | sleeve wall thickness |
| `manchon_longueur` | 30 | length of finger covered, from the tip |
| `barre_epaisseur` | 4 | thickness of the locating bar on the core |
| `barre_haut` | 4 | height of the locating bar |

## How it works

The sleeve is cast in the 1 mm gap between two printed parts:

- a **shell** in two halves, whose cavity is the finger tip grown by
  `manchon_epaisseur` (ellipse 18 × 15 mm, tip fillet `bout_rayon + manchon_epaisseur`);
- a **core**, which is the finger itself, so the sleeve fits the silicone
  finger exactly.

A **bar** across the core, with two pins, sits on the top face of the shell.
It sets both the depth of the core (1 mm gap at the tip) and its centring
(1 mm gap all around). The two shell halves are aligned by four pins, as in
the finger mould.

## Design choices

- **1 mm instead of a real epidermis (~0.1 mm).** A 0.1 mm silicone layer
  cannot be cast reliably. What the oximeter responds to is the total
  absorbance of the layer (thickness × pigment concentration, Beer–Lambert),
  so a thicker layer with less pigment gives the same absorbance. Each sleeve
  is characterised by its measured transmission, not by its recipe.
- **One mould for all sleeves.** The skin tone comes from the pigment, not
  from the mould. A thicker "amplified" sleeve only needs a new value of
  `manchon_epaisseur` and a new export.
- **Parting plane on the sides of the finger**, as in the finger mould, so
  the seam stays away from the light path (nail to pad).
- **Open top.** The ring-shaped opening around the core lets excess silicone
  and air escape when the core is pushed in.

## Casting procedure (planned, not yet tested)

1. Print the three parts. The shell halves print with the parting face up;
   the core prints standing on its base, with supports under the bar.
2. Close and clamp the shell, pour about 2 mL of degassed, pigmented silicone.
3. Push the core in slowly until the bar rests on the shell and its pins
   enter their holes. Excess silicone overflows at the top.
4. After curing, open the shell and peel the sleeve off the core.

## Limitations of v1

The thickness depends on the printing accuracy (about ±0.1–0.2 mm, i.e. up
to 20 % of the wall); each sleeve's thickness and transmission will be
measured. The sleeve's inner surface matches the finger exactly, with no
pre-stretch; a slightly tighter fit may be needed to avoid air gaps.
