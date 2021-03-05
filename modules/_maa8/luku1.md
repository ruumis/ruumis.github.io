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
                
| Lasten lkm| $f$ 	|
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
| **Yhteensä**	| **566242**| 
			
Yllä olevassa taulukossa ensimmäinen sarake "Lasten lkm" vastaa aineiston eri havaintoarvoja. Toinen sarake $f$ taas kertoo perheiden lukumäärän. Luku 15 ei ole havaintoarvo, koska missään perheessä ei ole 15 lasta. Se vaikuttaa mahdolliselta havainnolta, koska suurempiakin perheitä on olemassa. Sanotaan, että luku 15 on *mahdollinen havaintoarvo*, ja se otetaan tämän takia mukaan.

Lasten lukumääränä  17 myös on mahdollinen havaintoarvo; huomaa, että nolla ei ole mahdollinen havaintoarvo, koska tutkitaan perheitä, joissa on lapsia. Luokittelussa lapsiperheisiin liittyvät mahdolliset havaintoarvot rajataan ottamalla mukaan vain kaikki mahdollisuudet pienimmän havaintoarvon ja suurimman havaintoarvon väliltä.
				
{% include box.html  
type="definition"
header="Mahdollinen havaintoarvo" 
content="
*Mahdollinen havaintoarvo* on arvo tai suure, johon jokin havaintoyksikkö voisi liittyä.
" %}	

{% include box.html  
type="exercise"
header="Mahdollinen havaintoarvo: kotipihan linnut (jatkoa)" 
content="
Aleksanteri jatkaa linnunpönttöjen tutkimista tutkimalla myös naapurien linnunpöntöt.
1. Anna esimerkki lintulajista, joka on mielekäs mahdollinen havaintoarvo.
1. Anna esimerkki lintulajista, joka ei ole mielekäs mahdollinen havaintoarvo.
" 
extra="
1. Kaikki havaintoarvot ovat mahdollisia havaintoarvoja, joten Aleksanterin pihan lintulajit (havaintoarvot) kelpaavat vastaukseksi. Myös esimerkiksi talitiainen on mielekäs mahdollinen havaintoarvo.                                
1. Strutsi, koska se ei pesi pöntössä.
" %}
						
Luku, joka kertoo, kuinka moni havaintoyksikkö liittyy havaintoarvoon, on *frekvenssi*. 

Yllä olevasta taulukosta nähdään esimerkiksi, että havaintoarvon 10 frekvenssi on 262, eli kymmenlapsisia perheitä on Suomessa 262 kappaletta. Jos mahdollinen havaintoarvo ei ole havaintoarvo, niin siihen ei liity yhtään havaintoyksikköä, joten sen frekvenssi on nolla.
					
{% include box.html  
type="definition"
header="Frekvenssi ja suhteellinen frekvenssi" 
content="
Mahdollisen havaintoarvon *frekvenssi* on  sitä vastaavien havaintoyksiköiden lukumäärä. Frekvenssiä merkitään yleensä kirjaimella $f$.

Mahdollisen havaintoarvon *suhteellinen frekvenssi* on sen havaintoyksiköiden osuus kaikista havaintoyksiköistä.	Suhteellista frekvenssiä merkitään yleensä symbolilla $f$ %. 
" %}	

Esimerkiksi voidaan laskea, että kolmilapsisia perheitä on Suomessa $\frac{75326}{566242}=0{,}1330\ldots\approx 13{,}3$ %, joten havaintoarvon 3 suhteellinen frekvenssi on $13{,}3$ %.
	
{% include box.html  
type="exercise"
header="Suhteellinen frekvenssi ja teknisen apuvälineen käyttö: Suomen lapsiperheet" 
content="
Tehtävänä on täydentää taulukkoon suhteelliset frekvenssit.

| Lasten lkm| $f$ 	|
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
| **Yhteensä**	| **566242**|

1. Laske yksilapsisten perheiden osuus kaikista perheistä, eli havaintoarvon 1 suhteellinen frekvenssi.
1. Kopioi taulukko  maalaamalla solut ja liitä tiedot taulukkolaskentaohjelmaan, esimerkiksi LibreOffice Calc- ohjelmaan. 
1. Syötä suhteellisen frekvenssin sarakkeeseen havaintoarvoa 1 vastaavalle riville a-kohdan lausekkeesi kaavana. Jos luku 241709 on solussa B1, niin kirjoita viereiseen soluun `=B1/566242*100` ja paina enter. 		
1. Kopioi kaava jokaiseen havaintoarvoon tarttumalla edellisen kohdan solun oikeasta alakulmasta kiinni ja maalaamalla sarake Yhteensä-riville asti. 	
1. Tarkista vastauksesta, saitko tehtyä samanlaisen taulukon.										
" 
extra="
1. Koska tilastossa on lapsiperheitä yhteensä 566242 kappaletta, niin yksilapsisten perheiden osuus kaikista aineiston perheistä on 
					$$\frac{241709}{566242}\approx 42,7\ \%.$$                
1. Taulukkolaskentaohjelman avulla saadaan seuraava taulukko:

| Lasten lkm| $f$ 	| $f$ %	|	 
| ---		| ---	| ---	|
| 1			| 241709| 42,7 %|
| 2			| 220116| 38,9 %|		
| 3			| 75326	| 13,3 %|
| 4			| 18409	| 3,3 %	|
| 5			| 5493	| 1,0 %	|
| 6			| 2289	| 0,4 %	|
| 7			| 1235	| 0,2 %	|
| 8			| 751	| 0,1 %	|
| 9			| 476	| 0,08 %|
| 10		| 262	| 0,05 %|
| 11		| 117	| 0,03 %|
| 12		| 41	| 0,007 %|
| 13		| 12	| 0,002 %|
| 14		| 3		| 0,0005 %|
| 15		| 0		| 0 %	|
| 16		| 3		| 0,0005 %|
| **Yhteensä**	| **566242**| 100 % |
" %}	

Mahdollisten havaintoarvojen ja suhteellisten frekvenssien muodostamaa kokonaisuutta kutsutaan *jakaumaksi*. Jakaumiin tutustutaan tarkemmin luvussa [jakaumat]. 

{% include box.html  
type="exercise"
header="Frekvenssi ja suhteellinen frekvenssi: kotipihan linnut (jatkoa)" 
content="
Aleksin kotipihalla pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen. Kerää lintulajien frekvenssit ja suhteelliset frekvenssit taulukkoon.
" 
extra="
| Havaintoarvo	| $f$ 	| $f$ %	|	 
| ---			| ---	| ---	|
| punarinta		| 1		| $\frac{1}{6}\approx 16,7\ \%$|
| kirjosieppo	| 2		| $\frac{2}{6}\approx 33,3\ \%$|		
| sinitiainen	| 3		| $\frac{3}{6}=50\ \%$|
| **Yhteensä**	| 6		| 100 %	|
" %}

{% include box.html  
type="exercise"
header="Luokittelu ja suhteellinen frekvenssi" 
content="
Suomessa on yhteensä 311 kuntaa. Asukasluvultaan suurin on Helsinki \(635181 asukasta\). Manner-Suomen pienin kunta on Luhanka \(756 asukasta\) ja Ahvenanmaan pienin kunta on Sottunga \(96 asukasta\). Melkein kaikissa kunnissa on eri määrä asukkaita, joten havaintoarvot täytyy luokitella ennen frekvenssien laskemista.

[Kuntaliiton verkkosivujen](https://www.kuntaliitto.fi/vaestotietoja-kunnittain) \(luettu 21.10.2020\) kuvassa kunnat, eli havaintoyksiköt, on luokiteltu asukasmäärän, eli havaintoarvon, mukaan viiteen eri luokkaan.

![alt text](images/kunta.png "Suomen kunnat")

1. Miten asukasmäärät on luokiteltu?
1. Mitä tarkoittavat kuvan luvut 21, 34, 43, 80 ja 133?
1. Laske luokkien suhteelliset frekvenssit.
" 
extra="
1. alle 5000 asukasta, 5000–10000 asukasta, 10001–20000 asukasta, 20001–50000 asukasta ja yli 50000 asukasta.
1. Luokkien frekvenssit.	
" %}

Summafrekvenssi ja suhteellinen summafrekvenssi???	

## Keskiluvut

Aineistoja tutkittaessa mielenkiinnon kohteena on usein löytää aineiston "tyypillisin" tai "keskimmäisin" tapaus. Tätä kuvaamaan käytetään erilaisia keskilukuja. Niiden määrittämisen mielekkyys riippuu havaintoarvojen luonteesta, eli siitä mitä on mielekästä kutsua "tyypilliseksi" kyseisessä aineistossa.

Yksi keskiluku on aineiston yleisin havaintoarvo. Lapsiperheitä tutkiessa huomattiin, että  yksilapsisia perheitä on havaintoyksiköistä kaikkein eniten. Tilastotieteessä yleisintä havaintoarvoa kutsutaan *moodiksi*.
				