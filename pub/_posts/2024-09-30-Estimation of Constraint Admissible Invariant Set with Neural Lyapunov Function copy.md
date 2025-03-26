---
title: "Estimation of Constraint Admissible Invariant Set with Neural Lyapunov Function"
header:
  teaser: tumbnails/cdc24.png
conference: CDC
links: 
 - paper: 
   link: https://arxiv.org/abs/2409.19881
   name: "Paper"
#  - video:
#    link: https://www.youtube.com/watch?v=hPOXH6_0_IE
#    name: "Video"
#  - bibtex: 
#    name: "Bibtex"
---

Constraint admissible positively invariant (CAPI) sets play a pivotal role in ensuring safety in control and planning applications, such as the recursive feasibility guarantee of explicit reference governor and model predictive control. However, existing methods for finding CAPI sets for nonlinear systems are often limited to single equilibria or specific system dynamics. This limitation underscores the necessity for a method to construct a CAPI set for general reference tracking control and a broader range of systems. In this work, we leverage recent advancements in learning-based methods to derive Lyapunov functions, particularly focusing on those with piecewise-affine activation functions. Previous attempts to find an invariant set with the piecewise-affine neural Lyapunov function have focused on the estimation of the region of attraction with mixed integer programs. We propose a methodology to determine the maximal CAPI set for any reference with the neural Lyapunov function by transforming the problem into multiple linear programs. Additionally, to enhance applicability in real-time control scenarios, we introduce a learning-based approach to train the estimator, which infers the CAPI set from a given reference. The proposed approach is validated with multiple simulations to show that it can generate a valid CAPI set with the given neural Lyapunov functions for any reference. We also employ the proposed CAPI set estimation method in the explicit reference governor and demonstrate its effectiveness for constrained control.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{kim2024estimation,
  title={Estimation of Constraint Admissible Invariant Set with Neural Lyapunov Function},
  author={Kim, Dabin and Kim, H Jin},
  journal={arXiv preprint arXiv:2409.19881},
  year={2024}
}
```
