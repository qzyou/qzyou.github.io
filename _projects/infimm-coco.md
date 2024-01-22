---
layout: page
title: COCO IS "ALL" YOU NEED FOR VISUAL INSTRUCTION FINE-TUNING
description: COCO IS "ALL" YOU NEED FOR VISUAL INSTRUCTION FINE-TUNING
img: assets/img/mmreasoning/coco_all_you_need/coco.png
importance: 3
category: MLLM
related_publications: false
---

## Introduction

In this work, we establish a new IFT dataset, with images sourced from the COCO dataset along with more diverse instructions. Our experiments show that when fine-tuned with out proposed dataset, MLLMs achieve better performance on open-ended evaluation benchmarks in both single-round and multi-round dialog setting.

## Motivation

- Multi-round dialogs are expensive to construct.
- Current instruction following data makes the model overfit to single instruction.
- Multi-round evaluation benchmark is essential for evaluating the quality of instruction following.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mmreasoning/coco_all_you_need/llava_multi_round.drawio_0.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Demonstration of different models’ responses under multi-round dialog setting. This example explains our motivation, the model should follow each individual instruction for each dialog.
</div>

## Dataset summarization

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mmreasoning/coco_all_you_need/coco.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overlap of images across different datasets.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mmreasoning/coco_all_you_need/ift-format.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Templates used for converting datasets into conversational IFT format.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mmreasoning/coco_all_you_need/res.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Evaluation results on MM-Vet and InfiMM-Eval.
</div>

## Conclusions

This overfitting leads to a degradation in performance in multi-round dialog settings. We construct an IFT dataset by simply merging datasets with COCO images. Experiments show that models trained with our dataset demonstrate better instruction-following ability and achieve equal or better performance on open-ended evaluation benchmarks. The results suggest that the COCO dataset is ``all'' you need for visual IFT. We call for more comprehensive research to better understand IFT dataset construction, better evaluation benchmarks for modern open-ended MLLMs rather than traditional caption and VQA benchmarks.

# Links

[Arxiv](https://arxiv.org/pdf/2401.08968.pdf)
