---
layout: page
title: InfiMM
description: Advancing Multimodal Understanding from Flamingo's Legacy through Diverse LLM Integration
img: assets/img/infimm/assets_infimm-logo.webp
importance: 2
category: MLLM
related_publications: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/infimm/assets_infimm-logo.webp" title="Examples from our benchmark" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
    </div>
</div>

## Overview

InfiMM, inspired by the Flamingo architecture, sets itself apart with unique training data and diverse large language models (LLMs). This approach allows InfiMM to maintain the core strengths of Flamingo while offering enhanced capabilities. As the premier open-sourced variant in this domain, InfiMM excels in accessibility and adaptability, driven by community collaboration. It's more than an emulation of Flamingo; it's an innovation in visual language processing.

Our model is another attempt to produce the result reported in the paper "Flamingo: A Large-scale Visual Language Model for Multimodal Understanding" by DeepMind. Compared with previous open-sourced attempts ([OpenFlamingo](https://github.com/mlfoundations/open_flamingo) and [IDEFIC](https://huggingface.co/blog/idefics), InfiMM offers a more flexible models, allowing for a wide range of applications. In particular, InfiMM integrates the latest LLM models into VLM domain the reveals the impact of LLMs with different scales and architectures.

Please note that InfiMM is currently in beta stage and we are continuously working on improving it.

## Model Details

- **Developed by**: Institute of Automation, Chinese Academy of Sciences and ByteDance
- **Model Type**: Visual Language Model (VLM)
- **Language**: English
- **LLMs**: [Zephyr](https://huggingface.co/HuggingFaceH4/zephyr-7b-beta), [LLaMA2-13B](https://ai.meta.com/llama/), [Vicuna-13B](https://huggingface.co/lmsys/vicuna-13b-v1.5)
- **Vision Model**: [EVA CLIP](https://huggingface.co/QuanSun/EVA-CLIP)
- **Language(s) (NLP):** en
- **License:** see [License section](#license)

## Evaluation

### PreTraining Evaluation

We evaluate the pretrained models on the following downstream tasks: Image Captioning and VQA. We also compare with our results with [IDEFICS](https://huggingface.co/blog/idefics).

| Model             | Shots | COCO CIDEr | Flickr30K CIDEr | VQA v2 Acc | TextVQA Acc | OK-VQA Acc |
| ----------------- | ----- | ---------- | --------------- | ---------- | ----------- | ---------- |
| IDEFICS-9B        | 0     | 46         | 27.3            | 50.9       | 25.9        | 38.4       |
|                   | 4     | 93         | 59.7            | 55.4       | 27.6        | 45.5       |
| IDEFICS-80B       | 0     | 91.8       | 53.7            | 60         | 30.9        | 45.2       |
|                   | 4     | 110.3      | 73.7            | 64.6       | 34.4        | 52.4       |
| InfiMM-Zephyr-7B  | 0     | 78.8       | 60.7            | 33.7       | 15.2        | 17.1       |
|                   | 4     | 108.6      | 71.9            | 59.1       | 34.3        | 50.5       |
| InfiMM-Llama2-13B | 0     | 85.4       | 54.6            | 51.6       | 24.2        | 26.4       |
|                   | 4     | 125.2      | 87.1            | 66.1       | 38.2        | 55.5       |
| InfiMM-Vicuna13B  | 0     | 69.6       | 49.6            | 60.4       | 32.8        | 49.2       |
|                   | 4     | 118.1      | 81.4            | 64.2       | 38.4        | 53.7       |

### IFT Evaluation

In our analysis, we concentrate on two primary benchmarks for evaluating MLLMs: 1) Multi-choice Question Answering (QA) and 2) Open-ended Evaluation. We've observed that the evaluation metrics for tasks like Visual Question Answering (VQA) and Text-VQA are overly sensitive to exact answer matches. This approach can be misleading, particularly when models provide synonymous but technically accurate responses. Therefore, these metrics have been omitted from our comparison for a more precise assessment. The evaluation results are shown in the table below.

| Model               | ScienceQA-Img | MME                   | MM-VET | InfiMM-Eval  | MMbench | MMMU-Val | MMMU-Test |
| ------------------- | ------------- | --------------------- | ------ | ------------ | ------- | -------- | --------- |
| Otter-9B            | -             | 1292/306              | 24.6   | 32.2         | -       | 22.69    | -         |
| IDEFICS-9B-Instruct | 60.6          | -/-                   | -      | -            | -       | 24.53    | -         |
| InfiMM-Zephyr-7B    | 71.1          | P: 1406<br>C:327      | 32.8   | 36.0         | 59.7    | 39.4     | 35.5      |
| InfiMM-Llama-13b    | 73.0          | P: 1444.5<br>C: 337.6 | 39.2   | 0.4559/0.414 | 66.4    | 39.1     | 35.2      |
| InfiMM-Vicuna-13B   | 74.0          | P: 1461.2<br>C: 323.5 | 36.0   | 40.0         | 66.7    | 37.6     | 34.6      |

## Links

[Project HomePage](https://huggingface.co/Infi-MM)

[infimm-zephyr](https://huggingface.co/Infi-MM/infimm-zephyr)

[infimm-vicuna13b](https://huggingface.co/Infi-MM/infimm-vicuna13b)
