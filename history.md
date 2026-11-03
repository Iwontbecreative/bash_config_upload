# Square packing discovery history: N=100–324

Research snapshot: **3 November 2026**.

This report traces substantial published packing improvements to their original proponents, seed layouts and reported search procedures. It focuses on structural gains and treats numerical polishing and exact certification as separate contributions.

## Scope and reading guide

- Inspected **114 sub-grid case pages** and **88 upper-bound narratives.
- Retained **163 history entries across 72 cases**; **59 cases** have a documented method or parent lineage.
- The complete index covers all 225 counts from 100 through 324. A missing route means no substantial discovery route was established in the inspected material, not that the case has no history.
- All before/after/gain figures below are **container side lengths**, not competition-score changes. Divide a side reduction by √N to obtain the normalized score gain.
- Historical branches overlap; their gains must not be added together.
- Search routes are the authors’ reports. Checking a final witness does not reproduce its discovery.
- Private Kaggle coordinates and unpublished search logs were unavailable.
- A feasible witness, contact polynomial or numerical local optimum does not establish global optimality.

The local portfolio at the time of the report scored **22.243147837594588**, with **1,000/1,000 cases certified**. This is local portfolio context, not a claim that every listed historical packing is the latest record.

## Main structural discovery routes

1. **Construct a V-shaped band explicitly** (155, 156 and the first Ostashev 211), then choose upright staircase corner blocks with an integer program and settle the preselected band using soft-to-rigid search.
2. **Release the junction between components** (176, 211, 241): soften the whole arrangement in a held box so two separated tilted bands can merge. At 304 the blocks relaxed without forming a V.
3. **Interlock component boundaries** (SQUISH 176): cut a 2×3 notch, insert a five-square motif and let subsequent search accommodate another unit. The source’s prose filler count is inconsistent and is flagged below.
4. **Select several boundary patches** (153, 207, 302), including patches inherited from Xu 70. Reclose the retained contacts at compatible angles.
5. **Change count or scale before returning**: 182 from 211, 172 from 199, 260 from a searched 405 island, 299 through 334→373, and 308 from 307.
6. **Keep geometrically distinct nonwinners** (132, 154, 155, 183, 270, 303). Successful lineages sometimes cross above the grid bound before reaching a better packing.
7. **Improve smaller rectangular primitives and recompose** (175, 204, 232, 264, 303), with a subsequent whole-layout search able to release the original seams.

These operators go beyond preserving fixed rectangle seams. No exhaustive geometric test was performed to prove that each resulting layout lacks every possible four-rectangle representation.

## Particularly informative cases

