# Finger phantom (v1)

Parametric model of the silicone finger that the pulse oximeters clip onto.
The finger will be cast in silicone in a 3D-printed mould (next step); a soft
channel inside it carries the pulsed liquid that mimics arterial blood.

## Files

| File | Use |
|---|---|
| `finger_v1.f3d` | Autodesk Fusion source, with parameters and history |
| `finger_v1.step` | Neutral CAD format (SolidWorks, CATIA, FreeCAD…) |
| `finger_v1.stl` | Mesh for 3D printing or visual checks |

## Parameters (user parameters in Fusion, mm)

| Name | Value | Meaning |
|---|---|---|
| `doigt_largeur` | 16 | width at the nail |
| `doigt_epaisseur` | 13 | thickness nail → pad (the light path of the oximeter) |
| `doigt_longueur` | 60 | total length (a fingertip clip covers ~25–30 mm) |
| `bout_rayon` | 5 | fillet of the fingertip (must stay below `doigt_epaisseur/2`) |
| `vaisseau_diam` | 2 | diameter of the liquid channel |
| `vaisseau_fond` | 8 | silicone left between the channel end and the fingertip |

Width and thickness are approximate values for an average adult index finger;
they will be checked against published anthropometric data.

## Design choices

- **Elliptical cross-section, wider than thick**, like a real fingertip. The
  oximeter shines through the thickness, from nail to pad.
- **Rounded tip** so the clip seats as on a real finger and the silicone does
  not tear at a sharp edge when demoulding.
- **Blind channel on the finger axis**, filled and pulsed from the flat base.
  A channel running through the tip would hit the end of the clip. If liquids
  must be flushed continuously (switching between liquid A and liquid B), a
  U-shaped channel is the planned alternative.

## Limitations of v1

Constant cross-section (no taper), no nail, a single straight channel.
These are enough for a first casting test and will be revisited after it.
