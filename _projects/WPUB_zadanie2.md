---
layout: project
title: Second Assignment - Bachelor thesis in Docbook
course: Web Publishing
school: FIIT STU BA
tags: [docbook]
---
### Source [Github](https://github.com/nculakova/wp-z2)
____

V zadaní som prepisovala prvú časť mojej bakalárskej práce do docbook šablóny od Jiřího Koska.

## Členenie a zvýtaznenie textu

Členenie a zvýraznenie textu som zabezpečila niekoľkými tagmi:
* **emphasis** - použila som bežnú emphasis na text, ktorý je italicom ale aj atribút role="strong" pre bold text
* **itemizedlist** - pre zoznam bodov som využila itemizedlist/listitem využila som atribút mark="bullet" pre formátovanie odrážok 
* **chapter** - pre hlavné sekcie
* **section** - pre podsekcia a pod-podsekcie
* **para** - pre jednoduché paragrafy
* **title** - pre nadpisy

## Odkazy a poznámka pod čiarou

Pre odkazy na rôzne časti dokumentu ako kapitoly, sekcie či obrázky som využila možnosť priradiť rôznym elementom id a tiež tag:
* **link** - kde pomocou atribútu linkend=id určujem na ktorú časť sa má odkazovať
Poznámku pod čiarou som zabezpečila jednoduchým tagom:
* **footnote**

## Bibliografia a register pojmov

Bibliografiu som vytvorila pomocou niekolkých tagov:
* **citation** - tento tag som využila priamo na citovanie - na mieste citácie
* **bibliography** - pre vytvorenie bibliografickej sekcie
* **bibliomixed** - pre vytvorenie konkrétnych záznamov v bibliografii
* **abbrev** - pre vytvorenie tagu pre každý záznam pomocou ktorého sa neskôr cituje
Register pojmov som znovu vytvorila len pomocou zopár tagov
* **index**  - pre vygenerovanie sekcie registra pojmov
* **indexterm** - pre označenie jednotlivých pojmov do registra
* **primary** a **secondary** - pre zabezpečenie hierarchického usporiadania

## Obrázky a vzorce
Pre vloženie obrázkov som použila tag:
* **figure** - pre označenie miesta kam sa obrázok vkladá
* **mediaobject**
* **imageobject** a **imagedata** - pre vloženie konkrétneho odkazu na obrázok
* **textobject** a **phrase** - pre vloženie popisu k obrázku
Vzorce som riešila niekoľkými spôsobmi. Jednoduché vzorce som vložila len pomocou UTF-8 kódov znakov, zložitejšie som vkladala cez screenshoty vzorcov a pomocou tagov
* **equation** a **inlineequation** - podľa umiestnenia obrázku 
a cez 
* **graphic** - pomocou atribútu fileref=odkaz_na_obrazok
