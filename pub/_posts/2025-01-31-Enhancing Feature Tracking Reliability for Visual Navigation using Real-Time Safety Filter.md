---
title: "Enhancing Feature Tracking Reliability for Visual Navigation using Real-Time Safety Filter"
header:
  teaser: tumbnails/icra25.png
conference: ICRA
authors:
  - Dabin Kim*
  - Inkyu Jang*
  - Youngsoo Han
  - Sunwoo Hwang
  - H. Jin Kim
links: 
 - paper: 
   link: https://arxiv.org/pdf/2502.01092
   name: "Paper"
 - video:
   link: https://www.youtube.com/watch?v=pZ9nvobevcs
   name: "Video"
excerpt: This paper presents a real-time safety filter for robot navigation that maintains visual feature visibility by minimally adjusting velocity commands, ensuring reliable pose estimation even in GPS-denied environments. Validated in both simulation and real-world SLAM scenarios, the method outperforms standard controllers by preserving high-quality localization.
---

{% include youtubePlayer.html id="pZ9nvobevcs" %}

## 🚀 Making Visual Navigation More Reliable  
### Enhancing Feature Tracking with a Real-Time Safety Filter

In environments without GPS, many robots rely on **visual SLAM** — using a camera to track their position by detecting and following visual features (like corners or edges). But here’s the catch:

🔍 If the number of visible features suddenly drops, SLAM performance can fail dramatically — causing tracking loss, localization errors, or even crashes.

Our work addresses this with a simple question:  
**Can we make a robot proactively preserve its feature visibility — *before* it’s too late?**

---

## 📈 Why It Matters

- 🎯 **SLAM safety**: Prevents catastrophic failures due to sudden feature loss.
- ⚡ **Real-time**: The filter runs fast enough to be deployed on real robots.
- 🧠 **Minimal intervention**: Only adjusts motion when necessary — keeps nominal behavior otherwise.

---

## 🎯 Key Idea: A Real-Time Safety Filter for Features

We propose a **real-time safety filter** that runs alongside the robot’s control system. Instead of blindly following a planned velocity, the filter *modifies* the velocity to **keep enough visual features in field of view (FoV)**.

## 🔧 How Safety Filtering Works (In Simple Terms)

Here’s what happens at each time step:

1. A controller gives a reference velocity (`v_ref`) to the robot.
2. The onboard camera detects visual features and formulates inequality constraints that aim to keep a sufficient number of features within the FoV, ensuring their forward invariance.
3. A **quadratic program (QP)** solves for a new velocity (`v_filtered`) that:
   - Remains close to `v_ref`
   - Ensures the feature number score stays above a threshold


## 🧩 Key Challenge and Our Solution

Traditional safety filtering methods, such as those based on **Control Barrier Functions (CBFs)**, are designed to prevent the robot from violating hard safety constraints (e.g., collisions). However, directly applying such rigid constraints to feature visibility would **over-constrain** the system—preventing the robot from exploring, even when **new features** might become visible from newly observed regions.

Conversely, **blindly following** the reference command may cause the robot to lose too many features, degrading localization performance.

To resolve this trade-off, we propose a **parameterized safety filter** where each visual feature is assigned a parameter that reflects its importance. This parameter:

- Allows the filter to **relax** the constraint when a feature is less critical (parameter near zero), enabling the robot to let it move out of the FoV in favor of exploration.
- Enforces the constraint more strictly when the feature is important (parameter close to one), keeping it in view.

This behavior is embedded within a QP formulation that guarantees **recursive feasibility**—ensuring that a safe solution exists at every time step.

For a rigorous mathematical treatment, please refer to our paper.


### ✅ Simulation:  
- We tested in a simulated setup with a robot commanded to revolve in a circle (fixed orientation).
- Without the filter, the robot frequently lost visual features.
- With the filter, it adaptively slowed or adjusted its path to maintain feature visibility.

<div style="background: transparent; display: flex; gap: 20px; justify-content: center; text-align: center;">
  <div style="flex: 1;">
    <img src="/images/blog/icra25/sim_baseline.gif" alt="Sim" style="width: 100%; max-width: 400px;">
    <p><em>Baseline Result</em></p>
  </div>
  <div style="flex: 1;">
    <img src="/images/blog/icra25/sim_proposed.gif" alt="Real" style="width: 100%; max-width: 400px;">
    <p><em>Proposed Result</em></p>
  </div>
