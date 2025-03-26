---
title: "Aerial manipulation using model predictive control for opening a hinged door"
header:
  teaser: tumbnails/icra20.png
conference: ICRA
authors:
  - Dongjae Lee
  - Hoseong Seo
  - Dabin Kim
  - H. Jin Kim
links: 
 - paper: 
   link: https://ieeexplore.ieee.org/abstract/document/9197524/
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=uakQwNUzHWc
   name: "Video"
excerpt: We present a multirotor-based aerial manipulator capable of interacting with a moving structure—a hinged door—using model predictive control and robust trajectory tracking. The proposed system enables real-time, collision-aware manipulation of constrained environments, validated through hardware experiments.
---

{% include youtubePlayer.html id="uakQwNUzHWc" %}
---

Existing studies for environment interaction with an aerial robot have been focused on interaction with static surroundings. However, to fully explore the concept of an aerial manipulation, interaction with moving structures should also be considered. In this paper, a multirotor-based aerial manipulator opening a daily-life moving structure, a hinged door, is presented. In order to address the constrained motion of the structure and to avoid collisions during operation, model predictive control (MPC) is applied to the derived coupled system dynamics between the aerial manipulator and the door involving state constraints. By implementing a constrained version of differential dynamic programming (DDP), MPC can generate position setpoints to the disturbance observer (DOB)-based robust controller in real-time, which is validated by our experimental results. 

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@inproceedings{lee2020aerial,
  title={Aerial manipulation using model predictive control for opening a hinged door},
  author={Lee, Dongjae and Seo, Hoseong and Kim, Dabin and Kim, H Jin},
  booktitle={2020 IEEE International Conference on Robotics and Automation (ICRA)},
  pages={1237--1242},
  year={2020},
  organization={IEEE}
}
```