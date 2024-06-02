# Grile Test + Examen `PCom`
> grilelele au un singur raspuns corect


## Cand se fragmenteaza pachetele IPv6?
* `La sursa, cand sunt trimise intial`

În **IPv6**, fragmentarea pachetelor are loc la **sursă** înainte de a fi trimise inițial.
Sursa este responsabilă să descopere MTU-ul potrivit
și să fragmenteze pachetele corespunzător.


## Cand se fragmenteaza pachetele `IPv4`?
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