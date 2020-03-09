---
title: "Robust Real-time RGB-D Visual Odometry in Dynamic Environments via  Rigid Motion Model"
header:
  teaser: tumbnails/IROS2019.PNG
conference: IROS
links: 
 - paper: 
   link: https://arxiv.org/abs/1907.08388
   name: "Paper(draft)"
 - video:
   link: https://www.youtube.com/watch?v=G-fS2iqzi1w
   name: "Video"
 - bibtex: 
   name: "Bibtex"
---

{% include youtubePlayer.html id="G-fS2iqzi1w" %}

In the paper, we propose a robust real-time visual odometry in dynamic environments via rigid-motion model updated by scene flow. The proposed algorithm consists of spatial motion segmentation and temporal motion tracking. The spatial segmentation first generates several motion hypotheses by using a grid-based scene flow and clusters the extracted motion hypotheses, separating objects that move independently of one another. Further, we use a dual-mode motion model to consistently distinguish between the static and dynamic parts in the temporal motion tracking stage. Finally, the proposed algorithm estimates the pose of a camera by taking advantage of the region classified as static parts. In order to evaluate the performance of visual odometry under the existence of dynamic rigid objects, we use self-collected dataset containing RGB-D images and motion capture data for ground-truth. We compare our algorithm with state-of-the-art visual odometry algorithms. The validation results suggest that the proposed algorithm can estimate the pose of a camera robustly and accurately in dynamic environments.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
```
