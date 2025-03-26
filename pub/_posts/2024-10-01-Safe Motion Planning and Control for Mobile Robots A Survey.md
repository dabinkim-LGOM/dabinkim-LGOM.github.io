---
title: "Safe Motion Planning and Control for Mobile Robots: A Survey"
header:
  teaser: tumbnails/ijcas24.png
conference: IJCAS
links: 
 - paper: 
   link: https://link.springer.com/article/10.1007/s12555-024-0784-5
   name: "Paper"
---

Control engineering has made significant progress in addressing various challenges for real-world applications. For the next stage of robotics automation, it is necessary to guarantee formal safety as well as conventional control tasks including set point stabilization and trajectory tracking. This survey focuses on a review of safe motion planning and control, especially for mobile robots. We explore various advancements in safety-critical control problems that can ultimately be formulated as an ideal infinite-horizon optimal control, and classify them into two clusters: 1) receding horizon methods and 2) safety filtering approaches. Receding horizon methods, such as nonlinear model predictive control (NMPC) and reachability-based receding horizon motion planning, use finite-horizon sliding windows for tractability. Safety filtering methods, employing techniques such as control barrier function (CBF) and reference governor (RG), adjust nominal signals to enforce safety. This survey highlights the challenges of ensuring safety in dynamic and complex environments where mobile robots are deployed, where their computational limitations and uncertainties in dynamic models are significant factors. By providing a comprehensive review of current methodologies and specifying future research directions, we aim to offer a solid foundation for developing efficient safety-critical control methodologies for mobile robots.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{hwang2024safe,
  title={Safe Motion Planning and Control for Mobile Robots: A Survey},
  author={Hwang, Sunwoo and Jang, Inkyu and Kim, Dabin and Kim, H Jin},
  journal={International Journal of Control, Automation and Systems},
  volume={22},
  number={10},
  pages={2955--2969},
  year={2024},
  publisher={Springer}
}
```