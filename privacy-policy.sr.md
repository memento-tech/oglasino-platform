# Politika privatnosti — Oglasino

**Poslednje ažuriranje:** 09.06.2026.

---

## 1. Ko smo mi

Oglasino je onlajn platforma za male oglase za kupovinu, prodaju i razmenu novih i polovnih proizvoda. Platforma posluje preko dva državna portala — Srbija (rs) i Crna Gora (me) — i dostupna je i posetiocima iz drugih zemalja, uključujući Evropsku uniju. Oglasino ne obrađuje niti posreduje u plaćanjima između korisnika; sve transakcije se dogovaraju i sprovode direktno između kupaca i prodavaca.

Oglasino možete koristiti putem našeg veb-sajta i putem naših izvornih mobilnih aplikacija za iOS i Android. Ova Politika privatnosti odnosi se na sve njih. Mobilne aplikacije nude iste funkcije kao veb-sajt i obrađuju vaše podatke na isti način, osim tamo gde uređaj pravi razliku — dozvole aplikacije (kao što je kamera) i čuvanje podataka na uređaju — što izričito opisujemo u odeljcima 2.16 i 7.

Rukovalac podacima o ličnosti za Oglasino je:

**Igor Stojanović**
Bulevar 12. februar 32, 18000 Niš, Srbija
privacy@oglasino.com

Oglasino trenutno posluje kao preduzetnik pod gore navedenim imenom. Vlasnik namerava da u budućnosti osnuje privredno društvo kada platforma pokaže održiv rast. Kada se to dogodi, ova Politika privatnosti biće ažurirana kako bi odražavala novo pravno lice, a vi ćete o tome biti obavešteni putem platforme.

---

## 2. Podaci koje prikupljamo i zašto

Ovaj odeljak opisuje svaku kategoriju podataka o ličnosti koje Oglasino prikuplja, zašto ih prikupljamo i pravni osnov na koji se oslanjamo u skladu sa Opštom uredbom o zaštiti podataka (GDPR) i srpskim Zakonom o zaštiti podataka o ličnosti.

### 2.1 Podaci o nalogu

Kada kreirate nalog na Oglasinu, prikupljamo i čuvamo:

- **Imejl adresa** — neophodna za kreiranje naloga, prijavljivanje i obaveštenja u vezi sa nalogom.
- **Identifikator za autentifikaciju (Firebase UID)** — interni identifikator koji izdaje naš provajder autentifikacije, Firebase Authentication. Ovaj identifikator povezuje vaš nalog u našoj bazi podataka sa vašim zapisom za autentifikaciju.
- **Prikazano ime** — ime prikazano na vašem javnom profilu i oglasima. Birate ga prilikom registracije imejl adresom; za naloge kreirane putem Google prijavljivanja preuzima se iz vašeg Google profila. (Ako prikazano ime ikada nije dostupno prilikom registracije, kao rezerva se može upotrebiti deo vaše imejl adrese ispred znaka „@”.) Prikazano ime možete promeniti u svako doba u podešavanjima profila.
- **Provajder prijavljivanja** — da li ste se registrovali imejlom ili Google-om.
- **Status verifikacije imejla** — da li je vaš imejl verifikovan.
- **Lozinka** — vaša lozinka se nikada ne šalje Oglasinu niti je on čuva. Njome rukuje isključivo Firebase Authentication, naš provajder autentifikacije. Oglasino nema pristup njoj.
- **Vremenske oznake kreiranja naloga i poslednjeg ažuriranja.**

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b) GDPR-a) — ne možemo da pružimo uslugu zasnovanu na nalogu bez ovih podataka.

### 2.2 Podaci o profilu

Pored podataka o nalogu, vaš profil može sadržati:

- **Broj telefona** — opciono. Možete ga uneti u podešavanjima profila.
- **Profilna slika (avatar)** — ako se prijavite putem Google-a i vaš Google nalog ima profilnu sliku, pravimo kopiju te slike i čuvamo je na našoj infrastrukturi (Cloudflare R2). Ako nemate Google sliku, platforma prikazuje automatski generisan avatar na osnovu inicijala (prvo slovo vašeg prikazanog imena na obojenoj pozadini) — ovaj generisani avatar nije sačuvana slika i ne sadrži nikakve zasebne podatke o ličnosti. Profilnu sliku možete otpremiti, zameniti ili ukloniti u svako doba u podešavanjima.
- **Lični opis (biografija)** — opcioni slobodni tekst koji možete dodati o sebi. Ako svoju biografiju napišete na jednom jeziku, automatski je prevodimo na ostale podržane jezike platforme kako bi drugi korisnici mogli da je čitaju na svom jeziku (vidi odeljak 2.8 o automatskom prevođenju).
- **Ocena naloga** — numerička ocena izvedena iz recenzija koje ste dobili od drugih korisnika.
- **Status verifikacije** — interna oznaka koja pokazuje da li je platforma verifikovala vaš nalog.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) — podaci o profilu deo su usluge zasnovane na nalogu na koju ste se prijavili.

### 2.3 Podaci o lokaciji

Da biste kreirali ili pregledali oglase, platforma mora da zna koji državni portal koristite i vaše lokalno područje. Prikupljamo:

- **Državni portal (Srbija ili Crna Gora)** — izabran kada kreirate svoj prvi oglas.
- **Region** — izabran kada kreirate svoj prvi oglas.
- **Grad** — izabran kada kreirate svoj prvi oglas.

Vaša lokacija se postavlja na nivou vašeg naloga, a ne po pojedinačnom oglasu. Svi vaši oglasi povezani su sa istim regionom i gradom kao i vaš nalog; platforma ne podržava oglašavanje robe koja se nalazi u drugom regionu ili državi od prodavca. Ne koristimo GPS vašeg uređaja niti bilo koju drugu automatsku geolokaciju — uključujući i u našim mobilnim aplikacijama; vaše područje proizilazi isključivo iz portala, regiona i grada koje izaberete.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) — Oglasino je geografski ograničena platforma za lokalne oglase; funkcija oglasa ne može da radi bez vaše lokacije.

### 2.4 Podaci o oglasu

Kada kreirate oglas, prikupljamo i čuvamo:

