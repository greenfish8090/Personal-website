---
weight: 40
title: Emotion Recognition
summary: Ant Miner, a variation of Ant Colony Optimization for data mining applied to a preprocessed emotion recognition dataset
tags:
  - Data Mining
  - Bio-inspired algorithms
  - Emotion recogniton
date: '2021-11-28'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Pheromone map
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/greenfish8090/Emotion-Recognition
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: 
---

Ant Colony Optimization falls under the category of swarm intelligence algorithms, commonly used as a metaheuristic. It is, unsurprisingly, inspired from ants. The problem is formulated as a traversible field in which numerous ants are deployed. They follow a path dictated by the phermone levels and a problem-specific heuristic, in a probabilistic way. In this setting, the ants' paths are possible solutions and depending upon the quality, pheromones are updated in the field for the next batch of ants to consider. After sufficient iterations, the best solutions are taken.\
\
An adaptation of this system is the Ant Miner, a rule-based classifer which is commonly used for Data Mining tasks. This, along with an extension for handling continuous values called c-Ant Miner, is what was implemented in this project. The dataset used is the popular Ravdess Dataset for Emotion Recognition. Check out the code for details!