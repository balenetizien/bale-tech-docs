---
title: JavaScript
layout: default
nav_order: 4
has_children: true
permalink: /docs/javascript
---

# 🌐 JavaScript

JavaScript adalah satu-satunya bahasa yang berjalan **langsung di browser**. Setiap website interaktif yang pernah kamu lihat — animasi, form validation, efek hover — semuanya dibuat dengan JavaScript!

## Kenapa Belajar JavaScript?

- ✅ Wajib untuk web development
- ✅ Bisa dipakai di browser (frontend) dan server (Node.js)
- ✅ Basis untuk framework populer: React, Vue, Angular
- ✅ Komunitas terbesar di dunia

---

## TABLE OF CONTENTS

{% assign children = site.pages | where: "parent", page.title | sort: "nav_order" %}
{% for child in children %}
- [{{ child.title }}]({{ child.url | relative_url }})
{% endfor %}
