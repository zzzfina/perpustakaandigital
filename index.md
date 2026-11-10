---
layout: default
---
# Digital Library
Selamat Datang di Perpustakaan Digital
Berikut ini adalah koleksi yang dimiliki:

## Koleksi
1. [Enhancing Creative Learning in Thai Classical Dance Education: An Integration of Digital Preservation Framework with Ubiquitous Learning Environment](ebook/Digital Applications in Archaeology and Cultural Heritage.pdf) – Napatprapa Pathrapoowanun, Parama Kwangmuang, Apirat Siritaratiwat, dan Lan Thi Nguyen (2025)
*Powered by GitHub Pages*

{% assign ebooks = site.static_files | sort: "name" %}
{% assign total = 0 %}

<ol>
{% for file in ebooks %}
  {% assign ext = file.extname | downcase %}
  {% if file.path contains '/ebook/' and ext == '.pdf' %}
    {% assign total = total | plus: 1 %}
    {% assign title = file.name | remove: '.pdf' | replace: '-', ' ' | replace: '_', ' ' %}
    <li>
      <a href="{{ file.path | relative_url }}">{{ title }}</a>
      <br>
      Format: PDF
    </li>
    <br>
  {% endif %}
{% endfor %}
</ol>

Total collections: {{ total }} ebooks.

---

*Digital Library*