- **Naslov i opis** — koje pišete vi, na bilo kom od podržanih jezika platforme. Automatski ih prevodimo na ostale podržane jezike platforme (vidi odeljak 2.8).
- **Cena i valuta** — srpski dinar (RSD) i evro (EUR) podržani su na srpskom portalu; evro (EUR) je podržan na crnogorskom portalu.
- **Oznaka „Besplatno”** — da li je oglas za artikal koji poklanjate bez naknade (koristi se u Džabe zoni platforme).
- **Kategorija i potkategorija** — izabrane iz fiksne taksonomije.
- **Atributi specifični za kategoriju** — strukturirana polja koja se razlikuju po kategoriji (na primer, veličina, boja, godina za odgovarajuće kategorije).
- **Fotografije** — slike koje otpremate, sačuvane na Cloudflare R2 (vidi odeljak 4 o trećim stranama).
- **Status oglasa** — da li je oglas aktivan, zabranjen itd.
- **Brojači** — anoniman broj pregleda i broj dodavanja u omiljeno za svaki oglas. Ovi brojači prate samo ukupne vrednosti; ne beležimo koji su pojedinačni korisnici pregledali vaš oglas.
- **Broj izmena** — koliko ste puta izmenili oglas.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) — oglasi su osnovna funkcionalnost platforme.

### 2.5 Poruke i prilozi u ćaskanju

Platforma uključuje funkciju privatnog razmenjivanja poruka između korisnika. Čuvamo:

- **Poruke** — pošiljalac, primalac, sadržaj poruke, vremenska oznaka, status pročitanosti. Poruke se čuvaju na Google Firestore (vidi odeljak 4).
- **Prilozi sa slikama** — porukama možete priložiti slike. One se čuvaju na Cloudflare R2.
- **Opciona referenca na proizvod** — kada započnete razgovor sa drugim korisnikom klikom na „Pošalji poruku” na stranici oglasa, prva poruka koju pošaljete u tom razgovoru sadrži referencu na taj oglas.
- **Obaveštenja** — obaveštavamo vas o relevantnoj aktivnosti, a način na koji to radimo zavisi od događaja:
  - Za događaje kao što su dodavanje vašeg oglasa u omiljeno, praćenje vašeg naloga ili radnja administratora na vašem nalogu, čuvamo obaveštenje u aplikaciji na Firestore-u **i** šaljemo push obaveštenje na vaš uređaj (koristeći push token vašeg uređaja — vidi odeljak 2.15). Ona sadrže kratku naznaku događaja (na primer, tip događaja i prikazano ime drugog korisnika).
  - Za nove poruke u ćaskanju šaljemo **samo push obaveštenje** — ne čuvamo zaseban zapis obaveštenja u aplikaciji. Kako biste poruku mogli da pročitate sa ekrana obaveštenja vašeg uređaja (što je standard za razmenu poruka), push obaveštenje o poruci u ćaskanju prikazuje prikazano ime pošiljaoca i tekst poruke.

**Pristup porukama.** Administratori platforme mogu pristupiti sadržaju poruka radi istrage prijava o nedoličnom ponašanju ili kršenju naših Uslova korišćenja. Izvan poslova moderacije, vaše poruke su vidljive samo vama i drugom učesniku u razgovoru. Ova mogućnost moderacije neophodna je radi bezbednosti naših korisnika i predstavlja osnov na kome dozvoljavamo prijavljivanje poruka.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) za čuvanje i isporuku poruka; legitimni interes (član 6. stav 1. tačka f)) za pristup administratora porukama radi moderacije i bezbednosti.

### 2.6 Recenzije

Platforma omogućava kupcima i prodavcima da nakon interakcije ostave recenzije jedni o drugima. Za svaku recenziju čuvamo:

- **Autor recenzije** — korisnik koji je napisao recenziju.
- **Korisnik na koga se odnosi** — korisnik o kome je recenzija.
- **Referenca na proizvod** — ako se recenzija odnosi na određeni oglas.
- **Ocena** — broj od 1 do 5.
- **Komentar** — slobodni tekst. Komentare recenzija automatski prevodimo na ostale podržane jezike platforme (vidi odeljak 2.8).
- **Slike** — opcione fotografije priložene uz recenziju, sačuvane na Cloudflare R2.
- **Status verifikacije** — da li je autor recenzije imao legitimnu interakciju na platformi sa korisnikom na koga se recenzija odnosi, povezanu sa proizvodom.
- **Status odobrenja** — da li je administrator platforme odobrio recenziju za javno prikazivanje. Sve recenzije zahtevaju odobrenje administratora pre nego što postanu vidljive drugim korisnicima.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) — recenzije su deo sistema poverenja platforme.

### 2.7 Omiljeno

Kada sačuvate oglas u omiljeno, čuvamo zapis koji povezuje vaš nalog sa tim oglasom. To je vidljivo samo vama.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)).

### 2.8 Automatsko prevođenje vašeg sadržaja

Platforma podržava četiri jezika: srpski, engleski, ruski i crnogorski. Kada napišete naslov oglasa, opis oglasa, biografiju profila ili komentar recenzije na jednom jeziku, vaš tekst šaljemo kompaniji **OpenAI** (eksterna usluga sa sedištem u Sjedinjenim Američkim Državama) radi automatskog prevođenja na ostale podržane jezike platforme. Prevedene verzije čuvaju se uz vaš originalni tekst kako bi korisnici na platformi mogli da vide vaš sadržaj na željenom jeziku.

Uslovi OpenAI API-ja obavezuju da se podaci poslati putem njihovog API-ja ne koriste za obučavanje njihovih modela. Sam Oglasino ne obučava nijedan AI model na vašem sadržaju (vidi odeljak 6 za naše šire obaveze u vezi sa korišćenjem podataka).

Ova obrada podrazumeva prenos vašeg teksta van Evropskog ekonomskog prostora u Sjedinjene Američke Države. Vidi odeljak 5 o međunarodnim prenosima.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) — višejezični sadržaj je osnovna funkcija platforme.

### 2.9 Prijave

Svaki korisnik može prijaviti drugog korisnika, oglas ili recenziju zbog kršenja naših Uslova korišćenja. Kada se podnese prijava, čuvamo:

- **Ko je podneo prijavu** — nalog prijavioca.
- **Ko ili šta se prijavljuje** — ciljni korisnik, oglas ili recenzija.
- **Kategorija prijave** — jedna od: prevara, loša usluga, kršenje pravila, nasilje ili uznemiravanje, neprimeren sadržaj, obmanjujući ili lažan oglas, kršenje pravila portala, tehnički problem, drugo.
- **Opis** — slobodni tekst od prijavioca.
- **Status rešavanja** — da li je administrator pregledao prijavu i eventualne napomene o rešenju.

