---
layout:       default
title:        "Pools & Teams"
heading:      "Pools & Teams"
subheading:   "Get to know the pools & teams of AMS"
permalink:    "/about/pools-teams"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- assign items = site.pools_teams -%}
{%- assign items_head = "" -%}
{%- include card/item.html -%}
