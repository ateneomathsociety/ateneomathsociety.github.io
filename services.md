---
layout:       default
title:        "Services"
heading:      "Services"
subheading:   "Get to know the services of AMS"
permalink:    "/services"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- assign posts = site.services -%}
{%- assign posts_head = "" -%}
{%- include card/post.html -%}
