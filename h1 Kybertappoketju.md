## X) Darknet Diaries  
EP 156 Kill list: kyberammattilainen Chris Monteiro halusi selvittää onko darknetin palkkamurhaajasivustot todellisia. Hän nopesti selvitti, että kyseessä oli ennemminkin urbaani legenda ja kirjoitti asiasta RationalWiki-artikkelin. Artikkelia kuitenkin muokattiin nopeasti romanialaisesta ip-osoitteesta. Artikkeliin lisättiin tieto, että Besa Mafia -merkkinen sivusto on aitoa kamaa. Monteiro kiinnostui ja pääsi sivuston huonon suojauksen takia lukemaan tilaussivuston asiakkaiden pyyntöjä, maksutoimituksia ja yksityiskohtaisia tietoja tilauskeikasta. Kysessä oli petossivu, jossa maksetut palkkamurharahat valuivat Romaniaan. Vaikka palkkamurhaajaa ei tuolta sivulta saatu yritti Monteiso eri tavoin tiedottaa uhreja murhasuunnitelmista. Hän myös toimitti eri viranomaisille tietoa, mutta hänen oli vaikea saada riittävän nopeita kansainvälisiä poliisikontakteja. Useita kymmeniä sivuston kautta tunnistettuja uhreja on jo murhattu. 

**Hutchins ym.**
APT Advanced Persistent Threat > Tietojen vaarantaminen taloudellisen tai sotilaallisen edun saavuttamiseksi.  
Kohdistettujen hyökkäysten vastaan reagointi on haastavaa, koska reagointi tapahtuu pääsääntöisesti vasta tietomurron jälkeen.
APT-toimia kohdistetaan ihmisiin. APT-tunkeutumisten torjuminen vaatii kehitystä analyysimenetelmissä, prosesseissa ja teknologiassa. Tekojen estäminen vaatii tunkeutumisen ennakoimista ja tiedusteluun perustuvaa uhkakeskehkeistä lähestymistä jossa tunkeutumiset analysoidaan hyökkääjän näkökulmasta. 
"kill chain" malli > Havainto > Paikannus > Seuranta > Kohdistaminen > Hyökkäys > Arviointi (U.S. Department of Defense, 2007)

Kill chainia on käytetty IED (improvised explosive devices) hyökkäysten mallintamiseen, terrosrismin ehkäisyssä, tietoturva-alalla (ABSAC), ja sisäpiiriuhkien torjunnassa.  

**Kill chain -mallissa yksi onnistunut torjuntatoimi katkaisee ketjun ja estää hyökkääjän etenemisen**  
Indicators, vihjeet: 
 - Atomic yksittäiset elementit, joita ei voi jakaa opienempiin osiin menettämättä kontekstia. IP-osoitteet, sähköpostiosoitteet, _haavoittuvuustunnisteet_
 - Computed laskennalliset tiedot Hashit ja säännölliset lausekkeet
 - Behavioral edelliset vihjeet yhdessä ja niiden käyttötapojen lukeminen. Vaatii laajaa tietotaitoa ja yhteistyötä sekä hyvää raportointia.
_Tunkeutumisen kill chain_:
FIND, FIX, TRACK, TARGET, ENGAGE, ASSES (F2T2EA)  
  "Tunkeutumisen ydin on se, että hyökkääjän on kehitettävä hyökkäyspaketti (payload) tunkeutuakseen luotettuun ympäristöön, vakiinnutettava asemansa siellä ja suoritettava toimenpiteitä tavoitteidensa saavuttamiseksi."

  1. Tiedustelu (Reconnaissance)  
  2. Aseistaminen (Weaponization)  
  3. Toimitus (Delivery)  
  4. Hyödyntäminen (Exploitation)
  5. ASennus (Isntallation)
  6. Command and control
  7. tavoitteiden saavuttaminen (Action of objectives)

Vastatoimet: 
isäntäjärjestelmän tunkeutumisen havaitsemisjärjestelmä (HIDS)
Pachingin automatisointi
Etäkäytön esto, käyttäjien koulutus ym.

Hyökkäyksen jälkeinen analysointi auttaa valmistautumaan seuraavaan hyökkäykseen. 


