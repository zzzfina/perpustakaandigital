# Digital Library
Selamat Datang di Perpustakaan Digital
Berikut ini adalah koleksi yang dimiliki:

## Koleksi
1. [Enhancing Creative Learning in Thai Classical Dance Education: An Integration of Digital Preservation Framework with Ubiquitous Learning Environment](ebook/Digital Applications in Archaeology and Cultural Heritage.pdf) – Napatprapa Pathrapoowanun, Parama Kwangmuang, Apirat Siritaratiwat, dan Lan Thi Nguyen (2025)
*Powered by GitHub Pages*

{% for file in ebooks %}
{% if file.path contains '/ebook/' %}
{% assign ext = file.extname | downcase %}
{% if ext == '.pdf' %}

{% assign filename = file.name %}
{% assign title = filename | remove: '.pdf' | replace: '-', ' ' | replace: '_', ' ' %}
{% assign author = 'Not yet identified' %}
{% assign year = 'Not yet identified' %}

{% assign name = filename | downcase %}

{% if name contains 'cloud-based adoption' %}
{% assign title = 'A Cloud-Based Adoption Model for Digital Preservation Services for University Libraries' %}
{% assign author = 'Hassan Mallam Ibrahim, Kamsuriah Ahmad, and Hasimi Sallehudin' %}

{% elsif name contains 'balancing efficiency' %}
{% assign title = 'Balancing Efficiency and Responsibility in Generative AI Adoption' %}
{% assign author = 'Duy Khanh Phan, Bao Quoc Truong-Dinh, and Em Thi Diem Nguyen' %}

{% elsif name contains 'cryptobooks' %}
{% assign title = 'CryptoBooks: Next-Generation Library Management with NFTs and Blockchain Technology' %}
{% assign author = 'Vikrant Dubey and Shilpi Verma' %}

{% elsif name contains 'digital humanities' %}
{% assign title = 'Digital Humanities and Archival Studies: A Cross-Linguistic Analysis' %}
{% assign author = 'Chyi-Kuan Wang and Chiao-Min Lin' %}

{% elsif name contains 'digital applications' %}
{% assign title = 'Enhancing Creative Learning in Thai Classical Dance Education: An Integration of Digital Preservation Framework with Ubiquitous Learning Environment' %}
{% assign author = 'Napatprapa Pathrapoowanun, Parama Kwangmuang, Apirat Siritaratiwat, and Lan Thi Nguyen' %}
{% assign year = '2025' %}

{% elsif name contains 'entrepreneurial self-efficacy' %}
{% assign author = 'Anis Batrisyia Ardani, Nur Adilah Md Zain, Mohd Hafiz Hanafiah, Muhammad Aliff Asyraff, and Nyoman Diah Utari Dewi' %}

{% elsif name contains 'sustainability' %}
{% assign author = 'Muhammad Hamza and Ahsan Ullah' %}

{% elsif name contains 'multivalent evaluation' %}
{% assign author = 'Stephen Abrams' %}

{% endif %}

1. [{{ title }}]({{ file.path | relative_url }}) - {{ author }} ({{ year }})

{% endif %}
{% endif %}
{% endfor %}

*Powered by GitHub Pages*
