# Suess - Muon Decay in LEFT

A comprehensive analysis of muon decay in the Low Energy Effective Field Theory (LEFT) framework.

## Contents

### 1. Interactive Muon Decay Animation
**File:** `muon-decay.html`

A browser-based JavaScript animation visualizing the muon decay process:
- μ⁻ → e⁻ + ν̄ₑ + νμ

The animation shows:
- The muon particle before decay
- A visual decay event
- Three decay products (electron, electron antineutrino, muon neutrino) with colored particle trails
- Real-time countdown and statistics

**Usage:** Open `muon-decay.html` in any modern web browser.

---

### 2. Systematic LEFT Operator Analysis
**Files:**
- `muon-decay-LEFT.tex` - LaTeX document
- `muon-decay-LEFT-operators.m` - FormCalc implementation

#### Overview
A complete catalog of dimension-6 LEFT operators for muon decay using the **Jenkins et al. basis** (JHEP 1711, 059 (2017)).

#### Key Results

**Total Operators: 135**
- **90 Lepton-Number Conserving (LNC)** operators for μ⁻ → e⁻ + νₐ + ν̄ᵦ
- **45 Lepton-Number Violating (LNV)** operators for μ⁻ → e⁻ + ν̄ₐ + ν̄ᵦ

#### Operator Classification

**Lepton-Number Conserving (ΔL = 0):**
| Structure | Type | Count | Description |
|-----------|------|-------|-------------|
| VLL, VLR, VRL, VRR | Vector | 4×9 = 36 | Vector currents with L/R chirality |
| SRL, SRR, SLL, SLR | Scalar | 4×9 = 36 | Scalar currents |
| TRL, TLR | Tensor | 2×9 = 18 | Tensor currents with σ^μν |
| **Total** | | **90** | |

**Lepton-Number Violating (ΔL = 2):**
| Structure | Type | Count | Description |
|-----------|------|-------|-------------|
| VLL_LNV, VLR_LNV | Vector | 2×9 = 18 | Same-sign neutrinos |
| SRL_LNV, SRR_LNV | Scalar | 2×9 = 18 | Same-sign neutrinos |
| TRL_LNV | Tensor | 1×9 = 9 | Same-sign neutrinos |
| **Total** | | **45** | |

#### Neutrino Flavor Combinations

Each operator structure includes **9 flavor combinations** (α, β):
```
(νₑ, νₑ)   (νₑ, νμ)   (νₑ, ντ)
(νμ, νₑ)   (νμ, νμ)   (νμ, ντ)
(ντ, νₑ)   (ντ, νμ)   (ντ, ντ)
```

The Standard Model uses only: **VLL[νₑ, νμ]** at tree level via W-boson exchange.

#### FormCalc Implementation

The `muon-decay-LEFT-operators.m` script:
- Systematically defines all operator structures
- Enumerates all flavor combinations
- Analyzes Fierz identities and redundancies
- Validates operator counting
- Provides Wilson coefficient parameterization
- Discusses experimental constraints

**Key Insight:** The Jenkins basis is Fierz-complete and non-redundant, avoiding overcounting from equivalent operator representations.

#### Physics Applications

This operator basis enables studies of:
- **Non-Standard Neutrino Interactions (NSI)** - exotic ν flavor combinations
- **Lepton Flavor Violation** - correlations with μ → eγ, μ → 3e
- **Lepton Number Violation** - connections to neutrinoless double-beta decay
- **Majorana Neutrinos** - mass insertion contributions
- **New Physics Searches** - model-independent constraints at TeV scale
- **SMEFT Matching** - UV completion at electroweak scale

#### Experimental Constraints

Current precision measurements constrain:
- Muon lifetime: τμ = 2.1969811(22) × 10⁻⁶ s (~10 ppm precision)
- Michel parameters: ρ = 0.74979(26), δ = 0.75047(34)
- Wilson coefficients: |Cᵢ|/Λ² ≲ 10⁻⁶ GeV⁻²
- New physics scale: Λ ≳ 1 TeV (for O(1) coefficients)

---

## Files

```
suess/
├── README.md                          # This file
├── muon-decay.html                    # Interactive animation
├── muon-decay-LEFT.tex                # Complete LaTeX document
└── muon-decay-LEFT-operators.m        # FormCalc implementation
```

## References

1. Jenkins, E. E., Manohar, A. V., & Stoffer, P. (2018). *Low-energy effective field theory below the electroweak scale: Operators and matching.* JHEP, 2018(3), 016.
2. Cirigliano, V., et al. (2022). *Charged Lepton Flavor Violation at the EIC.* arXiv:2204.02490.
3. Crivellin, A., et al. (2017). *Lepton flavor violation in the Standard Model and beyond.* arXiv:1711.10391.

---

## Author

Generated for systematic muon decay analysis in LEFT framework.

## License

Open for research and educational purposes.