Trenutno prijave ručno pregleda administrator. U budućnosti planiramo da uvedemo automatsku obradu određenih kategorija prijava; ova Politika privatnosti biće ažurirana kada se ta promena sprovede.

**Pravni osnov:** legitimni interes (član 6. stav 1. tačka f)) — bezbednost platforme, sprečavanje zloupotreba i sprovođenje pravila.

### 2.10 Podaci o moderaciji i bezbednosti platforme

Radi održavanja bezbednosti platforme, čuvamo sledeće podatke o svakom korisniku:

- **Status moderacije** vaših oglasa — da li je svaki od vaših oglasa odobren ili zabranjen.
- **Broj kazni** izrečenih protiv vašeg naloga.
- **Status onemogućenosti** — da li je administrator onemogućio vaš nalog.
- **Interni status verifikacije** — da li je vaš nalog interno verifikovan.

**Pravni osnov:** legitimni interes (član 6. stav 1. tačka f)) — bezbednost platforme i sprovođenje pravila.

### 2.11 Preferencije komunikacije

Vaš nalog čuva vaše preferencije komunikacije, koje možete promeniti u svako doba u podešavanjima:

- Da li dozvoljavate transakcione imejlove o vašem nalogu.
- Da li dozvoljavate promotivne ili marketinške imejlove.
- Da li dozvoljavate drugim korisnicima da pozovu vaš broj telefona.

Izbori u vezi sa kolačićima i analitikom ne čuvaju se kao podešavanja naloga: na veb-sajtu ih pravite putem banera za pristanak na kolačiće (sačuvanog u vašem pregledaču), a u mobilnoj aplikaciji putem podešavanja analitike u aplikaciji (sačuvanog na vašem uređaju). Vidi odeljak 7. Obaveštenjima upravljaju dozvole za obaveštenja vašeg uređaja ili pregledača, a ne podešavanje naloga (vidi odeljke 2.5 i 2.15): isključivanje obaveštenja u vašem operativnom sistemu ili pregledaču ih zaustavlja, a odjavljivanje odvaja vaš uređaj od push obaveštenja.

Imajte u vidu da, čak i ako isključite „transakcione imejlove”, i dalje vam možemo slati imejlove koji su neophodni za vaše korišćenje platforme (na primer, potvrdu da je vaš nalog zakazan za brisanje). Zaista opcioni i promotivni imejlovi uslovljeni su prekidačem za „promotivne imejlove”.

**Pravni osnov:** pristanak (član 6. stav 1. tačka a)) za svaku preferenciju. Pristanak možete opozvati u svako doba promenom prekidača u podešavanjima; opoziv ne utiče na zakonitost obrade pre opoziva.

### 2.12 Tehnički podaci

Da bismo održavali platformu funkcionalnom, bezbednom i otpornom na zloupotrebe, obrađujemo:

- **IP adresa** — privremeno se beleži u našem Redis kešu radi ograničavanja učestalosti zahteva i sprečavanja zloupotreba. Zapisi o IP adresama vezani su za vaš nalog kada ste prijavljeni. Ove zapise čuvamo približno 30 minuta.
- **Dnevnici aplikacije** — operativni dnevnici aktivnosti na platformi, koji se koriste za otklanjanje grešaka, bezbednosni nadzor i reagovanje na incidente.
- **Kolačići** — vidi odeljak 7.

**Pravni osnov:** legitimni interes (član 6. stav 1. tačka f)) — bezbednost, sprečavanje zloupotreba i pouzdanost platforme.

### 2.13 Zapisi o brisanju naloga

Kada izbrišete svoj nalog, nakon brisanja zadržavamo ograničen revizorski zapis. Vidi odeljak 8 (Koliko dugo čuvamo vaše podatke) za pune detalje.

### 2.14 Analitički podaci

Da bismo razumeli kako se Oglasino koristi i kako bismo ga unapredili, prikupljamo analitičke podatke pomoću Google Analytics 4 (GA4) i na veb-sajtu i u mobilnoj aplikaciji — ali **samo ako date pristanak**. Kada je omogućen, GA4 prikuplja pseudonimne informacije o korišćenju, kao što su pregledane stranice ili ekrani, korišćene pretrage i filteri, pregledani oglasi i slični događaji interakcije, zajedno sa pseudonimnim analitičkim identifikatorom (na vebu, identifikator analitičkog kolačića; u mobilnoj aplikaciji, Firebase identifikator instance aplikacije). Ako ste prijavljeni, povezujemo ove događaje sa korisničkim identifikatorom vašeg naloga kako bi se korišćenje moglo razumeti kroz vaše sesije. Naša analitika je isključivo prve strane: ne koristimo je za oglašavanje, ciljanje oglasa niti praćenje na više sajtova ili aplikacija, a Google-ovi signali za oglašavanje su onemogućeni. Način na koji dajete ili uskraćujete pristanak razlikuje se po platformi: na veb-sajtu, putem banera za kolačiće; u mobilnoj aplikaciji, putem izbora na nivou uređaja koji pravite kada prvi put otvorite aplikaciju i koji možete promeniti u svako doba u podešavanjima aplikacije (za oba vidi odeljak 7). Analitika je podrazumevano isključena; ne omogućavamo prikupljanje analitike osim ako to niste dozvolili.

**Pravni osnov:** pristanak (član 6. stav 1. tačka a)). Pristanak možete opozvati u svako doba putem banera za kolačiće ili stranice sa preferencijama kolačića; opoziv ne utiče na zakonitost obrade pre opoziva.

### 2.15 Tokeni za push obaveštenja

Ako koristite mobilnu aplikaciju Oglasino i dozvolite obaveštenja, vašem uređaju se izdaje **push token** — identifikator koji nam omogućava da šaljemo push obaveštenja tom konkretnom uređaju. Vaš push token čuvamo u našoj bazi podataka i povezujemo ga sa vašim nalogom kako bismo vam mogli isporučivati obaveštenja (na primer, upozorenja o novim porukama; vidi odeljak 2.5). Vaš push token se odvaja od vašeg naloga kada se odjavite, a zamenjuje se ili uklanja kako se vaš uređaj ili njegove dozvole menjaju. Push obaveštenja se isporučuju preko provajdera navedenih u odeljku 4.

