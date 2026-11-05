---
layout: default
title: ತಂತ್ರಾಲೋಕ
description: ಅಭಿನವಗುಪ್ತರ ತಂತ್ರಾಲೋಕದ ಮೂಲಪಾಠ ಮತ್ತು ಕನ್ನಡ ವಿವರಣೆ
---

<section class="intro" aria-labelledby="page-title">
  <p class="eyebrow">ಕಾಶ್ಮೀರ ಶೈವದರ್ಶನ · ಡಿಜಿಟಲ್ ಪಠ್ಯ</p>
  <h1 id="page-title">ತಂತ್ರಾಲೋಕ</h1>
  <p class="intro-copy">ಅಭಿನವಗುಪ್ತರ ಶೈವದರ್ಶನದ ಮಹಾಗ್ರಂಥ. ಲಭ್ಯವಿರುವ ಶ್ಲೋಕಗಳು, ಕನ್ನಡ ಭಾವಾರ್ಥ ಮತ್ತು ವಿವರಣೆಗಳನ್ನು ಇಲ್ಲಿ ಓದಿ.</p>
  <a class="text-link" href="{{ '/intro/' | relative_url }}">ಗ್ರಂಥ ಪರಿಚಯ <span aria-hidden="true">↗</span></a>
</section>

<section class="library" aria-labelledby="library-title">
  <div class="section-heading">
    <div>
      <p class="eyebrow">ಪಠ್ಯಸೂಚಿ</p>
      <h2 id="library-title">ವಿಭಾಗಗಳನ್ನು ಓದಿ</h2>
    </div>
    <label class="search-box">
      <span class="visually-hidden">ವಿಭಾಗಗಳನ್ನು ಹುಡುಕಿ</span>
      <span class="search-icon" aria-hidden="true">⌕</span>
      <input id="section-search" type="search" placeholder="ಶ್ಲೋಕ ಅಥವಾ ವಿಭಾಗ ಹುಡುಕಿ" autocomplete="off">
    </label>
  </div>

  <div class="section-grid">
    <section class="section-list" aria-labelledby="verses-title">
      <div class="list-heading">
        <h3 id="verses-title">ಶ್ಲೋಕಗಳು</h3>
        <span class="list-count">{% assign verse_pages = site.pages | where_exp: "page", "page.name contains 'verses-'" | sort: "name" %}{{ verse_pages.size }} ವಿಭಾಗಗಳು</span>
      </div>
      <ul class="document-list">
        {% for page in verse_pages %}
          {% assign range = page.name | remove: 'verses-' | remove: '.md' | replace: '-', '–' %}
          <li class="document-row" data-search="{{ range }} ಶ್ಲೋಕ verses">
            <a href="{{ page.url | relative_url }}"><span class="document-title">ಶ್ಲೋಕಗಳು {{ range }}</span><span class="document-status">{% if page.content contains 'ಅನುವಾದ ಬಾಕಿ' %}ಅನುವಾದ ಬಾಕಿ{% else %}ಪಠ್ಯ ಲಭ್ಯ{% endif %}</span><span class="row-arrow" aria-hidden="true">↗</span></a>
          </li>
        {% endfor %}
      </ul>
    </section>

    <section class="section-list" aria-labelledby="stanzas-title">
      <div class="list-heading">
        <h3 id="stanzas-title">ಆಹ್ನಿಕ ವಿಭಾಗಗಳು</h3>
        <span class="list-count">{% assign stanza_pages = site.pages | where_exp: "page", "page.name contains 'stanzas-'" | sort: "name" %}{{ stanza_pages.size }} ವಿಭಾಗಗಳು</span>
      </div>
      <ul class="document-list">
        {% for page in stanza_pages %}
          {% assign range = page.name | remove: 'stanzas-' | remove: '.md' | replace: '-', '–' %}
          <li class="document-row" data-search="{{ range }} ಆಹ್ನಿಕ ವಿಭಾಗ stanzas">
            <a href="{{ page.url | relative_url }}"><span class="document-title">ಶ್ಲೋಕಗಳು {{ range }}</span><span class="document-status">{% if page.content contains 'ಅನುವಾದ ಬಾಕಿ' %}ಅನುವಾದ ಬಾಕಿ{% else %}ಪಠ್ಯ ಲಭ್ಯ{% endif %}</span><span class="row-arrow" aria-hidden="true">↗</span></a>
          </li>
        {% endfor %}
      </ul>
    </section>
  </div>
  <p class="empty-state" id="empty-state" hidden>ಹೊಂದುವ ವಿಭಾಗ ಕಂಡುಬಂದಿಲ್ಲ.</p>
</section>

<section class="references" aria-label="ಹೆಚ್ಚುವರಿ ಓದು">
  <a href="{{ '/further-information/' | relative_url }}"><span>ಗ್ರಂಥ ಮತ್ತು ಪಾಠದ ಕುರಿತು</span><span aria-hidden="true">↗</span></a>
</section>

<script>
  const search = document.querySelector('#section-search');
  const rows = [...document.querySelectorAll('.document-row')];
  const emptyState = document.querySelector('#empty-state');

  search.addEventListener('input', () => {
    const query = search.value.trim().toLocaleLowerCase();
    let visibleRows = 0;

    for (const row of rows) {
      const matches = row.dataset.search.toLocaleLowerCase().includes(query);
      row.hidden = !matches;
      visibleRows += Number(matches);
    }

    emptyState.hidden = visibleRows > 0;
  });
</script>