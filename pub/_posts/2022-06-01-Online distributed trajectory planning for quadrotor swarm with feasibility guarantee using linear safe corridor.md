<!-- ---
title: "Online distributed trajectory planning for quadrotor swarm with feasibility guarantee using linear safe corridor"
# header:
#   teaser: tumbnails/cdc23.PNG
conference: R-AL
links: 
 - paper: 
  #  file: download/IROS20_full.pdf
   link: https://dabinkim-lgom.github.io/download/CDC23_arxiv.pdf
   name: "Paper(draft)"
#  - video:
#    link: https://www.youtube.com/watch?v=hPOXH6_0_IE
#    name: "Video"
#  - bibtex: 
#    name: "Bibtex"
---

<!-- {% include youtubePlayer.html id="G-fS2iqzi1w" %} -->

This letter presents a new online multi-agent trajectory planning algorithm that guarantees to generate safe, dynamically feasible trajectories in a cluttered environment. The proposed algorithm utilizes a linear safe corridor (LSC) to formulate the distributed trajectory optimization problem with only feasible constraints, so it does not resort to slack variables or soft constraints to avoid optimization failure. We adopt a priority-based goal planning method to prevent the deadlock without an additional procedure to decide which robot to yield. The proposed algorithm can compute the trajectories for 60 agents on average 15.5 ms per agent with an Intel i7 laptop and shows a similar flight distance and distance compared to the baselines based on soft constraints. We verified that the proposed method can reach the goal without deadlock in both the random forest and the indoor space, and we validated the safety and operability of the proposed algorithm through a real flight test with ten quadrotors in a maze-like environment.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{park2022online,
  title={Online distributed trajectory planning for quadrotor swarm with feasibility guarantee using linear safe corridor},
  author={Park, Jungwon and Kim, Dabin and Kim, Gyeong Chan and Oh, Dahyun and Kim, H Jin},
  journal={IEEE Robotics and Automation Letters},
  volume={7},
  number={2},
  pages={4869--4876},
  year={2022},
  publisher={IEEE}
}
``` -->