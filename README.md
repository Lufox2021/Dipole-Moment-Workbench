# Dipole Moment Workbench

Second-generation molecular dipole tool for general and organic chemistry students. It replaces the drawing-based *Dipole Moment Lab* with a guided three-step analysis.

**Live tool (after GitHub Pages is turned on):** https://lufox2021.github.io/Dipole-Moment-Workbench/

## How it works

1. **Polar bonds.** The student sees the name, molecular formula and Lewis structure, and predicts whether the molecule has polar bonds. Then, for each kind of bond, the student enters both Pauling electronegativities (from the pop-up periodic table), the difference, and polar or nonpolar. The tool does not state the cutoff; it grades with *polar if the difference is greater than 0.40*.
2. **Shape (VSEPR).** For each central atom, the student picks the electron geometry and the molecular geometry. When both are right, the 3D model appears with a bond-dipole arrow on every polar bond. Arrow lengths are proportional to tabulated bond moments.
3. **Is the molecule polar?** After the answer, a bright magenta arrow shows the molecular dipole, labelled with the measured gas-phase μ.

3D controls: **right-drag rotates, left-drag moves, scroll zooms** (Shift-drag also rotates; on touch screens one finger rotates, two fingers move and zoom).

### Modes

- **Teaching:** specific hints, and a *Show me* button after two wrong tries.
- **Test:** no hints. Answers are filled in after three wrong tries (one try for yes/no questions). Score = items right on the first try.
- **Instructor:** add, edit or delete compounds (SMILES for the Lewis structure), preview the answer key with warnings about confusing cases, edit the bond-moment table, and download `problems.json`.

## Problem library (`problems.json`)

50 starter compounds (26 inorganic, 24 organic, levels 1–3). Edits made in the Instructor tab are stored in that browser only. To publish them, download `problems.json` and replace the file in this repository.

Library rules: no bond with an electronegativity difference between 0.36 and 0.44 (too close to the cutoff), none above about 1.6 (some textbooks call those ionic), and no molecule whose polarity disagrees with its polar bonds.

## Chemistry notes

- Electronegativities: Pauling scale.
- Bond moments: Smyth-type table and NIST CCCBDB diatomics where available. Rows marked *estimate* are placeholders (B–Cl, Si–Cl, P–Cl, S–Cl, N–F, O–F, S–F, Xe–F).
- The molecular-dipole direction is the vector sum of the polar bond dipoles; its label is the experimental value.

Built on the Dipole Moment Lab code (SMILES → Lewis structure, 3D geometry, WebGL viewer). Single self-contained `index.html`; no installation.
