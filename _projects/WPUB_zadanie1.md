---
layout: project
title: First Assignment - Personal Website
course: Web Publishing
school: FIIT STU BA
tags: [web, jekyll, markdown, css, github, github-pages]
---
### Source [Github](https://github.com/nculakova/nculakova.github.io)
____

## Kolekcie

V zadaní som použila niekoľko kolekcií pre uľahčenie práce:
* **hobbies** - na vytvorenie podsekcií rôznych záľub ako knihy, podcasty alebo fotografie
* **projects** - pre spravovanie projektov, školských aj samostatných

## Premenné

V rámci stránky som využila niekoľko rôznych premenných napríklad:
* Kolekcia __hobbies__
  * *author* - autor knihy či tvorcovia filmu
  * *my-date* - pri knihách a filmoch kedy vznikli a pri podcastoch ako často vychádzajú
  * *category* - typ knihy, filmu, podcastu
  * *type* - či je to film, seriál, kniha, podcast alebo fotka aby som vedela kam post zaradiť
* Kolekcia __projects__
  * *course* - na aký predmet bol projekt vytvorený
  * *school* - na akej škole bol vytvorený, podľa existencie tejto premennej zisťujem či ide o školský projekt alebo nie
  * *tags* - aké technológie a jazyky som použila
a ďalšie

## Layouty

Pre uľahčenie práce a obmedzenie redundancie som použila niekoľko layoutov:
* *default* - defaultný layout, ktorý je použitý na všetkých stránkach, obsahuje menu, header a footer
* *hobby* - layout, ktorý je použitý pre zobrazenie kníh, filmov a podcastov
* *photo* - layout pre zobrazenie detailu fotografie s popisom
* *post* - jednoduchý layout pre zobrazenie blogových príspevkov
* *project* - layout pre vyobrazenie rôznych projektov

## Filtre a tagy

V zadaní som využila niekoľko základných filtrov a tagov:
* *sort* - je použitý pre zoradenie zobrazenia navigácie (menu)
* *include* - používam ho pre includeovanie rôznych častí CV
* *for* - je využitý napríklad pre zobrazenie všetkých kolekcií
* *assign* - používam ho pri tagoch rovnako ako pri zoraďovaní menu pre jednoduchšiu prácu
* *if* a *unless* - používam na niekoľkých miestach pre zisťovanie ktoré podstránky kde zobraziť

## Plugin
Použila som jednoduchý jekyll-spotify plugin na zobrazenie mojich mesačných playlistov. [github](https://github.com/MertcanGokgoz/Jekyll-Spotify)