| Case | Discovery lesson |
|---:|---|
| [176](#n-176) | A 38+44 motif composition becomes a connected V after whole-layout hardening. |
| [183](#n-183) | Insertion into the best 182 donor failed; a worse but different donor supplied the successful route. |
| [211](#n-211) | Direct V construction and subsequent merging of two inherited bands are distinct successful routes. |
| [241](#n-241) | Two bands of 47 and 32 units merge into a V of 85. |
| [260](#n-260) | A useful island was improved at 405 and recomposed back into the smaller target. |
| [299](#n-299) | Cross-scale fault-line construction provided the main gain; four refill generations improved it again. |
| [302](#n-302) | Four boundary patches and two upright banks form a six-source construction. |

## Campaign-level evidence

### Ryan Xu: evolving the packing programs

The shared campaign used a shrink/shake/relax baseline with L-BFGS overlap relaxation. Across 128 generations, program mutations developed structured starts, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures. The reported campaign took two days and 7,500 CPU-hours, with $125 of tokens. It produced 25 reported records, including 20 counts in this range.

The per-case winning programs and seed logs are not published. The case entries therefore attribute the shared protocol without inventing a specific winning move for each count.

Sources: [original submission](https://github.com/jlevy/squares/issues/432), [author’s write-up](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### Population search and stepping stones

Daniel’s store-based approach preserves distinct packing geometries and parent/move lineages. The reported successful routes include uphill excursions, crossovers, count-changing moves and remove/refill operations. The N=183 report gives an explicit control: insertion into the record 182 parent did worse than insertion into a nonrecord descendant.

Sources: [architecture](https://github.com/evand/square-packing/blob/main/search/packer/DESIGN.md), [measured claims and limitations](https://github.com/evand/square-packing/blob/main/search/packer/CLAIMS.md), [N=183 discovery](https://github.com/jlevy/squares/issues/680).

## Case-by-case discovery histories

## N 102

Retained local side at the snapshot: **10.605828696528**. [Catalogue case and history](https://squaremath.org/cases/102.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **10.607174680176 → 10.605828696511**; reduction **0.00134598**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 103

Retained local side at the snapshot: **10.679232047458**. [Catalogue case and history](https://squaremath.org/cases/103.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **10.703516755572 → 10.679232047511**; reduction **0.0242847**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 105

Retained local side at the snapshot: **10.789303783743**. [Catalogue case and history](https://squaremath.org/cases/105.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **10.806077865540 → 10.790676575411**; reduction **0.0154013**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 106

Retained local side at the snapshot: **10.822908044231**. [Catalogue case and history](https://squaremath.org/cases/106.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 108

Retained local side at the snapshot: **10.904821012419**. [Catalogue case and history](https://squaremath.org/cases/108.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **10.925919390161 → 10.904824785111**; reduction **0.0210946**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Original neighbouring-count search

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **10.925919390161 → 10.920658939403**; reduction **0.00526045**.

One of the original nine cases seeded from SQUISH neighbouring-count packings by adding/removing squares, then basin hopping and polish.

**Disclosure limits / controls:** This original statement does not identify the exact parent count for this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401).

### 3. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **10.920658939403 → 10.909940073445**; reduction **0.0107189**.

SQUISH 110 minus 2, followed by nearby search

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

## N 110

Retained local side at the snapshot: **10.996783396732**. [Catalogue case and history](https://squaremath.org/cases/110.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 123

Retained local side at the snapshot: **11.591378145498**. [Catalogue case and history](https://squaremath.org/cases/123.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **11.601384658376 → 11.591378145712**; reduction **0.0100065**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **11.601384658376 → 11.600907778516**; reduction **0.00047688**.

Couzo 102 component grafted into the target's catalogue layout

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 126

Retained local side at the snapshot: **11.742640687119**. [Catalogue case and history](https://squaremath.org/cases/126.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **11.774735132388 → 11.742640687212**; reduction **0.0320944**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **11.774735132388 → 11.773303606607**; reduction **0.00143153**.

Couzo 105 component grafted into the target's catalogue layout; an earlier attempt started at the 126 record

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

## N 127

Retained local side at the snapshot: **11.810878787589**. [Catalogue case and history](https://squaremath.org/cases/127.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **11.822875655532 → 11.810936647512**; reduction **0.011939**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

## N 129

Retained local side at the snapshot: **11.870013850404**. [Catalogue case and history](https://squaremath.org/cases/129.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **11.881306218090 → 11.872029849212**; reduction **0.00927637**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **11.881306218090 → 11.879375206711**; reduction **0.00193101**.

Couzo 131 with squares removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 3. Crop a larger donor, reoptimize, then crop again

**Proponent:** Daniil Ostashev. **Route:** crop-and-reoptimize.

Historical side: **11.872029849081 → 11.870013850404**; reduction **0.002016**.

A 163-square(h+3)×h rectangle was cut from SQUISH 302, optimized alone, then stripped of its 3 rightmost unit columns, leaving 129 units in h×h.

1. Remove the enclosing-square constraints by extracting the rectangle.
2. Its tilted band resettles near 39.1° instead of 39.4°.
3. Crop the newly improved rectangle to the target square.

**Disclosure limits / controls:** It keeps a similar upright-block layout to Xu 129 but changes the tilted band. This is not a direct monotonic crop of 153.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/562).

## N 130

Retained local side at the snapshot: **11.902430645982**. [Catalogue case and history](https://squaremath.org/cases/130.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **11.911187706549 → 11.908693569212**; reduction **0.00249414**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Original neighbouring-count search

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **11.911187706549 → 11.904483032517**; reduction **0.00670467**.

One of the original nine cases seeded from SQUISH neighbouring-count packings by adding/removing squares, then basin hopping and polish.

**Disclosure limits / controls:** This original statement does not identify the exact parent count for this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401).

### 3. Thirteen successive web/native basin improvements

**Proponent:** Francisco Couzo. **Route:** local-new-minimum.

Historical side: **11.904483032516 → 11.902430645985**; reduction **0.00205239**.

Start from SQUISH/Gupta/PingYou 130 at 11.904483032516.10 fq updates,2 basin-hop updates and 1 nativeSLP update reach 11.902430645985 on the author’s own machines.11 bodies move>0.1 and tilted count 32→35.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/843).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 131

Retained local side at the snapshot: **11.949659588036**. [Catalogue case and history](https://squaremath.org/cases/131.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **11.954916830216 → 11.951150044912**; reduction **0.00376679**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

Francisco Couzo's s(182) (26 squares; register) + our s(155) (33; `sources/squish-s155-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 132

Retained local side at the snapshot: **11.985680198846**. [Catalogue case and history](https://squaremath.org/cases/132.html).

### 1. Escape above the grid into a new funnel

**Proponent:** Evan Daniel. **Route:** quality-diversity.

Historical side: **11.991327887692 → 11.987099332245**; reduction **0.00422856**.

An archive keeps distinct minima, including worse stepping stones. From Couzo 132, a move chain rises to 12.037 before reaching 11.987099. About 4 minutes on 2 cores.

1. Global/local kicks, angle swaps, row slides, cluster rotations and regional rounded melts.
2. Each proposal: lifted separating-line augmented-Lagrangian descent, then SLP polish.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/465).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 146

Retained local side at the snapshot: **12.583782190163**. [Catalogue case and history](https://squaremath.org/cases/146.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **12.600907778513 → 12.583782277512**; reduction **0.0171255**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cluster reconfiguration within Xu design

**Proponent:** Evan Daniel. **Route:** local-new-minimum.

Reported resulting side: **12.583782190152**.

Start from Xu 146. Two large random kicks and re-polish reach 12.5837821905. A corner-corner MILP direction and re-solve finish it. Only about 10 body cluster changes strongly; the original large side gain is Xu’s, not this finish.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/606).

## N 152

Retained local side at the snapshot: **12.830718800988**. [Catalogue case and history](https://squaremath.org/cases/152.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 153

Retained local side at the snapshot: **12.870013850416**. [Catalogue case and history](https://squaremath.org/cases/153.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **12.881666757009 → 12.881306218213**; reduction **0.000360539**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **12.881666757009 → 12.879679373333**; reduction **0.00198738**.

SQUISH 154 with squares removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 3. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(152) (two pieces of 34; `square-152_r2.svg`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 4. Select boundary patches and reclose contact returns

**Proponent:** PingYou Ltd. **Route:** boundary-patches.

Historical side: **12.872029849081 → 12.870013850407**; reduction **0.002016**.

Change which complete squares/contact constraints survive from Xu 70 and its reflection; reclose at a new angle. Final count 121 upright+17 tilted+15 tilted.

1. Keep complete unit squares, with their parent and ownership identities.
2. Choose compatible boundaries/contacts and solve their return condition.
3. Build and verify the complete rational witness.

**Disclosure limits / controls:** The package replays the finished construction but does not repeat the exploratory patch/owner selection or original floating solve.153 angle is explained by a degree 7 equation; 302 by 2 t³−3 t²−2 t+1=0. Neither is an optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/504).

## N 154

Retained local side at the snapshot: **12.921100940774**. [Catalogue case and history](https://squaremath.org/cases/154.html).

### 1. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **12.931663721167 → 12.926562245854**; reduction **0.00510148**.

SQUISH 155 with squares removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 2. Cross-count quality-diversity recovery

**Proponent:** Evan Daniel. **Route:** count-transfer.

Historical side: **12.923070202301 → 12.922566401934**; reduction **0.0005038**.

Historical 5 October 154/155/156 starts, all Couzo. Neighbour n+1/n+2 deletion plus rounds of basin exploration; 26 rounds of 4 minutes on 2 cores in the broad recovery test.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/552).

### 3. Nonrecord donor plus crossover, then band move

**Proponent:** Evan Daniel. **Route:** quality-diversity.

Reported resulting side: **12.921100940762**.

156→154 by deleting 2, then cross with carried 154 families. Retain a 12.928447 nonrecord. Fingerprint-diverse restart; kicks/row slides and a band move reach 12.92110094 at 771 seconds.12×40 minute followups do not improve it.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/694).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 155

Retained local side at the snapshot: **12.952260944663**. [Catalogue case and history](https://squaremath.org/cases/155.html).

### 1. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **12.955619592134 → 12.952503202605**; reduction **0.00311639**.

Couzo 156 with squares removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 2. Explicit V-band construction

**Proponent:** Daniil Ostashev. **Route:** explicit-band.

Historical side: **12.952498944014 → 12.952425406958**; reduction **7.35371e-05**.

Build a tilted V lattice first; an integer program chooses staircase-shaped upright corner blocks around it. This constructs the large-scale band instead of waiting for it to emerge from random positions.

1. Choose a band angle and geometry.
2. Fill around it with upright Young-diagram corner blocks.
3. Make squares soft; re-harden with the box held, then release/compress.
4. Polish and solve the contact system.

**Disclosure limits / controls:** Author says random global searches stall above about 130. Hardware model, seed count and exact winning parameter sequence are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/501), [source 2](https://github.com/dostashev/square-packing/blob/main/README.md), [source 3](https://ostashev.ai/square-packing/).

### 3. Long uphill lineage then neighbouring angle swaps

**Proponent:** Evan Daniel. **Route:** quality-diversity.

Historical side: **12.952425406958 → 12.952260944651**; reduction **0.000164462**.

Start from Ostashev 155. An 18-move chain climbs as high as 13.047 before returning below record. Final 2 moves swap neighbouring tilt angles. Found 75 minutes into a 2 hour run; 4 further 2 hour restarts fail.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/669).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 156

Retained local side at the snapshot: **12.979165853846**. [Catalogue case and history](https://squaremath.org/cases/156.html).

### 1. Explicit V-band construction

**Proponent:** Daniil Ostashev. **Route:** explicit-band.

Historical side: **12.982082698517 → 12.979172613644**; reduction **0.00291008**.

Build a tilted V lattice first; an integer program chooses staircase-shaped upright corner blocks around it. This constructs the large-scale band instead of waiting for it to emerge from random positions.

1. Choose a band angle and geometry.
2. Fill around it with upright Young-diagram corner blocks.
3. Make squares soft; re-harden with the box held, then release/compress.
4. Polish and solve the contact system.

**Disclosure limits / controls:** Author says random global searches stall above about 130. Hardware model, seed count and exact winning parameter sequence are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/501), [source 2](https://github.com/dostashev/square-packing/blob/main/README.md), [source 3](https://ostashev.ai/square-packing/).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 172

Retained local side at the snapshot: **13.617935698381**. [Catalogue case and history](https://squaremath.org/cases/172.html).

### 1. Find a nonrecord 199, then remove an L

**Proponent:** Evan Daniel. **Route:** count-transfer.

Historical side: **13.618988956900 → 13.617935698381**; reduction **0.00105326**.

Explore SQUISH/Gupta 199. A 24 start fingerprint-diverse sweep finds 199 at 14.617935698, not a 199 record. Remove one 27-square L-strip to obtain 172 at side−1.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/845).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 175

Retained local side at the snapshot: **13.764174317499**. [Catalogue case and history](https://squaremath.org/cases/175.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **13.778174593052 → 13.768899276614**; reduction **0.00927532**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Improved rectangular primitive unlocks a composition

**Proponent:** Daniil Ostashev. **Route:** composition.

Historical side: **13.767119024198 → 13.764174317487**; reduction **0.00294471**.

Two new 38-square pieces plus 99 upright units; follows Ellsworth 171 template.

1. 38 unit piece: random-start GPU soft-to-rigid, footprint(h+2)×h,h≈5.7641743175.
2. 44 unit piece: staircase + tilted-lattice start,h≈5.8086632344,width h+3.
3. 62 unit piece: staircase + tilted-lattice start,h≈5.9099582911,width h+6.
4. Use the appropriate piece, compose, then close the contact topology.

**Disclosure limits / controls:** Only the piece appropriate to this case is used; these remain composition examples rather than evidence all layouts are four rectangles.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/528).

## N 176

Retained local side at the snapshot: **13.795872318449**. [Catalogue case and history](https://squaremath.org/cases/176.html).

### 1. Mondrian: interlocked corner pieces

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** interlocking.

Francisco Couzo's s(127) (121, a 2 × 3 corner of cells taken out; #451, commit ffd900d) + the Kingbird catalogue's s(5) (whole), interlocked

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: one square added by the search

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check. Numerical inconsistency in source prose:121+5+47=173, whereas it calls the assembly 175. Do not use that prose filler count as a validated construction.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 2. Release rectangular seams and re-harden the whole layout

**Proponent:** Daniil Ostashev. **Route:** junction-rehardening.

Historical side: **13.807637226802 → 13.795872318436**; reduction **0.0117649**.

Start from the earlier 38+44 motif composition at 13.808663234. Its two half-bands join through the middle into a V; reported 63 tilted bodies in the joining band.

1. Use jittered copies of the structured parent.
2. Soften every square, not just seam bodies; hold the box while hardening.
3. For V outcomes, seed another hardening round from that V.
4. Release/compress, polish and solve contacts.

**Disclosure limits / controls:** Author reports the same whole-layout step did not improve the identical-piece compositions 175,204,303. The slack in an unequal, nonbinding piece may matter; this is a hypothesis, not a theorem.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/575).

## N 177

Retained local side at the snapshot: **13.822979734182**. [Catalogue case and history](https://squaremath.org/cases/177.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 179

Retained local side at the snapshot: **13.883795490524**. [Catalogue case and history](https://squaremath.org/cases/179.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **13.895341069976 → 13.893954942514**; reduction **0.00138613**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **13.895341069976 → 13.891312565741**; reduction **0.0040285**.

Couzo 180 with one square removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 3. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **13.895341069976 → 13.883795490512**; reduction **0.0115456**.

Couzo 180 minus 1, followed by nearby search

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

## N 180

Retained local side at the snapshot: **13.916993522491**. [Catalogue case and history](https://squaremath.org/cases/180.html).

### 1. Original neighbouring-count search

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **13.927888140498 → 13.923635004252**; reduction **0.00425314**.

One of the original nine cases seeded from SQUISH neighbouring-count packings by adding/removing squares, then basin hopping and polish.

**Disclosure limits / controls:** This original statement does not identify the exact parent count for this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401).

### 2. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **13.923635004252 → 13.917653417451**; reduction **0.00598159**.

SQUISH 182 minus 2, followed by nearby search

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 181

Retained local side at the snapshot: **13.950819531036**. [Catalogue case and history](https://squaremath.org/cases/181.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(154) (37, narrowed; `sources/squish-s154-a-source.cert.json`) + our s(154) (42, narrowed; `sources/squish-s154-b-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 182

Retained local side at the snapshot: **13.970916436215**. [Catalogue case and history](https://squaremath.org/cases/182.html).

### 1. L-cut from 211, then three structural moves

**Proponent:** Evan Daniel. **Route:** count-transfer.

Historical side: **13.974090713121 → 13.970916436215**; reduction **0.00317428**.

Remove a 29-unit L-strip from Ostashev 211. Rounded pressure hardening/quench gives 182 at 13.971254466. A large kick, local melt/re-square and crossover lead to 13.970916436. Winning L-cut job≈0.5 CPU-hour inside 32 jobs/16 CPU-hours.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/806).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 183

Retained local side at the snapshot: **13.999580178749**. [Catalogue case and history](https://squaremath.org/cases/183.html).

### 1. Add to a worse but different 182 donor

**Proponent:** Evan Daniel. **Route:** count-transfer.

Historical side: **14.000000000000 → 13.999580178737**; reduction **0.000419821**.

An explorer descendant of Couzo 182 has side 13.990326 after 17 moves. Dilate 0.2–1.2% and insert into one of 12 largest holes, screening≈120 donors. More than 90% collapse to grid; this donor yields 183 at 14.0335 without a full axis line.40 minutes:angle swap+2 crossovers reach 13.9998051.12×40 minute refinements all reach 13.9995801787.

1. Insertion into the 182 record itself:120 seeds and 4 explorer runs never below 14.0135.
2. Crossover mate IDs were not logged.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/680).

## N 199

Retained local side at the snapshot: **14.617572173606**. [Catalogue case and history](https://squaremath.org/cases/199.html).

### 1. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **14.618988956899 → 14.617572173598**; reduction **0.00141678**.

Graft the catalogue's 37-square construction into 199

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 204

Retained local side at the snapshot: **14.807627471881**. [Catalogue case and history](https://squaremath.org/cases/204.html).

### 1. Improved rectangular primitive unlocks a composition

**Proponent:** Daniil Ostashev. **Route:** composition.

Historical side: **14.822875655532 → 14.808663234387**; reduction **0.0142124**.

Two new 44-square pieces plus 116 upright units.

1. 38 unit piece: random-start GPU soft-to-rigid, footprint(h+2)×h,h≈5.7641743175.
2. 44 unit piece: staircase + tilted-lattice start,h≈5.8086632344,width h+3.
3. 62 unit piece: staircase + tilted-lattice start,h≈5.9099582911,width h+6.
4. Use the appropriate piece, compose, then close the contact topology.

**Disclosure limits / controls:** Only the piece appropriate to this case is used; these remain composition examples rather than evidence all layouts are four rectangles.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/562).

### 2. Seed at 176, evolve at 204, then refill

**Proponent:** Evan Daniel. **Route:** quality-diversity.

Historical side: **14.808642830514 → 14.807627471882**; reduction **0.00101536**.

Ostashev 176 is seeded at 204. Nine explorer generations reach 14.807642,3 refill generations reach 14.807630; final corner-corner MILP kick/re-solve gives 14.807627472.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/845).

## N 206

Retained local side at the snapshot: **14.860158663406**. [Catalogue case and history](https://squaremath.org/cases/206.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 207

Retained local side at the snapshot: **14.880960371569**. [Catalogue case and history](https://squaremath.org/cases/207.html).

### 1. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **14.893954634237 → 14.887992258308**; reduction **0.00596238**.

Reuse the newly improved SQUISH 88 component

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(11) (8; `square-11_r1a.svg`) + our s(130) (whole; #401)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 3. Select boundary patches and reclose contact returns

**Proponent:** PingYou Ltd. **Route:** boundary-patches.

Historical side: **14.885506308842 → 14.880960373044**; reduction **0.00454594**.

Two differently placed/reflected patches of Xu 70 retain 60 and 69 whole squares; add upright grids 42 and 36. Exact count 207.

1. Keep complete unit squares, with their parent and ownership identities.
2. Choose compatible boundaries/contacts and solve their return condition.
3. Build and verify the complete rational witness.

**Disclosure limits / controls:** The package replays the finished construction but does not repeat the exploratory patch/owner selection or original floating solve.153 angle is explained by a degree 7 equation; 302 by 2 t³−3 t²−2 t+1=0. Neither is an optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/503).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 208

Retained local side at the snapshot: **14.924518772043**. [Catalogue case and history](https://squaremath.org/cases/208.html).

### 1. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **14.926534459699 → 14.924518772033**; reduction **0.00201569**.

Couzo 209 with one square removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 209

Retained local side at the snapshot: **14.946223226460**. [Catalogue case and history](https://squaremath.org/cases/209.html).

### 1. Original neighbouring-count search

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **14.953939011857 → 14.949617952202**; reduction **0.00432106**.

One of the original nine cases seeded from SQUISH neighbouring-count packings by adding/removing squares, then basin hopping and polish.

**Disclosure limits / controls:** This original statement does not identify the exact parent count for this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(155) (42; `sources/squish-s155-source.cert.json`) + our s(240) (47; `sources/squish-s240-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: nearby search, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 210

Retained local side at the snapshot: **14.973001116602**. [Catalogue case and history](https://squaremath.org/cases/210.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 211

Retained local side at the snapshot: **14.993549626313**. [Catalogue case and history](https://squaremath.org/cases/211.html).

### 1. Explicit V-band construction

**Proponent:** Daniil Ostashev. **Route:** explicit-band.

Historical side: **14.997960704967 → 14.996336721336**; reduction **0.00162398**.

Build a tilted V lattice first; an integer program chooses staircase-shaped upright corner blocks around it. This constructs the large-scale band instead of waiting for it to emerge from random positions.

1. Choose a band angle and geometry.
2. Fill around it with upright Young-diagram corner blocks.
3. Make squares soft; re-harden with the box held, then release/compress.
4. Polish and solve the contact system.

**Disclosure limits / controls:** Author says random global searches stall above about 130. Hardware model, seed count and exact winning parameter sequence are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/501), [source 2](https://github.com/dostashev/square-packing/blob/main/README.md), [source 3](https://ostashev.ai/square-packing/).

### 2. Release rectangular seams and re-harden the whole layout

**Proponent:** Daniil Ostashev. **Route:** junction-rehardening.

Historical side: **14.996336721336 → 14.993694186583**; reduction **0.00264253**.

Start from deWinter 211, solved by Daniel. The 48- and 25-body tilted bands merge into a V of 76.

1. Use jittered copies of the structured parent.
2. Soften every square, not just seam bodies; hold the box while hardening.
3. For V outcomes, seed another hardening round from that V.
4. Release/compress, polish and solve contacts.

**Disclosure limits / controls:** Author reports the same whole-layout step did not improve the identical-piece compositions 175,204,303. The slack in an unequal, nonbinding piece may matter; this is a hypothesis, not a theorem.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/575).

## N 227

Retained local side at the snapshot: **15.563625652340**. [Catalogue case and history](https://squaremath.org/cases/227.html).

### 1. Asymmetric staircase corners around slipped tilted ribbons

**Proponent:** Joost de Winter. **Route:** slipped-ribbon.

Historical side: **15.571067811865 → 15.563796703670**; reduction **0.00727111**.

Start from the public catalogue; search asymmetric Young-diagram corner fills around slipped tilted ribbons, then optimize centers by LP and restore nonlinear wall supports and angles.227,229,260 belong to one family; 229 descends from 260.

**Disclosure limits / controls:** The publication names the construction family and finishers but not a full winning seed/parameter trace.25 distinct model workers over one session, at most 6 concurrent, is reported; CPU/GPU time is not specified.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/668).

## N 228

Retained local side at the snapshot: **15.604601475744**. [Catalogue case and history](https://squaremath.org/cases/228.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 229

Retained local side at the snapshot: **15.650161513891**. [Catalogue case and history](https://squaremath.org/cases/229.html).

### 1. Asymmetric staircase corners around slipped tilted ribbons

**Proponent:** Joost de Winter. **Route:** slipped-ribbon.

Historical side: **15.656854249492 → 15.650174756949**; reduction **0.00667949**.

Start from the public catalogue; search asymmetric Young-diagram corner fills around slipped tilted ribbons, then optimize centers by LP and restore nonlinear wall supports and angles.227,229,260 belong to one family; 229 descends from 260.

**Disclosure limits / controls:** The publication names the construction family and finishers but not a full winning seed/parameter trace.25 distinct model workers over one session, at most 6 concurrent, is reported; CPU/GPU time is not specified.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/668).

## N 232

Retained local side at the snapshot: **15.761657943703**. [Catalogue case and history](https://squaremath.org/cases/232.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's s(5) (whole) + ry-xu's s(175) (162; #432, commit 8dc4152)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: nearby search, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. Improved rectangular primitive unlocks a composition

**Proponent:** Daniil Ostashev. **Route:** composition.

Historical side: **15.767428349942 → 15.764174317487**; reduction **0.00325403**.

New 38-square piece +76-square crop from Friedman 85 +118 upright units.

1. 38 unit piece: random-start GPU soft-to-rigid, footprint(h+2)×h,h≈5.7641743175.
2. 44 unit piece: staircase + tilted-lattice start,h≈5.8086632344,width h+3.
3. 62 unit piece: staircase + tilted-lattice start,h≈5.9099582911,width h+6.
4. Use the appropriate piece, compose, then close the contact topology.

**Disclosure limits / controls:** Only the piece appropriate to this case is used; these remain composition examples rather than evidence all layouts are four rectangles.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/528).

### 3. GPU basin hopping then native basin/SLP

**Proponent:** Francisco Couzo after Alex Chilton. **Route:** quality-diversity.

Historical side: **15.763381419802 → 15.761661759482**; reduction **0.00171966**.

Chilton’s public 15.763381419802 start.3 GPU improvements in≈2 minutes contribute 0.00051; 2 native basin/SLP improvements contribute 0.00121. Uses lightningv 08 overlap kernel and Danielfq for one polish. Tilted count 132→84.

**Disclosure limits / controls:** Couzo could not trace the notebook start further back; its original discovery is not identified.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/844).

## N 236

Retained local side at the snapshot: **15.861934390622**. [Catalogue case and history](https://squaremath.org/cases/236.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **15.872219025607 → 15.870013850516**; reduction **0.00220518**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **15.872219025607 → 15.867800839426**; reduction **0.00441819**.

Reuse the newly improved SQUISH 88 component

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

### 3. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(152) (34; `square-152_r2.svg`) + our s(88) (whole; #422)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 4. Rebuild known components, find a different minimum

**Proponent:** Evan Daniel. **Route:** quality-diversity.

Historical side: **15.863955747159 → 15.861934390608**; reduction **0.00202136**.

Rebuild SQUISH Mondrian from 34 units of catalogue 152 and SQUISH 88, initially side s(88)+6. Exact upright refill; 45 minutes one-core basin exploration beats the published composition instead of merely recovering it.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/659).

### 5. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 237

Retained local side at the snapshot: **15.902603638274**. [Catalogue case and history](https://squaremath.org/cases/237.html).

### 1. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **15.911191683002 → 15.903676235191**; reduction **0.00751545**.

Couzo 238 with one square removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 238

Retained local side at the snapshot: **15.924106785336**. [Catalogue case and history](https://squaremath.org/cases/238.html).

### 1. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **15.931725503591 → 15.926146857012**; reduction **0.00557865**.

SQUISH 239 with one square removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(305) (68, narrowed; `sources/squish-s305-source.cert.json`) + our s(154) (42, narrowed; `sources/squish-s154-b-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair, nearby search

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 239

Retained local side at the snapshot: **15.948443327315**. [Catalogue case and history](https://squaremath.org/cases/239.html).

### 1. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **15.953819333481 → 15.949313169729**; reduction **0.00450616**.

Couzo 210 component grafted into the target's catalogue layout

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(209) (57, narrowed; #401, as refined by Siddharth Gupta) + our s(240) (52, narrowed; `sources/squish-s240-b-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 240

Retained local side at the snapshot: **15.969685337546**. [Catalogue case and history](https://squaremath.org/cases/240.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 241

Retained local side at the snapshot: **15.987117095165**. [Catalogue case and history](https://squaremath.org/cases/241.html).

### 1. Release rectangular seams and re-harden the whole layout

**Proponent:** Daniil Ostashev. **Route:** junction-rehardening.

Historical side: **15.988132439525 → 15.987134249051**; reduction **0.00099819**.

Start from Couzo 241, solved by Daniel. Bands of 47 and 32 merge into a V of 85.

1. Use jittered copies of the structured parent.
2. Soften every square, not just seam bodies; hold the box while hardening.
3. For V outcomes, seed another hardening round from that V.
4. Release/compress, polish and solve contacts.

**Disclosure limits / controls:** Author reports the same whole-layout step did not improve the identical-piece compositions 175,204,303. The slack in an unequal, nonbinding piece may matter; this is a hypothesis, not a theorem.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/575).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 258

Retained local side at the snapshot: **16.563448002149**. [Catalogue case and history](https://squaremath.org/cases/258.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **16.571067811865 → 16.563973475317**; reduction **0.00709434**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **16.571067811865 → 16.563448002139**; reduction **0.00761981**.

Couzo 259 with one square removed

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

## N 259

Retained local side at the snapshot: **16.591378145513**. [Catalogue case and history](https://squaremath.org/cases/259.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(50) (36; `square-50_r5.svg`) + ry-xu's s(123) (90; #432, commit 8dc4152)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 260

Retained local side at the snapshot: **16.633982502121**. [Catalogue case and history](https://squaremath.org/cases/260.html).

### 1. Improve a large donor island, crop it back

**Proponent:** Evan Daniel. **Route:** ruin-recreate.

Historical side: **16.637029558871 → 16.633982502122**; reduction **0.00304706**.

Use kirilltym 260 as donor in a 405 fault composition.15 generations at 405 remove line/disc regions, refill and relax. The≈100 body island improves:tilt 24.08→24.51 degrees, with≈15 slightly tilted transition bodies. Compose that island back into 260.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/845).

### 2. One strip/grid structural opening then long SLP descent

**Proponent:** Francisco Couzo after ntumlnoob. **Route:** ruin-recreate.

Historical side: **16.638533455862 → 16.637029558871**; reduction **0.0015039**.

From public 16.638533455862:one Ellsworth-style grid-snap/strip-shift cycle opens≈0.00029 side; 199 SLP updates contribute≈0.00121; 5 fq updates≈9.4e-7.134 bodies move>0.1.

**Disclosure limits / controls:** Notebook says cpu_refine_fq_only and its parent is unpublished. Exact winning structural-cycle knobs are not disclosed.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/844).

### 3. Asymmetric staircase corners around slipped tilted ribbons

**Proponent:** Joost de Winter. **Route:** slipped-ribbon.

Historical side: **16.656854249492 → 16.645778804182**; reduction **0.0110754**.

Start from the public catalogue; search asymmetric Young-diagram corner fills around slipped tilted ribbons, then optimize centers by LP and restore nonlinear wall supports and angles.227,229,260 belong to one family; 229 descends from 260.

**Disclosure limits / controls:** The publication names the construction family and finishers but not a full winning seed/parameter trace.25 distinct model workers over one session, at most 6 concurrent, is reported; CPU/GPU time is not specified.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/668).

## N 261

Retained local side at the snapshot: **16.678779875359**. [Catalogue case and history](https://squaremath.org/cases/261.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **16.682926829268 → 16.678779875417**; reduction **0.00414695**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

## N 263

Retained local side at the snapshot: **16.733166007915**. [Catalogue case and history](https://squaremath.org/cases/263.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **16.742270262025 → 16.740623426617**; reduction **0.00164684**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

### 2. Cross-count surgery and basin hopping

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **16.742270262025 → 16.740446480043**; reduction **0.00182378**.

Couzo 297 carved down to 263

1. Build the altered-count or grafted seed.
2. Run basin hopping / nearby search and polish.

**Disclosure limits / controls:** Removed square IDs, graft-interface choices and the full nearby-search implementation are not disclosed.120 later tiny perturbation/polish trials gave no >1e-11 gain.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401#issuecomment-6043191866).

### 3. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **16.742270262025 → 16.740419679539**; reduction **0.00185058**.

Carve Couzo 297 down to 263, nearby search, then squeeze

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

### 4. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's s(5) (whole) + its former s(202) (188; `square-202_r3.svg`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 5. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 264

Retained local side at the snapshot: **16.774735132404**. [Catalogue case and history](https://squaremath.org/cases/264.html).

### 1. Improved rectangular primitive unlocks a composition

**Proponent:** Daniil Ostashev. **Route:** composition.

Historical side: **16.778174593052 → 16.774735132388**; reduction **0.00343946**.

New 38-square piece +93-square crop from deWinter 126 +133 upright units. The 93-square piece sets the final side; the 38-square improvement unlocks compatibility.

1. 38 unit piece: random-start GPU soft-to-rigid, footprint(h+2)×h,h≈5.7641743175.
2. 44 unit piece: staircase + tilted-lattice start,h≈5.8086632344,width h+3.
3. 62 unit piece: staircase + tilted-lattice start,h≈5.9099582911,width h+6.
4. Use the appropriate piece, compose, then close the contact topology.

**Disclosure limits / controls:** Only the piece appropriate to this case is used; these remain composition examples rather than evidence all layouts are four rectangles.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/528).

## N 267

Retained local side at the snapshot: **16.838815269964**. [Catalogue case and history](https://squaremath.org/cases/267.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **16.846667192843 → 16.838831961117**; reduction **0.00783523**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

## N 268

Retained local side at the snapshot: **16.874361715873**. [Catalogue case and history](https://squaremath.org/cases/268.html).

### 1. Original discovery trail partly missing

**Proponent:** Public Kaggle lineage / subsequent certifiers. **Route:** undisclosed.

Public lightningv 08/Kirill layouts later certified/refined by Couzo and Daniel. Exact starting seed/operator for the main Kaggle geometry is not established in the reviewed record.

**Disclosure limits / controls:** Do not infer the original method from the later notebook title, kernel, or certificate.

**Sources:** [source 1](https://squaremath.org/result/t-240.html).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 269

Retained local side at the snapshot: **16.901513582205**. [Catalogue case and history](https://squaremath.org/cases/269.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(11) (8; `square-11_r1a.svg`) + Francisco Couzo's s(180) (whole; #451, commit ffd900d)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: nearby search, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 270

Retained local side at the snapshot: **16.928162252213**. [Catalogue case and history](https://squaremath.org/cases/270.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(209) (two pieces, 57 and 62; #401)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: nearby search, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(209) (whole; #481) + the Kingbird catalogue's former s(19) (3, narrowed; `square-19_r1.svg`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair, nearby search

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 3. Explore diverse nonrecord descendants

**Proponent:** Evan Daniel. **Route:** quality-diversity.

Reported resulting side: **16.928162252197**.

Start from SQUISH 500. Keep 8 generations, including a state 0.0092 above record. From 1069 stored 270 s choose 24 fingerprint-diverse starts 0.001–0.01 above best. Four 40 minute one-core runs make 1357 new nonrecords. Winning 5 move chain:kick,row slide,L-kick,2 crossovers; found 38 minutes in.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/703).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 271

Retained local side at the snapshot: **16.948947733730**. [Catalogue case and history](https://squaremath.org/cases/271.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(305) (68, narrowed; `sources/squish-s305-source.cert.json`) + our s(240) (47; #481 `sources/squish-s240-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair, nearby search

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 2. Single neighbouring tilt-angle swap

**Proponent:** Evan Daniel. **Route:** local-new-minimum.

Reported resulting side: **16.948947733714**.

From Couzo’s descendant of SQUISH 500, one neighbouring angle swap followed by polish wins after 90 seconds. Small new basin, not a major new construction.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/664).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 272

Retained local side at the snapshot: **16.965586474854**. [Catalogue case and history](https://squaremath.org/cases/272.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(240) (63; #481 `sources/squish-s240-source.cert.json`) + the Kingbird catalogue's former s(182) (58, narrowed; `square-182_r1.svg`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 273

Retained local side at the snapshot: **16.983925962666**. [Catalogue case and history](https://squaremath.org/cases/273.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 292

Retained local side at the snapshot: **17.591378145514**. [Catalogue case and history](https://squaremath.org/cases/292.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(50) (43; `square-50_r5.svg`) + ry-xu's s(123) (90; #432, commit 8dc4152)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 293

Retained local side at the snapshot: **17.633982502139**. [Catalogue case and history](https://squaremath.org/cases/293.html).

### 1. Transfer improved 260 with an L-shaped wrapper

**Proponent:** Evan Daniel. **Route:** count-transfer.

Historical side: **17.634146341464 → 17.633982502123**; reduction **0.000163839**.

Use the improved 260 island plus a 33-unit L-strip:260+2×16+1=293. Side rises by 1. Discovery happened in the 405 search, not a fresh 293 search.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/845).

## N 295

Retained local side at the snapshot: **17.704232790753**. [Catalogue case and history](https://squaremath.org/cases/295.html).

### 1. New geometry from evolved packing programs

**Proponent:** Ryan Xu. **Route:** program-evolution.

Historical side: **17.707106781186 → 17.704232791518**; reduction **0.00287399**.

Random shrink/shake/relax baseline with L-BFGS; 128 generations of program mutation. The population later evolved structured staircase/diagonal initializations, rational-slope angles, round/sharpen cycles, directional motion, hole relocation and selectively frozen structures.

1. Mutate packing algorithms, rather than only the coordinates.
2. Score programs against a sample of n; keep and diversify competitive programs.
3. Increase per-run time from 10 to 60 seconds when larger n time out; eventually 64 candidates/generation.

**Disclosure limits / controls:** Shared campaign:2 days,7,500 CPU-hours,$125 reported tokens. No published per-n winning-program/seed log; cannot attribute a particular move to this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/432), [source 2](https://slightlysupervised.substack.com/p/improving-25-square-packing-upper).

## N 297

Retained local side at the snapshot: **17.740417287561**. [Catalogue case and history](https://squaremath.org/cases/297.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 299

Retained local side at the snapshot: **17.801238549389**. [Catalogue case and history](https://squaremath.org/cases/299.html).

### 1. Fault-line pieces from 334→373, then recomposition

**Proponent:** Evan Daniel. **Route:** fault-line.

Historical side: **17.822875655533 → 17.803695435332**; reduction **0.0191802**.

Deotte 334 from public FTMC notebook relaxes 18.795715128→18.791043283. Add an L of 39 to reach 373 and search to 19.803695435. Crop a 78 body corner gadget from 373 and combine with an earlier 299 gadget along a diagonal fault between two shifted upright grids.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/824).

### 2. Four generations of line/disc refill

**Proponent:** Evan Daniel. **Route:** ruin-recreate.

Historical side: **17.803695435332 → 17.801238549389**; reduction **0.00245689**.

Starting from the preceding fault-line 299,4 generations remove a line/disc of bodies, replace them and relax:17.803695→17.801240. Exact MILP descent/re-solve takes only the last≈0.00000145 off.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/824).

## N 301

Retained local side at the snapshot: **17.846667192860**. [Catalogue case and history](https://squaremath.org/cases/301.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 302

Retained local side at the snapshot: **17.870013850421**. [Catalogue case and history](https://squaremath.org/cases/302.html).

### 1. Component replacement / carving update

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **17.885993892530 → 17.881306218096**; reduction **0.00468767**.

Reuse the newly improved SQUISH 88 component

**Disclosure limits / controls:** The successful 88 component itself came from updating the catalogue 88 with its newer 41-square core. Exact graft decisions are not published.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/422).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(152) (34; `square-152_r2.svg`) + ry-xu's s(129) (118; #432, commit 8dc4152)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 3. Select boundary patches and reclose contact returns

**Proponent:** PingYou Ltd. **Route:** boundary-patches.

Historical side: **17.872029849081 → 17.870275382734**; reduction **0.00175447**.

Four boundary patches of Xu 70 retain 16,9,9,16 units; add upright banks 105 and 147. Six source regions rather than two intact rectangular motifs. Final 254 upright+24+24 tilted.

1. Keep complete unit squares, with their parent and ownership identities.
2. Choose compatible boundaries/contacts and solve their return condition.
3. Build and verify the complete rational witness.

**Disclosure limits / controls:** The package replays the finished construction but does not repeat the exploratory patch/owner selection or original floating solve.153 angle is explained by a degree 7 equation; 302 by 2 t³−3 t²−2 t+1=0. Neither is an optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/564).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 303

Retained local side at the snapshot: **17.906978233799**. [Catalogue case and history](https://squaremath.org/cases/303.html).

### 1. Original neighbouring-count search

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** count-transfer.

Historical side: **17.924341009851 → 17.920312372920**; reduction **0.00402864**.

One of the original nine cases seeded from SQUISH neighbouring-count packings by adding/removing squares, then basin hopping and polish.

**Disclosure limits / controls:** This original statement does not identify the exact parent count for this n.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/401).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(11) (8; `square-11_r1a.svg`) + our s(208) (whole; #401)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: nearby search, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 3. Improved rectangular primitive unlocks a composition

**Proponent:** Daniil Ostashev. **Route:** composition.

Historical side: **17.913065462739 → 17.909958291070**; reduction **0.00310717**.

Two new 62-square pieces plus 179 upright units.

1. 38 unit piece: random-start GPU soft-to-rigid, footprint(h+2)×h,h≈5.7641743175.
2. 44 unit piece: staircase + tilted-lattice start,h≈5.8086632344,width h+3.
3. 62 unit piece: staircase + tilted-lattice start,h≈5.9099582911,width h+6.
4. Use the appropriate piece, compose, then close the contact topology.

**Disclosure limits / controls:** Only the piece appropriate to this case is used; these remain composition examples rather than evidence all layouts are four rectangles.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/562).

### 4. Flip a whole tilted band after a long lineage

**Proponent:** Evan Daniel. **Route:** band-flip.

Historical side: **17.909958291070 → 17.909772217275**; reduction **0.000186074**.

From Ostashev 303 keep 14 generations of nonrecords. Two later sweeps use crossovers and junction/band moves. Final 7 move chain includes uphill kicks,row slide,L-kick,symmetric kick,crossover,then reflect one tilted band along its wall:tilt sign flips and ends exchange.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/728).

### 5. Original discovery trail partly missing

**Proponent:** Public Kaggle lineage / subsequent certifiers. **Route:** undisclosed.

The later smaller Lavrentev public arrangement supersedes the Ostashev/Daniel branch. Donor lineage of the original CUDA output is not fully published.

**Disclosure limits / controls:** Do not infer the original method from the later notebook title, kernel, or certificate.

**Sources:** [source 1](https://squaremath.org/result/t-240.html).

### 6. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 304

Retained local side at the snapshot: **17.926898900360**. [Catalogue case and history](https://squaremath.org/cases/304.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(209) (whole; #481) + the Kingbird catalogue's former s(11) (8, narrowed; `square-11_r1a.svg`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 2. Release rectangular seams and re-harden the whole layout

**Proponent:** Daniil Ostashev. **Route:** junction-rehardening.

Historical side: **17.929565946848 → 17.929427758075**; reduction **0.000138189**.

Start from a 55+68 rectangle composition plus 181 upright units at 17.939518. Upright blocks and seams relax; the two bands remain separate, with no V.

1. Use jittered copies of the structured parent.
2. Soften every square, not just seam bodies; hold the box while hardening.
3. For V outcomes, seed another hardening round from that V.
4. Release/compress, polish and solve contacts.

**Disclosure limits / controls:** Author reports the same whole-layout step did not improve the identical-piece compositions 175,204,303. The slack in an unequal, nonbinding piece may matter; this is a hypothesis, not a theorem.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/575).

### 3. Original discovery trail partly missing

**Proponent:** Public Kaggle lineage / subsequent certifiers. **Route:** undisclosed.

The later 17.9268989 public geometry appears in kozykappa/Kirill outputs. Original finder and parent remain disputed/undocumented in T-241/T-242; certification is not discovery credit.

**Disclosure limits / controls:** Do not infer the original method from the later notebook title, kernel, or certificate.

**Sources:** [source 1](https://squaremath.org/result/t-242.html).

### 4. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 305

Retained local side at the snapshot: **17.950466482155**. [Catalogue case and history](https://squaremath.org/cases/305.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(209) (57; #401) + our s(306) (81; `sources/squish-s306-source.cert.json`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: nearby search, squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

our s(272) (two pieces of 63, narrowed; `sources/squish-s272-source.cert.json`, the 272 here before its squeeze)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: seam repair, nearby search

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings. Each result received 1 hour nearby search plus a deep squeeze; none gained more than7e-7 in that final check.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/500).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 306

Retained local side at the snapshot: **17.963433717508**. [Catalogue case and history](https://squaremath.org/cases/306.html).

### 1. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 307

Retained local side at the snapshot: **17.979249693611**. [Catalogue case and history](https://squaremath.org/cases/307.html).

### 1. Mondrian: cropped and narrowed components

**Proponent:** Nate Chaoweeraprasit / SQUISH. **Route:** composition.

the Kingbird catalogue's former s(241) (two pieces, 64 and 69; `square-241_r3.svg`)

1. Crop the named pieces; for issue 500, narrow the indicated pieces in their own rectangles first.
2. Place components, fill the remaining integer rows/columns.
3. After composition: squeeze

**Disclosure limits / controls:** The source describes the pieces and resulting certificate, but not all seam-repair/nearby-search settings.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/481).

### 2. Original discovery trail partly missing

**Proponent:** Public Kaggle lineage / subsequent certifiers. **Route:** undisclosed.

ntumlnoob publishes 17.979253973651 but labels it cpu_refine_fq_only of an unpublished parent. Subsequent Couzo gain≈2.7e-6 is not the main discovery.

**Disclosure limits / controls:** Do not infer the original method from the later notebook title, kernel, or certificate.

**Sources:** [source 1](https://squaremath.org/result/t-255.html).

### 3. September 49-case release: geometry, but method undisclosed

**Proponent:** Francisco Couzo. **Route:** undisclosed.

This count belongs to the 49-case September 27 publication. The retained release supplies improved arrangements and certificates, not a per-case discovery algorithm.

**Disclosure limits / controls:** Later fq/SLP/browser code does not establish which search found the September packing.

**Sources:** [source 1](https://squaremath.org/result/t-056.html), [source 2](https://github.com/franciscouzo/square-packing).

## N 308

Retained local side at the snapshot: **17.997149121288**. [Catalogue case and history](https://squaremath.org/cases/308.html).

### 1. 307 insertion, diverse restarts, mirror/kick sequence

**Proponent:** Evan Daniel. **Route:** count-transfer.

Historical side: **17.999309855163 → 17.997149121271**; reduction **0.00216073**.

Insert 1 into SQUISH 307. Five rounds of crossover/tilt/symmetric kicks find sub 18 states. Restart from 6 fingerprint-diverse 308 s, not just best. Five symmetric kicks, a kick and mirror move find 17.997149 at 710 seconds.12×40 minute followups stay there.

**Disclosure limits / controls:** Author-reported move lineage; not independently rerun here. Exact numerical local-stationarity evidence is not a global optimality proof.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/689).

### 2. Extend the two-wedge family and fit an extra square

**Proponent:** Kevin Fang. **Route:** explicit-band.

Historical side: **18.000000000000 → 17.999309855163**; reduction **0.000690145**.

Starting geometry comes from the Arslanov–Mustafin–Shangitbayev two-wedge family and Ellsworth/Stead 241,273,307 seeds. Extension reaches 308 below 18, one beyond 18²−18+1.

**Disclosure limits / controls:** Primary submission gives the family/seeds but not a complete winning search trace.

**Sources:** [source 1](https://github.com/jlevy/squares/issues/484).

## Complete N=100–324 index

The side column is our retained portfolio at the report date. “Grid baseline” does not assert optimality. “No substantial route established” refers only to this research coverage.

| N | Retained side | Discovery coverage | Catalogue |
|---:|---:|---|---|
| 100 | 10.000000000000 | Grid baseline | [case](https://squaremath.org/cases/100.html) |
| 101 | 10.535533906028 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/101.html) |
| 102 | 10.605828696528 | [2 history entries](#n-102) | [case](https://squaremath.org/cases/102.html) |
| 103 | 10.679232047458 | [2 history entries](#n-103) | [case](https://squaremath.org/cases/103.html) |
| 104 | 10.707106781284 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/104.html) |
| 105 | 10.789303783743 | [2 history entries](#n-105) | [case](https://squaremath.org/cases/105.html) |
| 106 | 10.822908044231 | [1 history entries](#n-106) | [case](https://squaremath.org/cases/106.html) |
| 107 | 10.846667192942 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/107.html) |
| 108 | 10.904821012419 | [3 history entries](#n-108) | [case](https://squaremath.org/cases/108.html) |
| 109 | 10.949747468405 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/109.html) |
| 110 | 10.996783396732 | [1 history entries](#n-110) | [case](https://squaremath.org/cases/110.html) |
| 111 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/111.html) |
| 112 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/112.html) |
| 113 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/113.html) |
| 114 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/114.html) |
| 115 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/115.html) |
| 116 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/116.html) |
| 117 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/117.html) |
| 118 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/118.html) |
| 119 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/119.html) |
| 120 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/120.html) |
| 121 | 11.000000000000 | Grid baseline | [case](https://squaremath.org/cases/121.html) |
| 122 | 11.535533905933 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/122.html) |
| 123 | 11.591378145498 | [3 history entries](#n-123) | [case](https://squaremath.org/cases/123.html) |
| 124 | 11.656854249492 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/124.html) |
| 125 | 11.707106781187 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/125.html) |
| 126 | 11.742640687119 | [2 history entries](#n-126) | [case](https://squaremath.org/cases/126.html) |
| 127 | 11.810878787589 | [1 history entries](#n-127) | [case](https://squaremath.org/cases/127.html) |
| 128 | 11.825091968214 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/128.html) |
| 129 | 11.870013850404 | [3 history entries](#n-129) | [case](https://squaremath.org/cases/129.html) |
| 130 | 11.902430645982 | [4 history entries](#n-130) | [case](https://squaremath.org/cases/130.html) |
| 131 | 11.949659588036 | [3 history entries](#n-131) | [case](https://squaremath.org/cases/131.html) |
| 132 | 11.985680198846 | [2 history entries](#n-132) | [case](https://squaremath.org/cases/132.html) |
| 133 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/133.html) |
| 134 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/134.html) |
| 135 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/135.html) |
| 136 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/136.html) |
| 137 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/137.html) |
| 138 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/138.html) |
| 139 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/139.html) |
| 140 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/140.html) |
| 141 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/141.html) |
| 142 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/142.html) |
| 143 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/143.html) |
| 144 | 12.000000000000 | Grid baseline | [case](https://squaremath.org/cases/144.html) |
| 145 | 12.535533905944 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/145.html) |
| 146 | 12.583782190163 | [2 history entries](#n-146) | [case](https://squaremath.org/cases/146.html) |
| 147 | 12.656854249504 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/147.html) |
| 148 | 12.656854249504 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/148.html) |
| 149 | 12.707106781198 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/149.html) |
| 150 | 12.778174593064 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/150.html) |
| 151 | 12.822875655544 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/151.html) |
| 152 | 12.830718800988 | [1 history entries](#n-152) | [case](https://squaremath.org/cases/152.html) |
| 153 | 12.870013850416 | [4 history entries](#n-153) | [case](https://squaremath.org/cases/153.html) |
| 154 | 12.921100940774 | [4 history entries](#n-154) | [case](https://squaremath.org/cases/154.html) |
| 155 | 12.952260944663 | [4 history entries](#n-155) | [case](https://squaremath.org/cases/155.html) |
| 156 | 12.979165853846 | [2 history entries](#n-156) | [case](https://squaremath.org/cases/156.html) |
| 157 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/157.html) |
| 158 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/158.html) |
| 159 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/159.html) |
| 160 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/160.html) |
| 161 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/161.html) |
| 162 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/162.html) |
| 163 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/163.html) |
| 164 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/164.html) |
| 165 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/165.html) |
| 166 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/166.html) |
| 167 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/167.html) |
| 168 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/168.html) |
| 169 | 13.000000000000 | Grid baseline | [case](https://squaremath.org/cases/169.html) |
| 170 | 13.535533905945 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/170.html) |
| 171 | 13.571428571441 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/171.html) |
| 172 | 13.617935698381 | [2 history entries](#n-172) | [case](https://squaremath.org/cases/172.html) |
| 173 | 13.656854249505 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/173.html) |
| 174 | 13.707106781199 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/174.html) |
| 175 | 13.764174317499 | [2 history entries](#n-175) | [case](https://squaremath.org/cases/175.html) |
| 176 | 13.795872318449 | [2 history entries](#n-176) | [case](https://squaremath.org/cases/176.html) |
| 177 | 13.822979734182 | [1 history entries](#n-177) | [case](https://squaremath.org/cases/177.html) |
| 178 | 13.846667192856 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/178.html) |
| 179 | 13.883795490524 | [3 history entries](#n-179) | [case](https://squaremath.org/cases/179.html) |
| 180 | 13.916993522491 | [3 history entries](#n-180) | [case](https://squaremath.org/cases/180.html) |
| 181 | 13.950819531036 | [2 history entries](#n-181) | [case](https://squaremath.org/cases/181.html) |
| 182 | 13.970916436215 | [2 history entries](#n-182) | [case](https://squaremath.org/cases/182.html) |
| 183 | 13.999580178749 | [1 history entries](#n-183) | [case](https://squaremath.org/cases/183.html) |
| 184 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/184.html) |
| 185 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/185.html) |
| 186 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/186.html) |
| 187 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/187.html) |
| 188 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/188.html) |
| 189 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/189.html) |
| 190 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/190.html) |
| 191 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/191.html) |
| 192 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/192.html) |
| 193 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/193.html) |
| 194 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/194.html) |
| 195 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/195.html) |
| 196 | 14.000000000000 | Grid baseline | [case](https://squaremath.org/cases/196.html) |
| 197 | 14.535533905946 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/197.html) |
| 198 | 14.571428571442 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/198.html) |
| 199 | 14.617572173606 | [2 history entries](#n-199) | [case](https://squaremath.org/cases/199.html) |
| 200 | 14.656854249506 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/200.html) |
| 201 | 14.707106781200 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/201.html) |
| 202 | 14.727922061372 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/202.html) |
| 203 | 14.778174593066 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/203.html) |
| 204 | 14.807627471881 | [2 history entries](#n-204) | [case](https://squaremath.org/cases/204.html) |
| 205 | 14.824451146138 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/205.html) |
| 206 | 14.860158663406 | [1 history entries](#n-206) | [case](https://squaremath.org/cases/206.html) |
| 207 | 14.880960371569 | [4 history entries](#n-207) | [case](https://squaremath.org/cases/207.html) |
| 208 | 14.924518772043 | [2 history entries](#n-208) | [case](https://squaremath.org/cases/208.html) |
| 209 | 14.946223226460 | [3 history entries](#n-209) | [case](https://squaremath.org/cases/209.html) |
| 210 | 14.973001116602 | [1 history entries](#n-210) | [case](https://squaremath.org/cases/210.html) |
| 211 | 14.993549626313 | [2 history entries](#n-211) | [case](https://squaremath.org/cases/211.html) |
| 212 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/212.html) |
| 213 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/213.html) |
| 214 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/214.html) |
| 215 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/215.html) |
| 216 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/216.html) |
| 217 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/217.html) |
| 218 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/218.html) |
| 219 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/219.html) |
| 220 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/220.html) |
| 221 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/221.html) |
| 222 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/222.html) |
| 223 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/223.html) |
| 224 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/224.html) |
| 225 | 15.000000000000 | Grid baseline | [case](https://squaremath.org/cases/225.html) |
| 226 | 15.535533905947 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/226.html) |
| 227 | 15.563625652340 | [1 history entries](#n-227) | [case](https://squaremath.org/cases/227.html) |
| 228 | 15.604601475744 | [1 history entries](#n-228) | [case](https://squaremath.org/cases/228.html) |
| 229 | 15.650161513891 | [1 history entries](#n-229) | [case](https://squaremath.org/cases/229.html) |
| 230 | 15.682926829283 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/230.html) |
| 231 | 15.707106781201 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/231.html) |
| 232 | 15.761657943703 | [3 history entries](#n-232) | [case](https://squaremath.org/cases/232.html) |
| 233 | 15.778174593067 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/233.html) |
| 234 | 15.822875655547 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/234.html) |
| 235 | 15.826605633443 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/235.html) |
| 236 | 15.861934390622 | [5 history entries](#n-236) | [case](https://squaremath.org/cases/236.html) |
| 237 | 15.902603638274 | [2 history entries](#n-237) | [case](https://squaremath.org/cases/237.html) |
| 238 | 15.924106785336 | [3 history entries](#n-238) | [case](https://squaremath.org/cases/238.html) |
| 239 | 15.948443327315 | [3 history entries](#n-239) | [case](https://squaremath.org/cases/239.html) |
| 240 | 15.969685337546 | [1 history entries](#n-240) | [case](https://squaremath.org/cases/240.html) |
| 241 | 15.987117095165 | [2 history entries](#n-241) | [case](https://squaremath.org/cases/241.html) |
| 242 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/242.html) |
| 243 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/243.html) |
| 244 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/244.html) |
| 245 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/245.html) |
| 246 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/246.html) |
| 247 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/247.html) |
| 248 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/248.html) |
| 249 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/249.html) |
| 250 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/250.html) |
| 251 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/251.html) |
| 252 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/252.html) |
| 253 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/253.html) |
| 254 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/254.html) |
| 255 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/255.html) |
| 256 | 16.000000000000 | Grid baseline | [case](https://squaremath.org/cases/256.html) |
| 257 | 16.535533905948 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/257.html) |
| 258 | 16.563448002149 | [2 history entries](#n-258) | [case](https://squaremath.org/cases/258.html) |
| 259 | 16.591378145513 | [2 history entries](#n-259) | [case](https://squaremath.org/cases/259.html) |
| 260 | 16.633982502121 | [3 history entries](#n-260) | [case](https://squaremath.org/cases/260.html) |
| 261 | 16.678779875359 | [1 history entries](#n-261) | [case](https://squaremath.org/cases/261.html) |
| 262 | 16.707106781202 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/262.html) |
| 263 | 16.733166007915 | [5 history entries](#n-263) | [case](https://squaremath.org/cases/263.html) |
| 264 | 16.774735132404 | [1 history entries](#n-264) | [case](https://squaremath.org/cases/264.html) |
| 265 | 16.778174593068 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/265.html) |
| 266 | 16.823028750772 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/266.html) |
| 267 | 16.838815269964 | [1 history entries](#n-267) | [case](https://squaremath.org/cases/267.html) |
| 268 | 16.874361715873 | [2 history entries](#n-268) | [case](https://squaremath.org/cases/268.html) |
| 269 | 16.901513582205 | [2 history entries](#n-269) | [case](https://squaremath.org/cases/269.html) |
| 270 | 16.928162252213 | [4 history entries](#n-270) | [case](https://squaremath.org/cases/270.html) |
| 271 | 16.948947733730 | [3 history entries](#n-271) | [case](https://squaremath.org/cases/271.html) |
| 272 | 16.965586474854 | [2 history entries](#n-272) | [case](https://squaremath.org/cases/272.html) |
| 273 | 16.983925962666 | [1 history entries](#n-273) | [case](https://squaremath.org/cases/273.html) |
| 274 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/274.html) |
| 275 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/275.html) |
| 276 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/276.html) |
| 277 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/277.html) |
| 278 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/278.html) |
| 279 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/279.html) |
| 280 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/280.html) |
| 281 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/281.html) |
| 282 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/282.html) |
| 283 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/283.html) |
| 284 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/284.html) |
| 285 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/285.html) |
| 286 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/286.html) |
| 287 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/287.html) |
| 288 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/288.html) |
| 289 | 17.000000000000 | Grid baseline | [case](https://squaremath.org/cases/289.html) |
| 290 | 17.535533905949 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/290.html) |
| 291 | 17.535533905949 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/291.html) |
| 292 | 17.591378145514 | [2 history entries](#n-292) | [case](https://squaremath.org/cases/292.html) |
| 293 | 17.633982502139 | [1 history entries](#n-293) | [case](https://squaremath.org/cases/293.html) |
| 294 | 17.656854249509 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/294.html) |
| 295 | 17.704232790753 | [1 history entries](#n-295) | [case](https://squaremath.org/cases/295.html) |
| 296 | 17.707106781203 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/296.html) |
| 297 | 17.740417287561 | [1 history entries](#n-297) | [case](https://squaremath.org/cases/297.html) |
| 298 | 17.778174593069 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/298.html) |
| 299 | 17.801238549389 | [2 history entries](#n-299) | [case](https://squaremath.org/cases/299.html) |
| 300 | 17.824123388495 | Older nontrivial packing; no substantial route established | [case](https://squaremath.org/cases/300.html) |
| 301 | 17.846667192860 | [1 history entries](#n-301) | [case](https://squaremath.org/cases/301.html) |
| 302 | 17.870013850421 | [4 history entries](#n-302) | [case](https://squaremath.org/cases/302.html) |
| 303 | 17.906978233799 | [6 history entries](#n-303) | [case](https://squaremath.org/cases/303.html) |
| 304 | 17.926898900360 | [4 history entries](#n-304) | [case](https://squaremath.org/cases/304.html) |
| 305 | 17.950466482155 | [3 history entries](#n-305) | [case](https://squaremath.org/cases/305.html) |
| 306 | 17.963433717508 | [1 history entries](#n-306) | [case](https://squaremath.org/cases/306.html) |
| 307 | 17.979249693611 | [3 history entries](#n-307) | [case](https://squaremath.org/cases/307.html) |
| 308 | 17.997149121288 | [2 history entries](#n-308) | [case](https://squaremath.org/cases/308.html) |
| 309 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/309.html) |
| 310 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/310.html) |
| 311 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/311.html) |
| 312 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/312.html) |
| 313 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/313.html) |
| 314 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/314.html) |
| 315 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/315.html) |
| 316 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/316.html) |
| 317 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/317.html) |
| 318 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/318.html) |
| 319 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/319.html) |
| 320 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/320.html) |
| 321 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/321.html) |
| 322 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/322.html) |
| 323 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/323.html) |
| 324 | 18.000000000000 | Grid baseline | [case](https://squaremath.org/cases/324.html) |

## Other primary and review sources

- [Squares Project result register](https://squaremath.org/results.html).
- [Ostashev’s illustrated write-up](https://ostashev.ai/square-packing/).
- [Ostashev’s original README](https://github.com/dostashev/square-packing/blob/main/README.md).
- [SQUISH original release](https://github.com/jlevy/squares/issues/401), [grafting/carving update](https://github.com/jlevy/squares/issues/422), [Mondrian component table](https://github.com/jlevy/squares/issues/481), [narrowing and interlocking](https://github.com/jlevy/squares/issues/500).
- [Joost de Winter’s slipped-ribbon family](https://github.com/jlevy/squares/issues/668).

## Proof-status correction

A separate earlier local annotation marked 778 rectangular motifs optimal using a corollary of Nagamochi’s 2005 rectangle theorem. The published theorem depends on a lemma with a known counterexample; its full-strength conclusion is unproved, not disproved. Those 778 badges were withdrawn, leaving 199 independently supported attained-bound indicators. No packing coordinates or certified score changed.

Reference: [correction record T-085](https://squaremath.org/result/t-085.html).
