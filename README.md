# Circuit · Programació 26-27

Apunts de M0485 Programació (1r DAMvi i DAW, Institut Sabadell).
Web pública: <https://programacio-26-27.github.io/>

El repo és **privat** (l'organització té GitHub Team gràcies al compte de professora):
el codi font no el veu ningú, però el web és públic. Cada `push` a `main` compila i publica
el web automàticament.

## Posada en marxa (un sol cop)

1. Comprova que l'organització `programacio-26-27` té el pla **GitHub Team**
   (Settings > Billing and plans). Si surt Free, aplica-hi el benefici de professora
   igual que vas fer amb `bases-de-dades-26-27`.
2. Crea el repo **privat** `programacio-26-27.github.io` i puja-hi tot el contingut d'aquesta
   carpeta, inclosa la carpeta oculta `.github`.
3. Settings > Pages > Build and deployment > Source: **GitHub Actions**.
   Si hi ha l'opció de visibilitat, deixa-la en **Public**.
4. Pestanya **Actions**: quan "Publica el web" acabi en verd, el web és a
   <https://programacio-26-27.github.io/>.

## Estructura

```
docs/
  index.md                 Portada amb el mapa del circuit
  turbo/index.md           El projecte fil comú
  etapes/                  Una pàgina per etapa
  interactius/             Els HTML interactius (presentacions i simuladors)
  esborranys/              NO es publica
  assets/logo.svg          Logo
  stylesheets/circuit.css  Identitat visual
mkdocs.yml                 Configuració i menú
```

## Afegir una etapa nova

1. Si hi ha interactiu, copia l'HTML a `docs/interactius/` (per exemple `funcions.html`).
2. Crea `docs/etapes/04-funcions.md` amb la plantilla de sota.
3. Afegeix-la al menú a `mkdocs.yml`, dins de `nav > Etapes`.
4. A `docs/index.md`, a l'etapa 04: canvia `class="propera"` per `class="feta"`,
   el `<div class="etapa">` per `<a class="etapa" href="etapes/04-funcions/">` (i el `</div>` per `</a>`)
   i l'estat a `Disponible`.

Mentre una pàgina no estigui llesta, deixa-la a `docs/esborranys/`.

Per veure-ho en local abans de pujar-ho:

```bash
pip install -r requirements.txt
mkdocs serve        # http://127.0.0.1:8000
```

## Plantilla d'etapa

````markdown
---
hide:
  - toc
title: "04 · Funcions"
---

# Funcions

<div class="fitxa">
  <span><b>Etapa</b> 04</span>
  <span><b>Al Turbo</b> què hi afegim</span>
  <span><b>Prerequisits</b> Fonaments, Arrays, Strings</span>
</div>

Una o dues frases sobre què es veu a l'etapa.

<div class="interactiu">
  <div class="interactiu__barra">
    <span class="interactiu__titol">Simulador pas a pas</span>
    <a class="interactiu__obrir" href="../../interactius/funcions.html" target="_blank" rel="noopener">Pantalla completa</a>
  </div>
  <iframe class="interactiu__marc" src="../../interactius/funcions.html" title="Funcions" loading="lazy"></iframe>
</div>

!!! turbo "Al Turbo"

    Com fem servir el concepte al projecte.

!!! repte "Repte"

    1. Exercici
````

- Per a presentacions en format 16:9, afegeix `interactiu__marc--169` a la classe de l'`iframe`.
- Blocs disponibles: `turbo` (groc), `boxes` (blau, per a errors típics), `repte` (vermell),
  i els estàndard (`note`, `tip`, `warning`...). Amb `???` en lloc de `!!!` el bloc surt plegat.

## No pugis al repo

Res que no vulguis que vegin els alumnes **dins de `docs/`** fora d'`esborranys/`
(solucions, exàmens...). Tot el que es publica es pot llegir amb "Veure codi font" del navegador.
