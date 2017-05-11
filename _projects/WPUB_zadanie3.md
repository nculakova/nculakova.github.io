---
layout: project
title: Third Assignment - Presentation with xml, xsl, xsd
course: Web Publishing
school: FIIT STU BA
tags: [xml, xsl, css, html, xml-schema, pdf]
---
### Source [Github](https://github.com/nculakova/wp-z3.git)

V zadaní som vytvárala prezentáciu pomocou xml a xsl technológií.

## Obsah prezentácie

Obsah prezentácie je v súbore presentation.xml kde pomocou tagov vytvárame jednotlivé časti a možnosti. Tagy ktoré prezentácia obsahuje:
* **presentation** - root element, ktorý obsahuje všetky ostatné elementy
* **slide: title/section-title/-** - element pre jednotlivý slide pomocou ktorého sa súbor rozdelí na strany, môže byť typu title pre titulný slide, section-title pre nadpisy jednotlivých sekcií alebo klasický bez typu pre textové/obrázkové slidy
* **text** - pre sekcie s obsahom
* **p** - pre textové paragrafy
* **b** - pre tučný text
* **presentation-title, section-title, title** - pre jednotlivé nadpisy
* **author, institution** - informácie o tom kto vytváral prezentáciu na úvodnú stranu
* **figure: image, description** - element pre obrázok s podelementmi obrázku s odkazom a popisom
* **list: itemized/enumerated** - očíslovaný a neočíslovaný list s elementmi *item* pre jednotlivé body

## Transformácia

V oboch XSL súboroch som vytvorila templatey pre jednotlivé elementy z XML pomocou *xsl:template match="element"*.

## Transformácia do HTML

Pre transformáciu som použila SAXON s použitím štýlovania cez CSS.

XSL pre transformáciu do HTML sme použili to_html.xsl so štýlovaním style.css. V XSL súbore sme využívali klasické HTML elementy aj niekoľko personalizovaných tried
* **div** - pre vyčlenenie časti 
* **p, h1, h2, h3** - pre nastavenie velkosti textu
* **b** - pre tučný text
* **img, figcaption** - pre zobrazenie obrázku a popisu
* **ul, ol, li** - pre číslovaný a nečíslovaný zoznam a body v ňom
* **title-page** - trieda pre nastavenie titulnej stránky
* **section-title-page** -trieda pre nastavenie titulnej stránky sekcie
* **footer** - trieda pre zápätie stránky s číslovaním
* **text** - trieda pre obsah stránky
* **title** - trieda pre nadpisy stránok
* **fig** - trieda pre obrázky

Používateľ si tiež môže personalizovať niektoré časti pomocou parametrizácie cez argumenty xsl
* **font** - pre nastavenie fontu
* **background-color** - pre nastavenie farby pozadia
* **text-color** - farba všeobecného textu
* **title-color** - farba nadpisov a nadpisu prezentácie
* **subtitle-color** - farba podnadpisov

## XML Schema

Opis dokumentu som spravila pomocou XML Schema kde som zadefinovala možné súčasti dokumentu a ich vnorenie. Prezentácia musí obsahovať aspoň jeden slide a list musí obsahovať aspoň jeden item inak má používateľ voľnosť použiť akékoľvek kombinácie chce.

## Transformácia do PDF

Pre transformáciu som použila XEP.

Formátovanie je vytvorené využitím 
* **fo:block, fo:block-container** - pre označenie jednotlivých častí textu
* **fo:list-block** - pre list - číslovaný/nečíslovaný
* **fo:list-item** - pre konkrétny bod listu
* **fo:list-item-label** - typ identifikátora pre body listu
* **fo:list-item-body** - telo listu
* **fo:external-graphic** - pre zobrazenie obrázkov
* **fo:inline** - pre využitie inline štýlov v text ako tučný text
