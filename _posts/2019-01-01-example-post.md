---
layout: post
title: Tilastolliset tunnusluvut
date: 2019-01-01 00:00:00 +0800
category: tutorial
thumbnail: /style/image/thumbnail.png
icon: book
---
<style>
.collapsible {
  background-color: #777;
  color: white;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
}

.active, .collapsible:hover {
  background-color: #555;
}

.collapsible:after {
  content: '\002B';
  color: white;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}

.active:after {
  content: "\2212";
}

.exercise-content {
  padding: 0 18px;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.2s ease-out;
  background-color: #f1f1f1;
}
</style>

* content
{:toc}

# Tilastolliset tunnusluvut
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

Tässä luvussa tutkitaan Suomessa asuvia lapsiperheitä, joissa on alle 18-vuotiaita lapsia. Lapsiperheitä koskevat tiedot on poimittu <a href="https://www.stat.fi/">Tilastokeskuksen sivulta</a>. Tämä lähestyminen seuraa <a href="http://yle.fi/plus/abitreenit/2020/kevat/2020-03-18_N_fi/index.html#6">kevään 2020 lyhyen matematiikan ylioppilaskokeen tehtävää 6</a>.

Tutkimista varten määritellään muutamia tilastotieteen keskeisiä käsitteitä.

{% include definition-start.html %}
### Havaintoyksikkö ja havaintoarvo
Tutkittavan joukon alkioita kutsutaan <em>havaintoyksiköiksi</em>. Havaintoyksikköön liittyvää arvoa tai suuretta kutsutaan <em>havaintoarvoksi</em>.
{% include definition-end.html %}

Tässä tutkittava joukko on Suomessa asuvat lapsiperheet, joissa on alle 18-vuotiaita lapsia. Jokainen perhe on havaintoyksikkö ja perheen alle 18-vuotiaiden lasten lukumäärä on havaintoarvo. 

{% include exercise-start.html id="test1" header="Havaintoyksikkö ja havaintoarvo: kotipihan linnut" %}
Aleksanteri tutkii kotipihallaan pesivien lintujen linnunpönttöjen asukkaat. Niissä pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen.
* Mikä Aleksanterin tutkimuksessa on havaintoyksikkö?
* Mikä Aleksanterin tutkimuksessa on havaintoarvo?
{% include exercise-end.html %}
