---
title: "Safe Multimodal Replanning via Projection-based Trajectory Clustering in Crowded Environments"
header:
  teaser: # tumbnails/iccv25.png
conference: RA-L
authors:
  - Yongjae Lim
  - Seungwoo Jung
  - Dabin Kim
  - Dongjae Lee
  - H. Jin Kim
links: 
 - paper: 
   link: https://ieeexplore.ieee.org/document/11359671
   name: "Paper"
excerpt: This work introduces a fast local trajectory replanning method for autonomous robots navigating crowded 3D environments, designed to identify diverse optimal trajectories without requiring predefined initial guidance. The approach ensures safety by projecting sampled trajectories onto safe constraint sets and clustering them using the Model Predictive Path Integral framework to determine optimal control inputs. Validated through both simulations and hardware experiments with a drone, this method achieves higher success rates and enables safer navigation compared to existing techniques.
---

<!-- {% include youtubePlayer.html id="FkY7t2IeWhE" %} -->

Fast replanning of the local trajectory is essential for autonomous robots to ensure safe navigation in crowded environments, as such environments require the robot to frequently update its trajectory due to unexpected and dynamic obstacles. In such settings, relying on the single trajectory optimization may not provide sufficient alternatives, making it harder to quickly switch to a safer trajectory and increasing the risk of collisions. While parallel trajectory optimization can address this limitation by considering multiple candidates, it depends heavily on welldefined initial guidance, which is difficult to obtain in complex environments. In this work, we propose a method for identifying the multimodality of the optimal trajectory distribution for safe navigation in crowded 3D environments without initial guidance. Our approach ensures safe trajectory generation by projecting sampled trajectories onto safe constraint sets and clustering them based on their potential to converge to the same locally optimal trajectory. This process naturally produces diverse trajectory options without requiring predefined initial guidance. Finally, for each trajectory cluster, we utilize the Model Predictive Path Integral framework to determine the optimal control input sequence, which corresponds to the local maxima of a multimodal optimal trajectory distribution. We first validate our approach in simulations, achieving higher success rates than existing methods. Subsequent hardware experiments demonstrate that our fast local trajectory replanning strategy enables a drone to safely navigate crowded environments.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
```