</div>

<!-- - The below figure shows that with safety filter, the tracked -->

<!-- Figure below the GIFs -->
<!-- <div style="text-align: center; margin-top: 20px;">
  <img src="/images/blog/icra25/sim_result.png" style="max-width: 60%; height: auto;">
  <p style="font-style: italic; font-size: 0.9rem;">Figure: Simulation Result</p>
</div> -->

## 🧪 Experiments
- We ran real-world experiments using a ground robot equipped with a stereo camera and a servo motor for active camera orientation.
- The task: traverse alongside a wall, keeping the camera facing perpendicular.
- Without the filter, the robot entered feature-poor regions and suffered tracking loss.
- With the filter, it proactively adjusted orientation to preserve feature visibility and only returned to the reference path once new features were found.

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; text-align: center; max-width: 900px; margin: auto;">
  <!-- Top Left -->
  <div>
    <img src="/images/blog/icra25/exp_baseline.gif"
         alt="Baseline - Third Person"
         style="width: 100%; height: 250px; object-fit: contain;">
    <p><em>Baseline (Third-Person View)</em></p>
  </div>

  <!-- Top Right -->
  <div>
    <img src="/images/blog/icra25/exp_baseline_onboard.gif"
         alt="Baseline - Onboard"
         style="width: 100%; height: 250px; object-fit: contain;">
    <p><em>Baseline (Onboard View)</em></p>
  </div>

  <!-- Bottom Left -->
  <div>
    <img src="/images/blog/icra25/exp_proposed.gif"
         alt="Proposed - Third Person"
         style="width: 100%; height: 250px; object-fit: contain;">
    <p><em>Proposed (Third-Person View)</em></p>
  </div>

  <!-- Bottom Right -->
  <div>
    <img src="/images/blog/icra25/exp_proposed_onboard.gif"
         alt="Proposed - Onboard"
         style="width: 100%; height: 250px; object-fit: contain;">
    <p><em>Proposed (Onboard View)</em></p>
  </div>
</div>

- The plot below shows that **without the filter**, a sudden drop in tracked features (left) leads to a sharp rise in localization error (right).  
- **With the filter**, the feature count remains stable and drift increases more gradually.

<div style="display: flex; justify-content: center; gap: 40px; text-align: center; margin-top: 20px;">
  <div style="flex: 1;">
    <img src="/images/blog/icra25/exp_feature_number.png" style="max-width: 100%; height: auto;">
  </div>
  <div style="flex: 1;">
    <img src="/images/blog/icra25/exp_estimation_error.png" style="max-width: 100%; height: auto;">
  </div>
</div>

---


## 🧩 Future Ideas

We’re excited to:
- Combine this with **active vision** to move toward richer feature regions, including **perception-aware planning** for full autonomy
- Use it in **autonomous exploration**, where exploring the unkown region while without losing features mid-flight to reduce drift

--- 
<!-- Vision sensors are extensively used for localizing a robot's pose, particularly in environments where global localization tools such as GPS or motion capture systems are unavailable. In many visual navigation systems, localization is achieved by detecting and tracking visual features or landmarks, which provide information about the sensor's relative pose. For reliable feature tracking and accurate pose estimation, it is crucial to maintain visibility of a sufficient number of features. This requirement can sometimes conflict with the robot's overall task objective. In this paper, we approach it as a constrained control problem. By leveraging the invariance properties of visibility constraints within the robot's kinematic model, we propose a real-time safety filter based on quadratic programming. This filter takes a reference velocity command as input and produces a modified velocity that minimally deviates from the reference while ensuring the information score from the currently visible features remains above a user-specified threshold. Numerical simulations demonstrate that the proposed safety filter preserves the invariance condition and ensures the visibility of more features than the required minimum. We also validated its real-world performance by integrating it into a visual simultaneous localization and mapping (SLAM) algorithm, where it maintained high estimation quality in challenging environments, outperforming a simple tracking controller. -->

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