**Pravni osnov:** izvršenje ugovora (član 6. stav 1. tačka b)) — isporuka obaveštenja deo je usluge razmene poruka i naloga na koju ste se prijavili. Push obaveštenja možete zaustaviti u svako doba isključivanjem u podešavanjima uređaja ili odjavljivanjem.

### 2.16 Korišćenje mobilne aplikacije — dozvole uređaja i podaci uređaja

Naše iOS i Android aplikacije traže vašu dozvolu za korišćenje određenih funkcija uređaja, i to samo kada su funkciji potrebne:

- **Kamera i galerija fotografija** — kada slikate ili izaberete fotografiju da je dodate oglasu, profilnoj slici, poruci ili recenziji. Aplikacija pristupa kameri ili galeriji fotografija samo u trenutku kada odlučite da dodate fotografiju; fotografije koje zatim izaberete obrađuju se kako je opisano u odeljcima 2.2, 2.4, 2.5 i 2.6.
- **Obaveštenja** — da bismo vam slali push obaveštenja. Ovo rezultira push tokenom za vaš uređaj (vidi odeljak 2.15).

Ove dozvole možete dati ili opozvati u svako doba u podešavanjima vašeg uređaja.

Da budemo jasni u vezi sa onim što mobilna aplikacija **ne** radi: ona **ne** pristupa lokaciji vašeg uređaja (GPS) — region i grad koji se koriste na platformi su vrednosti na nivou naloga koje sami birate (vidi odeljak 2.3), a ne lokacija vašeg uređaja; **ne** čita vaše kontakte; **ne** prikuplja identifikator za oglašavanje (kao što su Apple IDFA ili Android advertising ID); **ne** koristi Apple-ovu funkciju App Tracking Transparency; i **ne** prati vas kroz druge aplikacije ili veb-sajtove.

Aplikacija takođe čuva neke informacije na vašem uređaju; vidi odeljak 7.

---

## 3. Kako koristimo vaše podatke — sažetak

Da bi se odeljak 2 lakše pratio, evo sažetka svake svrhe za koju koristimo vaše podatke i pravnog osnova za svaku. Detaljna obaveštenja nalaze se u odeljku 2.

| Svrha                                                                      | Pravni osnov      |
| -------------------------------------------------------------------------- | ----------------- |
| Kreiranje i upravljanje vašim nalogom                                      | Ugovor            |
| Prikazivanje vašeg profila drugim korisnicima                              | Ugovor            |
| Objavljivanje vaših oglasa drugim korisnicima                              | Ugovor            |
| Isporuka poruka između korisnika                                           | Ugovor            |
| Prikazivanje recenzija o vama i od vas                                     | Ugovor            |
| Čuvanje vaših omiljenih oglasa                                             | Ugovor            |
| Automatsko prevođenje vašeg sadržaja na ostale podržane jezike             | Ugovor            |
| Slanje komunikacija na koje ste pristali                                   | Pristanak         |
| Postavljanje kolačića koji nisu neophodni u vašem pregledaču               | Pristanak         |
| Merenje i unapređenje veb-sajta pomoću analitike (samo ako date pristanak) | Pristanak         |
| Isporuka push obaveštenja na vaš uređaj                                    | Ugovor            |
| Sprečavanje prevara, zloupotreba i neželjene pošte                         | Legitimni interes |
| Moderacija sadržaja i sprovođenje pravila platforme                        | Legitimni interes |
| Održavanje bezbednosti i pouzdanosti platforme                             | Legitimni interes |
| Istraga prijava koje podnose korisnici                                     | Legitimni interes |
| Čuvanje heširanog revizorskog zapisa o brisanju naloga                     | Legitimni interes |

---

## 4. Treće strane koje obrađuju vaše podatke

Koristimo niz eksternih provajdera usluga za rad Oglasina. Svaki od njih obrađuje deo vaših podataka u naše ime. Nikada nikome ne prodajemo vaše podatke (vidi odeljak 6 o našim konkretnim obavezama).

| Provajder                                                                                         | Uloga                                                                                                      | Šta obrađuju                                                                                                                                                                                         | Lokacija                                          |
| ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| **Google Firebase Authentication**                                                                | Provajder autentifikacije                                                                                  | Vaš imejl, lozinka (drži je samo Firebase), tokeni za Google prijavljivanje                                                                                                                          | Region EU (Google Ireland Ltd kao strana u EEP-u) |
| **Google Firestore**                                                                              | Baza podataka u realnom vremenu za poruke i obaveštenja                                                    | Sadržaj poruka, obaveštenja, prikazana imena pošiljalaca                                                                                                                                             | Region EU (isti Firebase projekat)                |
| **Cloudflare R2**                                                                                 | Skladište objekata za slike                                                                                | Profilne slike, fotografije oglasa, prilozi u ćaskanju, fotografije recenzija                                                                                                                        | Istočna Evropa (EEUR)                             |
| **Cloudflare**                                                                                    | Mreža za isporuku sadržaja (CDN) i keširanje na ivici                                                      | Keširan statički sadržaj i slike                                                                                                                                                                     | Globalna ivična mreža                             |
| **OpenAI**                                                                                        | Automatsko prevođenje sadržaja koji pišu korisnici                                                         | Naslovi i opisi oglasa, biografije profila, komentari recenzija                                                                                                                                      | Sjedinjene Američke Države                        |
| **DigitalOcean**                                                                                  | Hosting bekend aplikacije                                                                                  | Svi podaci koje obrađuju naši bekend servisi                                                                                                                                                         | Frankfurt, Nemačka (region fra1)                  |
| **Vercel**                                                                                        | Hosting veb frontenda (uključujući renderovanje na serverskoj strani)                                      | Zahtevi stranica, kolačići sesije, tela zahteva                                                                                                                                                      | Frankfurt, Nemačka (region fra1)                  |
| **Google reCAPTCHA**                                                                              | Detekcija botova na formularima                                                                            | IP adresa, informacije o pregledaču, podaci o pokretima miša i vremenima, kolačići koje postavlja Google                                                                                             | Sjedinjene Američke Države                        |
| **Google Analytics 4 (Google LLC)**                                                               | Analitika korišćenja veb-sajta i mobilne aplikacije                                                        | Pseudonimni događaji korišćenja i analitički identifikatori (kolačić `_ga` na vebu; Firebase identifikator instance aplikacije u mobilnoj aplikaciji); prikuplja se samo ako pristanete na analitiku | Sjedinjene Američke Države                        |
| **Brevo**                                                                                         | Slanje imejlova o nalogu i platformi (npr. verifikacija imejla, resetovanje lozinke, obaveštenja o nalogu) | Vaša imejl adresa i sadržaj tih imejlova                                                                                                                                                             | Evropska unija                                    |
| **Expo Push Service, sa Apple Push Notification service (APNs) i Firebase Cloud Messaging (FCM)** | Isporuka push obaveštenja na vaš uređaj                                                                    | Push token vašeg uređaja i sadržaj obaveštenja (uključujući, za obaveštenja o porukama u ćaskanju, prikazano ime pošiljaoca i tekst poruke)                                                          | Sjedinjene Američke Države (Expo; Apple; Google)  |

