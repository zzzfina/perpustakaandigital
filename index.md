# Digital Library
Selamat Datang di Perpustakaan Digital
Berikut ini adalah koleksi yang dimiliki:

## Koleksi
1. [Enhancing Creative Learning in Thai Classical Dance Education: An Integration of Digital Preservation Framework with Ubiquitous Learning Environment](ebook/Digital Applications in Archaeology and Cultural Heritage.pdf) – Napatprapa Pathrapoowanun, Parama Kwangmuang, Apirat Siritaratiwat, dan Lan Thi Nguyen (2025)
*Powered by GitHub Pages*

---
layout: default
title: Digital Library
---

<style>
.library-container {
  max-width: 1050px;
  margin: auto;
  padding: 20px;
}

.library-header {
  background: linear-gradient(135deg, #174a7e, #347eb5);
  color: white;
  padding: 45px 20px;
  border-radius: 14px;
  text-align: center;
  margin-bottom: 30px;
}

.library-header h1 {
  color: white;
  font-size: 36px;
  margin-bottom: 10px;
}

.library-header p {
  color: white;
}

.library-search {
  width: 100%;
  padding: 14px;
  border: 1px solid #ccc;
  border-radius: 9px;
  font-size: 15px;
  margin: 15px 0 25px;
  box-sizing: border-box;
}

.collection-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
}

.book-card {
  border: 1px solid #ddd;
  border-radius: 12px;
  padding: 20px;
  background: white;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-shadow: 0 3px 10px rgba(0,0,0,.05);
  color: #222;
}

.book-card h3 {
  color: #174a7e;
  font-size: 17px;
  line-height: 1.5;
}

.book-card p {
  font-size: 13px;
  line-height: 1.6;
  color: #555;
}

.book-icon {
  font-size: 32px;
  margin-bottom: 10px;
}

.read-button {
  display: block;
  background: #174a7e;
  color: white !important;
  text-decoration: none;
  text-align: center;
  padding: 11px;
  border-radius: 8px;
  margin-top: 15px;
}

.read-button:hover {
  background: #286ba8;
}

.book-card.hidden {
  display: none;
}

.library-footer {
  text-align: center;
  padding: 25px;
  margin-top: 40px;
  border-top: 1px solid #ddd;
  color: #777;
}

.collection-count {
  background: #edf4fa;
  color: #174a7e;
  padding: 12px;
  border-radius: 8px;
  margin-bottom: 20px;
}
</style>

<div class="library-container">

  <div class="library-header">
    <h1>Digital Library</h1>
    <p>Selamat Datang di Perpustakaan Digital</p>
    <p>Temukan berbagai koleksi artikel dan ebook secara online.</p>
  </div>

  <h2>Koleksi Digital</h2>

  <p>
    Berikut merupakan koleksi yang tersedia
    di Digital Library.
  </p>

  <input
    type="text"
    id="bookSearch"
    class="library-search"
    placeholder="Cari judul atau pengarang..."
    oninput="searchBooks()"
  >

  {% assign ebooks = site.static_files | sort: "name" %}
  {% assign total = 0 %}

  <div class="collection-grid" id="bookCollection">

  {% for file in ebooks %}

    {% if file.path contains '/ebook/' %}
    {% assign ext = file.extname | downcase %}

    {% if ext == '.pdf' %}

      {% assign total = total | plus: 1 %}
      {% assign filename = file.name %}
      {% assign title = filename | remove: '.pdf' | remove: '.PDF' | replace: '-', ' ' | replace: '_', ' ' %}

      {% assign author = 'Belum dilengkapi' %}
      {% assign year = 'Belum teridentifikasi' %}

      {% assign name = filename | downcase %}

      {% if name contains 'sustainability of digital preservation' %}
        {% assign title = 'Sustainability of Digital Preservation at University Libraries of Pakistan' %}
        {% assign author = 'Muhammad Hamza dan Ahsan Ullah' %}

      {% elsif name contains 'multivalent evaluation' %}
        {% assign title = 'Multivalent Evaluation of Digital Preservation Success' %}
        {% assign author = 'Stephen Abrams' %}

      {% elsif name contains 'mnemonic infrastructures' %}
        {% assign title = 'Mnemonic Infrastructures and the Preservation of Literary Memory: Institutional Approaches to Digital Archiving in India' %}

      {% elsif name contains 'entrepreneurial self-efficacy' %}
        {% assign title = "Entrepreneurial Self-Efficacy in Women's Community-Based Tourism: A Systematic Review of Success Factors, Barriers and Theoretical Gaps" %}
        {% assign author = 'Anis Batrisyia Ardani, Nur Adilah Md Zain, Mohd Hafiz Hanafiah, Muhammad Aliff Asyraff, dan Nyoman Diah Utari Dewi' %}

      {% elsif name contains 'digital humanities' %}
        {% assign title = 'Digital Humanities and Archival Studies: A Cross-Linguistic Analysis' %}
        {% assign author = 'Chyi-Kuan Wang dan Chiao-Min Lin' %}

      {% elsif name contains 'digital applications' %}
        {% assign title = 'Enhancing Creative Learning in Thai Classical Dance Education: An Integration of Digital Preservation Framework with Ubiquitous Learning Environment' %}
        {% assign author = 'Napatprapa Pathrapoowanun, Parama Kwangmuang, Apirat Siritaratiwat, dan Lan Thi Nguyen' %}
        {% assign year = '2025' %}

      {% elsif name contains 'cryptobooks' %}
        {% assign title = 'CryptoBooks: Next-Generation Library Management with NFTs and Blockchain Technology' %}
        {% assign author = 'Vikrant Dubey dan Shilpi Verma' %}

      {% elsif name contains 'balancing efficiency' %}
        {% assign title = 'Balancing Efficiency and Responsibility in Generative AI Adoption' %}
        {% assign author = 'Duy Khanh Phan, Bao Quoc Truong-Dinh, dan Em Thi Diem Nguyen' %}

      {% elsif name contains 'cloud-based adoption' %}
        {% assign title = 'A Cloud-Based Adoption Model for Digital Preservation Services for University Libraries' %}
        {% assign author = 'Hassan Mallam Ibrahim, Kamsuriah Ahmad, dan Hasimi Sallehudin' %}

      {% endif %}

      <div class="book-card">
        <div>
          <div class="book-icon">📘</div>

          <h3>{{ title }}</h3>

          <p>
            <strong>Pengarang:</strong><br>
            {{ author }}
          </p>

          <p>
            <strong>Tahun Terbit:</strong>
            {{ year }}
          </p>

          <p>
            <strong>Format:</strong> PDF
          </p>
        </div>

        <a
          href="{{ file.path | relative_url }}"
          class="read-button"
          target="_blank"
          rel="noopener"
        >
          Baca Ebook
        </a>
      </div>

    {% endif %}
    {% endif %}

  {% endfor %}

  </div>

  <div class="collection-count">
    <strong>Jumlah koleksi: {{ total }} dokumen</strong>
  </div>

  {% if total == 0 %}
    <p>Belum ada koleksi PDF yang tersedia.</p>
  {% endif %}

  <div class="library-footer">
    <p><strong>Digital Library</strong></p>
    <p>Perpustakaan Digital</p>
    <p>Powered by GitHub Pages</p>
  </div>

</div>

<script>
function searchBooks() {
  const keyword = document
    .getElementById("bookSearch")
    .value.toLowerCase();

  const cards = document.querySelectorAll(".book-card");

  cards.forEach(function(card) {
    const content = card.textContent.toLowerCase();

    card.classList.toggle(
      "hidden",
      !content.includes(keyword)
    );
  });
}
</script>
