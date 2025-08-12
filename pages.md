---
layout:       default
title:        "Pages"
heading:      "Pages"
subheading:   "Visit the various pages of AMS"
permalink:    "/pages"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- assign items = site.data.pages -%}
{%- assign items_head = "" -%}
{%- include card/item.html -%}