---

## 5. Međunarodni prenosi

Većina naše obrade odvija se unutar Evropskog ekonomskog prostora (EEP), koji ima standarde zaštite podataka koje zahteva GDPR.

Nekoliko naših obrađivača ima sedište u Sjedinjenim Američkim Državama: **OpenAI** (za prevođenje sadržaja), **Google reCAPTCHA** (za detekciju botova), **Google Analytics** (za analitiku veb-sajta, samo ako pristanete) i provajderi koji isporučuju push obaveštenja na vaš uređaj (**Expo** i osnovne push usluge kompanija **Apple** i **Google**). Kada se vaši podaci pošalju ovim obrađivačima, oni napuštaju EEP.

Za ove prenose oslanjamo se na sledeće zaštitne mehanizme:

- **OpenAI** — podatke prenosimo na osnovu Standardnih ugovornih klauzula Evropske komisije i pridržavanja kompanije OpenAI okviru EU-US Data Privacy Framework (gde je primenljivo). Rukovalac (Oglasino) koristi OpenAI API usluge u skladu sa OpenAI Services Agreement. OpenAI Data Processing Addendum sastavni je deo tog ugovora i primenjuje se na korišćenje usluga.
- **Google reCAPTCHA** — oslanjamo se na pridržavanje kompanije Google okviru EU-US Data Privacy Framework i na Google-ove Standardne ugovorne klauzule.
- **Google Analytics** — za korisnike koji pristanu na analitiku, oslanjamo se na pridržavanje kompanije Google okviru EU-US Data Privacy Framework i na Google-ove Standardne ugovorne klauzule.
- **Isporuka push obaveštenja** — push obaveštenja se usmeravaju preko Expo-a i osnovnih push usluga kompanija Apple (APNs) i Google (FCM). Oslanjamo se na pridržavanje kompanija Apple i Google okviru EU-US Data Privacy Framework i na Standardne ugovorne klauzule.

Više informacija o ovim zaštitnim mehanizmima možete zatražiti tako što ćete nas kontaktirati na privacy@oglasino.com.

---

## 6. Šta nikada nećemo raditi sa vašim podacima

Pored obaveza koje prema vama imamo na osnovu GDPR-a, dajemo dve izričite obaveze u vezi sa vašim podacima:

**Ne prodajemo vaše podatke.** Nikada nismo i nikada nećemo. Ne prodajemo korisničke podatke oglašivačima, brokerima podataka niti bilo kojoj trećoj strani. Podatke delimo sa obrađivačima samo kako je opisano u odeljku 4, i to samo u meri u kojoj je neophodno za rad platforme.

**Ne obučavamo AI na vašim podacima.** Oglasino ne koristi vaš sadržaj — vaše oglase, vaše poruke, vaše recenzije, vaš profil — za obučavanje bilo kog modela veštačke inteligencije ili mašinskog učenja. Ova obaveza odnosi se konkretno na to šta mi radimo sa vašim podacima. Odvojeno od toga, naš provajder za prevođenje OpenAI u svojim API uslovima obavezuje se da se podaci poslati putem njihovog API-ja ne koriste za obučavanje njihovih modela; to je obaveza koju OpenAI daje o sopstvenom korišćenju podataka koje im šaljemo.

Ako ikada izmenimo bilo koju od ovih obaveza, jasno ćemo vam to saopštiti pre nego što promena stupi na snagu i daćemo vam mogućnost da izbrišete svoj nalog pre nego što započne bilo kakva nova obrada.

---

## 7. Kolačići i slične tehnologije

Veb-sajt Oglasino koristi kolačiće i slične mehanizme čuvanja u pregledaču (kao što su localStorage i IndexedDB); naše mobilne aplikacije umesto kolačića koriste slično čuvanje na uređaju. Ovaj odeljak pokriva oba — prvo veb-sajt, zatim mobilnu aplikaciju. Na veb-sajtu koristimo kolačiće i slično čuvanje u tri svrhe:

**Strogo neophodni** — potrebni za funkcionisanje veb-sajta. Tu spadaju vaša sesija za autentifikaciju (kojom upravlja Firebase Authentication, sačuvana u localStorage i IndexedDB), bezbednosni tokeni (na primer, zaštita od CSRF-a), samo stanje pristanka na kolačiće i mali broj sličnih tehničkih kolačića.

**Preferencije** — koriste se za pamćenje vaših izbora, kao što su željeni jezik, izabrani državni portal (Srbija ili Crna Gora) i slična podešavanja.

**Analitika** — koristi se za merenje kako se veb-sajt koristi kako bismo ga razumeli i unapredili. Koristimo Google Analytics 4 (GA4). Analitički kolačići (na primer, `_ga` i `_gid`) i prikupljanje analitike postavljaju se **samo ako pristanete** na kategoriju analitike; ako odbijete, ne postavljaju se nikakvi analitički kolačići i ne prikupljaju se nikakvi analitički podaci. Koristimo Google Consent Mode v2: od četiri Google-ova signala pristanka, vašim izborom može se omogućiti samo skladištenje za analitiku — tri signala povezana sa oglašavanjem (`ad_storage`, `ad_user_data`, `ad_personalization`) trajno su uskraćena, jer ne koristimo Google-ove funkcije oglašavanja. Naša analitika je isključivo prve strane; ne koristimo je za oglašavanje, ciljanje oglasa niti praćenje na više sajtova.

