---
title: El projecte Turbo
---

# El projecte Turbo

**Turbo** és un joc de curses per consola, escrit en Java, que anirem construint al llarg del curs. No el programem tot de cop: a cada etapa del circuit aprenem un concepte nou i el fem servir per afegir-hi una peça.

L'objectiu és que vegis per què serveix cada cosa que aprens. Un array no és un exercici abstracte: és on guardem els temps de volta. Un `String` no és teoria: és la matrícula que hem de validar abans de deixar sortir un cotxe a pista.

## Com creix el Turbo

| Etapa | Concepte | Què hi afegim |
|:---:|---|---|
| 01 | Fonaments | Guardem les dades del pilot i del cotxe en variables i decidim si cal entrar a boxes |
| 02 | Arrays | Guardem el temps de cada volta i calculem la volta ràpida i la mitjana |
| 03 | Strings | Validem matrícules i generem l'abreviatura del pilot |
| 04 | Funcions | Separem el programa en mètodes: `calcularMitjana`, `esMatriculaValida`... |
| 05 | Classes i objectes | Creem les classes `Cotxe`, `Pilot` i `Cursa` |

## Les regles del joc

El Turbo simula una cursa senzilla:

- Hi ha diversos **pilots**, cadascun amb un nom, una abreviatura de tres lletres (com a la F1: `ALO`, `HAM`) i un cotxe.
- Cada **cotxe** té una matrícula, una velocitat màxima i un dipòsit de combustible.
- La cursa té un nombre fix de **voltes**. A cada volta es calcula un temps i es gasta combustible.
- Si un cotxe es queda sense combustible ha d'entrar a **boxes**, i això li costa temps.
- En acabar, es mostra la **classificació** ordenada pel temps total.

!!! turbo "Al Turbo"

    A cada pàgina d'etapa trobaràs un bloc com aquest, que t'explica quina peça del Turbo construïm amb el que acabes d'aprendre.
