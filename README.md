# 2020_Ants_vs_SomeBees



### Kratak opis teme

  U ovom projektu zadatak je napraviti tower defense igru. Igra je inspirisana PopCap-ovom popularnom igrom Plants Vs. Zombies. Igrač treba da odabere mrave kojima će naseliti koloniju. Mravi treba da zaštite svoju kraljicu od zlih pčela koje napadaju njihovu teritoriju. Igrač je pobednik ako uspešno eliminiše sve pčele sa polja. 

### Uputstva za igru:

  Kao što je napomenuto, Ant vs SomeBees je tower defense igra, ili jednostavnije igra invazije.   
  Igra se sastoji od niza poteza. Igraču je na raspolaganju kolonija koja se sastoji od više uzastopnih mesta koja služe za pozicioniranje mrava i kretanje pčela. Koloniju čine 1 ili 3 tunela, u zavisnosti od opcije pokretanja. U svakom potezu nova pčela može ući u mravlju koloniju ili napredovati kroz nju (prelaskom iz polja u polje), i novi mrav može (ali ne mora) biti postavljen. Postavljanje mrava je moguće ako je u koloniji dovoljno hrane na raspolaganju (svaka vrsta mrava zahteva trošenje specifične količine hrane iz kolonije kako bi bio postavljen) i ako je na raspolaganju slobodno mesto na koje će mrav biti pozicioniran. Takođe, u okviru poteza insekti izvode i svoje karakteristične akcije: mravi u zavisnosti od vrste prave hranu ili napadaju, a pčele svojim žaokama ubadaju mrave. Pčela ima oklop koji ih štiti od udara lišćem, međutim on nije neuništiv i čuva pčele samo od 3 napada. Pčela je vodootporna, tj može da preleti polje koje je prekriveno vodom. Kraj igre je kada igrač uspe da onesposobi sve pčele, i tako sačuva svoju koloniju i zasluži pobedu u igri, ili pak ako pčela stigne do kraljice ili poslednjeg polja u koloniji i izvrši invaziju.  
    
  Igraču su na raspolaganju različite vrste mrava sa različitim sposobnostima. Za svakog mrava je specifična količina hrane koju troši pri postavljanju. Kod većine mrava je slučaj da bivaju savladani nakon prvog ujeda pčele.  

* **HarvesterAnt**  
                *troši hrane* : 2   
                *sposobnost:* U svakom potezu skupljaju dodatnu hranu za koloniju.  
                      
* **ThrowerAnt**    
               *troši hrane:* 4   
               *sposobnost:* U svakom potezu gađa lišćem najbližu pčelu.  
                    
* **FireAnt**         
               *troši hrane:* 4   
               *sposobnost:* Kada biva uništen, sprži sve pčele koje su na istom polju kao i on.  
                    
* **ShortThrower**    
              *troši hrane:* 3   
              *sposobnost:* ThrowerAnt koji baca lišće na pčele koje su udaljene najviše 3 polja.  
                    
* **LongThrower**     
               *troši hrane:* 3   
               *sposobnost:* ThrowerAnt koji baca lišće na pčele koje su udaljene najmnaje 4 polja.  
                    
* **WallAnt**         
                *troši hrane:* 4  
                *sposobnost:* Za razliku od ostalih, ovaj mrav može da izdrži 3 napada pčela.   
                    
* **NinjaAnt**     
                *troši hrane:* 6  
                *sposobnost:* Ovaj mrav ne blokira put pčelama, one prolaze pored njega bez da ga ubodu, ali on svakoj pčeli koja ga prođe nanese jedan udarac i time ošteti njihov oklop.    
                    
* **ScubaThrower**
                 *troši hrane:* 5   
                 *sposobnost:* Vodootporni ThrowerAnt, tj ThrowerAnt koji može da bude postavljen na polje prekriveno vodom.  
                    
* **HungryAnt**        
                 *troši hrane:* 4  
                 *sposobnost:* Ovaj mrav ima mogućnost da pojede pčelu koja se nađe na istom polju kao i on. On tek posle 3 poteza (od onesposobljavanja prethodne) može da pojede sledeću pčelu.  

* **BodyguardAnt**       
                  *troši hrane:* 4  
                  *sposobnost:* Ovaj mrav štiti druge mrave, tako što prvo pčele napadaju njega pa tek kada on biva onesposobljen pčela napada drugog mrava sa kojim on deli polje. On je jedini koji može da deli polje sa drugim mravom.  
                    
* **QueenAnt**        
                  *troši hrane:* 6  
                  *sposobnost:* Kraljica kolonije, vodootporni ScubaThrower. Kada kraljica baci list ona udvostruči štetu svih mrava koji se nalaze u istom tunelu kao i ona. Takođe ako se desi da se pčela nađe u polju gde je kraljica, to je kraj igre, pčele pobeđuju. Ako se u igri postavi više mrava koji su ove vrste, ovai kasnije postavljeni će biti uništeni nakon prvog bacanja lišća.   

* **SlowThrower**     
                  *troši hrane:* 4  
                  *sposobnost:* ThrowerAnt koji pogotkom usporava kretanje pčela.  
 
* **StunThrower**     
                  *troši hrane:*  6  
                  *sposobnost:* ThrowerAnt koji pogotkom omamljuje pčele.  
                    

### Planirani jezik: 
  Za pisanje igre koršćen je programski jezik Python3.   
  Projekat predstavlja kombinaciju funkcionalne i objektno orijentisane programske paradigme.   

### Pokretanje

Igra se može pokrenuti pomocu python interpretera na dva načina: u tekstualnom ili uz korišćenje grafičkog interfejsa.  
Komande za pokretanje tekstualne verzije :  

python3 ants.py (Linux)  
py ants.py (Windows)  

Komande za pokretanje grafičke verzije :

python3 ants_gui.py (Linux)  
py ants_gui.py (Windows)

Igra ima nekoliko dodatnih opcija koje se mogu koristiti. Pregled opcija se može dobiti opcijom --help pri pokretanju.

> python3 [ants.py|ants_gui.py] [OPTIONS]
    Run the Ants vs. SomeBees project.

    -h, --help      Prints this help message
    -t, --ten       Start with ten food
    -f, --full      Loads a full layout and assault plan
    -w, --water     Loads a full layout with water
    -i, --insane    Loads a difficult assault plan


### Operativni sistem:  
Igra se moze pokrenuti i na Linux i na Windows operativnom sistemu.
Dostupan je izvršni fajl (.exe) za Windows. Za pokretanje osnovnog moda igrice dovoljan je dupli klik na izvršni fajl, a ukoliko želite da isprobate sve dodatne opcije izvršni fajl treba pokrenuti iz command prompt uz gore pomenute opcije (-t, -f...).  


### Autori:

Anka Stanković ankastankovic98@gmail.com    
Lana Šoškić soskiclana16@gmail.com      
Filip Miljojković miljojkovicfilip@gmail.com  
