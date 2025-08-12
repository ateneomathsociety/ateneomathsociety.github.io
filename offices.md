---
layout:       default
title:        "Offices"
heading:      "Offices"
subheading:   "Get to know the offices of AMS"
permalink:    "/about/offices"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- assign items = site.offices -%}
{%- assign items_head = "" -%}
{%- include card/item.html -%}
