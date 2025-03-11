Tommi Pölkki

## Johdanto

Tarkoituksena on testata ohjelmaa, johon voidaan syöttää nimi, salasana ja ikä sekä rooli, varaaja tai admin. Työ kaluina käytän Virtual Boksia johon asensin kalin. Kalissa käytän ZaProxy ohjelmaa jolla voidaan etsiä haavoituvvuuksia ohjelmasta. Ensimmäisellä kerralla testaan vain helposti huomattavia ongelmia joita ohjelman turvallisuuteen liitty.


## Aikataulu

Aloitan työskentelyn 14.2.2025 ja lopetan 20.2.2025 työskentelen testauksen parissa 1-2 tuntia päivässä, tarpeen mukaan. Testaus ympäristönä toimii johdannossa mainittu Kali. Toinen testaus kierros 2-3.3.2025


## Testaus

Testasin ohjelmaa Zaproxy ohjelmallla.

Etsin Zaproxylla ohjelmasta sql injektiolla, mahdollisia tapoja keskeyttää kirjotuminen ja saada kirjautumis- tiedot. Koitin saada jo tallennettuja tietoja tunkeutumalla ohjelman tallentamiin tietoihin.


## Yhteenveto

On mahdollista päästä käsiksi ohjelman tallentamiin tietoihin ja käyttää niitä. Tietoja voidaan hankkia keskeyttämällä kirjautuminen, muuttamalla salasanan parametrejä ja jatkaa kirjautumis- prosessia, jolloin ohjelma ei tunnista tätä virheelliseksi. Hyökkäyksellä voidaan muokata formaattia, joka johtaa bufferointi virheisiin. Tällä hetkellä ohjelman tietoturva on heikko ja vaatii paljon parannuksia.


## Löydöt

# kierros 1

Format String Error

Ohjelma hyväksyy merkkijonon argumenttina, mutta se on peräisin ulkoisestalähteestä. Voidaan muokata ohjattua merkkijonoa ja tämä johtaa että ohjelma esittää tietoja, jotka pitäisi olla suojattuja eikä näkyvillä kaikille

SQL Injection

Kirjatessa sisään on mahdollista keskeyttää tapahtuma ja muuttaa salasana parametrejä jolloin voitiin luoda samalle käyttäjälle useampi salasana tai muuttaa ohjelma tunnistamaan tietyn merkin käyttäjän salanaksi.


Path Traversal

On mahdollista saada pääsy tiedostoihin, hakemistoihin ja komentoihin. Hyökkääjä voi manipuloida URL-osoitetta, että verkkosivusto paljastaa tiedostojen sisällön.

Appendice: Checkmarx ZAPv1.md 

# kierros 2
Suurin osa edellisen kierroksen haavoituvuuksista on postunut, eli korjaukset ovat toimivia. Automaattinen skannaus ei anna suoraan alertteja, mutta mahdollisia haavoituvuuksia edelleen löytyy, joita pitää tarkastella jatkossa seuraavissa tarkituksissa.



Appendice: Checkmarx ZAPv2.md