Ova lista kolačića može se ažurirati tokom vremena kako se platforma razvija; trudićemo se da ovaj odeljak bude aktuelan.

**Pristanak na kolačiće.** Kada prvi put posetite Oglasino, baner za pristanak vam omogućava da **Prihvatite sve**, **Odbijete sve** ili **Prilagodite** svoje izbore po kategorijama. Strogo neophodni kolačići ne mogu se odbiti jer sajt bez njih ne može da funkcioniše; kategorije preferencija i analitike su opcione i ostaju isključene dok ih ne dozvolite. Vaš izbor se beleži u malom kolačiću sačuvanom u vašem sopstvenom pregledaču (pod nazivom `og_consent`) — pošto se čuva u vašem pregledaču, a ne na vašem nalogu, izbor se odnosi na taj pregledač. Preferencije kolačića možete promeniti u svako doba na našoj stranici sa preferencijama kolačića (dostupnoj na `/owner/cookies` i iz podnožja veb-sajta), ili sa stranice podešavanja naloga ako ste prijavljeni. Kada izvršimo materijalnu izmenu ove Politike privatnosti ili naših Uslova korišćenja, baner za pristanak se ponovo pojavljuje kako biste mogli da pregledate i ponovo potvrdite svoje izbore.

**Skripte trećih strana.** Jedna skripta treće strane na našem sajtu zahteva posebno obaveštenje: **Google reCAPTCHA**. reCAPTCHA se učitava na stranicama sa formularima (registracija, prijavljivanje, kreiranje oglasa) radi sprečavanja automatizovanih zloupotreba. Postavlja sopstvene kolačiće (uključujući kolačić `_GRECAPTCHA`) i prikuplja informacije, uključujući vašu IP adresu, okruženje pregledača, pokrete miša i sadržaj svih Google kolačića sesije koje već imate. Na obradu putem reCAPTCHA-e oslanjamo se kao na legitimni interes u sprečavanju prevara. Za više informacija pogledajte Google-ova sopstvena obaveštenja o privatnosti na https://policies.google.com/privacy.

**Mobilna aplikacija — čuvanje na uređaju.** Mobilne aplikacije ne koriste kolačiće. Umesto toga, čuvaju informacije na vašem uređaju kako bi aplikacija radila, uključujući: vašu sesiju za prijavljivanje (drži je Firebase Authentication); vaš izabrani portal, jezik, temu i preferencije prikaza; vaš izbor analitike (vidi ispod); keširane prevode i podatke kataloga; vremenske oznake koje se koriste da se izbegne ponovno traženje dozvola ili ponovno prikazivanje istog obaveštenja; i keširanu kopiju slika koje je aplikacija prikazala. Većina toga su funkcionalni podaci ili podaci o preferencijama. Vaša sesija za prijavljivanje i sačuvana kopija profila vašeg naloga brišu se kada se odjavite; mali broj funkcionalnih stavki koje ne omogućavaju identifikaciju — na primer, oznaka koja beleži da je vaš nalog već podešen na uređaju i keš slika aplikacije — može ostati na uređaju nakon odjavljivanja dok ih vaš operativni sistem ne oslobodi. Sve možete obrisati odjavljivanjem i brisanjem aplikacije, ili putem kontrola za skladište aplikacija na vašem uređaju.

**Mobilna aplikacija — pristanak na analitiku.** Analitika u mobilnoj aplikaciji funkcioniše drugačije nego na veb-sajtu: nema banera za kolačiće i nema kolačića. Umesto toga, kada prvi put otvorite aplikaciju, pitamo vas da li da dozvolimo analitiku, a analitika je **podrazumevano isključena** — ne omogućavamo prikupljanje analitike osim ako to ne dozvolite. Svoj izbor možete promeniti u svako doba u podešavanjima aplikacije. Analitika mobilne aplikacije je isti GA4 prve strane opisan iznad, koji izveštava u isto analitičko svojstvo koristeći Firebase identifikator instance aplikacije; ona **ne** koristi Apple-ovu funkciju App Tracking Transparency i **ne** prikuplja identifikator za oglašavanje.

---

## 8. Koliko dugo čuvamo vaše podatke

Podrazumevano pravilo je jednostavno: dok je vaš nalog aktivan, čuvamo vaše podatke onoliko dugo koliko je potrebno za pružanje usluge. Kada izbrišete svoj nalog, brišemo vaše podatke — uz nekoliko konkretnih, vremenski ograničenih izuzetaka opisanih u nastavku.

### 8.1 Dok je vaš nalog aktivan

Podaci o vašem nalogu, podaci o profilu, oglasi, slike oglasa, poruke, prilozi u ćaskanju, recenzije i omiljeni oglasi čuvaju se onoliko dugo koliko je vaš nalog aktivan. Oglasi trenutno ne ističu automatski; pojedinačne oglase možete izbrisati u svako doba sa svog naloga.

U budućnosti planiramo da dodamo automatsko brisanje oglasa i poruka iz ćaskanja koji su duže vreme neaktivni. Kada to uvedemo, ažuriraćemo ovu Politiku privatnosti.

### 8.2 IP adrese i operativni dnevnici

- **IP adrese u našem kešu za ograničavanje učestalosti zahteva** čuvaju se približno 30 minuta.
- **Dnevnici aplikacije** čuvaju se **90 dana**, nakon čega se automatski brišu.

### 8.3 Kada izbrišete svoj nalog

Brisanje naloga na Oglasinu je dvostepeni proces osmišljen da vam pruži suvisli period za predomišljanje i, jednako važno, da drugim korisnicima pruži poštenu poslednju priliku da vas prijave ako smatraju da ste na platformi postupali u zloj veri.

**Faza 1 — Privremeno brisanje (7 dana).** Kada zatražite brisanje naloga iz podešavanja, vaš nalog odmah ulazi u stanje „zakazano za brisanje”:

