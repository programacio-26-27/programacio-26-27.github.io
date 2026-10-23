# Portada i tema dels apunts de Programació

Aquest repo fa dues coses:

1. Publica la portada a <https://programacio-26-27.github.io/>.
2. Defineix l'aspecte comú de tots els apunts (carpetes `_layouts`, `_includes` i `assets`). Si canvies el disseny aquí, canvia a totes les BA.

Funciona igual que el de Bases de dades. **Ha de ser públic**: si és privat, les BA no poden carregar el tema i no compilen.

## Editar la portada

- Nom, curs, mòdul i institut: `_config.yml`.
- Llista de blocs: `_data/blocs.yml`. Per obrir una BA, posa l'adreça del seu repo a `url` (per exemple `url: /funcions/`). Si `url` està buit, surt com a "Properament". Si `ra` està buit, surt un guió.

## Afegir una BA nova

1. Crea un repo privat a l'organització (per exemple `funcions`) amb un `README.md` que faci d'índex i els apunts a `teoria/`.
2. Copia-hi el `_config.yml` de la carpeta `plantilla-ba` i canvia-hi les dades del bloc.
3. Al repo nou: `Settings > Pages > Deploy from a branch`, branca `main`, carpeta `/ (root)`.
4. A `_data/blocs.yml` d'aquest repo, posa `url: /funcions/` a la BA corresponent.

## Elements per als apunts

Enllaç al codi de classe, a sota del títol:

```html
<p class="codi-classe"><span class="etiqueta">Codi de classe</span> <a href="URL-DEL-FITXER" target="_blank" rel="noopener">Fitxer.java</a></p>
```

Simulador pas a pas incrustat. `?tema=3&sol=1` obre només el tema 3, sense pestanyes. Posa `ample: true` al front matter perquè ocupi més amplada. L'alçada s'ajusta sola. Per a presentacions 16:9, afegeix la classe `diapos` al `div`.

```html
<div class="interactiu">
  <div class="interactiu-barra">
    <span class="interactiu-titol">pas a pas</span>
    <a class="interactiu-obrir" href="../../interactius/condicionals.html?tema=3" target="_blank" rel="noopener">Pantalla completa</a>
  </div>
  <iframe src="../../interactius/condicionals.html?tema=3&amp;sol=1" title="else if" loading="lazy"></iframe>
</div>
```

Navegació entre apartats, al final de la pàgina:

```html
<nav class="passos-nav" aria-label="Apartats">
  <a class="anterior" href="if-else.html"><small>Anterior</small><strong>2.2 if else</strong></a>
  <a class="seguent" href="condicions-compostes.html"><small>Següent</small><strong>2.4 Condicions compostes</strong></a>
</nav>
```

A la BA1, totes aquestes pàgines es generen amb `eines/genera_pagines.py`.

## Consells per als fitxers .md

GitHub Pages és més estricte que la vista de GitHub:

- Deixa sempre una línia en blanc abans i després de cada taula.
- Deixa una línia en blanc abans de `---` (si no, el text de sobre es converteix en títol).
- Deixa una línia en blanc abans de `<!--` quan amaguis temes de l'índex.
- Si un bloc de codi conté `{{` o `{%`, envolta'l amb `{% raw %}` i `{% endraw %}`.
