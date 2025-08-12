---
layout:       default
title:        "Departments"
heading:      "Departments"
subheading:   "Get to know the departments of AMS"
permalink:    "/about/departments"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- assign items = site.departments -%}
{%- assign items_head = "" -%}
{%- include card/item.html -%}
