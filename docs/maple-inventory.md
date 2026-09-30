# Maple inventory and dependency review

Reviewed against commit `5d8b83be6aba4c0bcde0451e06f06c5ef462b07b`. **No Maple files have been deleted.** The review includes the four XML worksheets, the SQLite workbook's referenced executable Equation contents, and the LaTeX manuscript/presentation.

## Research sources to keep

| File | Evidence | Action |
| --- | --- | --- |
| `Sobolev4.mw` | 188 Input regions containing procedures and calculations; three external `read` operations. | Keep as research source. |
| `tfg6.mw` | 307 Input regions; matrix, polynomial and singular-value calculations; 13 literal `save` operations. | Keep as source and experiment record. |
| `tfg7.mw` | 29 Input regions; calculations, a dynamically assembled output filename and an explicit saved-state read. | Keep as source. |
| `tfg7.maple` | SQLite workbook; 33 Equation records, 30 executable regions. Their referenced ModelContents were decoded for this review. | Keep; it is not a byte duplicate of `tfg7.mw`. |
| `presentacion.mw` | Two Input regions, including self-contained plotting code for intervals. No read/save operation found in those inputs. | Keep for presentation figures. |

Worksheet files also contain cached outputs. That does not make their executable inputs disposable, nor establish sole authorship of every included routine.

## What is generated, and what is required?

All **57 `.m` files are serialized Maple result/state files**, beginning with `M7R0` and saved matrix data. They are not standalone source scripts.

- **Building the manuscript or slides:** the LaTeX sources reference existing PNG figures and contain no direct Maple-state input. The `.m` files are not required for TeX compilation; preserve the figures.
- **Running the current `tfg7.mw`:** Input 24 explicitly reads `r11.c1(-.5)(-.5)c2(0.)(0.).m`. Keep it unless the workflow is changed and verified.
- **Regenerating experiments:** `tfg6.mw` explicitly saves 11 existing states plus two files absent from this tree: `a-0b10c20d30.m` and `id-025-10Pas.m`. `tfg7.mw` and the workbook assemble output filenames from parameters. These are evidence of generation, not proof that every current state can be regenerated identically.
- **Additional reproduction gaps:** `Sobolev4.mw` reads `carga` twice and `homo` once; corresponding standalone files are absent from `maple/`. No Maple installation is available here to resolve its library/search-path behavior. Keep the source and document this dependency rather than claiming a clean reproduction.

## Concrete deletion proposal

| Proposed deletion | Identical file to retain | Shared Git blob SHA |
| --- | --- | --- |
| `aabbccddt2.t10..m` | `a-1.b1.c-1.d1.t2.t10..m` | `e0707925a4caab9d673ac786a3f499194cbd4b6b` |
| `aabbt0..m` | `a-1.b1.t0..m` | `2874f82e91e634bc64f4fb7d1545b57a1e14df0f` |

Neither alias appears in decoded executable inputs of the four worksheets or the workbook. The observed reads are a literal filename or the external names `carga`/`homo`; no read assembled from these aliases was found. Deleting these two files would retain identical bytes under the descriptive filenames. **Await approval before deleting them.**

Keep the other **55 saved states** for now. A broader deletion should follow a Maple run that regenerates the relevant experiments and checks the retained manuscript figures. This review does not claim numerical identity without execution.

## File-by-file decisions

All paths are relative to `maple/`.

| File | Evidence/classification | Action |
| --- | --- | --- |
| `a-1.b1.c-1.d1.t10.t2..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-1.b1.c-1.d1.t2.t10..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-1.b1.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-1.b1.t2..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-11b1c-1d1.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a-15.b-5.c5.d14.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-15.b-5.c5.d16.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-15b-5c5d14.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a-15b-5c5d15.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-15b-5c5d16.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a-1b1t0.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a-1b1t2.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a0.b1.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0.b1.t2..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0.b10.c30.d40.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0.b10.c30.d40.t0.t0.e60f70.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0.b10.c30.d50.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0.b10.c30d40t2..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0.b20.c30.d40.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0b10c30d40.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a0b10c30d50.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a0b10c50d60.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a0b1t0.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a0b1t2.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a0b1tt0.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a0b20c30d40.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a30.b40.c0.d10.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a30.b40.c0.d20.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a30.b50.c0.d10.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a30b40c0d10.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a30b40c0d20.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a30b50c0d10.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `a40.b30.c0.d10.t0.t0..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a40b30c0d10.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `a50b60c0d10.m` | Explicit `save` output in `tfg6.mw` | Keep pending a verified Maple regeneration |
| `aabbccddt2.t10..m` | Exact duplicate of `a-1.b1.c-1.d1.t2.t10..m` | Propose deletion; await approval |
| `aabbt0..m` | Exact duplicate of `a-1.b1.t0..m` | Propose deletion; await approval |
| `r1.25c1-10r21.c20.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c1(-.5)(-.5)c2(0)(0).m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c1(-.5)(-.5)c2(0.)(0.).m` | Explicit `read` in `tfg7.mw`, Input 24 | Keep: currently loaded by a worksheet |
| `r11.c1(-.5)(-.5)c20..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c1(-.5)(0.)c2(0)(0).m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c1(0)(0)c2(10)(0).m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c1-.5c20..m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10c2(.5)(.5).m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10c2(.5)(0.).m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10c2(0.)(.5).m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10c2.5.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10c20.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10c210.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r2.25c2-10.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r2.4c2.4.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r2.5c210.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r21.c2-10.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r21.c21.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r210.c2.5.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |
| `r11.c10r22.c2.5.m` | Generated saved state; no exact literal input reference found | Keep pending a verified Maple regeneration |

## Verification boundary

The current worksheet bytes match their Git blob SHAs (excluding the extra newline added by the earlier local audit export); the workbook matches directly. Exact duplicate pairs were rechecked against the current tree. This is a static dependency review. Maple execution, figure regeneration and a clean TeX build have not been performed.
