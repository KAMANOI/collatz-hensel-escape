# Hensel Memory and the 2-adic Escape Target

**Paper O — Divergence as 2-adic Convergence to −3⁻¹ and Archimedean Escape to Infinity**

Proves that arithmetic "memory" in Collatz height record sequences is not a failure of mixing but an algebraic consequence of Hensel's lifting lemma. Reformulates the Collatz conjecture as the impossibility of a 2-adic escape pair.

> This repository does not claim a proof of the Collatz conjecture.

---

## Erratum (2026-11-12)

- **Theorem 4.2 is conditional, not proved.** The PDF itself lists it as "Proved (conditional)": it assumes that every orbit with unbounded a_t has infinitely many gate-1 records, and gate-2 records are left open. The table below previously said "proved".
- The direction "no escape pair implies Collatz" also invokes Theorem Monotonicity (Paper M), whose "each height once" part is false (see the erratum of the series summary), and it does not address nontrivial cycles.
- Unaffected: the Hensel nesting lemma and Theorem HMC parts (a) and (c).

The PDF in `paper/` is the original, uncorrected version.

---

## Overview

Gate-1 synchronization targets r_K = −3⁻¹ mod 2^K form a nested Cauchy sequence in ℤ₂ converging to r_∞ = −3⁻¹. If a Collatz orbit achieves infinitely many gate-1 height records with Kᵢ → ∞, the odd-core values must simultaneously converge 2-adically to −3⁻¹ and diverge in ℝ — a "2-adic escape pair."

The central results are:

- **Theorem HMC** (Hensel Memory Compatibility): If an orbit has infinitely many gate-1 height records at times τ₁ < τ₂ < ··· with heights Kᵢ → ∞, then q_{τᵢ} → −3⁻¹ in ℤ₂ (2-adic convergence) AND q_{τᵢ} → ∞ in ℝ (Archimedean divergence)
- **Theorem 4.2** (2-adic escape equivalence): The Collatz conjecture is equivalent to: no Collatz orbit has a 2-adic escape pair
- **Lemma**: −3⁻¹ ∉ ℤ_{>0}, so the two conditions are simultaneously satisfiable only by a divergent orbit

---

## Main Results

### Proved (Rigorous)

| Result | Method | Status |
|--------|--------|--------|
| Hensel nesting: r_{K′} ≡ r_K (mod 2^K) for K′ ≥ K | Hensel's lemma | ✓ proved |
| Theorem HMC: 2-adic convergence + Archimedean divergence | 2-adic analysis | ✓ proved |
| Theorem 4.2: Collatz ⟺ no 2-adic escape pair | Equivalence | conditional, see Erratum |
| −3⁻¹ ∉ ℤ_{>0} | Elementary | ✓ proved |

### Open

| Problem | Status |
|---------|--------|
| Gate-2 full analysis | Open |
| Mixed gate-1/gate-2 record chains | Open |

---

## Structure

```
§1   Introduction
§2   The gate-1 record target system
§3   Theorem HMC: Hensel Memory Compatibility     ✓
§4   The 2-adic escape reformulation               ✓
§5   Gate-2 records and the complete picture       open
§6   Summary
```

---

## Open Problems

- Complete gate-2 jump target analysis
- Mixed gate-1/gate-2 chains: characterisation of all possible height record sequences
- Proving the impossibility of a 2-adic escape pair

---

## Repository Structure

```
collatz-hensel-escape/
├── README.md
├── paper/
│   └── paper_o_hensel_memory_2adic_escape.pdf
└── LICENSE
```

---

## Related Work

This paper is part of a series on Collatz dynamics:

- [collatz-act1](https://github.com/KAMANOI/collatz-act1) — Foundational paper: prime survival dynamics and Chen-type theorem (v11)
- [collatz-renewal-structure](https://github.com/KAMANOI/collatz-renewal-structure) — Paper A: exact operator structure and finite information memory
- [collatz-finite-mixing-geometry](https://github.com/KAMANOI/collatz-finite-mixing-geometry) — Paper B: finite-level mixing geometry
- [collatz-spectral-amplification](https://github.com/KAMANOI/collatz-spectral-amplification) — Paper C: spectral amplification
- [collatz-scale-coherence](https://github.com/KAMANOI/collatz-scale-coherence) — Paper D: scale-coherence rigidity
- [collatz-valuation-renewal](https://github.com/KAMANOI/collatz-valuation-renewal) — Valuation renewal, finite residue connectivity, and orbitwise gap
- [collatz-residual-core](https://github.com/KAMANOI/collatz-residual-core) — The residual core: structural decomposition
- [collatz-congruence-synchronization](https://github.com/KAMANOI/collatz-congruence-synchronization) — Paper H: nested congruence constraints on synchronization
- [collatz-record-renewal](https://github.com/KAMANOI/collatz-record-renewal) — Paper N: record renewal compatibility
- [collatz-hensel-escape](https://github.com/KAMANOI/collatz-hensel-escape) — Paper O: Hensel memory and 2-adic escape target
- [collatz-hensel-scarcity](https://github.com/KAMANOI/collatz-hensel-scarcity) — Paper T: Hensel conditional scarcity and telescoping contradiction
- [collatz-prefix-counting](https://github.com/KAMANOI/collatz-prefix-counting) — Paper V: direct prefix counting and synchronization collapse
- [collatz-first-passage](https://github.com/KAMANOI/collatz-first-passage) — Paper W: first-passage obstruction (closes series A–V)
- [collatz-series-summary](https://github.com/KAMANOI/collatz-series-summary) — Series summary: research program on Collatz synchronization dynamics
- [collatz-prime-survival](https://github.com/KAMANOI/collatz-prime-survival) — Paper X v20: prime survival in affine Collatz dynamics

---

## Author

Hiroki Kamanoi
hirokikamanoi@gmail.com
2026
