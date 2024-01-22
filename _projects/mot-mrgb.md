---
layout: page
title: RT Multi-Camera MoT System
description: Real-time Multi-Camera Multiple Object Tracking System
img: assets/img/mot/dmct.png
importance: 1
category: MOT
related_publications: false
---

## Introduction

Tracking a crowd in 3D using multiple RGB cameras is a challenging task. Most previous multi-camera tracking algorithms are designed for offline setting and have high computational complexity. Robust real-time multi-camera 3D tracking is still an unsolved problem. In this work, we propose a novel end-to-end tracking pipeline, Deep Multi-Camera Tracking (DMCT), which achieves reliable
real-time multi-camera people tracking. Our DMCT consists of 1) a fast and novel perspective-aware Deep GroudPoint Network, 2) a fusion procedure for groundplane occupancy heatmap estimation, 3) a novel Deep Glimpse Network for person detection and 4) a fast and accurate online tracker.

## Pipeline

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/pipeline.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<ul>
    <li> Demo video of our sytem on our dataset. <br/>
        <video width="640px" controls>
            <source src="https://onedrive.live.com/download?cid=AB6522E29F6ED9A0&resid=AB6522E29F6ED9A0%2194326&authkey=ABMhiAx5QBoY4hk" type="video/mp4">
            Your browser does not support the video tag.
        </video> 
    </li>
    <li> Demo video of our sytem on <a href="https://www.epfl.ch/labs/cvlab/data/data-wildtrack/" target="_blank">WILDTRACK</a>.  <br/>
        <video width="640px" controls>
            <source src="https://onedrive.live.com/download?cid=AB6522E29F6ED9A0&resid=AB6522E29F6ED9A0%2194325&authkey=AKtFkGZ-sBWiBqY" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </li>
</ul>

<li> Projection of human circle on each camera view </li>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/projection.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Examples

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/demo_example.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Example images from a new environment with three network cameras (best viewed in color).
</div>

# Links

Quanzeng You and Hao Jiang. [Real-time 3D Deep Multi-Camera Tracking](https://arxiv.org/pdf/2003.11753.pdf), arXiv preprint arXiv:2003.11753 (2020).
