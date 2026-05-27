---
lang: es
lang-ref: home
layout: home
description: |
  <p class="feature-title">Observatorio Aguas Amazónicas</p>

  <div class="searchWrapper">
      <!-- Tab links -->
      <div class="tab">
        <button class="tablinks active" onclick="openTab(event, 'searchTab_name')">Todos los campos</button>
        <button class="tablinks " onclick="openTab(event, 'searchTab_basin')">Subcuenca</button>
        <button class="tablinks " onclick="openTab(event, 'searchTab_scientificName')">Nombre científico</button>
        <button class="tablinks " onclick="openTab(event, 'searchTab_publisher')">Socios</button>
      </div>

      <!-- Tab content -->
      <div id="searchTab_name" class="tabcontent" style="display: block;">
        <form action="/occurrence/search" method="GET">
          <input id="home_specimen_input" name="q" class="input" type="text" placeholder="Busca por texto" style="width: 100%;">
          <button type="submit" class="button is-ghost" aria-label="Buscar">
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg">
            <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>

      <div id="searchTab_basin" class="tabcontent">
        <form action="/occurrence/search" method="GET">
          <input id="basin" name="basin" class="input" type="text" placeholder="Busca por cuenca" style="width: 100%;">
          <button type="submit" class="button is-ghost" aria-label="submit the search query">
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg">
            <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>

      <div id="searchTab_scientificName" class="tabcontent">
        <form action="/occurrence/search" method="GET">
          <input id="verbatimScientificName" name="verbatimScientificName" class="input" type="text" placeholder="Busca por nombre científico" style="width: 100%;">
          <button type="submit" class="button is-ghost" aria-label="submit the search query" >
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg">
            <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>

        <div id="searchTab_publisher" class="tabcontent">
        <form action="/occurrence/search" method="GET">
          <input id="publisher" name="pubisher" class="input" type="text" placeholder="Busca por publicador" style="width: 100%;">
          <button type="submit" class="button is-ghost" aria-label="submit the search query" >
            <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg">
            <path fill="none" d="M0 0h24v24H0z"></path><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"></path>
            </svg>
          </button>
        </form>
      </div>
  </div>
  <p class="orSeperator">O</p>
  <div>
    <div class="heroButton">
        <a href="/occurrence/search">Explora todos los registros</a>
    </div>
  </div>
  <script>
      window.setTimeout(function() {
        let a = document.getElementById('headline-offset');
        if (a !== undefined && a !== null) {
        a.parentElement.style.marginLeft = '-' + a.offsetWidth + 'px';}
      }, 300);

      function openTab(evt, tabName) {
        // Declare all variables
        var i, tabcontent, tablinks;

        // Get all elements with class="tabcontent" and hide them
        tabcontent = document.getElementsByClassName("tabcontent");
        for (i = 0; i < tabcontent.length; i++) {
          tabcontent[i].style.display = "none";
        }

        // Get all elements with class="tablinks" and remove the class "active"
        tablinks = document.getElementsByClassName("tablinks");
        for (i = 0; i < tablinks.length; i++) {
          tablinks[i].className = tablinks[i].className.replace(" active", "");
        }

        // Show the current tab, and add an "active" class to the button that opened the tab
        document.getElementById(tabName).style.display = "block";
        evt.currentTarget.className += " active";
      }
  </script>
background: /assets/images/placeholders/templates/w1600h800.png
imageLicense: None for this image
height: 100vh
permalink: /
composition:
  - type: heroImage
  - data: home.buttons
    type: floatingText
  - data: home.stats
    type: stats
  - data: home.welcome
    type: split
---
