---
lang: es
lang-ref: home
layout: home
description: |
  <p class="feature-title">Observatorio<br>Aguas Amazónicas</p>
  <p class="hero-subtitle">Datos para entender la vida de los ríos amazónicos</p>

  <div class="heroSearchBlock">
    <div class="searchWrapper">
      <div class="tab">
        <button type="button" class="tablinks active" onclick="openTab(event, 'searchTab_name')">Nombre común</button>
        <button type="button" class="tablinks" onclick="openTab(event, 'searchTab_basin')">Subcuenca</button>
        <button type="button" class="tablinks" onclick="openTab(event, 'searchTab_scientificName')">Nombre científico</button>
        <button type="button" class="tablinks" onclick="openTab(event, 'searchTab_publisher')">Socios</button>
      </div>

      <div id="searchTab_name" class="tabcontent is-active">
        <form action="/occurrence/search" method="GET">
          <input id="home_specimen_input" name="q" class="input searchInput" type="text" placeholder="Busca una especie">
          <button type="submit" class="searchSubmit" aria-label="Buscar">
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>

      <div id="searchTab_basin" class="tabcontent">
        <form action="/occurrence/search" method="GET">
          <input id="basin" name="basin" class="input searchInput" type="text" placeholder="Busca por subcuenca">
          <button type="submit" class="searchSubmit" aria-label="Buscar por subcuenca">
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>

      <div id="searchTab_scientificName" class="tabcontent">
        <form action="/occurrence/search" method="GET">
          <input id="verbatimScientificName" name="verbatimScientificName" class="input searchInput" type="text" placeholder="Busca por nombre científico">
          <button type="submit" class="searchSubmit" aria-label="Buscar por nombre científico">
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>

      <div id="searchTab_publisher" class="tabcontent">
        <form action="/occurrence/search" method="GET">
          <input id="publisher" name="publisher" class="input searchInput" type="text" placeholder="Busca por socio">
          <button type="submit" class="searchSubmit" aria-label="Buscar por socio">
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
              <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>
    </div>

    <div class="heroSearchActions">
      <a href="/occurrence/search" class="heroSearchCta">Buscar todos los registros</a>
    </div>
  </div>

  <script>
    function openTab(evt, tabName) {
      var wrapper = evt.currentTarget.closest('.searchWrapper');
      var tabcontent = wrapper.querySelectorAll('.tabcontent');
      var tablinks = wrapper.querySelectorAll('.tablinks');
      var i;

      for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].classList.remove('is-active');
      }

      for (i = 0; i < tablinks.length; i++) {
        tablinks[i].classList.remove('active');
      }

      document.getElementById(tabName).classList.add('is-active');
      evt.currentTarget.classList.add('active');
    }
  </script>
background: https://aguasamazonicas.org/wp-content/uploads/2025/11/banner-home-page.png
imageLicense: None for this image
height: 100vh
permalink: /
composition:
  - type: heroImage
  - data: home.bannerText
    type: product
  - data: home.stats
    type: stats
  - data: home.welcome
    type: split
---
