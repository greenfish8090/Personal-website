---
weight: 30
title: Anime Recommender System
summary: A collaborative filtering model that recommends anime shows to users based on preferences of similar users
tags:
  - Deep Learning
  - Recommender system
date: '2021-11-17'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: 
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/greenfish8090/Anime-Recommender-System

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

We often find ourselves wondering what show/movie to watch next after we've just finished an amazing one. If it's on Netflix, it always has something ready for us under the "similar users have liked..." section. But how does it do it exactly?\
\
Netflix, along with most popular content streaming sites, employ what's called a recommender system with the primary goal of serving personalized recommendations to users. Broadly, based on its working, it can be classified into two types (Although in practice, it's usually a mix of them):
- Content based filtering
- Collaborative filtering

In content based filtering, items (products / movies / songs) are recommended solely based on the item's description and your preference history. It tries to recommend items with descriptions similar to ones you've liked.\
\
On the other hand, in collaborative filtering, the engine looks at the entire userbase of the app, and recommends items based on what others similar to you have liked. For this scheme, descriptions of items are not required. This is what I've implemented in this project.\
\
The subset of the [Dataset](https://www.kaggle.com/datasets/azathoth42/myanimelist) I used consists of just 3 columns: *user_id*, *anime_id* and *rating*. Arranging this into a matrix with rows as anime and columns as users, its cells can be filled with the rating (between 1 and 10) that the particular user rated the anime. An important feature of this resulting 5,000 x 100,000 matrix is that it's sparse. Very, very sparse.\
\
Roughly only 4.5% of the matrix is filled. Now comes our herculean task of filling in the missing values. If we achieve this, our "filled-in" values can serve as our predictions of what those users would rate those anime.\
\
To do this, matrix factorization can be used. The 5,000 x 100,000 dimensional sparse ratings matrix is decomposed into a 5,000 x 10 dimensional *anime_matrix* and a 10 x 100,000 dimensional *user_matrix*. These matrices are initialized at random, and are iteratively updated to converge them such that their product matches the original ratings matrix, wherever the ratings are available. After training, we simply multiply the two matrices and we have a whole array of predictions per user.\
\
I've tested it with my friends and myself, the predictions were rather accurate! For technical details and a walkthrough on how I went about implementing matrix factorization and generating predictions, check out the code on GitHub!