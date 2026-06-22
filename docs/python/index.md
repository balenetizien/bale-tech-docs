---
title: Python
layout: default
nav_order: 2
has_children: true
permalink: /docs/python
---

# 🐍 Python

Python adalah bahasa pemrograman yang **mudah dipelajari** dan sangat populer di dunia. Cocok banget untuk pemula!

## Kenapa Python?

- ✅ Sintaks yang mudah dibaca seperti bahasa Inggris
- ✅ Dipakai di Web, Data Science, AI, Automation
- ✅ Komunitas besar = mudah cari bantuan
- ✅ Library melimpah

## Versi yang Direkomendasikan

Gunakan **Python 3.10+** (jangan Python 2, sudah deprecated).

Download di: [python.org](https://www.python.org/downloads/)

---

## TABLE OF CONTENTS

{% assign children = site.pages | where: "parent", page.title | sort: "nav_order" %}
{% for child in children %}
- [{{ child.title }}]({{ child.url | relative_url }})
{% endfor %}
