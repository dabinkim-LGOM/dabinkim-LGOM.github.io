---
title: "Multi-robot active sensing and environmental model learning with distributed Gaussian process"
header:
  teaser: tumbnails/ral20.png
conference: RA-L
authors:
  - Dohyun Jang
  - Jaehyun Yoo
  - Clark Youngdong Son
  - Dabin Kim
  - H. Jin Kim
links: 
 - paper: 
   link: https://ieeexplore.ieee.org/abstract/document/9144385/
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=N1KlGbbv20w
   name: "Video"
excerpt: This letter proposes a distributed multi-robot exploration algorithm that enables real-time mapping and peak-seeking in unknown environments using Gaussian process regression. The approach supports online learning, decentralized coordination, and collision avoidance, and is validated through simulations and real-world UAV experiments.
---

{% include youtubePlayer.html id="N1KlGbbv20w" %}
---

This letter deals with the problem of multiple robots working together to explore and gather at the global maximum of the unknown field. Given noisy sensor measurements obtained at the location of robots with no prior knowledge about the environmental map, Gaussian process regression can be an efficient solution to construct a map that represents spatial information with confidence intervals. However, because the conventional Gaussian process algorithm operates in a centralized manner, it is difficult to process information coming from multiple distributed sensors in real-time. In this work, we propose a multi-robot exploration algorithm that deals with the following challenges: i) distributed environmental map construction using networked sensing platforms; ii) online learning using successive measurements suitable for a multi-robot team; iii) multi-agent coordination to discover the highest peak of an unknown environmental field with collision avoidance. We demonstrate the effectiveness of our algorithm via simulation and a topographic survey experiment with multiple UAVs.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{jang2020multi,
  title={Multi-robot active sensing and environmental model learning with distributed Gaussian process},
  author={Jang, Dohyun and Yoo, Jaehyun and Son, Clark Youngdong and Kim, Dabin and Kim, H Jin},
  journal={IEEE Robotics and Automation Letters},
  volume={5},
  number={4},
  pages={5905--5912},
  year={2020},
  publisher={IEEE}
}
```