# h2 Täysin Laillinen Sertifikaatti  
## x) lue ja tiivistä: 
**OWASP Top 10:2021 A01:2021 – Broken Access Control** 
    Käyttöoikeuksien hallinnan murtaminen ja hallitseminen. Johon käytetään mm. seuraavia heikkouksia:
    Vähimmän oikeuden periaatteen rikkominen tai salliminen oletusarvoisesti.   
    Käyttöoikeustarkastusten ohittaminen muokkaamalla osoiteriviä. 
    Mahdollisuus tarkastella tai muokat atoisen käyttäjän tiliä unique identifierin kautta.   
    Pääsy Application programming interface eli APi:in ilman käyttöoikeuksia.  
    Oikeuksien korotus ilman lupaa. esmin käyttäjästä adminiksi.   
    Metadatan manipulointi esim JSON web token  
    CORS virheet saattavat hyväksyä API-pyyntöjä vääristä lähteistä. 
    Väkisin selaaminen  sivulle pääsee selaamaan kirjautumatta tai pääsy halluntapaneeliin ilman admin-tunnuksia.   
**OWASP Top 10:2021 A10:2021 Server-Side Request Forgery (SSRF)**  
    SSRF -haavoittuvuus antaa mahdollisuuden hyökkääjälle hakea etäresurssia URL-osoitetta tarkastamatta. 
    Hyökkääjä pakottaa palvelimen tekemään verkkopyynnön hyökkääjän haluamaan osoitteeseen. Eli jos haavoittuvuus on olemassa, niin hyökkääjä saa serverin sisäisiä tietoja käyttöönsä, koska pyynnöt näyttövät tulevan omalata palvelimelta. Käyetäänkö tätä palvelunestohyökkäyksiin?

    

  

    
    
    
    
LÄHTEET:  
Broken Access Control [Owasp top 10, 2021 A01](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)  luettu 9.4.2025  
Server-Side Request Forgery (SSRF) [Owasp top 10, 2021 A10](https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29/)  luettu 9.4.2025
