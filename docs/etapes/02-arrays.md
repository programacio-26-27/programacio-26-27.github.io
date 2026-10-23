---
hide:
  - toc
title: "02 · Arrays"
---

# Arrays

<div class="fitxa">
  <span><b>Etapa</b> 02</span>
  <span><b>Al Turbo</b> temps de volta</span>
  <span><b>Prerequisits</b> Fonaments</span>
</div>

Crear, omplir, recórrer, obtenir i modificar valors, printar un array, la classe `Arrays` i les tres trampes típiques. Executa el codi pas a pas i respon les preguntes abans de veure el resultat.

<div class="interactiu">
  <div class="interactiu__barra">
    <span class="interactiu__titol">Simulador pas a pas</span>
    <a class="interactiu__obrir" href="../../interactius/arrays.html" target="_blank" rel="noopener">Pantalla completa</a>
  </div>
  <iframe class="interactiu__marc" src="../../interactius/arrays.html" title="Arrays en Java" loading="lazy"></iframe>
</div>

!!! turbo "Al Turbo"

    Ara el Turbo guarda el temps de cada volta en un array i, en acabar la cursa, busca la volta ràpida amb el mateix patró que el dia més calorós: guardem la **posició**, no el valor.

    ```java
    double[] temps = {92.4, 91.8, 93.1, 91.2, 92.0};

    int posMillor = 0;
    for (int i = 1; i < temps.length; i++) {
        if (temps[i] < temps[posMillor]) {
            posMillor = i;
        }
    }
    System.out.println("Volta ràpida: volta " + (posMillor + 1) + " (" + temps[posMillor] + " s)");
    ```

!!! repte "Repte"

    1. Calcula el temps total de la cursa i la mitjana per volta.
    2. Compta quantes voltes han estat més ràpides que la mitjana.
    3. Fes una còpia de l'array, ordena-la amb `Arrays.sort` i comprova que l'original no ha canviat.
