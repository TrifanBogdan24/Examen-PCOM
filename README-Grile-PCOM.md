# Grile Test + Examen `PCom`
> grilelele au un singur raspuns corect


## Cand se `fragmenteaza` pachetele `IPv6`?
* `La sursa, cand sunt trimise intial`

În **IPv6**, fragmentarea pachetelor are loc la **sursă** înainte de a fi trimise inițial.
Sursa este responsabilă să descopere MTU-ul potrivit
și să fragmenteze pachetele corespunzător.


## Cand se `fragmenteaza` pachetele `IPv4`?
* `Cand se trece intr-o retea cu MTU mai mic decat dimensiunea pachetului`

> `MTU` = Maximum Transmission Unit


Fragmentarea pachetelor `IPv4` are loc aunci cand un pachet trebuie sa treaca
printr-o retea cu un `MTU` (Maximum Transmission Unit) mai mic decat dimensiunea pachetului.


> Fragmentarea pachetelor `IPv4` nu are loc în mod normal la sursă.


## Pe ce se bazeaza protocolul `RIP`?
* `Distance vector (vectorul distantelor)`

Protocolul `RIP` se bazeaza pe algoritmul distance vector,
care calculeaza ruta optima bazata pe distanta dintre noduri.



## UDP...
* `este best effort`

Protoculul `UDP` este 'best effort', ceea ce inseamna ca nu ofera garantii
privind livrarea corecta si in ordine a pachetelor, ci doar face eforturi pt a le transmite.



## Cine administreaza domeniile de nivel inalt?
* `ICANN`

`ICANN` (Internet Corporation for Assigned Names and Numbers) este organizatia responsabila de adminstrarea domeniilor de nivel inalt.



## TCP este:
* `Asigura transmiterea corecta sin in ordine a pachetelor`

`TCP` (Transmission Control Protocol) asigură transmiterea corectă și în ordine a pachetelor prin utilizarea confirmărilor și a mecanismelor de control al fluxului și congestiei.




## Cum este trimisa cererea `ARP`?
* `Broadcast in retea`

> `ARP` = Address Resolution Protocol

Cererea `ARP` este trimisa ca un mesaj broadcast in retea pt a determina
adresa `MAC` corespunzatoare unei adrese `IP`.


## Cum poate un socket al unui server `TCP` sa permita primirea de cereri pe conexiune?
* `functia listen`


Funcția `listen` este folosită pentru a permite unui socket să primească cereri de conexiune,
transformându-l într-un **socket pasiv** care poate fi folosit pentru a **accepta conexiuni** noi.



## La `nivelul transport` identificarea punctelor de acces se face prin:
* `adresa IP si port`


## O inregistrare de resursa din baza de date `DNS` se numeste:
* `Resourse Record`

O înregistrare de resursă (`Resource Record`) din baza de date `DNS` conține 
informații despre un nume de domeniu și tipul său, cum ar fi `adresa IP`,
serverele de mail, serverele de nume etc.



## Ce rol are  o cerere inversa `DNS`?
* `cauta un nume de domeniu asociat cu o anumita adresa IP`



## Dupa trimiterea unui pachet `FIN` datele primite sunt acceptate in continuare.
* `False`


După trimiterea unui pachet `FIN`, protocolul `TCP` nu mai acceptă date noi de la partenerul de comunicație.

Conexiunea este în curs de închidere și nu vor fi acceptate date adiționale.



## Ce se intampla la protocolul `Ethernet` daca 2 host-uri incearca sa trimit in acelasi timp?
* `Are loc o coloziune si host-urile vor incerca sa retrimita dupa un timp`


Când două host-uri în rețeaua `Ethernet` încearcă să transmită în același timp, are loc o coliziune.

Ambele host-uri vor detecta coliziunea
și vor încerca să retrimită după un **interval de timp aleatoriu**.



## Daca se ajunge la valoarea maxima pentru numarul de secventa, transmitatorul va face urmatorul lucru:
* `Va trimite urmatoarele segmente, repornind de la 0 numerele de secventa`


Dacă se ajunge la valoarea maximă pentru numărul de secvență,
transmitătorul nu așteaptă până când se poate asigura
că nu mai există în tranzit pachete cu același număr de secvență.

