---
layout: page
title: 4D Vision System
description: Action4D Online Action Recognition in the Crowd and Clutter
img: assets/img/mot/rgbd.png
importance: 2
category: MOT
related_publications: false
---

## Introduction

We propose a new method to track people in 4D, which can reliably detect and follow each person in real time. Then, we build a new deep neural network, the Action4DNet, to recognize the action of each tracked person. Such a model gives reliable and accurate results in the real-world settings. We also design an adaptive 3D convolution layer and a novel discriminative temporal feature learning objective to further improve the performance of our model. Our method is invariant to camera view angles, resistant to clutter and able to handle crowd. The experimental results show that the proposed method is fast, reliable and accurate. Our method paves the way to action recognition in the real-world applications and is ready to be deployed to enable smart homes, smart factories and smart stores.

## Approach
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/rgbd_det.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
People classification network and the tracking association algorithm.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/action4dnet.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Our proposed attention Action4DNet.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/4d_actions.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
We recognize actions using volumes (color represents the height of each voxel).
</div>


<ul>
    <li>News Report: <a href="https://www.vision-systems.com/cameras-accessories/article/14073208/4d-tracking-system-recognizes-the-actions-of-dozens-of-people-simultaneously-in-real-time">4D tracking system recognizes the actions of dozens of people simultaneously in real time</a></li>
    <li> Demo video of our sytem. <br/>
        <video width="640px" controls>
            <source src="https://onedrive.live.com/download?cid=AB6522E29F6ED9A0&resid=AB6522E29F6ED9A0%21101631&authkey=AAjl9JufOsGRyOE" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </li>
    <li> Check <a href="http://www.hao-jiang.net/videos/4dv.mp4" target="_blank">this video </a> for more details.</li>
</ul>
<li> Projection of human circle on each camera view </li>



## Examples

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mot/demo_example.png" title="pipeline of our system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Example images from a new environment with three network cameras (best viewed in color).
</div>


/Users/bytedance/src/homepages/al-folio/assets/img/mot/action4dnet.png

# Links
Quanzeng You and Hao Jiang. [Action4D: Online Action Recognition in the Crowd and Clutter](https://openaccess.thecvf.com/content_CVPR_2019/papers/You_Action4D_Online_Action_Recognition_in_the_Crowd_and_Clutter_CVPR_2019_paper.pdf).