- **Vaš profil ostaje javno vidljiv** i obeležen je oznakom statusa „Zakazano za brisanje” kako bi drugi korisnici mogli da vide da ste zatražili brisanje. Namerno zadržavamo vaš profil vidljivim tokom ovog perioda, umesto da ga sakrijemo, kako bi korisnici koji su sa vama imali interakciju i dalje imali priliku da podnesu prijavu ako imaju legitimnu zabrinutost u vezi sa vašim ponašanjem.
- **Vaš broj telefona je sakriven** tokom ovog perioda, kako vas ne bi kontaktirali dok je vaše brisanje na čekanju.
- **Vaši oglasi su sakriveni** od javnog prikaza.
- **Recenzije o vama ostaju vidljive** kako bi se sačuvao kontekst za eventualne prijave.
- **Ne možete slati ni primati poruke** tokom perioda počeka. Postojeće poruke ostaju dostupne drugim učesnicima u vašim razgovorima radi prijavljivanja, pri čemu se vaše prikazano ime pošiljaoca menja u „Obrisani korisnik”, ali se nikakve nove poruke ne mogu slati sa ili na vaš nalog.
- **Prijave protiv vas ostaju otvorene.** Svaki korisnik koji je imao interakciju sa vama i dalje može podneti prijavu tokom perioda počeka.
- Odjavljeni ste.

Tokom ovih 7 dana, svoj nalog možete vratiti u svako doba jednostavnim ponovnim prijavljivanjem. To radimo kako ne biste izgubili svoje podatke zbog slučajnog brisanja, trenutka frustracije ili promene mišljenja. Ako se prijavite tokom perioda počeka, vraćaju se vaš profil, oglasi, vidljivost broja telefona i razmena poruka.

**Faza 2 — Trajno brisanje (nakon 7 dana).** Osmog dana, vaš nalog se trajno briše, uz izuzetke odlaganja opisane u odeljku 8.4. Trajno brisanje znači:

- Zapis o vašem nalogu, oglasi, slike oglasa, poruke iz ćaskanja, prilozi u ćaskanju, obaveštenja, omiljeni oglasi i recenzije o vama trajno se brišu iz naših baza podataka.
- Vaša profilna slika i sve slike koje ste otpremili brišu se iz našeg skladišta.
- Vaš zapis za autentifikaciju kod Firebase-a se briše.
- Recenzije koje ste ostavili o drugim korisnicima čuvaju se, pri čemu se vaše ime zamenjuje sa „Obrisani korisnik” — ove recenzije odražavaju iskustvo korisnika kog ste recenzirali, a njihovo brisanje izbrisalo bi deo njegove evidencije. Ovde vam to obelodanjujemo kako biste, kada ostavljate recenziju, znali da ona nadživljava brisanje vašeg naloga (anonimizovana).

Nakon trajnog brisanja, jedini podaci koje zadržavamo su ograničen revizorski zapis opisan u nastavku.

### 8.4 Kada brisanje može biti odloženo

U ograničenim okolnostima, možemo odložiti trajno brisanje vašeg naloga van standardnog perioda počeka od 7 dana. To se primenjuje samo u dva slučaja:

- **Pravne istrage.** Kada organ za sprovođenje zakona (kao što su policija ili sud) zatraži od nas da sačuvamo vaše podatke u vezi sa istragom koja je u toku, zakonski smo obavezni da postupimo i odložićemo brisanje onoliko dugo koliko pravni zahtev nalaže.
- **Interne istrage zloupotreba.** Kada imamo razloga da verujemo da je vaš nalog korišćen za ozbiljnu zloupotrebu platforme — na primer, prevaru više korisnika — i aktivno istražujemo, možemo odložiti brisanje radi očuvanja dokaza relevantnih za istragu.

U oba slučaja, ako je vaše brisanje odloženo, obavestićemo vas da je brisanje odloženo i, u meri u kojoj nam je to zakonski dozvoljeno, zašto. Tokom odlaganja ostaćete odjavljeni i nećete moći da koristite nalog; jedini efekat je da je trajno brisanje pauzirano. Kada se pravna ili interna istraga okonča, trajno brisanje se nastavlja.

**Pravni osnov za odlaganje:** zakonska obaveza (član 6. stav 1. tačka c)) za zahteve organa za sprovođenje zakona za očuvanje podataka, i legitimni interes (član 6. stav 1. tačka f)) za interne istrage zloupotreba.

### 8.5 Revizorski zapisi koji se zadržavaju nakon brisanja

Nakon trajnog brisanja, zadržavamo sledeće ograničene zapise:

- **Opšti revizorski zapis o brisanju** — heširana verzija vašeg korisničkog identifikatora i imejla (pomoću SHA-256, jednosmernog heša koji se ne može preokrenuti radi povraćaja vašeg originalnog imejla), zajedno sa datumom brisanja vašeg naloga i razlogom. Čuva se **30 dana** nakon brisanja, a zatim se automatski briše.
- **Revizorski zapis o zabranjenom korisniku (samo ako je vaš nalog bio zabranjen u trenutku brisanja)** — heširana verzija vašeg imejla i razlog za zabranu. Koristi se da spreči zabranjene korisnike da se odmah ponovo registruju sa istom imejl adresom. Čuva se **12 meseci**, a zatim se automatski briše.

Ovi zapisi ne sadrže nikakve lično prepoznatljive informacije koje se mogu povratiti — samo jednosmerne heševe. Nakon isteka perioda čuvanja, briše se čak i heš.

### 8.6 Prijave koje podnose korisnici ili koje se odnose na korisnike

Trenutno se prijave o korisnicima ili oglasima čuvaju neograničeno kako bi administratori mogli da uoče obrasce ponovljenih zloupotreba. Planiramo da uvedemo automatsko brisanje rešenih prijava nakon utvrđenog perioda; kada to uradimo, ažuriraćemo ovu Politiku privatnosti.

---

## 9. Vaša prava

Na osnovu GDPR-a i srpskog zakona o zaštiti podataka, imate sledeća prava u vezi sa vašim podacima o ličnosti. Mi podržavamo svako od njih.

**Pravo na pristup.** Možete zatražiti kopiju podataka o ličnosti koje čuvamo o vama. Pošaljite svoj zahtev na privacy@oglasino.com. Odgovorićemo u roku od mesec dana, kako to zahteva GDPR.

**Pravo na ispravku.** Većinu svojih podataka o ličnosti možete ispraviti direktno u podešavanjima profila. Za podatke koje ne možete sami da uredite (kao što su informacije povezane sa moderacijom), pošaljite imejl na privacy@oglasino.com i ispravićemo sve netačnosti.

