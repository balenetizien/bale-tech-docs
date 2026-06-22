---
title: CSS
layout: default
nav_order: 5
has_children: true
permalink: /docs/css
---

# 🎨 CSS

CSS (Cascading Style Sheets) adalah bahasa untuk **mendekorasi tampilan website**. HTML membuat strukturnya, CSS membuatnya cantik!

## Kenapa Belajar CSS?

- ✅ Wajib untuk web development
- ✅ Bisa buat website jadi cantik dan profesional
- ✅ Responsive design (tampil bagus di HP & desktop)
- ✅ Animasi dan efek visual yang keren

---

## TABLE OF CONTENTS

{% assign children = site.pages | where: "parent", page.title | sort: "nav_order" %}
{% for child in children %}
- [{{ child.title }}]({{ child.url | relative_url }})
{% endfor %}
