---
title: "Visibility-Constrained Control of Multirotor via Reference Governor"
header:
  teaser: tumbnails/cdc23.PNG
conference: CDC
authors:
  - Dabin Kim
  - Matthias Pezzutto
  - Luca Schenato
  - H. Jin Kim
links: 
 - paper: 
  #  file: download/IROS20_full.pdf
   link: https://arxiv.org/abs/2308.05334
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=SquHiHjRsMQ
   name: "Video"
excerpt: This paper presents a novel reference governor for multirotor control that enforces visibility constraints while tracking time-varying references, ensuring safe vision-based navigation. The method guarantees theoretical feasibility and is validated through both simulations and real-world experiments.
---

{% include youtubePlayer.html id="SquHiHjRsMQ" %}
---

For safe vision-based control applications, perception-related constraints have to be satisfied in addition to other state constraints. In this paper, we deal with the problem where a multirotor equipped with a camera needs to maintain the visibility of a point of interest while tracking a reference given by a high-level planner. We devise a method based on reference governor that, differently from existing solutions, is able to enforce control-level visibility constraints with theoretically assured feasibility. To this end, we design a new type of reference governor for linear systems with polynomial constraints which is capable of handling time-varying references. The proposed solution is implemented online for the real-time multirotor control with visibility constraints and validated with simulations and an actual hardware experiment.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@inproceedings{kim2023visibility,
  title={Visibility-constrained control of multirotor via reference governor},
  author={Kim, Dabin and Pezzutto, Matthias and Schenato, Luca and Kim, H Jin},
  booktitle={2023 62nd IEEE Conference on Decision and Control (CDC)},
  pages={5714--5721},
  year={2023},
  organization={IEEE}
}
```