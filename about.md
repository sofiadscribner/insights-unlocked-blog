---
layout: default
title: About 
---

<style>
.about-container {
  display: flex;
  align-items: center;
}

.about-container img {
  width: 150px; /* Adjust size as needed */
  height: auto;
  border-radius: 50%; /* Makes it circular */
  margin-right: 20px;
}
</style>

## About this Blog

{{site.description}}

<div class="about-container">
  <img src="/assets/portrait.jpg" alt="Your Name">
  <div>
    ## About Me  
    {{site.author_description}}
  </div>
</div>
