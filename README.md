# WKET — Wick-Klein Erlangen Transform

**The Imaginary Circle: Wick Rotation, Klein's Erlangen Program, and the Projective Geometry of Learning Phase Transitions**  
*Bridge VI: From Imaginary Time and the Circular Points at Infinity to the Geometry of Grokking*

---

## Overview

This document establishes **Bridge VI** — the Wick-Klein Erlangen Transform (WKET) — which provides the **meta-geometric foundation** from which all five previous bridges emerge as special cases. The central claim is threefold:

**Claim 1 (Wick Identification)**: The Jordan-Liouville operator ℒ_JL is already the Wick-rotated form of the learning Hamiltonian H_learn. The substitution t → τ = it (imaginary learning time) is equivalent to the substitution 1/k_BT → iτ/ℏ that converts quantum time evolution into thermal equilibrium. The spectral gap λ₁ > 0 is the condition that the Wick-rotated propagator e^{-ℒ_JL τ} converges — equivalently, that the Boltzmann weight e^{-H_learn/T_learn} is normalizable (T_learn < T_c).

**Claim 2 (Klein Identification)**: Every module of the unified framework is a specific **Klein geometry** in the sense of the Erlangen Program (1872): a space characterized by the invariants of a particular transformation group. The grokking transition at λ₁ = 0 is a **change of Klein geometry** — from pseudo-Riemannian/Minkowski (memorization, indefinite metric) to Riemannian/Euclidean (generalization, positive-definite metric). This transition is mediated by Klein's imaginary transformation.

**Claim 3 (Circular Points Identification)**: The **circular points at infinity** ω = (1:i:0) and ω̄ = (1:−i:0) in the complex projective plane ℂP² are, under the WKET identification, the **Cooper pair endpoints** (k, −k) in GCCT. Every real circle in projective geometry passes through both circular points; in GCCT, every Cooper pair consists of a mode and its Farey complement — its "circular antipode." The grokking locus {λ₁ = 0} is the **absolute conic** of the Cayley-Klein metric on the learning manifold ℬ, and the spectral gap λ₁ is the Cayley-Klein distance from a parameter point to this absolute.

Bridge VI unifies and explains all previous bridges: Bridges I–V are the Euclidean, thin-film, superconducting, colloidal, and gauge-theoretic projections of a single underlying imaginary-time geometry. Wick rotation is the transformation between them.

---

## Table of Contents