În schimb, va începe să trimită următoarele segmente,
**repornind de la 0** numerele de secvență.

Aceasta asigură că **numerele de secvență nu se epuizează**
și că **toate segmentele pot fi identificate în mod unic**.





## Care `flag` se foloseste pentru a initia o conexiune `TCP`?
* `SYN`

Flag-ul `SYN` este utilizat pentru a iniția o conexiune `TCP`
prin intermediul unui proces numit `three-way handshake`.


`SYN` = Synchronize sequence numbers
  1. initierea unei conexiuni TCP
  2. setarea acestui flag inseamna ca expeditorul doreste sa stabileasca o conexiuni si sincronizeaza numerele de secventa initiale



## Daca avem nevoie de un protocol cu latenta mica si nu ne intereseaza daca se paird sau sunt corpute unele pachete, este indicat sa folosim:
* `UDP`

Protocolul `UDP` (User Datagram Protocol) este mai potrivit pentru situații în care 
latenta scăzută este importantă și pierderea sau coruperea pachetelor nu reprezintă o problemă majoră.



## Care nivel al stivei `OSI` se ocupa cu `propagarea pachetelor prin noduri imtermediare`, de la sursa pana la destinatie?
* `Retea`

Nivelul Retea se ocupă cu propagarea pachetelor prin noduri intermediare,
de la sursa pana la destinatie.



## Prin folosirea unui `checksum` este posibila:
* Detectia erorilor de transmisie

`Checksum`-ul este folosit pentru a detecta erorile de transmisie prin calcularea
și compararea sumelor de verificare ale datelor trimise și primite.


> IMPORTANT
>
> `checksum`-ul doar detecteaza erori, nu le si corecteaza
> la fel si `CRC`-ul, un algoritm mai complex bazat pe impartiri de polinoame, doar le detecteaza, nu le si corecteaza




> Pentru detectia si corectia erorilor: `Distanta Hamming`
> submultime `W`
> `Sn` = multimea cuvintelor cu sens din `W`
> `Fn` = multimea cuvintelor fara sens din `W` (erorile)
>
> pt **detectia** a cel mult **k** erori: `d(u, v) >= k + 1`,    oricare u, v din `Sn`
> pt **corectia** a cel mult **k** erori: `d(u, v) >= 2 * k + 1`, oricare u, v din `Sn`
>
> `d(u, v)` = numarul de simboluri diferite intre cele doua




## Cand apare o `coliziune` la deschiderea unei conexiuni `TCP`?
* `Cand 2 host-uri incearca sa deschida o conexiune unul cu celalalt in acelasi timp`


Coliziunile apar atunci când două host-uri încearcă
să deschidă simultan o conexiune unul cu celălalt,
iar aceasta este rezolvată prin algoritmul `TCP` de sincronizare (`SYN`) simultană.




## Care din metodele de retransmisie pentru `fereastra glisantă` asigură faptul că se trimite un `minim de cadre duplicate`?
* `Selective repeat`


`Selective repeat` este o metodă de retransmisie pentru `fereastra glisantă` care asigură faptul că se trimite un `minim de cadre duplicate`. Acest lucru este realizat prin faptul că receptorul reține pachetele primite corect, iar expeditorul retransmite doar pachetele care nu au fost confirmate.



## Dacă la nivelul legăturii de date se realizează transmisia transparentă prin caractere de control, ce se trimite dacă în câmpul de date apare caracterul `DLE`?
* `DLE DLE`


În transmisia transparentă prin caractere de control, anumite caractere (cum ar fi caracterul DLE - Data Link Escape) sunt considerate speciale și pot fi confundate cu caractere de control. Pentru a evita acest lucru, se folosește o tehnică numită 'byte stuffing', prin care caracterul special este înlocuit cu o secvență de caractere care nu poate fi confundată cu caractere de control. În cazul caracterului DLE, se trimite secvența DLE DLE în locul acestuia.


##  Intre metodele de retransmisie `Go back N` si `Selective repeat` care are nevoie sa pastreze intr-un buffer cadrele primite corect la receptor, pana se primesc si cadrele retransmise.
* `Selective repat`


## Protocolul `IP` garanteaza primirea corecta a pachetelor la destinatie?
* `NU`

