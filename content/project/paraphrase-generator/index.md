---
weight: 20
title: Paraphrase Generator
summary: The T5 multi-task transformer model pretrained on a wide array of tasks, fine-tuned for paraphrase generation while preserving performance on old tasks. Alleviated Catastrophic forgetting using EWC. 
tags:
  - Deep Learning
  - Sequence Processing
  - Natural Language Processing
  - Continual Learning
date: '2021-12-05'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: 
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/greenfish8090/Transformer-Continual-Learning
  - icon: note-sticky
    icon_pack: fas
    name: Paper
    url: '/uploads/Continual_Learning_with_EWC.pdf'
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: paraphraser
---

In the domain of Natural Language Processing, it is unheard of for models to be trained on multiple
tasks sequentially. This is because after the first task, there is
a significant dip in performance on the first task while training
for the second task. This is known as catastrophic forgetting.
Continual learning aims to combat this problem by retaining
knowledge of previous tasks while being able to adapt to any
new task. We utilize a loss based method called Elastic Weights Consolidation and apply it on the T5 transformer to enable it to adapt to almost any NLP task while
being fast and memory efficient.\
\
Check out the slides, paper and the code on GitHub for more details!