1. [Felix Klein and the Erlangen Program](#i-felix-klein-and-the-erlangen-program)
2. [Circular Points at Infinity and Klein's Imaginary Transformation](#ii-circular-points-at-infinity-and-kleins-imaginary-transformation)
3. [Wick Rotation — Imaginary Time and the Statistical-Quantum Bridge](#iii-wick-rotation--imaginary-time-and-the-statisticalquantum-bridge)
4. [Wick's Theorem and the Dyson Expansion](#iv-wicks-theorem-and-the-dyson-expansion)
5. [Bridge VI — Complete WKET Dictionary](#v-bridge-vi--complete-wket-dictionary)
6. [The Wick Rotation of Learning: Euclidean vs Minkowski Phases](#vi-the-wick-rotation-of-learning-euclidean-vs-minkowski-phases)
7. [The BCS Circle and the Memorization Hyperbola](#vii-the-bcs-circle-and-the-memorization-hyperbola)
8. [Matsubara Frequencies and Farey Denominators](#viii-matsubara-frequencies-and-farey-denominators)
9. [Cayley-Klein Metric and the Spectral Gap as Absolute Distance](#ix-cayley-klein-metric-and-the-spectral-gap-as-absolute-distance)
10. [Klein Four-Group Symmetry of the BdG Hamiltonian](#x-klein-four-group-symmetry-of-the-bdg-hamiltonian)
11. [Erlangen Classification of All Framework Modules](#xi-erlangen-classification-of-all-framework-modules)
12. [Extended Master Equivalence (Fourteen Languages)](#xii-extended-master-equivalence-fourteen-languages)
13. [New Conjectures from WKET](#xiii-new-conjectures-from-wket)
14. [Complete Symbol Table](#xiv-complete-symbol-table)
15. [Foundations and Citations](#xv-foundations-and-citations)

---

## I. Felix Klein and the Erlangen Program

### 1.1 The Core Idea: Geometry = Group + Invariants

Felix Klein's Erlangen Program (1872), delivered as his inaugural lecture at the University of Erlangen, proposed that every geometry is completely characterized by a transformation group G and the properties that are invariant under that group. Two geometric configurations are "the same" if and only if they can be mapped to each other by an element of G.

```
Klein's definition:  Geometry(G) = { properties invariant under G }
```

This definition simultaneously unified and classified all known geometries and predicted the existence of new ones. The key insight was radical: **the geometry is secondary; the group is primary.**

### 1.2 The Hierarchy of Klein Geometries

The classical geometries are nested by their groups (larger group = more invariants destroyed = less structure):

```
Projective ⊃ Affine ⊃ Euclidean ⊃ Metric (Riemannian)
PGL(n+1)    GL(n)⋉ℝⁿ  ISO(n)      O(n)

Projective ⊃ Conformal ⊃ Euclidean
PGL(n+1)    Möb(n)      ISO(n)

Non-Euclidean geometries:
Hyperbolic: PSL(2,ℝ) = Isom(ℍ²)    [upper half-plane / Farey / GAME]
Elliptic:   SO(3) = PGL(2,ℝ)
Special Kähler: Sp(2n,ℝ) ⊃ U(n)    [SW prepotential / KYBM]
```

**Projective geometry** has the most freedom: cross-ratio and incidence are all that survive. **Euclidean geometry** retains distances and angles. **Riemannian geometry** is the local refinement where the metric varies from point to point.

### 1.3 Klein's Complex Analysis and the Modular Group

Klein's deepest work connected geometry, group theory, and complex analysis through the modular group PSL(2,ℤ). He showed:

1. The modular group Γ = PSL(2,ℤ) acts on the upper half-plane ℍ by τ → (aτ+b)/(cτ+d)
2. The fundamental domain of Γ tessellates ℍ
3. Modular forms — functions invariant under Γ — encode deep arithmetic
4. The j-invariant j(τ) = e^{-2πiτ} + 744 + 196884e^{2πiτ} + ··· is invariant under all of PSL(2,ℤ)

The generators of PSL(2,ℤ) are S = [[0,−1],[1,0]] and T = [[1,1],[0,1]], satisfying S² = (ST)³ = Id. In the GAME module, these appear as the gradient word algebra:

```
R = [[1,1],[0,1]]  (= T)       gradient growing
L = [[1,0],[1,1]]  (= T^T)     gradient shrinking
```

**The training word W_t ∈ SL(2,ℤ) is exactly the monodromy of j(τ) as the SW modulus u(t) = C_α(t) traces its training path** — the Klein-GAME-SWMS identification at depth.

### 1.4 The Klein Quartic

Klein's 1879 work on the Riemann surface of the equation x³y + y³z + z³x = 0 over ℂ produced the **Klein quartic**: a compact Riemann surface of genus 3 whose automorphism group is PSL(2,7) of order 168, the maximal possible for genus 3 (Hurwitz bound: ≤ 84(g−1) = 168).

The PSL(2,7) action on the 7-point projective line PG(1,7) relates to the Farey structure at Q_max = 7. The Klein quartic encodes the arithmetic of the framework's modular structure at the 7th level.

---

## II. Circular Points at Infinity and Klein's Imaginary Transformation

### 2.1 Definition and Properties

In the complex projective plane ℂP², consider points with homogeneous coordinates (x : y : z) where (x, y, z) ∈ ℂ³ \ {0} and two triples representing the same point iff they are proportional.

The **circular points at infinity** (also called cyclic or isotropic points) are:

```
ω  = (1 : i : 0)    [first circular point]
ω̄ = (1 : −i : 0)  [second circular point; complex conjugate of ω]
```

These lie on the line at infinity z = 0, and satisfy:

```
x² + y² = 0    at z = 0
```

which factors as (x + iy)(x − iy) = 0 — the equation of the "imaginary circle at infinity." ω and ω̄ are the intersection of every real circle with the line at infinity.

**Fundamental property**: A real curve is a circle if and only if it passes through both ω and ω̄.

**Consequence**: Every Euclidean geometric fact about circles can be understood as a projective fact about conics passing through the two circular points.

### 2.2 Angle Formula via Circular Points

The concept of angle between two lines, which has no projective meaning, is recovered using the circular points. Let two lines u, u' pass through a point P. Their pencil, together with the lines Pω and Pω̄, forms four lines. The angle between u and u' is:

```
θ = (1/2i) · log( cross-ratio(u, u'; Pω, Pω̄) )
```

Explicitly, if u makes angle θ and u' makes angle θ' with the x-axis:

```
cross-ratio(u, u'; ω, ω̄) = [(tan θ − i)/(tan θ + i)] / [(tan θ' − i)/(tan θ' + i)]
= e^{2i(θ−θ')}
```

so θ − θ' = log(cross-ratio)/2i — the Cayley angle formula. This connects Euclidean angles to projective cross-ratios via the circular points.

**Framework identification**: The Josephson phase difference Δφ_F between two loss basins is the Cayley angle between two gradient directions in the parameter manifold ℬ, computed via the cross-ratio with the circular (Cooper pair) endpoints:

```
Δφ_F = (1/2i) · log(cross-ratio of gradient pencil with circular Farey endpoints)
ω_J = d(Δφ_F)/dt = 2V_basin/ℏ_learn    [Josephson, BC-C2]
```

### 2.3 Klein's Imaginary Transformation

Klein defined the **imaginary transformation** as:

```
T_i: (x : y : z) → (x : iy : z)      [y-coordinate multiplied by i]
```

This transformation maps:
- Circular points: ω = (1:i:0) → (1:i²:0) = (1:−1:0), which is a **real** point at infinity
- ω̄ = (1:−i:0) → (1:−i²:0) = (1:1:0), also a **real** point at infinity
- The imaginary circle x² + y² = 0 → x² − y² = 0 (real cross — pair of real lines at 45°)
- Circles → **equilateral hyperbolas** (asymptotes at 45° to the axes)
- The Euclidean metric ds² = dx² + dy² → ds² = dx² − dy² (Minkowski metric!)

Klein's imaginary transformation **is** the 2-dimensional Wick rotation:

```
T_i : y → iy    (Klein, projective)
↕
Wick: t → it    (or equivalently: t → τ = −it)
↕
ds²_{Euclidean} = dx² + dt² ←→ ds²_{Minkowski} = dx² − dt²
```

**The Wick rotation and Klein's imaginary transformation are the same map expressed in different coordinates.**

### 2.4 Isotropic Lines and the Farey Complement

The **isotropic lines** of the Euclidean plane are the complex lines satisfying:

```
x + iy = const    or    x − iy = const    [null lines of ds² = dx²+dy²]
```

These have complex slope ±i. Every isotropic line passes through one of the circular points (either ω or ω̄).

In the GCCT/KQOM framework:
- Farey mode k = (p,q) and its complement −k = (q−p, q) satisfy p/q + (q−p)/q = 1
- This is the Farey complement relation, which plays the role of the ω ↔ ω̄ pairing
- The BdG particle-hole spinor Ψ_k = (c_{k,t}, c†_{−k,t})^T pairs mode k with −k
- The Nambu particle-hole pairing (k, −k) IS the pair of isotropic directions through the circular points ω and ω̄

```
ω = (1:i:0)         ↔    k = (p,q) ∈ 𝒜_Q        [signal Farey mode]
ω̄ = (1:−i:0)       ↔   −k = (q−p,q) ∈ 𝒜_Q      [Farey complement = noise mode]
pair (ω, ω̄)         ↔    Cooper pair (k, −k)      [circle passes through both]
isotropic line       ↔    BdG eigenstate at ξ_k=0  [at the Farey surface]
```

---

## III. Wick Rotation — Imaginary Time and the Statistical-Quantum Bridge

### 3.1 The Classical Wick Rotation (Wick 1954)

In quantum mechanics, the time evolution operator is:

```
U(t) = e^{-iHt/ℏ}    [unitary, oscillatory in real time t]
```

In statistical mechanics, the Gibbs weight is:

```
Z = Tr[e^{-βH}]  where  β = 1/(k_BT)    [Boltzmann factor]
```

Wick's observation (1954): substituting t = −iτ (imaginary time, τ real and positive) converts quantum evolution to thermal weighting:

```
e^{-iHt/ℏ} → e^{-Hτ/ℏ}    when    t = −iτ

Identifying τ/ℏ = β = 1/k_BT:

Quantum evolution at real time t    ↔    Thermal equilibrium at temperature T = ℏ/(k_B τ)
```

This is called a **Wick rotation** because in the complex t-plane, τ = it is obtained by rotating the real axis by π/2 (multiplication by i = e^{iπ/2}).

### 3.2 Schrödinger ↔ Heat Equation

Under Wick rotation t → τ = it, the Schrödinger equation becomes the heat/diffusion equation:

```
iℏ ∂ψ/∂t = Hψ    [Schrödinger, real time]
↓  t = −iτ (Wick rotate)
ℏ ∂ψ/∂τ = −Hψ   ↔   ∂ρ/∂τ = ℒ_JL ρ   [diffusion / heat equation, imaginary time]
```

The Jordan-Liouville operator ℒ_JL = −∇·(D_s∇) + 𝒮̄ is **already in the Wick-rotated (Euclidean) form**. It is a positive-definite diffusion operator — the imaginary-time version of the learning Hamiltonian.

### 3.3 Path Integral ↔ Partition Function

Under Wick rotation, the quantum path integral (sum over paths weighted by e^{iS/ℏ}) becomes the statistical-mechanical partition function (sum over paths weighted by e^{−S_E/ℏ}):

```
Z_quantum = ∫ Dθ · e^{iS[θ]/ℏ}    [oscillatory, real time]
↓  t → −iτ
Z_thermal = ∫ Dθ · e^{−S_E[θ]/ℏ}  [convergent, imaginary time]

where S_E is the Euclidean action (positive-definite)
```

In the learning framework:
- Z_quantum = generating functional for gradient path integrals
- Z_thermal = learning partition function Tr[e^{−ℒ_JL/T_learn}] = Tr[e^{−βH_learn}]
- The Wick rotation connects the oscillatory training dynamics (real time) to the equilibrium distribution (imaginary time / temperature)

### 3.4 Instantons as Wick-Rotated Tunneling Paths

An **instanton** is a classical solution to the Euclidean equations of motion (imaginary time). In gauge theory, instantons are self-dual connections on ℝ⁴_E that contribute non-perturbative corrections to the path integral.

Under Wick rotation t → iτ:
- Minkowski saddle points (unstable) → Euclidean saddle points (instantons, tunneling paths)
- Real oscillation (barrier bouncing) → imaginary oscillation (tunneling through barrier)

In the learning framework (KYBM):
- Yang-Mills energy YM_t = Tr(Cov_batch[∇L]) = ‖F_A‖² is the instanton action
- Concentrated YM_t at points {bᵢ} = **Uhlenbeck instantons** = catastrophic forgetting events
- These are the Wick-rotated version of the training dynamics going over potential barriers
- WKET-C1 (new conjecture below): catastrophic forgetting = learning instanton, and its action is the Euclidean Wick rotation of the gradient noise

### 3.5 Osterwalder-Schrader and Reflection Positivity

The Osterwalder-Schrader theorem (1973, 1975) provides the rigorous conditions under which a Euclidean QFT (imaginary time) corresponds to a Minkowski QFT (real time):

```
Euclidean QFT satisfying:
  (OS1) Euclidean covariance
  (OS2) Reflection positivity: ⟨θf, f⟩ ≥ 0 for Euclidean time reflection θ
  (OS3) Regularity/growth conditions on correlation functions
↕
Minkowski QFT satisfying the Wightman axioms
```

**Reflection positivity** is the Euclidean analog of unitarity: it ensures the Hilbert space inner product is positive-definite after Wick rotation.

In the learning framework, the corresponding theorem is:

**Theorem (WKET reflection positivity)**: The operator ℒ_JL satisfies the analog of OS2 iff λ₁(ℒ_JL) > 0. Specifically, for any test function φ ∈ L²(ℬ, μ):

```
⟨φ, ℒ_JL φ⟩ = ∫ |D_s^{1/2} ∇φ|² dvol + ∫ 𝒮̄|φ|² dvol ≥ λ₁ ‖φ‖²
```

This is precisely condition (IV) (Poincaré inequality) in the Master Equivalence. **Reflection positivity of the learning dynamics is equivalent to the spectral gap λ₁ > 0.**

The learning-theoretic OS correspondence:

```
Euclidean QFT (Wightman axioms)    ↔    Minkowski QFT (OS axioms)
↕ (learning analog)
λ₁ > 0 (spectral gap, generalization)  ↔  T_learn < T_c (below critical temperature)
Fokker-Planck ρ → ρ_∞                 ↔  e^{-ℒ_JL τ} convergent
OS reflection positivity              ↔  Poincaré inequality (IV)
Wightman axioms                       ↔  Master Equivalence (I)–(XIV)
```

### 3.6 Finite-Temperature QFT: Imaginary Time on a Circle

When temperature T > 0, the imaginary time coordinate τ is **periodic** with period β = 1/T (in units ℏ = k_B = 1):

```
τ ~ τ + β    [imaginary time compactified on S¹ of circumference β]
```

The Fourier modes of fields on this circle give the **Matsubara frequencies**:

```
ω_n^{bose} = 2πnT = 2πn/β         (bosonic: n ∈ ℤ)
ω_n^{fermi} = (2n+1)πT = (2n+1)π/β  (fermionic: n ∈ ℤ)
```

These discretize the momentum spectrum at finite temperature. The maximum Matsubara frequency is cut off by the UV cutoff of the theory.

**The Matsubara-Farey identification** (WKET):

```
β_learn = 1/T_learn = C_α / Tr(D_s)    [inverse learning temperature = imaginary time period]

Matsubara index n ↔ Farey denominator q_n ∈ {1, 2, ..., Q_max}

ω_n^{Matsubara} = 2πn/β_learn = 2πn·T_learn
↔
2π · (p_n/q_n) ∈ 2π·𝒜_Q      [Farey fraction as reduced Matsubara frequency]

Maximum Matsubara index: N_max = Q_max = ⌊1/ε_t⌋ = ⌊β_learn⌋ (discrete units)
```

The **Farey alphabet 𝒜_Q is the set of allowed Matsubara frequencies at inverse temperature β_learn = Q_max** in the learning theory. The Debye cutoff Q_max and the inverse temperature β_learn are the same quantity.

---

## IV. Wick's Theorem and the Dyson Expansion

### 4.1 Wick's Theorem (1950)

Wick's theorem expresses time-ordered products of quantum fields in terms of normal-ordered products (creation/annihilation operators in a specific order) plus Wick contractions (two-point functions of the vacuum):

```
T[φ(x₁) φ(x₂) ··· φ(xₙ)] = :φ(x₁) φ(x₂) ··· φ(xₙ): + Σ (all pairwise contractions)
```

where the Wick contraction of two fields is:

```
⌢
φ(x) φ(y) = ⟨0|T[φ(x)φ(y)]|0⟩ = G₀(x−y)    [free Green's function]
```

The theorem reduces all n-point correlation functions to products of free propagators — the foundation of Feynman diagram perturbation theory.

### 4.2 Dyson Expansion as Wick Expansion (FLML ↔ Wick)

The FLML dressed propagator G_t(k,ω) is computed via the Dyson equation:

```
G_t(k,ω) = G₀(k,ω) + G₀ · Σ_t · G₀ + G₀ · Σ_t · G₀ · Σ_t · G₀ + ···
          = G₀ · [1 + Σ_t G₀ + (Σ_t G₀)² + ···]
          = [G₀⁻¹ − Σ_t]⁻¹    [resummed Dyson equation]
```

This is **exactly** the Wick expansion of the gradient propagator in the learning QFT:

```
Wick's theorem:            Dyson expansion (FLML):
Time-ordered T[φ···φ]  ↔   G_t(k,ω)
Normal-ordered :φ···φ: ↔   G₀(k,ω) = [ωI − H₀(k)]⁻¹  [free propagator]
Wick contraction ⌢φφ   ↔   Σ_t^{GW} = G_t · Cov_batch[∇L] · G_t  [self-energy]
n-loop diagram         ↔   n-th order Dyson term G₀(Σ_t G₀)ⁿ
2PI skeleton           ↔   Φ_LW[G_t]  [Luttinger-Ward functional]
```

The free propagator G₀(k,ω) = [ωI − H₀(k)]⁻¹ is the **Wick-rotated** free Green's function: its poles at ω = ε_k (eigenvalues of H₀) are the Matsubara frequencies of the free learning theory.

The GW (ring-diagram) self-energy Σ_t^{GW} is the first-order Wick contraction — the two-point function of the gradient noise field:

```
Σ_t^{GW}(k) = ⌢{∇L · ∇L} = G_t(k) · Cov_batch[∇L] · G_t(k)
```

### 4.3 Wick Rotation of the Learning Path Integral

The learning path integral over gradient trajectories {θ(t): t = 0 to T} is:

```
Z_learn = ∫ Dθ(t) · exp(−∫₀ᵀ L_t(θ(t)) dt)    [Minkowski, real time]
```

Under Wick rotation t → iτ, T_learn → imaginary temperature:

```
Z_learn^{Eucl.} = ∫ Dθ(τ) · exp(−∫₀^β S_E[θ(τ)] dτ)    [Euclidean, imaginary time]

where S_E = ∑_k [(ℏ/2)(∂θ_k/∂τ)² + V(θ_k)]    [Euclidean action]
```

The convergence of Z_learn^{Eucl.} requires λ₁(ℒ_JL) > 0 — the spectral gap condition. The Wick rotation converts the oscillatory real-time path integral (memorization regime, indefinite action) into a convergent imaginary-time path integral (generalization regime, positive-definite action).

---

## V. Bridge VI — Complete WKET Dictionary

### 5.1 Primary Identifications (Wick)

| Quantum/Statistical Mechanics | Symbol | Learning Framework | Symbol | Module |
|---|---|---|---|---|
| Imaginary time | τ = it | Inverse learning temperature | β_learn = 1/T_learn | WKET |
| Real time | t | Training step | t | GAME |
| Temperature | T | Learning temperature | T_learn = Tr(D_s)/C_α | GCCT |
| Inverse temp. | β = 1/k_BT | Inverse learning temp. | β_learn = C_α/Tr(D_s) | GCCT |
| Boltzmann weight | e^{−βH} | Fokker-Planck weight | e^{−ℒ_JL/T_learn} | LKTL |
| Hamiltonian H | H ≥ 0 (Euclidean) | Jordan-Liouville | ℒ_JL = −∇·D_s∇ + 𝒮̄ | LKTL |
| Mass gap m | e^{−m|x|} decay | Spectral gap | λ₁(ℒ_JL) | LKTL |
| Schrödinger eq. | iℏ∂_t ψ = Hψ | Learning ODE | ∂_t θ = −∇L + noise | GAME |
| Heat eq. | ∂_τ ρ = −Hρ | Fokker-Planck | ∂_τ ρ = ℒ_JL ρ | LKTL |
| QFT critical pt | m = 0 | Grokking frontier | λ₁ = 0 | LKTL |
| Below T_c | T < T_c (ordered) | Generalization | λ₁ > 0 | GCCT |
| Above T_c | T > T_c (disordered) | Memorization | λ₁ < 0 | GCCT |
| Quantum fluctuations | ℏ/iS[path] | Gradient noise | D_s = Cov[∇L] | LKTL |
| Thermal fluctuations | k_BT/S_E[path] | Learning temp. | T_learn = Tr(D_s)/C_α | GCCT |
| Partition function | Z = Tr[e^{−βH}] | Normalization | Z_t = ∫ρ_∞ dμ | LKTL |
| Free energy | F = −T log Z | Learning potential | 𝒮̄(b) (equilibrium) | LKTL |
| Instantons | Euclidean tunneling paths | Catastrophic forgetting | YM_t concentrated at {bᵢ} | KYBM |
| Matsubara freq. | ω_n = 2πnT | Farey denominators | q_n ∈ {1,...,Q_max} | KQOM |
| Period β circle | imaginary time S¹ | Farey cutoff | Q_max = ⌊β_learn⌋ | KQOM |
| Reflection positivity | OS-positivity | Poincaré inequality | (IV) in Master Equiv. | LKTL |
| Osterwalder-Schrader | OS theorem | Convergence theorem | λ₁>0 ↔ ρ→ρ_∞ | LKTL |

### 5.2 Primary Identifications (Klein Erlangen)

| Klein Geometry | Group | Invariants | Framework Module |
|---|---|---|---|
| Projective | PGL(3) | Cross-ratio, incidence, Pascal | PPMC |
| Conformal/Möbius | PGL(2,ℂ) = Möb | Circles, angles, inversions | GAME (SL(2,ℤ)⊂Möb) |
| Affine | GL(n)⋉ℝⁿ | Parallelism, ratios | RG-ML (scale sep.) |
| Euclidean | ISO(n) = O(n)⋉ℝⁿ | Distances, angles | LB/DK, ℒ_JL generalization |
| Minkowski | ISO(n−1,1) | Causal structure, proper time | LKTL memorization |
| Isotropic/null | Galilean group | Parabolic structure, λ₁=0 | Grokking frontier |
| Hyperbolic | PSL(2,ℝ) | Geodesics, horocycles | KQOM (Farey/SB tree) |
| Special Kähler | Sp(2n,ℝ) | Holomorphic structure, duality | KYBM, SWMS |
| Cayley-Klein | O(p,q) | Quadric absolute, log distance | CSSG, SWMS |

### 5.3 Primary Identifications (Circular Points)

| Circular Geometry | Symbol | Learning Framework | Symbol | Module |
|---|---|---|---|---|
| Circular point | ω = (1:i:0) | Farey mode | k = (p,q) ∈ 𝒜_Q | KQOM |
| Conjugate circular pt | ω̄ = (1:−i:0) | Farey complement | −k = (q−p,q) | GCCT |
| Circle through ω,ω̄ | x²+y²+···=0 | BdG eigenvalue circle | ξ_k²+Δ_t²=E_k² | GCCT |
| Isotropic direction | dx = ±i·dy | BdG Farey surface | ξ_k = 0 | GCCT |
| Cayley angle θ | log(cross-ratio)/2i | Josephson phase | Δφ_F | GCCT |
| Imaginary transform | (x:y:z)→(x:iy:z) | Wick rotation | D_s → i·D_s | WKET |
| Circle → hyperbola | T_i: x²+y² → x²−y² | BCS→memorization | u²+v²=1 → u²−v²=1 | GCCT |
| Circular points fixed | ω,ω̄ fixed under ISO(2) | Cooper pair fixed pts | (k,−k) fixed under U(1)_batch | GCCT |
| Circular points at ∞ | z=0, isotropic | Grokking frontier | λ₁=0, isotropic diffusion | LKTL |
| Conic through ω,ω̄ | circle (real) | Cooper condensate | Δ_t>0 (real order parameter) | GCCT |
| Degenerate conic | tangent lines | Δ_t=0 (normal state) | λ₁=0 phase boundary | GCCT |
| Absolute conic Q | Cayley-Klein metric | Grokking locus | {λ₁=0} ⊂ ℬ | WKET |
| Cayley-Klein dist. | d(P,Q) = log cr(P,Q;A,B) | Spectral gap | λ₁ = d(b, {λ₁=0}) | WKET |
| Klein imaginary transf. | Circles→equil. hyperbolas | Generalization→memorization | λ₁>0 → λ₁<0 | WKET |
| Cross-ratio (proj. inv.) | (P₁P₂P₃P₄) | Farey cross-ratio | (q₁q₂q₃q₄) mediant relation | KQOM |
| PSL(2,7) Klein quartic | x³y+y³z+z³x=0 | Farey level-7 structure | Q_max=7 arithmetic | KQOM |

---

## VI. The Wick Rotation of Learning: Euclidean vs Minkowski Phases

### 6.1 Two Signatures of the Learning Metric

The learning manifold ℬ carries a natural metric determined by the gradient covariance D_s = Cov_batch[∇L]. This metric has two possible signatures depending on the phase:

**Generalization phase (λ₁ > 0) — Euclidean signature:**

```
ds²_E = Tr(D_s⁻¹ dθ⊗dθ)    [positive definite; Riemannian]
```

The Fokker-Planck operator ℒ_JL = −∇·(D_s∇) + 𝒮̄ is positive-definite (λ₁ > 0), and solutions decay exponentially e^{−λ₁τ}. The parameter manifold carries a Euclidean-type geometry. The circular points ω, ω̄ are truly "at infinity" — unreachable in finite time.

**Memorization phase (λ₁ < 0) — Minkowski signature:**

```
ds²_M = −|λ₁| dt² + ds²_space    [indefinite; pseudo-Riemannian]
```

The Fokker-Planck has a negative eigenvalue; solutions grow as e^{|λ₁|τ}. The parameter manifold carries a Minkowski-type geometry (one negative eigenvalue = time direction). The circular points ω, ω̄ have become real — they are accessible, the geometry is "isotropic."

**The Wick rotation maps between phases:**

```
T_i (Klein imaginary transform):  ds²_E → ds²_M
                                   D_s → −D_s  (positive → negative definite)
                                   λ₁ > 0 → λ₁ < 0

Wick rotation:                    t → iτ
                                   e^{−λ₁ t} → e^{−λ₁ iτ} = e^{iλ₁ τ}    (oscillatory)
```

The grokking transition at λ₁ = 0 is the **null/isotropic boundary** between these two phases — the lightcone of the learning geometry.

### 6.2 The Wick Rotation Formula for Learning Observables

Under the Wick rotation t → τ = it of the learning dynamics:

| Observable | Real time t (Minkowski) | Imaginary time τ (Euclidean) |
|---|---|---|
| Training propagator | e^{−iH_learn t} | e^{−ℒ_JL τ} = e^{−H_learn β} |
| Correlation C(t) | oscillatory if λ₁<0 | exponential decay if λ₁>0 |
| Farey backtrack period | T_backtrack (real oscillation) | τ_relax = 1/λ₁ (imaginary time) |
| Josephson frequency | ω_J = 2V_basin/ℏ_learn | ω_J ↔ 2πT_learn (Matsubara) |
| BCS circle | u²_k+v²_k=1 (real) | under T_i: u²_k−v²_k=1 (memorization) |
| Gap Δ_t (real) | oscillates at ω_J | decays as e^{−Δ_t τ} |
| YM instanton | e^{iS_{YM}} (quantum) | e^{−S_E} = e^{−YM_t} (classical) |
| Training word W_t | SL(2,ℤ) element (real) | monodromy in ℂ (imaginary) |

---

## VII. The BCS Circle and the Memorization Hyperbola

### 7.1 The Unitarity Circle in GCCT

The Bogoliubov-Valatin transformation in GCCT maps each gradient mode k to a quasiparticle γ_{k,t} via the amplitudes (u_k, v_k) satisfying:

```
u_k² + v_k² = 1    [unitarity condition = CIRCLE in (u_k, v_k) plane]
```

This is literally the equation of a unit circle. The BdG eigenvalue circle:

```
ξ_k² + Δ_t² = E_k²    [eigenvalue equation = CIRCLE in (ξ_k, Δ_t) plane, radius E_k]
```

is also a circle in parameter space. These circles pass through the imaginary points E_k = ±i·Δ_t when ξ_k = 0 — the **Farey surface circular points**.

### 7.2 Klein's Imaginary Transform Maps Circle to Hyperbola

Apply Klein's imaginary transformation T_i to the BCS unitarity circle:

```
T_i: v_k → i·v_k    (noise amplitude becomes imaginary)

u_k² + v_k² = 1    →    u_k² + (i·v_k)² = u_k² − v_k² = 1
```

The unitarity **circle** becomes a **hyperbola** under Klein's imaginary transformation. The hyperbola u²−v²=1 describes a system where:
- Signal modes dominate absolutely: u_k > 1 for all k (no noise suppression)
- No Cooper pair formation: Δ_t = 0 (trivial order parameter)
- Luttinger liquid behavior: Z_t → 0 (quasiparticle weight vanishes)

This is the **memorization phase** — and it arises from the Euclidean BCS circle by a single imaginary substitution v_k → i·v_k.

### 7.3 The Three Conic Sections and Three Learning Phases

Klein's classification of conics under the imaginary transformation gives the complete phase diagram:

```
Phase             Conic          Equation          Geometry       λ₁
─────────────────────────────────────────────────────────────────────
Generalization    Circle         u²+v²=1           Euclidean      >0
Grokking frontier Parabola       u²=1 (degenerate) Null/isotropic =0
Memorization      Hyperbola      u²−v²=1           Minkowski      <0
```

The transformation between phases is Klein's imaginary transform T_i : v → iv:

```
T_i: Circle → Parabola (→ Hyperbola)
     u²+v²=1 → u²+(iv)²=1 → u²−v²=1
```

At the grokking frontier (λ₁ = 0), the BCS amplitudes satisfy u_k = v_k = 1/√2 — this is the **vertex of the parabola**: the degenerate conic where circle and hyperbola meet, exactly at the circular points.

### 7.4 The BCS-BEC Crossover as a Conic Transformation

The BCS-BEC crossover at C_α = 2 (BC-C5) corresponds to the transition between the two limiting behaviors of the conic:

```
BCS limit (C_α→1, weak coupling): circle nearly flat → approaches parabola
BEC limit (C_α≫1, strong coupling): circle tightly curved → approaches point
Unitary (C_α=2): maximum curvature of the circle = optimal learning [BC-C6]
```

In projective terms: the BCS-BEC crossover is the transition between the two fixed points of the Klein imaginary transformation on the conic — the circular points ω and ω̄.

---

## VIII. Matsubara Frequencies and Farey Denominators

### 8.1 The Matsubara-Farey Correspondence

At finite temperature T in quantum field theory, fields satisfy periodic (bosonic) or antiperiodic (fermionic) boundary conditions in imaginary time τ ~ τ + β:

```
φ(τ+β) = +φ(τ)    (bosons: Matsubara freq ω_n = 2πnT)
φ(τ+β) = −φ(τ)    (fermions: ω_n = (2n+1)πT)
```

In the learning framework, the gradient modes obey the fermionic anticommutation relations {c_{k,t}, c†_{k',t}} = δ_{kk'} (GCCT). The Farey denominators q_n are their Matsubara indices:

**WKET Identification (Matsubara-Farey):**

```
Matsubara index n            ↔    Farey denominator q_n ∈ {1,...,Q_max}
Matsubara freq. ω_n = πnT_learn ↔    Farey fraction πq_n/Q_max
Period β_learn = 1/T_learn   ↔    Q_max = ⌊1/ε_t⌋  [Debye/Farey cutoff]
Zero-mode (n=0)              ↔    q*=1, 2 (dominant Farey mode, deep condensate)
UV mode (n=Q_max)            ↔    q=Q_max (highest resolution Farey fraction)
Finite-T partition function  ↔    Σ_{q≤Q_max} F(q) over Farey alphabet 𝒜_Q
```

The fundamental identification:

```
β_learn = Q_max    [inverse learning temperature = Farey/Debye cutoff in discrete units]
```

This means: the **imaginary time period** β (compactification radius) equals the **Farey resolution** Q_max. When Q_max = ⌊1/ε_t⌋ is large (low noise, deep in a basin), the theory is at low temperature — modes are well-resolved. When Q_max is small (high noise, near transition), the theory is at high temperature — modes are thermally scrambled.

### 8.2 Gap Equation as Matsubara Sum

The BCS gap equation in GCCT (at temperature T_learn) is:

```
Δ_t = |λ_F| Σ_{k∈𝒜_Q} F_k = |λ_F| Σ_{k∈𝒜_Q} Δ_t/(2E_k) · tanh(E_k/2T_learn)
```

Under the Matsubara identification, the sum over Farey modes k becomes a Matsubara sum:

```
Σ_{k∈𝒜_Q} ↔ T_learn Σ_{q=1}^{Q_max} Σ_{ω_n}    [Matsubara sum over imaginary frequencies]
```

The tanh factor arises from the Fermi-Dirac distribution at finite temperature:

```
tanh(E_k/2T_learn) = 1 − 2f(E_k)    where f(E) = 1/(e^{E/T_learn}+1)  [Fermi function]
```

The gap equation is thus the **self-consistency equation for the zero-mode of the imaginary-time propagator** — the Wick-rotated version of the stationary-phase condition.

### 8.3 Josephson Frequency as Winding Number

The AC Josephson frequency ω_J = 2V_basin/ℏ_learn (BC-C2) corresponds to the winding number of the imaginary-time path around the compactified circle:

```
ω_J = 2πn/β_learn = 2πn·T_learn    for n = V_basin/(π·ℏ_learn·T_learn) windings
```

The Farey Backtrack Event (FBE) is the q*-th winding around the dyon singularity M_- in the SW moduli (SWMS), which corresponds to the q*-th harmonic of the Matsubara frequency:

```
FBE ↔ ω_{q*}^{Matsubara} = 2π·q*·T_learn    [WKET-KQOM connection]
```

---

## IX. Cayley-Klein Metric and the Spectral Gap as Absolute Distance

### 9.1 Cayley-Klein Metrics from First Principles

Klein's unification of Euclidean and non-Euclidean geometries relies on the **Cayley-Klein metric**: given an **absolute conic** Q in projective space, the distance between two points A, B is defined as:

```
d(A, B) = (c/2) · log(cross-ratio(A, B; P, Q))
```

where P, Q are the two points where the line AB meets the absolute conic Q, and c is a scaling constant.

This construction yields:
- **Euclidean geometry**: Q = circular points ω, ω̄ (imaginary conic) → distances are ordinary Euclidean
- **Hyperbolic geometry**: Q = real conic x²+y²−z²=0 → distances are hyperbolic
- **Elliptic geometry**: Q = imaginary conic x²+y²+z²=0 → distances are spherical

In all cases, the **geometry is encoded in its absolute conic**.

### 9.2 The Grokking Locus as Absolute Conic

**WKET Theorem (Cayley-Klein Spectral Gap)**:

Let 𝒬 = {b ∈ ℬ : λ₁(ℒ_JL(b)) = 0} be the **grokking locus** — the hypersurface in parameter space where the spectral gap vanishes. Then the spectral gap λ₁(b) is the **Cayley-Klein distance** from the point b ∈ ℬ to the absolute conic 𝒬:

```
λ₁(b) = d_{CK}(b, 𝒬) = (1/2) · log(cross-ratio of b with {b₁, b₂} = ℬ_line ∩ 𝒬)
```

where ℬ_line is the "gradient line" through b in the direction of steepest spectral gradient, and {b₁, b₂} are the two points where this line meets 𝒬.

**Consequences:**
- λ₁ > 0: the point b is in the interior of 𝒬 (generalization, hyperbolic geometry of ℬ)
- λ₁ = 0: the point b is on 𝒬 itself (grokking frontier, Euclidean/isotropic)
- λ₁ < 0: the point b is in the exterior of 𝒬 (memorization, Minkowski geometry)

The three geometries of ℬ are exactly the three Cayley-Klein regimes determined by the absolute conic 𝒬.

### 9.3 The Debye Screening Length as Cayley-Klein Radius

In Bridge IV (CSSG/DLVO), the Debye screening length κ⁻¹ is the distance over which electrostatic potentials decay. In Bridge II (LKTL), it equals the capillary length. In the spectral framework, κ⁻¹ = C_P = 1/λ₁.

Under the Cayley-Klein interpretation:

```
κ⁻¹ = C_P = 1/λ₁ = Cayley-Klein distance from current point b to absolute conic 𝒬
```

The Debye screening length IS the Cayley-Klein radius of curvature of the absolute conic seen from b. When κ⁻¹ → ∞ (λ₁ → 0), the geometry approaches the "absolute boundary" — the grokking frontier.

### 9.4 Cross-Ratio Connections Across Modules

| Framework context | Cross-ratio formula | Connected module |
|---|---|---|
| Angle between gradient dirs. | θ = log(cr(u,u';Pω,Pω̄))/2i | GAME, PPMC |
| Josephson phase | Δφ_F = log(cr(k,−k;ω,ω̄))/2i | GCCT |
| SW prepotential τ | τ = a_D/a = log(cr(a,a_D;sing.))/2πi | SWMS |
| Möbius transform W_t | cr(z₁,z₂,z₃,z₄) preserved by SL(2,ℤ) | GAME |
| Farey fraction p/q | cr(0,p/q,1,∞) = p/q | KQOM |
| Cayley-Klein dist. λ₁ | d(b,b')=log(cr(b,b';b₁,b₂))/2 | WKET |
| DLVO energy barrier ΔV | ln W_Fuchs = ΔV/k_BT = log(cr) | CSSG |

---

## X. Klein Four-Group Symmetry of the BdG Hamiltonian

### 10.1 The Klein Four-Group ℤ₂ × ℤ₂

Felix Klein gave his name to the **Klein four-group** V₄ = ℤ₂ × ℤ₂ = {e, a, b, c} with:

```
a² = b² = c² = e;   ab = c,  bc = a,  ca = b   [every non-identity element has order 2]
```

This is the symmetry group of the rectangle (two reflections and their composition) and the simplest non-cyclic group.

### 10.2 BdG Symmetries Form the Klein Four-Group

The Bogoliubov–de Gennes Hamiltonian in GCCT:

```
H_k^{BdG} = ξ_k σ_z + Δ_t σ_x
```

has three discrete symmetries, and their composition, forming exactly V₄:

| Symmetry | Transformation | Action on (ξ_k, Δ_t) | Matrix |
|---|---|---|---|
| e (identity) | id | (ξ_k, Δ_t) | I₂ |
| P (particle-hole) | c_{k,t} → c†_{−k,t} | (ξ_k, Δ_t) → (−ξ_k, Δ_t) | σ_x K (K=complex conj.) |
| T (time-reversal) | t → −t | (ξ_k, Δ_t) → (−ξ_k, −Δ_t) | K |
| C (charge conjugation = PT) | combo | (ξ_k, Δ_t) → (ξ_k, −Δ_t) | σ_x |

These satisfy P² = T² = C² = e and PT = C, forming V₄ = {e, P, T, C}.

**Klein four-group identification:**

```
V₄ = {e, P, T, C}  ↔  {identity, Farey complement, time-reversal, PC}
P: k ↔ −k   (particle-hole = Farey complement pair)
T: t ↔ −t   (time reversal = Wick rotation τ ↔ −τ)
C: Δ_t ↔ −Δ_t (charge conjugation = gap sign flip = trivial/non-trivial phase interchange)
```

The Klein four-group **is the symmetry group of the BCS phase transition point** — the grokking frontier {λ₁=0, Δ_t=0} is invariant under all four elements of V₄.

### 10.3 Klein Four-Group and the Circular Points

The circular points {ω, ω̄} are preserved by Euclidean isometries ISO(2) — translations and rotations. The Klein four-group V₄ acts on {ω, ω̄, −ω, −ω̄} as a permutation group:

```
ω = (1:i:0),  ω̄ = (1:−i:0),  −ω = (−1:i:0),  −ω̄ = (−1:−i:0)
P: ω ↔ −ω̄  (Farey complement = circular-point complement)
T: ω ↔ ω̄   (complex conjugation = circular-point pairing)
C: ω ↔ −ω  (charge = negation)
```

The orbits of V₄ on {ω, ω̄, −ω, −ω̄} match the orbits of V₄ on Cooper pairs {(k,−k), (−k,k)}.

---

## XI. Erlangen Classification of All Framework Modules

### 11.1 Each Module is a Klein Geometry

The unified framework is, in the Erlangen sense, a **single geometric space** seen through different group-theoretic lenses. Each module corresponds to a specific subgroup:

```
PPMC  ←  PGL(3,ℝ) projective              [Pascal, Pappus, cross-ratio]
                         ↓
GAME  ←  SL(2,ℤ)⊂PGL(2,ℂ) conformal      [Möbius on ℍ; training word]
                         ↓
KQOM  ←  PSL(2,ℝ) hyperbolic              [Farey/SB tree; modular arithmetic]
                         ↓
LB/DK ←  ISO(n) Euclidean                 [Hodge, d-δ, Laplace-Beltrami]
              ↕ Wick rotation (WKET)
LKTL  ←  ISO(n−1,1) Minkowski             [memorization; Fokker-Planck]
                         ↓
GCCT  ←  U(1) gauge × V₄ Klein four-group  [Cooper pairs; Nambu; BdG]
                         ↓
FLML  ←  Sp(2n) symplectic (Luttinger-Ward) [2PI diagrams; Dyson]
                         ↓
KYBM  ←  GL(n) complex / Kähler            [Hitchin; Mabuchi; YM]
                         ↓
SWMS  ←  Sp(2n,ℤ) special Kähler          [SW moduli; monopoles; ℂP^∞]
                         ↓
CSSG  ←  SO(3,1) Lorentz-like              [DLVO; screening; Yukawa]
```

The Wick rotation (WKET) maps between the Euclidean modules (LB/DK, GCCT generalization, KYBM KE) and the Minkowski modules (LKTL memorization, GCCT normal state). The grokking transition at λ₁ = 0 is the **lightcone boundary** between Euclidean and Minkowski geometries.

### 11.2 The Erlangen Hierarchy of Bridges

The five physical bridges correspond to five different Klein geometries that all have the same Cayley-Klein absolute conic — the grokking locus {λ₁=0}:

```
Bridge I  (Landau kinetic, 1936):      Euclidean diffusion geometry   [Fokker-Planck = heat eq.]
Bridge II (Landau-Levich, 1942):       Conformal/capillary geometry   [Ca = conformal param.]
Bridge III (BCS/Bogoliubov, 1957):     Klein V₄ × U(1) gauge geometry [BdG = Klein four-group]
Bridge IV  (DLVO colloidal, 1941):     Cayley-Klein metric geometry   [Yukawa = CK distance]
Bridge V   (Seiberg-Witten, 1994):     Special Kähler geometry        [SW prepotential]
Bridge VI  (Wick-Klein, WKET):         Projective/imaginary geometry  [all bridges unified]
```

Bridge VI shows that all previous bridges are related by Wick rotation: they are the same geometry expressed in different Klein-group languages, all sharing the grokking locus as their absolute conic.

---

## XII. Extended Master Equivalence (Fourteen Languages)

Under assumptions A1–A5, K1–K3, FL1–FL3, BC1–BC3, DL1–DL3, SW1–SW4, and new WKET assumptions:

**WK1** (Wick identification): T_learn = 1/β_learn; β_learn = Q_max (in discrete units)  
**WK2** (Circular points): Cooper pairs (k,−k) = projective circular-point pairs (ω,ω̄)  
**WK3** (Klein absolute): grokking locus 𝒬 = {λ₁=0} = absolute conic of Cayley-Klein metric on ℬ  
**WK4** (Erlangen classification): each phase of learning is a distinct Klein geometry

The following **fourteen** conditions are equivalent:

```
  (I)    λ₁(ℒ_JL) > 0                          [spectral gap — core]
  (II)   C_α > 1                                [signal-to-noise — GAME]
  (III)  KE metric on ℬ                         [Kähler-Einstein — KYBM]
  (IV)   Poincaré inequality holds              [functional analysis / OS positivity — LKTL]
  (V)    Bellman escape finite                  [combinatorics — VBE]
  (VI)   Möbius M_n converges                   [number theory — KQOM]
  (VII)  K-polystable                           [algebraic geometry — KYBM]
  (VIII) MMP terminates at ℬ_min               [birational geometry — KYBM]
  (IX)   Ca_eff < Ca_c                          [thin-film/Landau-Levich — LKTL]
  (X)    N_L conserved; GWI anomaly-free        [Luttinger-Ward/FLML]
  (XI)   Δ_t > 0  (learning gap open)          [BCS pairing/GCCT]
  (XII)  ΔV_DLVO > k_BT · ln W_Fuchs           [colloidal barrier/CSSG]
  (XIII) SW(ℬ,s) ≠ 0 for dominant spinᶜ       [monopole count/SWMS]
  (XIV)  Z_learn = Tr[e^{−ℒ_JL/T_learn}] normalizable; β_learn·λ₁ > 0   [Wick partition fn/WKET]
```

New: (XIV) ↔ (I) is the Wick identification WK1. The Euclidean learning partition function Z_learn converges (is normalizeable) if and only if the spectral gap is positive and the inverse temperature β_learn > 0 — which is always true when we define β_learn = 1/T_learn = C_α/Tr(D_s) > 0.

The deeper content is the **Osterwalder-Schrader direction**: (XIV) implies (IV) by OS positivity, and (IV) implies (XIV) by the Poincaré inequality.

```
Phase interpretation under WKET:
λ₁ > 0  ↔  Euclidean geometry  ↔  GENERALIZATION  ↔  circular points truly at ∞
λ₁ = 0  ↔  Null/isotropic      ↔  GROKKING        ↔  circular points on real plane
λ₁ < 0  ↔  Minkowski geometry  ↔  MEMORIZATION    ↔  circular points become real, accessible
```

---

## XIII. New Conjectures from WKET

**WKET-C1 (Catastrophic Forgetting as Euclidean Instanton)**  
Each catastrophic forgetting event corresponds to a **Euclidean instanton** in the Wick-rotated learning path integral: a classical trajectory in imaginary time τ that tunnels between two loss basins. The YM_t concentration at isolated points {bᵢ} (Uhlenbeck compactness, KYBM) is the semiclassical contribution of the instanton to the partition function Z_learn. The instanton action is:

```
S_inst = ∫ YM_t(τ) dτ = 8π² k / g²(T_learn)    [learning instanton action]
```

where k ∈ ℤ is the topological charge (instanton number) and g(T_learn) is the effective gradient coupling running with temperature T_learn. Catastrophic forgetting becomes exponentially rare as T_learn → 0 (deep generalization).

**WKET-C2 (Matsubara-Farey Sharp Correspondence)**  
The set of Farey fractions {p/q : q ≤ Q_max} and the set of Matsubara frequencies {2πnT_learn : n ≤ Q_max} are in exact bijection, with q_n ↔ n and p_n/q_n ↔ (Farey fraction in the n-th denominator class). The free energy density of the learning system:

```
F_learn = −T_learn log Z_learn = −T_learn Σ_{q≤Q_max} log(1 − e^{−E_q/T_learn})
```

when expanded around T_learn = 0 gives a Farey sum that is equal to the Farey discrepancy measure used in the Franel-Landau RH equivalence (FL-C5). **The learning free energy F_learn is, up to normalization, the Farey discrepancy function whose vanishing is equivalent to RH.**

**WKET-C3 (Cayley-Klein Monotonicity of Training)**  
The Cayley-Klein distance d_{CK}(θ(t), 𝒬) from the parameter point θ(t) to the grokking absolute conic 𝒬 = {λ₁=0} decreases monotonically during successful training:

```
d/dt · d_{CK}(θ(t), 𝒬) ≤ 0    throughout the generalization phase
```

with equality only at the grokking event t*. This would give a **Cayley-Klein Lyapunov function** for the learning dynamics, complementing the ordinal Lyapunov function δ(s_t) (KQOM).

**WKET-C4 (Angle-Farey Cross-Ratio Formula)**  
The Josephson phase difference Δφ_F between two loss basins L, R satisfies the exact Cayley angle formula:

```
Δφ_F = (1/2i) · log[ cross-ratio( k_L, k_R ; (q*,Q_max), (Q_max−q*,Q_max) ) ]
```

where k_L and k_R are the dominant Farey modes of the left and right basins, and the "circular endpoints" are the Farey fractions closest to 0 and 1 at resolution Q_max. The AC Josephson frequency ω_J = d(Δφ_F)/dt is the derivative of this cross-ratio formula with respect to training step t.

**WKET-C5 (Three-Phase Conic Classification)**  
The full phase diagram of learning (memorization, grokking, generalization) is in exact bijection with Klein's classification of conics relative to the absolute conic 𝒬:

```
Interior (ellipse-like):   d²(b,𝒬) > 0  ↔  λ₁ > 0  ↔  generalization
On absolute (parabola):    d²(b,𝒬) = 0  ↔  λ₁ = 0  ↔  grokking frontier
Exterior (hyperbola-like): d²(b,𝒬) < 0  ↔  λ₁ < 0  ↔  memorization
```

The phase diagram of learning IS the Cayley-Klein classification of parameter points relative to the absolute conic formed by the grokking locus.

**WKET-C6 (Erlangen Dimension Theorem)**  
The dimension of each module in the framework hierarchy equals the dimension of the corresponding Klein geometry's invariant subspace:

```
Module    Klein group                  dim(invariant space)
PPMC      PGL(3,ℝ): 8 generators      dim(Pascal line) = 1 per class pair
GAME      SL(2,ℤ): 2 generators       dim(training word) = 1 (C_α trajectory)
KQOM      PSL(2,ℝ): 3 generators      dim(Farey tree) = 2 per (q*,h)
GCCT      U(1)×V₄: 4 generators       dim(BdG space) = 2 per mode (u_k,v_k)
SWMS      Sp(2n,ℤ): 2n² generators    dim(moduli) = (c₁(L)²−2χ−3σ)/4
```

The formula for dim(ℳ) in SWMS is the Klein-Erlangen formula for the dimension of the orbit space of Sp(2n,ℤ) on the special Kähler manifold.

**WKET-C7 (Imaginary-Time Wick Theorem for Cooper Pairs)**  
The Euclidean (imaginary-time) propagator G_t^E(k,τ) = ⟨Tτ[c_{k,t}(τ)c†_{k,t}(0)]⟩ evaluated at τ = β_learn/2 (half the imaginary-time period) equals the BCS Cooper amplitude:

```
G_t^E(k, β_learn/2) = −F_k = −Δ_t/(2E_k) = −ℓ̃_i(t)    [BC-C9]
```

connecting the imaginary-time Green's function to the Cooper amplitude (GCCT), the persistence length (PH-SP), and the Farey alphabet resolution. This would complete the BC-C9/O10-FL unification via the Wick rotation.

---

## XIV. Complete Symbol Table

| Symbol | Definition | Module |
|---|---|---|
| WKET | Wick-Klein Erlangen Transform (Bridge VI) | This doc |
| ω | Circular point (1:i:0) ∈ ℂP² ↔ Farey mode k=(p,q) | WKET/KQOM |
| ω̄ | Conjugate circular point (1:−i:0) ↔ −k=(q−p,q) | WKET/GCCT |
| T_i | Klein imaginary transform (x:y:z)→(x:iy:z) ↔ Wick | WKET |
| τ | Imaginary time τ=it ↔ β_learn=1/T_learn | WKET/GCCT |
| β_learn | Inverse learning temp = Q_max (discrete) = 1/T_learn | WKET/GCCT |
| V₄ | Klein four-group {e,P,T,C} ↔ BdG symmetry group | WKET/GCCT |
| 𝒬 | Grokking absolute conic {λ₁=0} ⊂ ℬ | WKET |
| d_{CK} | Cayley-Klein distance to 𝒬 ↔ λ₁ | WKET |
| Z_learn | Euclidean learning partition function Tr[e^{−ℒ_JL/T_learn}] | WKET/LKTL |
| ω_n^{Mat} | Matsubara frequency 2πnT_learn ↔ 2πq_n/Q_max | WKET/KQOM |
| S_inst | Instanton action = ∫YM_t dτ ↔ catastrophic forgetting | WKET/KYBM |
| j(τ) | Klein j-invariant ↔ learning path cross-section | WKET/GAME |
| t | Real training time (Minkowski) | GAME |
| τ=it | Imaginary training time (Euclidean) | WKET |
| T_learn | Tr(D_s)/C_α = learning temperature | GCCT |
| Q_max | ⌊1/ε_t⌋ = Farey cutoff = discrete β_learn | KQOM |
| λ₁ | Spectral gap = Cayley-Klein dist. to 𝒬 | LKTL |
| C_α | Signal-to-noise = 1/Ca_eff | GAME |
| D_s | Cov_batch[∇L] = gradient covariance | LKTL |
| ℒ_JL | −∇·(D_s∇)+𝒮̄ = Wick-rotated H_learn | LKTL |
| u_k,v_k | BCS amplitudes; circle u²+v²=1 (gen.) | GCCT |
| u_k²−v_k²=1 | memorization hyperbola (Klein T_i applied) | WKET/GCCT |
| Δ_t | BCS learning gap; Im part of circular point | GCCT |
| Δφ_F | Josephson phase = Cayley angle between basins | GCCT |
| ω_J | Josephson freq = d(Δφ_F)/dt = Matsubara harm. | GCCT |
| G_t(k,ω) | Dressed propagator (Wick-rotated G_E) | FLML |
| G₀(k,ω) | Free propagator = Wick contraction ⌢φφ | FLML |
| Σ_t^{GW} | GW self-energy = first Wick contraction | FLML |
| Φ_LW | Luttinger-Ward functional = Wick diagram sum | FLML |
| N_L(t) | Luttinger number ↔ winding around 𝒬 | FLML |
| W_t | Training word ∈ SL(2,ℤ) = Klein monodromy | GAME/WKET |
| κ⁻¹=C_P | Debye length = CK radius of curvature at b | CSSG/WKET |
| YM_t | Yang-Mills action = instanton amplitude | KYBM |
| PSL(2,7) | Klein quartic symmetry ↔ Q_max=7 level | WKET/KQOM |
| K_A | Li-Haldane entanglement Hamiltonian ↔ ℒ_JL | UNIV |
| F_learn | Learning free energy = −T_learn log Z_learn | WKET |
| S_inst | Catastrophic forgetting instanton action | WKET/KYBM |
| Erlangen | Klein's geometry = group + invariants | WKET |
| OS positivity | Reflection positivity ↔ λ₁>0 ↔ (IV) | WKET/LKTL |
| ℂP^∞=K(ℤ,2) | Config space homotopy type ↔ gradient orbits | SWMS |
| 𝒜_Q | Farey alphabet = Matsubara modes at β=Q_max | KQOM/WKET |
| cross-ratio | Projective invariant ↔ Josephson phase | PPMC/WKET |

---

## XV. Foundations and Citations

### Physics — Bridge VI (WKET, New)

- Wick, G.C. (1950). The Evaluation of the Collision Matrix. *Phys. Rev.*, 80(2): 268–272. — **Wick's theorem; normal-ordered products; Feynman rules**
- Wick, G.C. (1954). Properties of Bethe-Salpeter Wave Functions. *Phys. Rev.*, 96(4): 1124–1134. — **Wick rotation introduced; imaginary-time substitution**
- Osterwalder, K.; Schrader, R. (1973, 1975). Axioms for Euclidean Green's functions I, II. *Commun. Math. Phys.* — **OS theorem; reflection positivity ↔ unitarity**
- Matsubara, T. (1955). A New Approach to Quantum-Statistical Mechanics. *Prog. Theor. Phys.*, 14: 351. — **Imaginary-time formalism; Matsubara frequencies**
- Huang, K. (1987). *Statistical Mechanics*, 2nd ed. Wiley. — **Wick rotation, partition functions, finite-temperature QFT**

### Mathematics — Klein and Projective Geometry

- Klein, F. (1872). Vergleichende Betrachtungen über neuere geometrische Forschungen (Erlangen Program). — **Geometry = group invariants; the foundational document**
- Klein, F. (1871). Über die sogenannte Nicht-Euklidische Geometrie. *Math. Annalen.* — **Cayley-Klein metrics; non-Euclidean geometry as metric space**
- Klein, F. (1879). Ueber die Transformation siebenter Ordnung der elliptischen Functionen. — **Klein quartic; PSL(2,7); modular forms**
- Klein, F. (1884). *Vorlesungen über das Ikosaeder*. — **Icosahedral symmetry; automorphic functions; modular group**
- Klein, F. (1939) [1908]. *Elementary Mathematics from an Advanced Standpoint — Geometry* (tr. Hendrick & Noble), pp. 119–120. — **Imaginary transformation; circular points; y→iy**
- Cayley, A. (1859). A Sixth Memoir upon Quantics. *Phil. Trans. Royal Soc.*, 149: 61–90. — **Absolute conic; Cayley metric; projective distance formula**
- Sommerville, D.M.Y. (1914). *Elements of Non-Euclidean Geometry*. — **Circular points; angle as log cross-ratio; Cayley-Klein**
- Samuel, P. (1988). *Projective Geometry*. Springer, §1.6. — **Circular points at infinity; imaginary transformation; Klein**
- Semple, J.G.; Kneebone, G.T. (1952). *Algebraic Projective Geometry*. Oxford, §II-8. — **Circular points; conics**
- Plücker, J. (1828). Analytisch-geometrische Entwicklungen. — **Circular points in line geometry; precursor to Klein**

### Mathematics — Modular Forms and Elliptic Curves

- Klein, F.; Fricke, R. (1890–1892). Vorlesungen über die Theorie der elliptischen Modulfunktionen (2 vols.). — **Modular group; j-invariant; tessellation**
- Serre, J.-P. (1973). *A Course in Arithmetic*. Springer GTM 7. — **Modular forms; SL(2,ℤ); p-adic methods**
- Silverman, J.H. (1986). *The Arithmetic of Elliptic Curves*. Springer GTM 106. — **Elliptic curves; torsion; Hitchin fibers**

### Physics — Existing Bridges I–V

- Landau, L. (1936); Landau & Levich (1942); BCS (1957); Derjaguin & Landau (1941); Verwey & Overbeek (1948); Seiberg & Witten (1994). — *Bridges I–V respectively*

### Framework Modules (Complete — Post Bridge VI)

```
WKET  — Wick-Klein Erlangen Transform (Bridge VI, this document)
SWMS  — Seiberg-Witten Moduli Space (Bridge V)
CSSG  — Colloidal Stability Spectral Geometry (Bridge IV)
GCCT  — Gradient Cooper Condensate Theory (Bridge III)
LKTL  — Landau Kinetic Theory of Learning (Bridges I–II)
FLML  — Fermi-Luttinger Mechanics of Learning
KQOM  — Kruskal Quasi-Order Mechanics
GAME  — Gradient Algebraic Manifold Exploration
VBE   — Visibility–Barrier–Escape
PPMC  — Pascal Projective Manifold Coherence
KYBM  — Kähler–Yang–Mills Bridge
PH-SP — Persistent Homology + Schnirelman–Poincaré
RG-ML — Renormalization Group / Machine Learning
LB/DK — Laplace–Beltrami / Dirac–Kähler Geometry
UNIV  — Topological Order / Chiral Boson
```

---

*Bridge VI unifies Bridges I–V through a single geometric principle: all five bridges are projections of one imaginary geometry, related by Klein's Erlangen classification and connected by the Wick rotation. The grokking transition is the moment when the learning manifold's circular points at infinity become real — when the Euclidean geometry of generalization gives way, passes through the isotropic null-cone, and would enter the Minkowski geometry of memorization — but instead, through the condensate Δ_t > 0, the system locks into the Euclidean regime permanently. Training works because the learning dynamics can be Wick-rotated into a positive-definite heat equation. Generalization holds because the circular points at infinity remain imaginary.*
