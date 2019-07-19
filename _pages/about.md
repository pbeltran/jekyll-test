---
title: "Pablo's Page"
layout: splash
permalink: /about/
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: assets/art/oriheader.png
  actions:
    - label: "Saber más"
      url: 
  caption: "@pbeltranp"
excerpt: "Bacon ipsum dolor sit amet salami ham hock ham, hamburger corned beef short ribs kielbasa biltong t-bone drumstick tri-tip tail sirloin pork chop."
intro: 
  - excerpt: 'Nullam suscipit et nam, tellus velit pellentesque at malesuada, enim eaque. Quis nulla, netus tempor in diam gravida tincidunt, *proin faucibus* voluptate felis id sollicitudin. Centered with `type="center"`'
feature_row:
  - image_path: assets/art/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
    title: "Repositorio GitHub"
    excerpt: "Un lugar donde compartir mis proyectos a la vez que los desarrollo."
  - image_path: assets/art/unsplash-gallery-image-2-th.jpg
    image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"
    alt: "placeholder image 2"
    title: "Blog Tierra de números"
    excerpt: "Cosicas varias sobre educación matemática"
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: assets/art/unsplash-gallery-image-3-th.jpg
    title: "Mi web académica"
    excerpt: "Artículos..."
feature_row2:
  - image_path: assets/art/ddaa.png
    alt: "placeholder image 2"
    title: Matemáticas animadas
    excerpt: 'Artículos en la sección de la revista EDMA 0-6'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: assets/art/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Mis cosicas de Twitter"
    excerpt: <a class="twitter-timeline" data-height="500" data-theme="light" href="https://twitter.com/pbeltranp">Tweets by pbeltranp</a> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row4:
  - image_path: assets/art/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Center Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Centered with `type="center"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
