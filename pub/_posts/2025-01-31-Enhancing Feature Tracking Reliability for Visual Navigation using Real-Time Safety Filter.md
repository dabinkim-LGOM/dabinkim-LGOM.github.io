---
title: "Enhancing Feature Tracking Reliability for Visual Navigation using Real-Time Safety Filter"
header:
  teaser: tumbnails/icra25.png
conference: ICRA
links: 
 - paper: 
   link: https://arxiv.org/pdf/2502.01092
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=pZ9nvobevcs
   name: "Video"
excerpt: This paper presents a real-time safety filter for robot navigation that maintains visual feature visibility by minimally adjusting velocity commands, ensuring reliable pose estimation even in GPS-denied environments. Validated in both simulation and real-world SLAM scenarios, the method outperforms standard controllers by preserving high-quality localization.
---

{% include youtubePlayer.html id="G-fS2iqzi1w" %}

Vision sensors are extensively used for localizing a robot's pose, particularly in environments where global localization tools such as GPS or motion capture systems are unavailable. In many visual navigation systems, localization is achieved by detecting and tracking visual features or landmarks, which provide information about the sensor's relative pose. For reliable feature tracking and accurate pose estimation, it is crucial to maintain visibility of a sufficient number of features. This requirement can sometimes conflict with the robot's overall task objective. In this paper, we approach it as a constrained control problem. By leveraging the invariance properties of visibility constraints within the robot's kinematic model, we propose a real-time safety filter based on quadratic programming. This filter takes a reference velocity command as input and produces a modified velocity that minimally deviates from the reference while ensuring the information score from the currently visible features remains above a user-specified threshold. Numerical simulations demonstrate that the proposed safety filter preserves the invariance condition and ensures the visibility of more features than the required minimum. We also validated its real-world performance by integrating it into a visual simultaneous localization and mapping (SLAM) algorithm, where it maintained high estimation quality in challenging environments, outperforming a simple tracking controller.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{kim2025enhancing,
  title={Enhancing Feature Tracking Reliability for Visual Navigation using Real-Time Safety Filter},
  author={Kim, Dabin and Jang, Inkyu and Han, Youngsoo and Hwang, Sunwoo and Kim, H Jin},
  journal={arXiv preprint arXiv:2502.01092},
  year={2025}
}
```