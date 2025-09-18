---
title: "HERE: Hierarchical Active Exploration for Radiance-field with Epistemic Uncertainty Minimization (Under Review)"
# header:
#   teaser: tumbnails/iccv25.png
conference: RA-L
authors:
  - Taekbeom Lee*
  - Dabin Kim*
  - H. Jin Kim
links: 
 - paper: 
#    link: https://arxiv.org/pdf/2502.01092
   name: "Paper"
 - video:
#    link: https://www.youtube.com/watch?v=pZ9nvobevcs
   name: "Video" 
excerpt: We present HERE, an active 3D reconstruction framework for neural radiance fields (NeRF) that uses uncertainty-guided exploration to efficiently generate camera trajectories for accurate and comprehensive scene reconstruction. By leveraging epistemic uncertainty and a hierarchical planning strategy, HERE achieves superior efficiency and accuracy in large, complex environments.
---

<!-- {% include youtubePlayer.html id="G-fS2iqzi1w" %} -->

We present HERE, an active 3D scene reconstruction framework for neural radiance fields (NeRF), an implicit map representation that enables high-fidelity scene reconstruction while maintaining a compact memory. Our approach centers around an active learning strategy for camera trajectory generation, enabling both efficient data acquisition and accurate scene reconstruction. The key of our approach is epistemic uncertainty quantification, which directly captures data insufficiency and exhibits a strong correlation with reconstruction errors. This allows our framework to more reliably identify unexplored or poorly reconstructed regions compared to existing methods, leading to more informed and targeted exploration. Additionally, we design a hierarchical exploration strategy that leverages learned epistemic uncertainty for both fine-grained local planning and global coverage planning, which ensures comprehendsive and efficient scene coverage, even in large and complex environments. Experiments on photorealistic datasets with indoor scene simulator validate the effectiveness of the proposed method, demonstrating its superior efficiency and accuracy in uncertainty-guided active 3D reconstruction.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
```