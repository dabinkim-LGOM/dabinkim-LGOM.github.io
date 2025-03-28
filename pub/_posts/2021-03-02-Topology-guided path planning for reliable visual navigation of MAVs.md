---
title: "Topology-guided path planning for reliable visual navigation of MAVs"
header:
  teaser: tumbnails/IROS21_thumbnail.png
conference: IROS
authors:
  - Dabin Kim*
  - Gyeong Chan Kim*
  - Youngseok Jang
  - H. Jin Kim
links: 
 - paper: 
   link: https://dabinkim-lgom.github.io/download/IROS2021_final.pdf
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=hPOXH6_0_IE
   name: "Video"
excerpt: This paper proposes a perception-aware path planner for MAVs that leverages topological information to select visually rich routes, enhancing visual navigation accuracy and efficiency. By analyzing topological classes derived from Voronoi diagrams, the method outperforms sampling-based planners in both simulation and real-world tests.
---

{% include youtubePlayer.html id="hPOXH6_0_IE" %}
---

Visual navigation has been widely used for state estimation of micro aerial vehicles (MAVs). For stable visual navigation, MAVs should generate perception-aware paths which guarantee enough visible landmarks. Many previous works on perception-aware path planning focused on sampling-based planners. However, they may suffer from sample inefficiency, which leads to computational burden for finding a global optimal path. To address this issue, we suggest a perception-aware path planner which utilizes topological information of environments. Since the topological class of a path and visible landmarks during traveling the path are closely related, the proposed algorithm checks distinctive topological classes to choose the class with abundant visual information. Topological graph is extracted from the generalized Voronoi diagram of the environment and initial paths with different topological classes are found. To evaluate the perception quality of the classes, we divide the initial path into discrete segments where the points in each segment share similar visual information. The optimal class with high perception quality is selected, and a graph-based planner is utilized to generate path within the class. With simulations and real-world experiments, we confirmed that the proposed method could guarantee accurate visual navigation compared with the perception-agnostic method while showing improved computational efficiency than the sampling-based perception-aware planner.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@inproceedings{kim2021topology,
  title={Topology-guided path planning for reliable visual navigation of mavs},
  author={Kim, Dabin and Kim, Gyeong Chan and Jang, Youngseok and Kim, H Jin},
  booktitle={2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={3117--3124},
  year={2021},
  organization={IEEE}
}
```