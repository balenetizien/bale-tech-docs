---
title: PHP
layout: default
nav_order: 3
has_children: true
permalink: /docs/php
---

# 🐘 PHP

PHP adalah bahasa pemrograman yang berjalan di **server-side** dan sangat populer untuk membuat website dinamis. WordPress, Facebook (awalnya), dan banyak website besar dibangun dengan PHP!

## Kenapa Belajar PHP?

- ✅ Sangat cocok untuk membuat website dinamis
- ✅ Mudah di-hosting (hampir semua hosting mendukung PHP)
- ✅ Komunitas besar, banyak tutorial
- ✅ Dipakai di WordPress, Laravel, dll

## Versi yang Direkomendasikan

Gunakan **PHP 8.1+** untuk fitur modern.

---

## TABLE OF CONTENTS

{% assign children = site.pages | where: "parent", page.title | sort: "nav_order" %}
{% for child in children %}
- [{{ child.title }}]({{ child.url | relative_url }})
{% endfor %}
