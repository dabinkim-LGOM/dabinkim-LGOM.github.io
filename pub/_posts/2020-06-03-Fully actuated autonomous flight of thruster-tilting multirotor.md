---
title: "Fully Actuated Autonomous Flight of Thruster-Tilting Multirotor"
header:
  teaser: tumbnails/tmech20.png
conference: T-Mech
authors:
  - Seung Jae Lee
  - Dongjae Lee
  - Junha Kim
  - Dabin Kim
  - Inkyu Jang
  - H. Jin Kim
links: 
 - paper: 
   link: https://ieeexplore.ieee.org/abstract/document/9107475
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=-1MihNBS7Zw
   name: "Video"
excerpt: This article introduces the T³-multirotor, a novel fully actuated multirotor platform capable of independent six-degree-of-freedom flight through a unique tilting-thruster mechanism. A robust control algorithm is developed and validated in both simulations and experiments, showcasing the platform's ability to surpass conventional multirotor limitations.
---

{% include youtubePlayer.html id="-1MihNBS7Zw" %}

This article introduces a fully actuated multirotor flight system utilizing the tilting-thruster-type multirotor (T³-multirotor), a new type of multirotor platform that enables six-controllable-degree-of-freedom flight with minimal structural heterogeneity compared to conventional multirotor designs. This new multirotor platform consists of upper and lower parts (or thruster and fuselage parts), with a unique kinematic structure and dedicated servomechanism that controls the relative attitude between the two parts. With the new mechanism, the fuselage of the T³-multirotor can control the translational and rotational motions independently of each other, allowing six-degree-of-freedom motion that was not possible with conventional multirotors. A dedicated robust control algorithm is developed based on a thorough analysis of system dynamics to derive accurate six-degree-of-freedom motion of the platform. The flight control performance of the platform is validated through simulations and actual experiments. Several flight tasks are also performed to demonstrate the potential of the T³-multirotor in overcoming the limitations of conventional multirotors.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{lee2020fully,
  title={Fully actuated autonomous flight of thruster-tilting multirotor},
  author={Lee, Seung Jae and Lee, Dongjae and Kim, Junha and Kim, Dabin and Jang, Inkyu and Kim, H Jin},
  journal={IEEE/ASME Transactions on Mechatronics},
  volume={26},
  number={2},
  pages={765--776},
  year={2020},
  publisher={IEEE}
}
```