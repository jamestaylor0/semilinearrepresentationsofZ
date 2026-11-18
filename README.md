# Semilinear Representations of $\mathbb{Z}$ - Magma Code

This repository conditions magma code to accompany the paper [A Normal Form for Invertible Semilinear Maps and the Category of Isocrystals Over a Finite Field](https://arxiv.org/abs/2611.23162)

Below we describe the contents of each file. These are implemented primarily for number fields - in some cases this is necessary, but most work more generally. For more details on the algorithms, see the final section of the associated paper.

---

### Running Files

To run the code without a magma installation, one can use the online magma calculator: https://magma.maths.usyd.edu.au/calc/

Some files call others, so in this case the contents of the called file need to be pasted in first.

---


### Questions and Mistakes

For any mistakes found, or questions relating to this repository, please contact us (the authors). We are more than happy to help, including with providing assistance with helping run any of the code found here.

---
---
---

### The Generalised Jordan Normal Form: GJNF.magma
    
This takes in a field $L$, and a square matrix $A$, and return the primary decomposition of $A$, and the corresponding generalised Jordan normal form of $A$. This works over any field $L$ for which there is a factorisation algorithm.

---
---

### Testing $\sigma$-Conjugacy: sigmaconjugacy.magma

This takes in a field $L$ and a finite order automorphism $\sigma$, and two invertible square matrices $A$ and $B$ over $L$ of the same dimension. It determines if $A$ and $B$ are $\sigma$-conjugate.

---
---

### Lifting Representatives for Semilinear Normal Form: liftingrepresentatives.magma
    
This takes in a number field $L$, and a finite order automorphism $\sigma$ of order $r$. Input: an irreducible monic polynomial $p(x)$, a root $\alpha$ in $\overline{L}$, and a solution $A \in \text{GL}_m(L(\alpha))$ to $N_m^{\tau_{\alpha}}(A) = \alpha I_m$, where $m = m_L^{\sigma}(p(x))$. Output: a representative for the corresponding indecomposable representation of $Z$ over $L$ module of any prescribed level $t \geq 1$.

---
---

### Compute Semilinear Schur Index over Number Field: SLschurindexnumberfield.magma
    
This takes in a number field $L$, and a finite order automorphism $\sigma$ of order $r$. For an irreducible monic polynomial $p(x) \neq x$ over $L$, returns $m_L^{\sigma}(p(x))$, the semilinear Schur index of $p(x)$.

---
---

### Compute Semilinear Normal Form Factors: semilinearnormalformfactors.magma
    
This takes in a number field $L$, and a finite order automorphism $\sigma$ of order $r$. For an invertible matrix $A$, it computes the blocks and their multiplicities appearing in the semilinear normal form of $A$. This calls ```SLschurindexnumberfield.magma``` above.

---
---

### Compute Explicit Semilinear Normal Form: SLnormalform.magma
    
This takes in a number field $L$, and a finite order automorphism sigma of **prime** order $r$. For an invertible matrix $A$, this computes a matrix in semilinear normal form which is $\sigma$-conjugate to $A$.

---
---
