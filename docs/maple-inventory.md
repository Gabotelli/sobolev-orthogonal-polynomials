# Maple file inventory and proposed cleanup

Reviewed against the current `main` tree. **No Maple deletion has been applied.**

## Sources to retain

| File | Evidence | Proposed action |
| --- | --- | --- |
| `Sobolev4.mw` | XML worksheet with 188 Input regions, procedures and calculation inputs. | Keep as research source. |
| `tfg6.mw` | XML worksheet with 307 Input regions; polynomial/operator calculations, singular values, save/read operations. | Keep as research source and experiment record. |
| `tfg7.mw` | XML worksheet with 29 Input regions, procedures, further calculations and read/save operations. | Keep; compare with the workbook before considering consolidation. |
| `tfg7.maple` | SQLite Maple workbook with 33 Equation records. | Keep; binary workbook is not automatically a duplicate of the XML worksheet. |
| `presentacion.mw` | XML worksheet with 2 Input regions and presentation plotting code. | Keep for presentation figures. |

The 57 `.m` files below all begin with `M7R0` and serialized `D_matX` data. They are saved Maple states/results rather than standalone source scripts. Some also contain calculated spectral quantities and parameter values.

**Compile versus regenerate:** the LaTeX documents use the existing PNG figures; these caches are not direct TeX inputs. However, the Maple worksheets include `read` and `save` operations, some filenames are assembled dynamically, and a clean Maple run has not been performed. Removing every cache now could break an existing experimental workflow. No cache is asserted to be unnecessary for regeneration solely because its filename does not appear literally.

## Exact duplicates proposed for deletion

| Delete after approval | Identical retained file | Evidence |
| --- | --- | --- |
| `aabbccddt2.t10..m` | `a-1.b1.c-1.d1.t2.t10..m` | Same Git blob SHA: `e0707925a4caab9d673ac786a3f499194cbd4b6b`. |
| `aabbt0..m` | `a-1.b1.t0..m` | Same Git blob SHA: `2874f82e91e634bc64f4fb7d1545b57a1e14df0f`. |

Even duplicate filenames may be referenced by worksheets, so dependent reads should be checked before the approved deletion.

## File-by-file classification

All paths below are relative to `maple/`. Keep the other 55 saved states for now. After a portable Maple regeneration verifies the manuscript/presentation experiments, place required reference results under `results/` and drop regenerable caches with approval.

| File | Classification | Current proposed action |
| --- | --- | --- |
| `a-1.b1.c-1.d1.t10.t2..m` | Generated serialized result | Retain pending verified regeneration |
| `a-1.b1.c-1.d1.t2.t10..m` | Generated serialized result | Retain pending verified regeneration |
| `a-1.b1.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a-1.b1.t2..m` | Generated serialized result | Retain pending verified regeneration |
| `a-11b1c-1d1.m` | Generated serialized result | Retain pending verified regeneration |
| `a-15.b-5.c5.d14.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a-15.b-5.c5.d16.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a-15b-5c5d14.m` | Generated serialized result | Retain pending verified regeneration |
| `a-15b-5c5d15.m` | Generated serialized result | Retain pending verified regeneration |
| `a-15b-5c5d16.m` | Generated serialized result | Retain pending verified regeneration |
| `a-1b1t0.m` | Generated serialized result | Retain pending verified regeneration |
| `a-1b1t2.m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b1.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b1.t2..m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b10.c30.d40.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b10.c30.d40.t0.t0.e60f70.m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b10.c30.d50.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b10.c30d40t2..m` | Generated serialized result | Retain pending verified regeneration |
| `a0.b20.c30.d40.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a0b10c30d40.m` | Generated serialized result | Retain pending verified regeneration |
| `a0b10c30d50.m` | Generated serialized result | Retain pending verified regeneration |
| `a0b10c50d60.m` | Generated serialized result | Retain pending verified regeneration |
| `a0b1t0.m` | Generated serialized result | Retain pending verified regeneration |
| `a0b1t2.m` | Generated serialized result | Retain pending verified regeneration |
| `a0b1tt0.m` | Generated serialized result | Retain pending verified regeneration |
| `a0b20c30d40.m` | Generated serialized result | Retain pending verified regeneration |
| `a30.b40.c0.d10.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a30.b40.c0.d20.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a30.b50.c0.d10.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a30b40c0d10.m` | Generated serialized result | Retain pending verified regeneration |
| `a30b40c0d20.m` | Generated serialized result | Retain pending verified regeneration |
| `a30b50c0d10.m` | Generated serialized result | Retain pending verified regeneration |
| `a40.b30.c0.d10.t0.t0..m` | Generated serialized result | Retain pending verified regeneration |
| `a40b30c0d10.m` | Generated serialized result | Retain pending verified regeneration |
| `a50b60c0d10.m` | Generated serialized result | Retain pending verified regeneration |
| `aabbccddt2.t10..m` | Generated serialized result; exact duplicate | Delete only after approval and read-path check |
| `aabbt0..m` | Generated serialized result; exact duplicate | Delete only after approval and read-path check |
| `r1.25c1-10r21.c20.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c1(-.5)(-.5)c2(0)(0).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c1(-.5)(-.5)c2(0.)(0.).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c1(-.5)(-.5)c20..m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c1(-.5)(0.)c2(0)(0).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c1(0)(0)c2(10)(0).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c1-.5c20..m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10c2(.5)(.5).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10c2(.5)(0.).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10c2(0.)(.5).m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10c2.5.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10c20.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10c210.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r2.25c2-10.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r2.4c2.4.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r2.5c210.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r21.c2-10.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r21.c21.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r210.c2.5.m` | Generated serialized result | Retain pending verified regeneration |
| `r11.c10r22.c2.5.m` | Generated serialized result | Retain pending verified regeneration |

## Reproduction gap

Maple is not installed in the audit environment, so no worksheet execution, source-to-figure identity or minimum required-cache set has been verified. Preserve the existing PNGs used by the thesis/presentation. Proposed future work: normalize worksheet read/write paths, record each experimental configuration, regenerate into a separate output directory and compare with the manuscript figures. This is a proposal, not an executed rewrite.
