**English** | [简体中文](DATA_SOURCES.zh-CN.md)

# Scientific data provenance

Facet 0.1.0-beta.1 · 2026-11-08

## Contents

1. [Findings](#findings)
2. [Covalent radii](#covalent)
3. [Van der Waals radii](#vdw)
4. [Electron configurations](#configurations)
5. [Atomic weights and examples](#masses)
6. [Palettes and reference styles](#palettes)
7. [Compatibility and remaining limits](#compatibility)
8. [References](#references)

<a id="findings"></a>
## Findings

Current findings are in [beta1-data-review.json](beta1-data-review.json); [historical-data-audit.json](historical-data-audit.json) is the pre-correction snapshot. No automated tests were run. Numerical agreement establishes a match to a reference, not an acquisition route or applicability to every coordination, spin or oxidation state.

<a id="covalent"></a>
## Covalent radii

Frontend and Rust share 96 H–Cm values matching Cordero 2008 Table 2. C uses the sp3 radius, 0.76 Å; Mn/Fe/Co use low-spin values 1.39/1.32/1.26 Å. These choices do not automatically vary with environment. The original 84 values are unchanged. Twelve entries are added below; ten values change, while At/Rn gain reference provenance without a numeric change.

| Element | Reference (Å) | Previous (Å) |
| --- | ---: | ---: |
| Pm | 1.99 | 1.50 |
| Po | 1.40 | 1.50 |
| At | 1.50 | 1.50 |
| Rn | 1.50 | 1.50 |
| Fr | 2.60 | 1.50 |
| Ra | 2.21 | 1.50 |
| Ac | 2.15 | 1.50 |
| Pa | 2.00 | 1.50 |
| Np | 1.90 | 1.50 |
| Pu | 1.87 | 1.50 |
| Am | 1.80 | 1.50 |
| Cm | 1.69 | 1.50 |

Bk–Og retain 22 labeled 1.50 Å fallbacks, not attributed to Cordero. Revision `cordero2008-20261108` participates in covalent-cache fingerprints. Future Rust consumers receive this table when rebuilt; the public ftkit archive was not rebuilt.

<a id="vdw"></a>
## Van der Waals radii

The existing 95 explicit values and 2.00 Å default are retained. This mixed set is not a single Alvarez table; a reference label does not imply direct measurement. Across 118 elements, there are 73 reference, 3 estimated, 13 compiled and 29 fallback values.

| Source | Count | Interpretation |
| --- | ---: | --- |
| Mantina 2009, Table 12 | 41 | Main-group recommended/theoretical references. |
| Batsanov 2001, Table 9 upper row | 26 | Crystallographic references. |
| Bondi 1964, Tables I/XIV | 6 | H, Li, Br, Ni, Cu, Zn. |
| Batsanov 2001, Table 2 | 1 | Fe 2.00 Å estimate, not Table 9's 2.05 Å. |
| Hu 2003; Hu 2009 comparison column | 1 | Ag 2.03 Å estimate; the 2009 recommendation of 2.11 Å is not substituted. |
| Hu 2009, Table 1 note c | 1 | Cd 2.18 Å from Cd(II)–O bond valence. |
| Pinned BODR compilation | 13 | Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu. |
| Software fallback | 29 | Pm, Ac, Pa, Np, Pu, Am, Cm, Bk–Og, all 2.00 Å. |

Six existing explicit 2.00 Å entries are reclassified as fallbacks without changing values or claiming to recover historical intent. BODR is pinned to `c22a200776984388564ef90536d8af24ae09d21e`; its repository CC0 versus stale XML MIT metadata is disclosed in sources.json. Status labels identify estimates/compilations/fallbacks; tooltips and accessible descriptions give sources.

<a id="configurations"></a>
## Electron configurations

All 108 H–Hs entries match NIST neutral-atom ground-state records. Ten Mt–Og entries match Smits et al. (2023), Table 2, p. 34, after expanding [No]/[Cn] cores and combining relativistic subshell notation. Only Lr changes: `[Rn] 5f14 6d1 7s2` becomes `[Rn] 5f14 7s2 7p1`, using NIST rather than the review's older Lr row. Rf–Og are labeled theoretical predictions; other references are not presented as universally measured.

The local valence-display convention retains f shells for f-block elements, so Lr displays `5f14 7s2 7p1`. This is neither the full configuration nor a universal valence definition. Complete NIST non-SRD terms are retained without a blanket global-public-domain claim. Smits uses CC BY 4.0 with attribution, link, full license and adaptation notice. Unverified LANL policy links are not used as the current permission basis.

<a id="masses"></a>
## Atomic weights and examples

The 83 ABACUS masses were originally transcribed via ASE and independently compared with Meija et al., the IUPAC 2013 evaluation published in 2016: 69 match Table 1, 12 are Table 3 conventional values, and Tc=97.90721 / Pm=144.91276 are Table 4 isotope masses for 98Tc / 145Pm, not standard atomic weights. The vague “most stable isotope” comment is replaced by explicit mass numbers; values are unchanged. ASE executable code is not distributed.

Only APNS filenames and masses for 83 elements are bundled, without pseudopotential/orbital binaries. The previously recorded v1 efficiency archive SHA-256 is `869ba0765194c4c699153d8856078f5a1d7330b146dfe4b07235d13d3541d68f`; the full input archive was not downloaded again or relicensed. Built-in structures are demonstration models, not authenticated experimental structures. All external samples were not comprehensively audited.

<a id="palettes"></a>
## Palettes and reference styles

The author confirmed newVESTA ownership on 2026-11-08. Five inherited NV_* palettes match the predecessor at 25 entries each; code ownership does not establish provenance of separately acquired data. The 84 base colors, named palettes and IDs are unchanged.

- JMOL matches 30/30 values from Jmol 12.1.15 / revision 14469. Conservative LGPL-2.1-or-later and copyright notices are retained; no Jmol runtime or LGPL declaration for Facet-owned code is implied.
- NV_MATERIAL_STUDIO matches Jmol for 23/25 entries, except Mo/Te. A variable name does not establish a commercial Materials Studio source.
- The legacy VESTA table has 9 matches and 18 differences among 27 entries compared with official 3.5.8 elements.ini. It is not an exact default palette. Official files were inspected locally, not redistributed.
- Studio has 118 entries and local extension/tuning history (617e3956), but no complete official-version/acquisition record. Difference from Jmol does not prove independent origin; the CPK name is not a specific license grant.
- Matplotlib 3.10.7 magma/inferno/plasma/viridis/cividis/turbo each have 256 verified nodes: all 1,536 rounded 8-bit colors and positions match. No Python runtime is bundled.
- Pretty Lattice is pinned to `7980a9a2e7c7ed21f4b5ef534ed0cc264a4db3c7`: 97 vesta-soft entries including D/XX match, as do metalness 0.1, roughness 0.6, ambient 0.8, directional intensity 2.2, offset [0.3,0.2,0], bond radius 0.1 Å and cell color #444444. Its MIT text matches. Later local adaptations do not imply identical rendering.
- Five ColorBrewer BrBG stops combine the three-color scheme with eleven-color endpoints; they are not the original five-class table. Source `7d135fc4e19eda73f2eb1bf55fcdf4a04fe4881f`, Apache-2.0, author credit and interpolation/adaptation notes are retained. Legacy coolwarm/grayscale/sparse viridis and eight screenshot-based reference maps are not represented as full Matplotlib or other official tables.

<a id="compatibility"></a>
## Compatibility and remaining limits

Saved multipliers apply to current radii, so sizes, covalent bonds and related views/exports can change for ten elements. Covalent caches rebuild by revision; absolute-distance inputs are unchanged. Coordinates, lattice, manual bonds, deletion overrides, colors, multipliers and project/undo/recovery formats are retained. Save a copy of important older projects.

Original VESTA/Studio/CPK acquisition records remain incomplete. Numerical matches do not establish a complete rights history; unsupported exact-default claims are removed. The 320 entries and 215 notice texts do not automatically resolve all historical rights questions. Raw papers, NIST responses and local review material are not distributed.

<a id="references"></a>
## References

| Reference | Reviewed details |
| --- | --- |
| Meija et al., Atomic weights of the elements 2013 | Pure Appl. Chem. 88, 265–291 (2016), [DOI](https://doi.org/10.1515/pac-2015-0305); Tables 1, 3, 4. |
| Cordero et al., Covalent radii revisited | Dalton Trans., 2832–2838 (2008), [DOI](https://doi.org/10.1039/B801115J); Table 2, p. 2836. |
| Bondi, van der Waals Volumes and Radii | J. Phys. Chem. 68, 441–451 (1964), [DOI](https://doi.org/10.1021/j100785a001); Tables I and XIV, pp. 443, 449. |
| Mantina et al., Consistent van der Waals Radii for the Whole Main Group | J. Phys. Chem. A 113, 5806–5812 (2009), [Table 12](https://pmc.ncbi.nlm.nih.gov/articles/PMC3658832/#T12), [DOI](https://doi.org/10.1021/jp8111556). |
| Batsanov, Van der Waals Radii of Elements | Inorganic Materials 37, 871–885 (2001), [DOI](https://doi.org/10.1023/A:1011625728803); Tables 2 and 9, pp. 873, 879. |
| Hu, Zhou, Tsai, Average van der Waals Radii of Atoms in Crystals | Acta Phys.-Chim. Sin. 19, 1073–1077 (2003), [DOI](https://doi.org/10.3866/PKU.WHXB20031118); Ag correspondence also explicit in Hu 2009. |
| Hu, Zhou, Robertson, Consistent approaches to van der Waals radii for the metallic elements | Z. Kristallogr. 224, 375–383 (2009), [DOI](https://doi.org/10.1524/zkri.2009.1158); Table 1, p. 378. |
| Smits, Indelicato, Nazarewicz, Piibeleht, Schwerdtfeger, Pushing the limits of the periodic table — A review on atomic relativistic electronic structure theory and calculations for the superheavy elements | Physics Reports 1035, 1–57 (2023), [DOI](https://doi.org/10.1016/j.physrep.2023.09.004); Table 2, p. 34; CC BY 4.0. |
| NIST Periodic Table of the Elements | [Official compilation](https://www.nist.gov/pml/periodic-table-elements), [terms](https://www.nist.gov/open/license); 108 records retrieved 2026-11-08. |
| Blue Obelisk Data Repository | [Pinned source](https://github.com/BlueObelisk/bodr/tree/c22a200776984388564ef90536d8af24ae09d21e); repository COPYING/README: CC0 1.0. |

[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) · [supplemental/](supplemental/)
