---
layout:       default
title:        "Projects"
heading:      "Projects"
subheading:   "Get to know the projects of AMS"
permalink:    "/projects"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- include functions.html func='filter_collection' collection=site.projects key='project-tag' value='major' -%}
{%- assign items = return -%}
{%- assign items_head = "Our Major Project" -%}
{%- if items.size > 1 -%}{%- assign items_head = items_head | append: "s" -%}{%- endif -%}
{%- include card/item.html -%}

{%- include functions.html func='filter_collection' collection=site.projects key='project-tag' value='special' -%}
{%- assign items = return -%}
{%- assign items_head = "Our Special Project" -%}
{%- if items.size > 1 -%}{%- assign items_head = items_head | append: "s" -%}{%- endif -%}
{%- include card/item.html -%}

{%- include functions.html func='filter_collection' collection=site.projects key='project-tag' value='minor' -%}
{%- assign items = return -%}
{%- assign items_head = "Our Minor Project" -%}
{%- if items.size > 1 -%}{%- assign items_head = items_head | append: "s" -%}{%- endif -%}
{%- include card/item.html -%}
