---
layout: post
title: Tilastolliset tunnusluvut
date: 2019-01-01 00:00:00 +0800
category: tutorial
thumbnail: /style/image/2-Dice-Icon.svg
icon: book
chapter: 1
module: Tilastot ja todennäköisyys (MAA8)
---

* content
{:toc}

## Luvun tavoitteet
Tämän luvun tavoitteena on, että pystyt xxxx. Osaat
* xxxxx
* xxxxx
* xxxxx
* xxxxx
* xxxxx
* xxxxx
* xxxxx

## Frekvenssi
Kiinnistava aloitus tilastojen merkityksestä yhteiskunnassa esim. korona.

Tässä luvussa tutkitaan Suomessa asuvia lapsiperheitä, joissa on alle 18-vuotiaita lapsia. Lapsiperheitä koskevat tiedot on poimittu <a href="https://www.stat.fi/">Tilastokeskuksen sivulta</a>. Tämä lähestyminen seuraa [kevään 2020 lyhyen matematiikan ylioppilaskokeen tehtävää 6](http://yle.fi/plus/abitreenit/2020/kevat/2020-03-18_N_fi/index.html#6>).

Tutkimista varten määritellään muutamia tilastotieteen keskeisiä käsitteitä.


{% include box.html 
type="definition"
header="Havaintoyksikkö ja havaintoarvo" 
content="
Tutkittavan joukon alkioita kutsutaan *havaintoyksiköiksi*. Havaintoyksikköön liittyvää arvoa tai suuretta kutsutaan *havaintoarvoksi*.
" %}

Tässä tutkittava joukko on Suomessa asuvat lapsiperheet, joissa on alle 18-vuotiaita lapsia. Jokainen perhe on havaintoyksikkö ja perheen alle 18-vuotiaiden lasten lukumäärä on havaintoarvo. 
  
{% include box.html  
type="exercise"
header="Havaintoyksikkö ja havaintoarvo: kotipihan linnut" 
content="
Aleksanteri tutkii kotipihallaan pesivien lintujen linnunpönttöjen asukkaat. Niissä pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen.
1. Mikä Aleksanterin tutkimuksessa on havaintoyksikkö? 
1. Mikä Aleksanterin tutkimuksessa on havaintoarvo?
" 
extra="
1. Linnunpöntöt ovat havaintoyksiköitä, niitä on kuusi kappaletta. 
1. Jokaiseen havaintoyksikköön liittyy suure, joka on linnun laji. Linnun laji on siis havaintoarvo.
" %}
  
{% include box.html 
header="Lisätieto: Tilastollinen muuttuja" 
content="
*Tilastolliseksi muuttujaksi* kutsutaan funktiota, joka kuvaa jokaisen havaintoyksikön sitä vastaavalle havaintoarvolle.
" %}  

Tässä moduulissa tutustutaan vain tilanteisiin, joissa havaintoarvoja on äärellinen määrä tai joissa havaintoarvot voidaan numeroida luonnollisilla luvuilla. Tällaisia tilanteita kutsutaan *diskreeteiksi*. Jos tutkittava ominaisuus voi saada mitä tahansa reaalilukuarvoja jollakin välillä, kuten koulun oppilaiden pituudet, ei kyse ole diskreetistä tilanteesta. Näitä tilanteita tutkitaan moduulissa MAA12.
               
Jos joukossa on vähän havaintoyksiköitä, niin havaintoarvot voi esittää luettelemalle ne peräkkäin. Jos havaintoyksiköitä on paljon, niin havaintoarvojen luetteleminen on epäkäytännöllistä ja epähavainnollista. Tällöin havaintoyksiköt pitää *luokitella*. Luokittelussa lasketaan, kuinka moni havaintoyksikkö vastaa kutakin havaintoarvoa. Jos havaintoarvoja on hyvin paljon, täytyy ne ensin luokitella sopiviin luokkiin ennen havaintoyksikköjen laskemista.

Lapsiperheiden luokittelussa lasketaan, kuinka monessa perheessä, eli havaintoyksikössä, on yksi lapsi (havaintoarvo 1), kuinka monessa on kaksi lasta (havaintoarvo 2), jne. Tiedot on koottu alla olevaan taulukoon:
                
| Lasten lkm| f 	|
| ---		| ---	|
| 1			| 241709|
| 2			| 220116| 			
| 3			| 75326	| 
| 4			| 18409	| 
| 5			| 5493	| 
| 6			| 2289	| 
| 7			| 1235	| 
| 8			| 751	| 
| 9			| 476	| 
| 10		| 262	| 
| 11		| 117	| 
| 12		| 41	| 
| 13		| 12	| 
| 14		| 3		| 
| 15		| 0		| 
| 16		| 3		| 
| Yhteensä	| 566242| 
| ---		| ---	|
			
			