**KKO 2003:36 R2001/678** 
Käyttäjä a on skannannut 23.11.1998 Osuuspankkikeskuksen portit pääsemättä läpi palomuurista. 
Tietomurron yritys nuorena henkilönä, korvausvaade: 
"Rikoslain 38 luvun 8 §:n 1 momentin mukaan se, joka käyttämällä hänelle kuulumatonta käyttäjätunnusta taikka turvajärjestelyn muuten murtamalla oikeudettomasti tunkeutuu tietojärjestelmään, jossa sähköisesti tai muulla vastaavalla teknisellä keinolla käsitellään, varastoidaan tai siirretään tietoja, taikka sellaisen järjestelmän erikseen suojattuun osaan, on tuomittava rangaistukseen tietomurrosta. Saman pykälän 3 momentin mukaan myös yritys on rangaistava." On ollut tuolloin voimassa ja on voimassa edelleen. Sakkoa-2 vuotta vankeutta ellei muualla asiasta määrätä suurempaa rangaistusta. Pääsääntöisesti asianomistajarikos. 

## a) Kali asennettuna virtuaalikoneeseen
versio: kali-linux-2025.1a-live-amd64 
Loin kloonin jo aiemmin luodusta Kalista.  

## b) ping

<img width="565" alt="netti poikki" src="https://github.com/user-attachments/assets/9c242867-db1f-4f4f-8c5c-1bf40ad936e4" />    

Oikeasta yläkulmasta kaapeli irti. 

## c) Porttiskannaa 100 tavallisinta tcp-porttia omasta koneestasi komennolla nmap -TA -A localhost

nmap -TA -A localhost  //man nmap  
nmap > porttiskannaustyökalu, joka käyttää ip-paketteja sen selvittämiseen mm. mitä hosteja,   
-T4 > nopeuttaa skannausta  
-A > ottaa mukaan skannaukseen myös OS version havaitsemisen  
localhost > koneen oletus kotisivu 127.0.0.1  

<img width="414" alt="nmap localhost" src="https://github.com/user-attachments/assets/2baa9b29-ce8f-4d77-b163-24c4a938a733" />

skannattiin klo 23:44 localhost -osoitettani 127.0.0.1   
verkko on toiminnassa.   
localhostilla on muita osoitteita "localhostin" lisäksi ip loppuu ::1  
mitään skaanaamistani tuhannesta portista ei ole auki.  
ei näytetä 1000 tcp porttia  

## e) Megasploitable 2 +  Vagrant 
$ sudo apt-get -y install virtualbox vagrant curl  
$ mkdir metas/  
$ cd metas/  


**Tässä vaiheessa nukkumaan. Testailu ja raportointi jatkuu ehkä ensi yönä. ** 2.4.2025 klo 0:19 😴







     

LÄHTEET: 
Kurssin läksysivu: https://terokarvinen.com/tunkeutumistestaus/  
Jack Rhysider, Darknet Diaries [EP 156](https://darknetdiaries.com/episode/156/) kuunneltu 29.3.2025   
Eric M. Hutchins, Michael J. Cloppert, Rohan M. Amin, Ph.D.‡ Lockheed Martin Corporation: Intelligence-Driven Computer Network Defense
Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains [Whitepaper-intel-driven-defence](https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)  käännetty chatgptlla ja tiivistetty 1.4.2025  
KKO 2003:36 [ennakkopäätös](https://finlex.fi/fi/oikeuskaytanto/korkein-oikeus/ennakkopaatokset/2003/36#OT0_OT0) luettu 1.4.2025
ajantasainen lainsäädäntö [rikoslaki](https://finlex.fi/fi/lainsaadanto/1889/39-001?language=fin&highlightId=591158&highlightParams=%7B%22type%22%3A%22BASIC%22%2C%22search%22%3A%22rikoslaki%22%7D#chp_38v19950578__sec_10v20110441__heading) luettu 1.4.2025
$ man nmap luettu osaksi 1.4.2025
Karvinen 2018 [Install Metasploitable 3 – Vulnerable Target Computer](https://terokarvinen.com/2018/install-metasploitable-3-vulnerable-target-computer/)
