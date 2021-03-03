---
layout: page
title: Physical doodling
permalink: physics
---

<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      extensions: [
        "MathMenu.js",
        "MathZoom.js",
        "AssistiveMML.js",
        "a11y/accessibility-menu.js"
      ],
      jax: ["input/TeX", "output/CommonHTML"],
      TeX: {
        extensions: [
          "AMSmath.js",
          "AMSsymbols.js",
          "noErrors.js",
          "noUndefined.js",
        ]
      }
    });
</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js"></script>

Oh hi, I didn't see you there! I'll be writing about a few exercises I'm doing during my Physics-III course. That means that this page will continuously get longer and more rich, I hope it turns out well.


<div class="posts">
  {% for post in site.physics_posts %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>
    <span class="post-date">{{ post.topic }}</span>

    {{ post.content }}
  </div>
  {% endfor %}
</div>