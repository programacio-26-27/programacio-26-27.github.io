---
hide:
  - toc
title: "01 · Fonaments"
---

# Fonaments de la programació

<div class="fitxa">
  <span><b>Etapa</b> 01</span>
  <span><b>Al Turbo</b> dades del pilot i del cotxe</span>
  <span><b>Prerequisits</b> cap</span>
</div>

De l'algorisme a la lògica binària: què és un algorisme, variables, operadors matemàtics, condicions, operadors lògics i portes lògiques.

<div class="interactiu">
  <div class="interactiu__barra">
    <span class="interactiu__titol">Presentació interactiva</span>
    <a class="interactiu__obrir" href="../../interactius/fonaments.html" target="_blank" rel="noopener">Pantalla completa</a>
  </div>
  <iframe class="interactiu__marc interactiu__marc--169" src="../../interactius/fonaments.html" title="Fonaments de la programació" loading="lazy" allowfullscreen></iframe>
</div>

!!! turbo "Al Turbo"

    La primera peça del Turbo són les dades: el pilot i el cotxe es guarden en variables, i amb una condició decidim si el cotxe pot fer una volta més o ha d'entrar a boxes.

    ```java
    String pilot = "Alonso";
    double combustible = 12.5;        // litres al dipòsit
    final double CONSUM_PER_VOLTA = 2.8;

    boolean potFerVolta = combustible >= CONSUM_PER_VOLTA;

    if (potFerVolta) {
        combustible = combustible - CONSUM_PER_VOLTA;
        System.out.println(pilot + " fa una volta. Queden " + combustible + " L");
    } else {
        System.out.println(pilot + " entra a boxes");
    }
    ```

!!! repte "Repte"

    1. Afegeix una variable `boolean pneumaticsGastats`. El cotxe ha d'entrar a boxes si no té prou combustible **o** si els pneumàtics estan gastats.
    2. Si queden menys de tres voltes de combustible, mostra el missatge `Reserva!`.
