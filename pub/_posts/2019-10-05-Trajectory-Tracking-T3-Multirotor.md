---
title: "Trajectory Tracking for Cooperative Transportation with T3-multirotor"
# header:
#   teaser: tumbnails/res_261.jpg
conference: ICCAS
links: 
 - paper: 
   link: http://www.dbpia.co.kr/Journal/articleDetail?nodeId=NODE09261517
   name: "Paper"
 - bibtex: 
   name: "Bibtex"
---

This paper suggests a new cooperative transportation system with T³-multirotors. From the promising characteristics of T³-multirotor for fully-actuated motion, the proposed system is able to track a desired payload trajectory which is impossible with a conventional underactuated multirotor. Unlike other cooperative methods such as slung-load transportation and aerial manipulator, the system can accommodate simpler mechanism by directly attaching cargo to the multirotor body. We build the dynamic model of the system and design a trajectory tracking controller considering low-level control. Dynamic equations show that the system is overactuated and it can follow arbitrary twice-differentiable trajectory if input and mechanical feasibilities are satisfied. For tracking control, linear control methods with linear quadratic regulator(LQR) and PID are sufficient for stable and efficient tracking. Control allocation is used for the sake of determining input for each actuator. Further improvement is expected by combining the proposed approach with a trajectory generation module.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{kim2019trajectory,
  title={Trajectory Tracking for Cooperative Transportation with T$^3$-multirotor},
  author={Kim, Dabin and Lee, Seung Jae and Kim, H Jin},
  journal={Control, Automation and Systems (ICCAS), 2019 19th International Conference on},
  pages={765--770},
  year={2019},
  organization={IEEE}
}
```