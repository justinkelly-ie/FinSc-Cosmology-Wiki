# 📘 Idris2-Cosmology-Wiki (Layer 9 Specification & Verification)

This repository contains the executable wiki specifications, QuickCheck property suites, and formal proof witnesses for **Layer 9** (`Idris2-Cosmology`).

---

## 📚 Literate Specifications & Property Suites

- **[`GaloisAdjunctionSpec.md`](Library/Wiki/GaloisAdjunctionSpec.md):** 
  - Verifies Galois Adjunction ($\alpha \dashv \gamma$) abstraction duality ($\gamma(\alpha(c)) \equiv c$).
  - Verifies widening operator monotonicity and isometric metric preservation under scale expansion.
  - Includes static proof witness `prfStaticGaloisIdentity`.

- **[`MacroEnvelopeSpec.md`](Library/Wiki/MacroEnvelopeSpec.md):** 
  - Verifies Primorial 210 mass budget conservation ($27 \text{ Baryon} + 55 \text{ Dark} + 128 \text{ H}_2\text{O} = 210$).
  - Verifies star formation Jeans mass threshold check ($B \ge 27$).
  - Verifies metrical coarse-graining mass budget invariance ($M_{\text{Total}} = c + 183$).
  - Includes static proof witnesses `prfStaticCosmicBudget` and `prfStaticCoarseGrainMass`.

---

## ⚡ Running Verification Executable

To build and run the complete Layer 9 test suite inside `fedora-toolbox-44`:

```bash
toolbox run -c fedora-toolbox-44 bash -c "cd /var/home/justin/Projects/Idris2-Cosmology && idris2 --install Idris2-Cosmology.ipkg && cd /var/home/justin/Projects/Idris2-Cosmology-Wiki && idris2 --build Idris2-Cosmology-Wiki.ipkg && ./build/exec/lcosmology-wiki"
```