**Pravo na brisanje („pravo na zaborav”).** Svoj nalog možete izbrisati u svako doba iz podešavanja naloga; vidi odeljak 8.3 za to šta ovo podrazumeva. Ako niste u mogućnosti da koristite samouslužni postupak brisanja — na primer, zato što je vaš nalog onemogućen — kontaktirajte support@oglasino.com da zatražite brisanje i odgovorićemo u roku od 30 dana, kako to zahteva GDPR. Za sve druge upite u vezi sa brisanjem povezane sa privatnošću, pošaljite imejl na privacy@oglasino.com.

**Pravo na ograničenje obrade.** Možete nas zamoliti da ograničimo način na koji obrađujemo vaše podatke o ličnosti — na primer, dok osporavate odluku o moderaciji. Pošaljite svoj zahtev i razlog na privacy@oglasino.com.

**Pravo na prenosivost podataka.** Možete zatražiti kopiju podataka o ličnosti koje ste nam dostavili, u strukturisanom, uobičajeno korišćenom i mašinski čitljivom formatu (kao što je JSON). Ovo pravo se odnosi na podatke koje ste nam vi direktno dostavili (vaš profil, oglasi, poruke, recenzije); ne obuhvata podatke koje smo mi izveli o vama (kao što su vaša ocena ili revizorski zapisi). Pošaljite imejl na privacy@oglasino.com da zatražite prenosivi izvoz.

**Pravo na prigovor.** Možete uložiti prigovor na našu obradu vaših podataka kada se oslanjamo na legitimni interes. Na primanje promotivnih imejlova možete uložiti prigovor isključivanjem odgovarajućeg prekidača u podešavanjima, što ćemo uvek poštovati. Za druge prigovore, pošaljite imejl na privacy@oglasino.com i razmotrićemo vaš prigovor.

**Pravo na opoziv pristanka.** Tamo gde se oslanjamo na vaš pristanak (kolačići i analitika, preferencije komunikacije), možete ga opozvati u svako doba:

- Preferencije kolačića i analitike na veb-sajtu: putem naše stranice sa preferencijama kolačića (na `/owner/cookies`, povezane u podnožju veb-sajta) ili podešavanja naloga.
- Analitika u mobilnoj aplikaciji: putem podešavanja analitike u aplikaciji.
- Preferencije komunikacije: putem prekidača na stranici podešavanja naloga.

Opoziv pristanka ne utiče na zakonitost bilo koje obrade koju smo izvršili pre opoziva.

**Pravo na podnošenje pritužbe nadzornom organu.** Ako smatrate da nismo zakonito postupali sa vašim podacima o ličnosti, imate pravo da podnesete pritužbu organu za zaštitu podataka. U Srbiji, nadležni organ je Poverenik za informacije od javnog značaja i zaštitu podataka o ličnosti — https://www.poverenik.rs/. Ako se nalazite u EU, takođe možete podneti pritužbu organu za zaštitu podataka u vašoj zemlji prebivališta.

**Kako odgovaramo na zahteve.** Nastojimo da na sve zahteve lica na koje se podaci odnose odgovorimo u roku od mesec dana od prijema. U ograničenim slučajevima koji uključuju naročito složene zahteve, GDPR nam dozvoljava da ovaj rok produžimo za najviše dva dodatna meseca, o čemu ćemo vas obavestiti u toku prvog meseca.

**Automatizovano donošenje odluka.** Oglasino trenutno ne donosi značajne odluke o vama koristeći isključivo automatizovane procese. Validacija sadržaja pokreće se automatski kada kreirate ili izmenite oglas (na primer, provera zabranjenog sadržaja), ali sve odluke o sprovođenju — zabrana oglasa, onemogućavanje naloga, rešavanje prijave — donosi administrator (čovek). Ako u budućnosti uvedemo automatizovano donošenje odluka, ažuriraćemo ovu Politiku privatnosti.

---

## 10. Bezbednost

Preduzimamo razumne tehničke i organizacione mere za zaštitu vaših podataka o ličnosti od neovlašćenog pristupa, izmene, otkrivanja i gubitka. Tu spadaju:

- Šifrovanje podataka u prenosu (HTTPS za sve veze između vašeg pregledača i naših servisa).
- Šifrovanje podataka u mirovanju od strane naših provajdera infrastrukture (Firebase, Firestore, Cloudflare R2, Postgres na DigitalOcean-u).
- Kontrole autentifikacije i autorizacije koje ograničavaju pristup korisničkim podacima.
- Beleženje i nadzor administratorskog pristupa.
- Heširanje sačuvanih imejl adresa i identifikatora u našim revizorskim zapisima o brisanju (tako da se ni naši zadržani revizorski podaci ne mogu preokrenuti radi identifikacije obrisanih korisnika).

Nijedan sistem nije savršeno bezbedan i ne možemo garantovati apsolutnu bezbednost. Ako saznamo za povredu podataka o ličnosti koja stvara rizik za vaša prava, obavestićemo nadležni nadzorni organ i, gde to GDPR zahteva, obavestiti vas direktno.

---

## 11. Deca

Oglasino je namenjen korisnicima uzrasta **18 godina i starijim**. Ne prikupljamo svesno podatke o ličnosti od bilo koga mlađeg od 18 godina. Ako ste mlađi od 18 godina, molimo vas da se ne registrujete niti koristite platformu. Ako smatrate da se maloletno lice registrovalo, molimo vas da kontaktirate privacy@oglasino.com i preduzećemo hitne mere za uklanjanje naloga.

---

## 12. Izmene ove Politike privatnosti

Ovu Politiku privatnosti možemo s vremena na vreme ažurirati — na primer, kada dodamo funkcije, promenimo obrađivače ili kao odgovor na izmene zakona. Kada izvršimo materijalnu izmenu:

- Ažuriraćemo datum „Poslednje ažuriranje” na vrhu ovog dokumenta.
- Prikazaćemo obaveštenje na platformi.
- Ponovo ćemo prikazati baner za pristanak na kolačiće kako biste mogli da pregledate svoje preferencije kolačića u odnosu na izmene.

Nastavak korišćenja platforme nakon izmene znači da prihvatate ažuriranu Politiku privatnosti. Ako ne prihvatate izmene, možete izbrisati svoj nalog (vidi odeljak 8.3).

---

## 13. Kontakt

Za svako pitanje o ovoj Politici privatnosti ili o tome kako Oglasino obrađuje vaše podatke, kontaktirajte nas na:

**privacy@oglasino.com**

Za sva ostala pitanja (koja se ne tiču privatnosti), molimo vas da koristite opšte kanale podrške platforme.

---

_Kraj nacrta._