Protocolul `IP` (Internet Protocol) nu garanteaza primirea corecta a pachetelor la destinatie.
Acesta este un `protocol de livrare nesigur`, ceea ce inseamna ca nu exista garantii ca un pachet va ajunge la destinatie, sau ca va ajunge in ordinea corecta. In schimb, IP se bazeaza pe alte protocoale, cum ar fi `TCP` sau `UDP`, pentru a oferi servicii de transport sigure, cu control de flux si erori de transmisie.


## Un protocol `Stop and Wait` are nevoie neaparat de un canal de transmisie `Full Duplex`?
* `Nu. Este suficient un canal Half Duplex`


##  La nivelul legatura de date, pentru un protocol cu `fereastra glisanta`, cand se `shifteaza fereastra` transmitatorului?
* `Cand a primit ACK pentru primul cadru din fereastra de transmisie`


Într-un protocol cu `fereastra glisantă`,
transmiterea datelor se face prin transmiterea unui număr fix de cadre (fereastra de transmisie) înainte de așteptarea confirmării primirii acestora de către receptor. După ce primul cadru din fereastra de transmisie este trimis, transmitătorul așteaptă să primească un ACK (acuzație de primire) pentru acest cadru înainte de a deplasa fereastra de transmisie către următoarele cadre. În acest fel, transmitătorul poate asigura că receptorul a primit primul cadru și poate accepta noile cadre din fereastra de transmisie pentru transmitere. `După primirea ACK-ului pentru primul cadru, fereastra de transmisie se deplasează cu un cadru și procesul se repetă` până când toate cadrele din fereastra de transmisie au fost trimise și confirmate de receptor.


## In ce fel de `algoritm de dirijare` poate aparea `problema numararii la infinit`?
* Distance vector


`Problema numărării la infinit` poate apărea în algoritmul de dirijare `Distance Vector`. În această situație, două sau mai multe rutere se trimit reciproc în circulăție informații despre costul rutei, fără a ajunge la o soluție de dirijare.


## Daca la nivelul legatura de date se realizeaza `transmisia transparenta` prin caractere de control, care este caracterul folosit pentru `escapare`?
* `DLE`

`DLE` este caracterul folosit pentru escapare la nivelul legăturii de date în cazul transmisiei transparente prin caractere de control.



## La `nivelul retea`, cum se poate asigura faptul că pachetele ajung la destinație în aceeași ordine în care au fost trimise?
* `Circuite virtuale`

`Circuitele virtuale` asigură că pachetele ajung la destinație în aceeași ordine în care au fost trimise, deoarece pachetele sunt transmise pe același traseu fix, într-o anumită ordine, și sunt numerotate în consecință.


## Cum este marcat ultimul fragment dintr-un pachet?
* `Flag-ul MF are valoare 0`

Ultimul fragment dintr-un pachet este marcat prin faptul că flag-ul MF (More Fragments) are valoarea 0, indicând că nu mai sunt fragmente ulterioare.



## Ce se foloseste pentru a marca un pachet `IPv4` care `nu se poate fragmenta`?
* `flag-ul DF`


