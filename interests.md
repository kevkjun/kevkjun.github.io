---
layout: default
title: Interests - Pursuits
url: /interests/
permalink: /interests/
---

{% include interests_nav.html %}

<div class="reading-now">
  <div class="reading-now-label">
    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"></path>
      <path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"></path>
    </svg>
    <span>Reading Now</span>
  </div>
  <div class="reading-now-books">
    <div class="reading-now-book" data-isbn="0143136879" data-title="Diary of a Void" data-author="Emi Yagi"></div>
    <div class="reading-now-book" data-isbn="1683964446" data-title="Crisis Zone" data-author="Simon Hanselmann"></div>
  </div>
</div>

<script>
  document.querySelectorAll('.reading-now-book').forEach(function(book) {
    const isbn = book.dataset.isbn;
    const title = book.dataset.title;
    const author = book.dataset.author;
    const src = `https://covers.openlibrary.org/b/isbn/${isbn}-M.jpg`;

    const img = new Image();
    img.onload = function() {
      if (img.width > 1) {
        book.innerHTML = `
          <img src="${src}" alt="${title} cover">
          <div class="reading-now-meta">
            <div class="book-title">${title}</div>
            <div class="book-author">${author}</div>
          </div>
        `;
      } else {
        book.innerHTML = `
          <div class="reading-now-meta">
            <div class="book-title">${title}</div>
            <div class="book-author">${author}</div>
          </div>
        `;
      }
    };
    img.src = src;
  });
</script>

<hr class="section-divider">

<div class="building-now">
  <div class="building-now-label">
    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <polyline points="4 17 10 11 4 5"></polyline>
      <line x1="12" y1="19" x2="20" y2="19"></line>
    </svg>
    <span>Building Now</span>
  </div>
  <div class="building-now-project">
    <div class="project-title">Homelab</div>
  </div>
</div>

<hr class="section-divider">

<div class="playing-now">
  <div class="playing-now-label">
    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M3 18v-6a9 9 0 0 1 18 0v6"></path>
      <path d="M21 19a2 2 0 0 1-2 2h-1a2 2 0 0 1-2-2v-3a2 2 0 0 1 2-2h3z"></path>
      <path d="M3 19a2 2 0 0 0 2 2h1a2 2 0 0 0 2-2v-3a2 2 0 0 0-2-2H3z"></path>
    </svg>
    <span>Playing Now</span>
  </div>

  <div class="playing-now-section-label">Listening</div>
  <div class="playing-now-book" id="album-block">
    <div class="playing-now-meta">
      <div class="project-title">The Money Store</div>
      <div class="project-description">Death Grips</div>
    </div>
  </div>

  <div class="playing-now-section-label" style="margin-top: 16px;">Playing</div>
  <div class="playing-now-book">
    <svg xmlns="http://www.w3.org/2000/svg" width="60" height="60" viewBox="0 0 100 100" style="flex-shrink: 0;">
      <text y=".9em" font-size="90">🪕</text>
    </svg>
    <div class="playing-now-meta">
      <div class="project-title">Ukulele</div>
      <div class="project-description">Learning fingerpicking</div>
    </div>
  </div>
</div>

<script>
  const apiKey = "{{ site.lastfm_api_key }}";
  const artist = "Death Grips";
  const album = "The Money Store";

  fetch(`https://ws.audioscrobbler.com/2.0/?method=album.getinfo&api_key=${apiKey}&artist=${encodeURIComponent(artist)}&album=${encodeURIComponent(album)}&format=json`)
    .then(r => r.json())
    .then(data => {
      const images = data.album && data.album.image;
      const img = images && images.find(i => i.size === "large");
      if (img && img["#text"]) {
        const block = document.getElementById("album-block");
        block.innerHTML = `
          <img src="${img["#text"]}" alt="${album} cover" style="width: 60px; border-radius: 3px; box-shadow: 2px 3px 8px rgba(0,0,0,0.15); flex-shrink: 0;">
          <div class="playing-now-meta">
            <div class="project-title">${album}</div>
            <div class="project-description">${artist}</div>
          </div>
        `;
      }
    });
</script>
