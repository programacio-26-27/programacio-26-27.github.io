---
hide:
  - toc
title: "03 · Strings"
---

# Strings

<div class="fitxa">
  <span><b>Etapa</b> 03</span>
  <span><b>Al Turbo</b> matrícules i abreviatures</span>
  <span><b>Prerequisits</b> Fonaments, Arrays</span>
</div>

Crear i mida, recórrer, comparar, buscar, retallar i transformar un String; passar de String a array i tornada; construir textos amb `StringBuilder`, i les trampes típiques.

<div class="interactiu">
  <div class="interactiu__barra">
    <span class="interactiu__titol">Simulador pas a pas</span>
    <a class="interactiu__obrir" href="../../interactius/strings.html" target="_blank" rel="noopener">Pantalla completa</a>
  </div>
  <iframe class="interactiu__marc" src="../../interactius/strings.html" title="Strings en Java" loading="lazy"></iframe>
</div>

!!! turbo "Al Turbo"

    Abans de sortir a pista, el Turbo comprova que la matrícula tingui el format `1234-BCD`: quatre xifres, un guió i tres consonants majúscules.

    ```java
    String m = sc.nextLine().trim().toUpperCase();
    boolean valida = m.length() == 8 && m.charAt(4) == '-';

    for (int i = 0; i < 4 && valida; i++) {
        valida = Character.isDigit(m.charAt(i));
    }
    for (int i = 5; i < 8 && valida; i++) {
        char c = m.charAt(i);
        valida = c >= 'A' && c <= 'Z' && "AEIOU".indexOf(c) == -1;
    }
    ```

!!! repte "Repte"

    1. A partir del nom complet d'un pilot (`"Lewis Hamilton"`), genera la seva abreviatura: les tres primeres lletres del cognom en majúscules (`"HAM"`).
    2. Llegeix una línia amb el format `ALO;92.4;91.8;93.1`, separa-la amb `split` i calcula la mitjana dels temps.
    3. Amb un `StringBuilder`, construeix la línia `V1 V2 V3 ... V10` sense espai al final.