Pentru a marca un pachet IPv4 care nu se poate fragmenta se foloseste flag-ul DF (Don't Fragment). Acesta este setat in header-ul pachetului si indica faptul ca pachetul nu poate fi fragmentat pe parcursul tranzitarii retelei. In cazul in care o retea intermediara nu poate trimite pachetul fara sa-l fragmenteze, acesta va fi eliminat si va fi trimis un mesaj ICMP (Internet Control Message Protocol) de tipul 'Destination Unreachable - Fragmentation Needed and Don't Fragment Bit Set'.




## Prin folosirea unui `checksum` este posibila:
* `dectectia erorilor de transmisie`

> doar detectia, nu si corectarea



Checksum este o metodă utilizată pentru detectarea erorilor de transmisie în cadrul unui set de date. Se calculează o sumă de control (checksum) pentru datele transmise și se compară cu o sumă de control primită de la receptor. Dacă cele două sunt diferite, se poate presupune că au apărut erori de transmisie în datele transmise. Nu este posibilă detectarea și corectarea erorilor de transmisie utilizând doar checksum. Pentru a corecta erorile de transmisie, este necesară utilizarea altor metode, cum ar fi codurile de corecție a erorilor. De asemenea, checksum nu fixează lungimea maximă a unui cadru.


## Care din metodele de retransmisie pentru `fereastra glisanta` asigura faptul ca `receiver-ul primeste cadrele corecte in ordine`?
* `Go Back N` && `Selective Repeat`

Metoda de retransmisie Go Back n asigura faptul ca receiver-ul primeste cadrele corecte in ordine. Aceasta metoda presupune ca receptorul confirma primirea pachetelor printr-un mesaj ACK (Acknowledgement), iar daca un pachet este pierdut sau corupt, toate pachetele ulterioare sunt ignorate. In schimb, metoda Selective Repeat permite retransmiterea unor pachete individuale care s-au pierdut sau au fost corupte, fara a afecta celelalte pachete, insa aceasta metoda nu garanteaza faptul ca pachetele vor fi receptionate in ordine.


## Ce fel de adrese se folosesc pentru protocolul `Ethernet`?
* `adresele MAC`


## Care nivel al stivei de protocoale `ISO OSI` se ocupa de `corectia erorilor` si `controlul fluxului` pe un canal de comunicatie?
* `Nivelul legatura de date`

Nivelul legătură de date (`Layer 2`) este responsabil pentru gestionarea transferului fiabil de date între două noduri adiacente pe o rețea de comunicații. Acest nivel se ocupă de corectarea erorilor și de controlul fluxului pe un canal de comunicare.



## Catre care `next_hop` se trimite un pachet daca sunt mai multe potriviri in tabela de rutare?
* `longest prefix match`


Când există mai multe potriviri în tabela de rutare pentru adresa de destinație a unui pachet, se va folosi potrivirea cu cel mai lung prefix, cunoscută și sub numele de longest prefix match.



## Cand se `reasambleaza` fragmentele unui pachet `IP`?
* `la destinatia finala`



## La nivelul legatura de date, daca vrem sa trimitem un `payload de 16 biti`, de cati `biti de control` avem nevoie pentru metoda `Hamming`?
* `5`

Pentru a utiliza metoda Hamming pentru a trimite un payload de 16 biți, avem nevoie de 5 biți de control. Aceasta se datorează faptului că metoda Hamming utilizează o matrice de control cu 5 linii și 16 coloane pentru a verifica și a corecta erorile de transmisie. Deci, răspunsul corect este 5.


## Cum influenteaza fragmentarea pachetelor daca este setat flagul `DF` din header-ul `IPv4`?
* `Pachetul nu se va fragmenta niciodata`


## Care nivel al stivei de protocoale `ISO OSI` se ocupa de `determinarea rutei` de la sursa la destinatie prin `noduri intermediare`?
* `Nivelul retea`


## Ce reprezintă câmpul `offset` dintr-un fragment IP`?
* `pozitia fragmentului in pachet ca grup de 8 bytes`

Câmpul offset dintr-un fragment IP indică poziția fragmentului în pachetul original, exprimată ca un număr de grupuri de 8 octeți (64 de biți).


##  In cadrul `CIDR`, ce semnificatie are notatia de forma `141.85.99.142/24` ?
* `Adresa retelei are 24 de biti si adresa host-ului are 8 biti`

În notarea CIDR, numărul de biti din adresa de rețea este specificat prin `/24`, ceea ce înseamnă că primii 24 de biți ale adresei IP reprezintă adresa de rețea, iar ultimii 8 biți reprezintă adresa host-ului.



##  Ce se intampla in cadrul unui protocol cu `fereastra glisanta` cand sender-ul primeste un `ACK` pentru un cadru din fereastra sa?
* `Shifteaza fereastra si trimite urmatorl cadru doar dca esta ACK pentru primul cadru din fereastra`

Într-un protocol cu fereastra glisantă, sender-ul mută fereastra la dreapta și trimite următorul cadru numai dacă primește un ACK pentru primul cadru din fereastra.


## Pentru ce `nu` poate fi folosit protocolul `ICMP`?
* `ARP`


Protocolul ICMP (Internet Control Message Protocol) poate fi folosit pentru a efectua diverse operatiuni de diagnostice in retele, cum ar fi ping, traceroute sau aflare path MTU. Cu toate acestea, ICMP nu poate fi folosit pentru a rezolva adrese MAC in adrese IP, ceea ce inseamna ca nu poate fi folosit pentru ARP (Address Resolution Protocol). Pentru a rezolva adresele MAC, este nevoie de un protocol precum ARP sau NDP (Neighbor Discovery Protocol) pentru IPv6.


> `ICMP` poate fi folosit pt: `ping`, `tracerout`, `aflare path MTU`


## Cum se aplica `masca de retea` pentru verificarea intr-o tabela de rutare?
* `AND`


Pentru a verifica dacă o adresă IP se află într-o anumită rețea, se aplică masca de rețea la adresa IP utilizând operația AND. Rezultatul va fi adresa de rețea corespunzătoare adresei IP date, care va fi căutată în tabela de rutare.



## Ce tip de canal poate fi folosit pentru un protocol `Stop and wait`?
* `half duplex sau full duplex`

Un canal half duplex sau full duplex poate fi folosit pentru un protocol Stop and Wait. Protocolul Stop and Wait necesită ca receptorul să confirme primirea fiecărui pachet trimis de emitător, prin urmare, emițătorul și receptorul nu trebuie să trimită simultan.


##  În cadrul unui protocol cu `fereastra glisantă`, ce rol are cadrul de tip `RR`?
* `Receive Ready`

Cadrul de tip RR (Receive Ready) este folosit într-un protocol cu fereastra glisantă pentru a confirma primirea cu succes a unui anumit număr de pachete. Acesta poate fi trimis de către receptor către emitător pentru a indica că poate primi mai multe pachete.



##  Ce se intampla in cazul unui protocol de tip `Stop and wait` daca se pierde un mesaj de la sender la receiver?
* `Sender-ul va retrimite ultimul mesaj dupa timeout`

În cazul unui protocol de tip Stop and Wait, dacă un mesaj este pierdut, sender-ul va retrimite ultimul mesaj după ce a expirat timeout-ul.


## Ce `nu` este posibil printr-un canal `half-duplex`?
* `transfer de date in ambele sensuri simultan`

Un canal half-duplex permite transferul de date în ambele sensuri, dar nu în același timp, deoarece transmisia este alternativă. Din acest motiv, transferul de date în ambele sensuri simultan nu este posibil prin canalul half-duplex.


## Cum este împărțită o adresă `IP` în adresă de `rețea` și adresă de `host`?
* `prefixul este adresa de reteam, sufixul este adresa pentru host`


Prefixul adresei IP identifică adresa de rețea, în timp ce sufixul identifică adresa de gazdă. Adresa de rețea identifică o rețea, în timp ce adresa de gazdă identifică un dispozitiv specific din acea rețea.



## Ce fel de zone pot exista in cadrul unui `Autonomous System` (`AS`)?
* `o zona backbone si mai multe zone stub`


În cadrul unui Autonomous System (AS) poate exista o zonă backbone și mai multe zone stub. Zona backbone este responsabilă pentru dirijarea traficului între zonele stub, iar zonele stub sunt conectate la zona backbone și nu dirijează traficul prin ele.



## Cum se realizeaza `incapsularea` pentru trimiterea unui pachet `IPv4`?
* `pachetul IPv4 este in payload-ul cadrului Ethernet`

Pentru a transmite un pachet IPv4 pe o rețea Ethernet, acesta trebuie încapsulat într-un cadrul Ethernet. În acest caz, pachetul IPv4 va fi pus în payload-ul cadrului Ethernet și se va adăuga un antet Ethernet care va conține adresele MAC ale dispozitivelor sursă și destinație.


## Pe ce se bazeaza protocolul `RIP`?
* `distance vector`


## Cum se foloseste protocolul `ICMP` pentru a afla `Path MTU`?
* `se trimit pachete ICMP din ce in ce mai mici pana cand nu se mai primeste o eroare`

Pentru a afla Path MTU, se trimit pachete ICMP cu flag-ul 'Don't Fragment' setat si cu o dimensiune tot mai mare. In cazul in care unul dintre pachete nu poate fi transmis din cauza dimensiunii prea mari, reteaua va returna un mesaj ICMP 'Fragmentation Needed and Don't Fragment was Set'. Acest mesaj va indica dimensiunea maxima a pachetelor care pot fi transmise pe acea ruta.
