# Portada i tema dels apunts de Programació

Aquest repo fa dues coses:

1. Publica la portada a <https://programacio-26-27.github.io/>.
2. Defineix l'aspecte comú de tots els apunts (carpetes `_layouts`, `_includes` i `assets`). Si canvies el disseny aquí, canvia a totes les BA.

Funciona igual que el de Bases de dades. La marca és **Circuit** (asfalt, vorada vermella i blanca i groc bandera) i el fil comú del curs és el projecte **Turbo**.

## Editar la portada

- Nom, curs, mòdul i institut: `_config.yml`.
- Llista de blocs: `_data/blocs.yml`. Per obrir una BA, posa l'adreça del seu repo a `url` (per exemple `url: /funcions/`). Si `url` està buit, surt com a "Properament". Si `ra` està buit, surt un guió.
- Les etapes del Turbo de la portada: secció `fil` de `_layouts/portada.html`.

## Afegir una BA nova

1. Crea un repo privat a l'organització (per exemple `funcions`) amb un `README.md` que faci d'índex i els apunts a `teoria/`.
2. Copia-hi el `_config.yml` de la carpeta `plantilla-ba` i canvia-hi les dades del bloc.
3. Al repo nou: `Settings > Pages > Deploy from a branch`, branca `main`, carpeta `/ (root)`.
4. A `_data/blocs.yml` d'aquest repo, posa `url: /funcions/` a la BA corresponent.

## Blocs especials dins dels apunts

Fitxa a l'inici d'un tema (llista amb la classe `fitxa`):

```markdown
- **Tema** 4.1
- **Al Turbo** temps de volta
{: .fitxa}
```

"Al Turbo" (groc) i "Repte" (vermell): una cita amb la classe a sota.

```markdown
> **Al Turbo**
>
> Text i codi...
{: .turbo}

> **Repte**
>
> 1. Exercici
{: .repte}
```

Interactiu incrustat (un HTML a la carpeta `interactius/` del repo de la BA). Per a presentacions 16:9, afegeix la classe `diapos`. Posa `ample: true` al front matter perquè ocupi més amplada.

```html
<div class="interactiu">
  <div class="interactiu-barra">
    <span class="interactiu-titol">Simulador pas a pas</span>
    <a class="interactiu-obrir" href="../interactius/arrays.html" target="_blank" rel="noopener">Pantalla completa</a>
  </div>
  <iframe src="../interactius/arrays.html" title="Arrays en Java" loading="lazy"></iframe>
</div>
```

## Consells per als fitxers .md

GitHub Pages és més estricte que la vista de GitHub:

- Deixa sempre una línia en blanc abans i després de cada taula.
- Deixa una línia en blanc abans de `---` (si no, el text de sobre es converteix en títol).
- Deixa una línia en blanc abans de `<!--` quan amaguis temes de l'índex.
- Si un bloc de codi conté `{{` o `{%`, envolta'l amb `{% raw %}` i `{% endraw %}`.
