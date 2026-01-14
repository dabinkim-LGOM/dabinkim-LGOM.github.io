---
title: "HERE: Hierarchical Active Exploration for Radiance-field with Epistemic Uncertainty Minimization"
# header:
#   teaser: tumbnails/iccv25.png
conference: RA-L
authors:
  - Taekbeom Lee*
  - Dabin Kim*
  - Youngseok Jang
  - H. Jin Kim
links: 
 - paper: 
   link: https://arxiv.org/abs/2601.07242
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=FkY7t2IeWhE
   name: "Video" 
excerpt: We present HERE, an active 3D reconstruction framework for neural radiance fields (NeRF) that uses uncertainty-guided exploration to efficiently generate camera trajectories for accurate and comprehensive scene reconstruction. By leveraging epistemic uncertainty and a hierarchical planning strategy, HERE achieves superior efficiency and accuracy in large, complex environments.
---

{% include youtubePlayer.html id="v=FkY7t2IeWhE" %}

We present HERE, an active 3D scene reconstruction framework based on neural radiance fields, enabling high-fidelity implicit mapping. Our approach centers around an active learning strategy for camera trajectory generation, driven by accurate identification of unseen regions, which supports efficient data acquisition and precise scene reconstruction. The key to our approach is epistemic uncertainty quantification based on evidential deep learning, which directly captures data insufficiency and exhibits a strong correlation with reconstruction errors. This allows our framework to more reliably identify unexplored or poorly reconstructed regions compared to existing methods, leading to more informed and targeted exploration. Additionally, we design a hierarchical exploration strategy that leverages learned epistemic uncertainty, where local planning extracts target viewpoints from high-uncertainty voxels based on visibility for trajectory generation, and global planning uses uncertainty to guide large-scale coverage for efficient and comprehensive reconstruction. The effectiveness of the proposed method in active 3D reconstruction is demonstrated by achieving higher reconstruction completeness compared to previous approaches on photorealistic simulated scenes across varying scales, while a hardware demonstration further validates its real-world applicability.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
```