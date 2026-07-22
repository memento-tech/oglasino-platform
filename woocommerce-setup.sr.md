# Kako da povežeš svoju WooCommerce prodavnicu sa Oglasinom

Imaš veb prodavnicu. Oglasino može automatski da prikazuje tvoje proizvode kao oglase. Podesiš jednom, i posle toga se cene, fotografije i zalihe ažuriraju same.

Ovaj vodič te vodi kroz sve, korak po korak. Ne treba ti nikakvo tehničko znanje — ako umeš da koristiš WooCommerce admin stranicu, umeš i ovo.

Ako negde zapneš, piši nam: **support@oglasino.com**.

## Sadržaj

- [Šta je uvoz prodavnice?](#šta-je-uvoz-prodavnice)
- [Pre nego što počneš](#pre-nego-što-počneš)
- [Brzi početak](#brzi-početak)
- [Korak 1: Pripremi svoju WooCommerce prodavnicu](#korak-1-pripremi-svoju-woocommerce-prodavnicu)
- [Korak 2: Poveži prodavnicu na Oglasinu](#korak-2-poveži-prodavnicu-na-oglasinu)
- [Korak 3: Pregled](#korak-3-pregled)
- [Korak 4: Objavi svoje proizvode](#korak-4-objavi-svoje-proizvode)
- [Kako radi sinhronizacija](#kako-radi-sinhronizacija)
- [Dodavanje novih proizvoda kasnije](#dodavanje-novih-proizvoda-kasnije)
- [Upravljanje oglasima](#upravljanje-oglasima)
- [Promena kategorije](#promena-kategorije)
- [Filteri](#filteri)
- [Kada nešto bude odbijeno](#kada-nešto-bude-odbijeno)
- [Premeštanje proizvoda na drugo tržište](#premeštanje-proizvoda-na-drugo-tržište)
- [Oznake: sva pravila](#oznake-sva-pravila)
- [Pauziranje ili zatvaranje veze](#pauziranje-ili-zatvaranje-veze)
- [Ograničenja i pravila](#ograničenja-i-pravila)
- [Treba ti pomoć?](#treba-ti-pomoć)

## Šta je uvoz prodavnice?

Uvoz prodavnice povezuje tvoju WooCommerce prodavnicu sa Oglasinom. Evo cele ideje u četiri rečenice:

1. U svojoj prodavnici staviš **oznaku** (malu etiketu) na svaki proizvod koji želiš na Oglasinu.
2. Oglasino pročita te proizvode iz tvoje prodavnice i napravi oglase od njih.
3. Od tada Oglasino redovno proverava tvoju prodavnicu. Ako promeniš cenu ili fotografiju, ili se proizvod rasproda, oglas se ažurira sam.
4. Nikada više ne moraš da unosiš proizvode ručno.

Dve važne stvari pre nego što počneš:

- **Oglasino može samo da čita tvoju prodavnicu. Nikada ne može da je menja.** Napravićeš poseban ključ koji dozvoljava samo čitanje ("Read"). Ništa što mi radimo ne može da dirne tvoju prodavnicu.
- **Ništa se ne pojavljuje na Oglasinu bez tvoje dozvole.** Novi proizvodi prvo prolaze kratak pregled kod našeg tima, a i posle odobrenja *ti* odlučuješ kada idu uživo. Nema iznenađenja.

## Pre nego što počneš

Treba ti:

- WooCommerce (WordPress) prodavnica koja je onlajn.
- Admin pristup toj prodavnici (moraš moći da otvoriš njen Dashboard).
- Oko 15–20 minuta.
- Okvirna ideja koje proizvode želiš na Oglasinu — sve, ili samo neke.

To je sve. Spreman? Krećemo.

## Brzi početak

Ceo proces, u jednoj listi. Svaki korak je detaljno objašnjen niže.

1. U WooCommerce-u napravi oznaku (na primer `oglasino`).
2. Stavi tu oznaku na svaki proizvod koji želiš na Oglasinu.
3. U WooCommerce-u napravi API ključ sa **Read** dozvolom. Kopiraj oba ključa koja dobiješ.
4. Na Oglasinu otvori svoju kontrolnu tablu i idi na **Prodavnica**. Izaberi **WooCommerce**.
5. Unesi adresu prodavnice i nalepi oba ključa.
6. Izaberi na koje tržište idu tvoji proizvodi i upiši svoju oznaku.
7. Poveži kategorije svoje prodavnice sa Oglasino kategorijama i podesi filtere.
8. Klikni **Pošalji na pregled** i sačekaj — naš tim sve proverava.
9. Kada se pregled završi, dobijaš obaveštenje. Idi na **Spremno za sinhronizaciju** i objavi odobrene proizvode.

Gotovo. Od tog trenutka tvoja prodavnica i Oglasino ostaju usklađeni automatski.

## Korak 1: Pripremi svoju WooCommerce prodavnicu

Sve u ovom koraku se dešava u tvojoj **WooCommerce admin stranici** — ne na Oglasinu.

### Napravi oznaku

Oznaka je samo etiketa. Njome kažeš Oglasinu "želim *ovaj* proizvod na Oglasinu" — uvoze se samo označeni proizvodi. Sve ostalo u tvojoj prodavnici se ignoriše.

1. U WordPress admin meniju idi na **Products → Tags**.
2. U polje **Name** upiši oznaku koju ćeš koristiti za Oglasino. `oglasino` je dobar, jednostavan izbor — ali ime biraš sam. Zapamti ga, trebaće ti kasnije.
3. Klikni **Add new tag**.
4. Tvoja nova oznaka se pojavljuje u listi desno.

![Pravljenje oznake u WooCommerce-u](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-product-tags-page.png)

### Stavi oznaku na proizvode

Sada označi proizvode koje želiš na Oglasinu. Najbrže je označiti više proizvoda odjednom:

1. Idi na **Products → All Products**.
2. Štikliraj kućicu pored svakog proizvoda koji želiš na Oglasinu. (Možeš štiklirati kućicu na samom vrhu da izabereš celu stranicu.)
3. U padajućem meniju **Bulk edit** iznad liste izaberi **Edit**, pa klikni **Apply**.

![Biranje proizvoda za grupno označavanje](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-bulk-tag-select.png)

4. Iznad proizvoda se otvara panel. Nađi polje **Tags**, upiši svoju oznaku (`oglasino`) i klikni **Update**.

![Upisivanje oznake u panelu za grupno menjanje](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-bulk-tag-apply.png)

To je to — ti proizvodi su sada označeni za Oglasino.

Za označavanje jednog proizvoda (na primer novog koji dodaš sledećeg meseca): otvori proizvod za izmenu, nađi kutiju **Product tags** sa desne strane, upiši oznaku i ažuriraj proizvod.

![Označavanje jednog proizvoda](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-product-tag-single.png)

### Napravi API ključ

API ključ je kao posebna lozinka. On dozvoljava Oglasinu da *pročita* proizvode iz tvoje prodavnice. Napravićeš ga samo sa **Read** dozvolom — to znači da Oglasino može da gleda, ali nikada ne može ništa da menja ili briše u tvojoj prodavnici.

Ključ dolazi u dva dela: **Consumer key** i **Consumer secret**. Kopiraćeš oba i nalepiti ih u Oglasino u Koraku 2.

1. U WordPress admin meniju idi na **WooCommerce → Settings**.
2. Otvori karticu **Advanced**.
3. Klikni **REST API keys**.
4. Klikni **Add key**.

![Gde se pravi API ključ](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-rest-api-page.png)

5. Popuni formu:
   - **Description:** upiši `Oglasino` (da znaš čemu ključ služi).
   - **User:** izaberi svoj admin nalog.
   - **Permissions:** izaberi **Read**. Ne "Read/Write" — samo **Read**. To je garancija da Oglasino nikada ne može da menja tvoju prodavnicu.
6. Klikni **Generate API key**.

![Popunjavanje forme za ključ](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-api-key-form.png)

7. Sledeća stranica prikazuje tvoja dva ključa: **Consumer key** (počinje sa `ck_`) i **Consumer secret** (počinje sa `cs_`). **Kopiraj oba odmah** — nalepi ih negde na sigurno, na primer u belešku na računaru.

**Važno:** WooCommerce prikazuje tajni ključ **samo ovaj jedan put**. Ako napustiš stranicu bez kopiranja, ne možeš ga vratiti — morao bi da obrišeš ključ i napraviš novi. Nije katastrofa, ali jeste gnjavaža. Zato: kopiraj oba, odmah.

![Odmah kopiraj oba ključa](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-api-key-generated.png)

Tvoja prodavnica je spremna. Sada na Oglasino.

## Korak 2: Poveži prodavnicu na Oglasinu

Prijavi se na Oglasino i otvori svoju kontrolnu tablu. U meniju ćeš naći sekciju **Prodavnica** — to je centrala za sve iz ovog vodiča. Unutra su: **Veza**, **Proizvodi prodavnice**, **Novi proizvodi**, **Spremno za sinhronizaciju**, **Mapiranja kategorija** i **Problemi**. Ne brini šta sve to znači — vodič pokriva svaku od njih.

Otvori **Veza**. Kreće kratak čarobnjak. Možeš stati i vratiti se bilo kada; ništa nije konačno dok na kraju ne klikneš **Pošalji na pregled**. Ako želiš ispočetka, klikni **Odbaci nacrt** — podaci za pristup prodavnici se iz odbačenog nacrta nikada ne čuvaju.

### Izaberi platformu

Izaberi **WooCommerce**.

![Biranje WooCommerce platforme](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-shop-platform.png)

### Poveži svoju prodavnicu

Tri polja:

- **URL prodavnice** — adresa tvoje prodavnice, počinje sa `https://`. Na primer `https://tvojaprodavnica.com`.
- **Consumer ključ** — nalepi `ck_...` ključ koji si kopirao u Koraku 1.
- **Consumer tajna** — nalepi `cs_...` ključ.

Polja za ključeve sakrivaju ono što kucaš, kao polja za lozinku. Klikni na ikonicu oka ako želiš da proveriš šta si nalepio.

Ispod polja, na ovom koraku su i prekidači tvoje veze. Sve ih možeš promeniti i kasnije, tako da ne moraš sada da lomiš glavu:

- **Automatski aktiviraj uvezene proizvode** — uključeno: proizvodi postaju vidljivi čim se uvezu. Isključeno: i dalje se sinhronizuju, ali ostaju sakriveni dok ih sam ne aktiviraš. (Nije isto što i Pauza — Pauza u potpunosti zaustavlja sinhronizaciju.)
- **Automatsko objavljivanje posle prve provere** i **Automatsko objavljivanje posle kasnijih provera** — da li odobreni proizvodi idu uživo sami posle pregleda, ili čekaju tebe. Detaljno objašnjeno u [Koraku 4](#korak-4-objavi-svoje-proizvode).
- **Interval sinhronizacije (minuti)** — koliko često proveravamo promene u tvojoj prodavnici. Počinje na 360 (na svakih 6 sati); minimum je 60.

![Unošenje adrese prodavnice i ključeva](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-credentials.png)

Kada nastaviš, Oglasino se povezuje sa tvojom prodavnicom i sve proverava — videćeš "Validating your store…" poruku o proveri. Ako nešto ne valja, dobijaš jasnu poruku. Dve najčešće:

- *"Prodavnica je odbila tvoje API ključeve."* — Proveri da si nalepio oba ključa u celosti i da ključ ima **Read** dozvolu.
- *"Ne možemo da pristupimo tvojoj prodavnici."* — Proveri adresu i da li je tvoj sajt zaista onlajn.

### Sajtovi i oznake

Oglasino ima više od jednog tržišta — opšte tržište i moto tržište. Na ovom koraku biraš **gde idu tvoji proizvodi** i **koja ih oznaka označava**.

1. Štikliraj tržište (ili tržišta) na kojima želiš da objavljuješ.
2. Za svako od njih upiši oznaku iz Koraka 1 u polje **Oznake proizvoda**.

Pravilo je jednostavno: uvoze se samo proizvodi sa nekom od ovih oznaka, i **jedan proizvod može pripadati samo jednom tržištu**. Ako prodaješ na oba tržišta, koristi različitu oznaku za svako (na primer `oglasino` za jedno, `oglasino-moto` za drugo) — i svakom proizvodu daj samo jednu od njih.

Za jedno tržište možeš uneti više oznaka, odvojenih zarezom. Bilo koja od njih se računa.

![Biranje tržišta i unošenje oznake](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-sites-tags.png)

### Povezivanje kategorija

Sada Oglasino čita tvoje označene proizvode i grupiše ih po kategorijama *tvoje* prodavnice. Za svaku tvoju kategoriju kažeš kojoj **Oglasino kategoriji** ti proizvodi pripadaju. To se zove mapiranje. Primer: tvoja kategorija "Zimske čarape" → Oglasino kategorija "Čarape".

Da bude brže, Oglasino predlaže najbliže poklapanje za svaku tvoju kategoriju — videćeš oznaku **Predloženo**. Predlog možeš prihvatiti, promeniti, ili ostaviti kategoriju nepovezanu (nepovezano samo znači da ti proizvodi neće dobiti kategoriju iz mapiranja — postavljaš ih jedan po jedan).

- Kategorija koju izabereš za sekciju važi za **svaki proizvod u toj sekciji**...
- ...osim ako otvoriš proizvod i daš mu **njegovu sopstvenu** kategoriju. Sopstveni izbor proizvoda uvek pobeđuje.

**Nisi siguran koja kategorija odgovara?** Izaberi najbolju procenu i nastavi dalje. Naš tim proverava svaki proizvod tokom pregleda i ispravlja kategorije gde treba. Ovde ne možeš "pogrešiti" ni na koji štetan način.

Svaki proizvod mora imati kategoriju pre nego što pošalješ — čarobnjak ti prikazuje koliko ih još nema.

![Povezivanje tvojih kategorija sa Oglasino kategorijama](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-mapping.png)

### Filteri

Filteri su sitni detalji kojima kupci sužavaju pretragu — stvari kao stanje (novo ili korišćeno) i isporuka. Oglasi sa dobrim filterima se češće pronalaze, pa ovaj korak vredi jedan minut.

Vrednosti filtera podešavaš **jednom po sekciji**, i svaki proizvod u toj sekciji ih koristi. Kao i kod kategorija, pojedinačni proizvod može imati svoje vrednosti — otvori proizvod, klikni **Izmeni filtere** i promeni šta ti treba. Vrednost koju sam podesiš na proizvodu nosi oznaku da je izmenjena, i uvek se možeš vratiti na vrednosti sekcije.

Dve posebne stvari:

- Filter označen sa **Obavezno** mora imati vrednost pre slanja. (Za početak je to *stanje* — novo ili korišćeno.)
- Filter *dostupnosti* se vodi automatski iz zaliha tvoje prodavnice. Njega nikada ne podešavaš.

![Podešavanje filtera sekcije](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-filters.png)

![Dijalog filtera proizvoda](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-product-filters.png)

### Pregledaj i pošalji

Poslednji korak prikazuje pregled svega: tvoja prodavnica, tržište, oznaka, broj proizvoda, kategorije. Još jedna stvar koju treba da znaš, otvoreno:

> Kada pošalješ, tvoji proizvodi idu našem timu na pregled. Ništa se ne pojavljuje na sajtu dok ne bude odobreno.

Dobro je znati i: fotografije proizvoda dolaze direktno iz tvoje prodavnice i biće prikazane na Oglasinu.

Zadovoljan pregledom? Klikni **Pošalji na pregled**.

![Završni pregled](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-review.png)

## Korak 3: Pregled

Kada pošalješ, tvoja veza prikazuje **Čeka pregled**. Evo šta to znači, iskreno i u celosti:

- Naš tim gleda svaki proizvod koji si poslao — imena, fotografije, kategorije — i svaki odobrava, ili odbija uz kratko objašnjenje. Ako si negde izabrao pogrešnu kategoriju, mi je jednostavno ispravimo.
- **Dok je pregled otvoren, ta runda je zaključana.** Ne možeš menjati te proizvode i ne vidiš odluke dok se donose. To je namerno: sve odluke stižu **odjednom**, kada se pregled završi, pa dobijaš jedan jasan rezultat umesto zbunjujućeg kapanja.
- Tvoja prodavnica sve vreme normalno radi, naravno — pregled se tiče samo onoga što je na Oglasinu.

Kada se pregled završi, dobijaš obaveštenje (u aplikaciji i mejlom). Onda:

- **Odobreni proizvodi** su spremni za objavu — vidi sledeći korak.
- **Odbijeni proizvodi** (ako ih ima) se pojavljuju na tvojoj stranici **Problemi**, svaki sa razlogom. Možeš popraviti stvari ili zatražiti novi pregled — vidi [Kada nešto bude odbijeno](#kada-nešto-bude-odbijeno).

![Dok tvoj pregled traje](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-pending-review.png)

## Korak 4: Objavi svoje proizvode

Evo pravila koje Oglasino nikada ne krši: **oglas nikada ne ide uživo bez tvog pristanka.** Odobrenje našeg tima nije objavljivanje — *ti* objavljuješ (ili uključiš prekidač koji objavljuje za tebe; oba su tvoja odluka).

Otvori **Spremno za sinhronizaciju**. Tu čeka svaki odobreni, još neobjavljeni proizvod.

- Objavi jedan proizvod, štikliraj više njih pa klikni **Objavi izabrano**, ili klikni **Objavi sve**.
- Objavljeni proizvod postaje živ oglas na tržištu, vidljiv kupcima.
- Povremeno je neki red onemogućen uz napomenu — taj proizvod čeka na nešto (na primer promenu kategorije koja je još na pregledu). Blokiran je samo taj red; sve ostalo može.

![Objavljivanje sa stranice Spremno za sinhronizaciju](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-ready-for-sync.png)

**Ne želiš da klikćeš svaki put?** Dva prekidača iz Koraka 2 to rešavaju:

- **Automatsko objavljivanje posle prve provere** — kada se tvoj prvi pregled završi, odobreni proizvodi odmah idu uživo.
- **Automatsko objavljivanje posle kasnijih provera** — isto, za svaki pregled posle prvog.

Sa oba isključena, sve uvek čeka tebe na stranici Spremno za sinhronizaciju. A treći prekidač, **Automatski aktiviraj uvezene proizvode**, odlučuje kako proizvodi stižu: uključeno — postaju vidljivi čim se uvezu; isključeno — sinhronizuju se, ali ostaju sakriveni dok ih sam ne aktiviraš.

Sva tri su tvoj izbor, i možeš ih promeniti bilo kada na stranici **Veza**.

![Prekidači tvoje veze](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-connection-settings.png)

## Kako radi sinhronizacija

Kada se tvoj prvi pregled završi, veza postaje **Aktivno** i Oglasino počinje redovno da proverava tvoju prodavnicu. "Sinhronizacija" je samo ta provera.

**Šta se automatski ažurira na tvojim živim oglasima:**

- Promene cena.
- Promene imena, opisa i fotografija.
- Zalihe: proizvod koji se rasproda automatski se skida sa sajta; kada se vrati na zalihe, vraća se i oglas. (Ovo nikada ne gazi tvoje odluke — proizvod koji si sakrio ostaje sakriven.)
- Novi označeni proizvodi se *otkrivaju* — pojavljuju se na tvojoj stranici **Novi proizvodi** i čekaju tebe. Vidi [Dodavanje novih proizvoda kasnije](#dodavanje-novih-proizvoda-kasnije).

**Šta se NIKADA ne dešava automatski:**

- Objavljivanje novog oglasa. Novi proizvodi uvek idu kroz pregled, pa kroz Spremno za sinhronizaciju (ili tvoj prekidač automatskog objavljivanja). Uvek.

**Tempo i kontrola:**

- Koliko često proveravamo određuje **Interval sinhronizacije** na tvojoj stranici Veza. Podrazumevano je na svakih 6 sati; minimum je 60 minuta.
- Ne možeš da čekaš? Klikni dugme za trenutnu sinhronizaciju na stranici Veza. (Jednom na sat.)
- Stranica Veza uvek prikazuje tvoju **Poslednju sinhronizaciju**: kada je bila, šta je uradila (koliko je napravljeno / ažurirano / uklonjeno) i koje je proizvode preskočila, sa razlogom.

Ako sinhronizacija preskoči proizvod, razlog ti kaže čiji je potez: nešto što se popravlja u tvojoj prodavnici, privremeni problem koji se sam ponovi, ili nešto na našoj strani gde ti ne moraš ništa.

## Dodavanje novih proizvoda kasnije

Ovo je svakodnevna rutina, i kratka je:

1. U WooCommerce-u stavi svoju oznaku na novi proizvod. To je jedino što radiš u prodavnici.
2. Na sledećoj sinhronizaciji proizvod se pojavljuje na tvojoj stranici **Novi proizvodi** na Oglasinu.
3. Obično već ima kategoriju (iz tvog mapiranja). Promeni je ako želiš, ili izaberi ako nedostaje — proizvod ne može da se pošalje bez kategorije.
4. Podesi mu filtere ako treba (obavezni filteri moraju imati vrednost).
5. Štikliraj proizvode i klikni **Pošalji izabrano**.
6. Grupa ide na pregled. Kada se završi, dobijaš obaveštenje, a odobreni proizvodi stižu na **Spremno za sinhronizaciju** kao i obično.

Proizvodi koji još ne mogu da se pošalju su istaknuti sa razlogom na samom redu — najčešće "prvo izaberi kategoriju" ili problem sa oznakom (vidi [Oznake: sva pravila](#oznake-sva-pravila)).

![Novi proizvodi te čekaju](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-new-products.png)

## Upravljanje oglasima

**Proizvodi prodavnice** prikazuju svaki živi oglas koji je došao iz tvoje prodavnice. Otvori bilo koji proizvod da vidiš njegove akcije: pregledaj oglas, pogledaj ga u svojoj prodavnici, zatraži promenu kategorije, ili izmeni njegove filtere.

![Akcije jednog proizvoda](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-product-actions.png)

Sa ove stranice možeš:

- Otvoriti bilo koji oglas i videti ga kao što ga vide kupci.
- **Sakriti oglas.** Sakrivanje ga skida sa sajta za kupce, ali on sve vreme prima ažuriranja iz tvoje prodavnice (cena, zalihe, fotografije). Kada ga poželiš nazad, prikaži ga ponovo — sledeća sinhronizacija ga vraća onlajn. Sakrivanje je po oglasu i potpuno povratno.
- **Zatražiti promenu kategorije** za proizvod — vidi sledeću sekciju.

Dobro je znati: oglasi uvezeni iz tvoje prodavnice su *vođeni tvojom prodavnicom*. Proizvod menjaš u WooCommerce-u — ne na Oglasinu — i promene stižu na sledećoj sinhronizaciji. To i jeste cela poenta: jedno mesto za menjanje.

![Tvoji živi oglasi iz prodavnice](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-shop-products.png)

## Promena kategorije

Kategorije su jedina stvar koja ide kroz pregled čak i kada je proizvod već živ — kategorija odlučuje gde te kupci pronalaze, pa naš tim potvrđuje promene. Dve vrste:

**Promena kategorije jednog proizvoda.** Na stranici **Proizvodi prodavnice** otvori proizvod i klikni **Zatraži promenu kategorije**. Izaberi novu kategoriju, podesi filtere za nju, i izaberi šta se dešava dok zahtev čeka:

- **Sakrij do odluke** — oglas se sklanja dok se pregled ne završi.
- **Ostavi aktivno** — oglas ostaje živ pod trenutnom kategorijom dok se pregled ne završi.

Zatim **Pošalji zahtev za promenu**. Ako bude odobren, promena se primenjuje automatski i proizvod ide (ili ostaje) uživo. Ako bude odbijen, sve ostaje tačno kako je bilo, a razlog ćeš naći na stranici **Problemi**. Dok zahtev čeka, taj proizvod je označen kao na pregledu i njegovo dugme za promenu je onemogućeno — jedan otvoren zahtev po proizvodu.

**Promena podrazumevane kategorije mapiranja.** Stranica **Mapiranja kategorija** prikazuje svaku kategoriju tvoje prodavnice i njenu podrazumevanu Oglasino kategoriju — onu koju nasleđuju budući proizvodi.

- Red bez podrazumevane kategorije ima dugme za njeno postavljanje. Prvo postavljanje važi samo za buduće proizvode — i prolazi kratak pregled.
- Red sa postojećom ima **Promeni podrazumevanu kategoriju**. Kada takva promena bude odobrena, ažuriraju se i proizvodi koji već koriste tu podrazumevanu kategoriju. Proizvodi kojima si dao sopstvenu kategoriju se nikada ne diraju.
- Podrazumevana kategorija koju je naš tim potvrdio nosi oznaku **Potvrđeno**.

Dok je pregled koji uključuje neko mapiranje otvoren, njegova dugmad su onemogućena uz kratko objašnjenje — nikada sklonjena, samo čekaju.

![Tvoja mapiranja kategorija](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-category-mappings.png)

## Filteri

Sve iz koraka sa filterima nastavlja da radi i posle pokretanja, a filtere možeš menjati bilo kada — **izmene filtera ne idu na pregled**.

- **Filteri sekcije:** na stranici **Mapiranja kategorija** svaka sekcija ima dugme **Filteri sekcije**. Vrednosti koje tu sačuvaš važe za svaki proizvod u sekciji — osim za proizvode gde si podesio sopstvene vrednosti.
- **Filteri proizvoda:** na stranicama **Proizvodi prodavnice** (i **Novi proizvodi**) otvori proizvod i izmeni njegove filtere da podesiš vrednosti samo za njega. Tvoje sopstvene vrednosti su označene kao izmenjene; uvek ih možeš vratiti pod kontrolu sekcije.
- **Obavezni** filteri uvek moraju imati vrednost — obaveznu vrednost možeš promeniti, ali je ne možeš ostaviti praznu.
- Filter *dostupnosti* je automatski (prati zalihe tvoje prodavnice) i ne može se menjati.

Jedna iskrena napomena: pošto izmene filtera preskaču pregled, postoji dnevno ograničenje koliko ih možeš napraviti. Velikodušno je — primetićeš ga samo ako nešto na tvojoj strani poludi i ispali hiljade izmena.

![Menjanje filtera jedne sekcije](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-filter-popup.png)

## Kada nešto bude odbijeno

Ponekad naš tim odbije proizvod ili kategoriju. To nije kraj ničega — evo kako radi.

Sve što traži tvoju pažnju živi na jednoj stranici: **Problemi**. Tu ćeš naći:

- **Odbijeno pregledom** — odbijene proizvode, svaki sa razlogom pregledača. Proizvodi odbijeni zajedno kao grupa dele jedan razlog.
- **Odbijene promene kategorija** — sa dugmetom da zatražiš promenu ponovo ako želiš još jedan pokušaj.
- **Odbijena premeštanja** — vidi [sekciju o premeštanju](#premeštanje-proizvoda-na-drugo-tržište).
- **Dodatne oznake tržišta** — žive proizvode koji nose oznaku za drugo tržište. Skloni dodatnu oznaku u svojoj prodavnici i ovo se samo čisti. U međuvremenu možeš sakriti oglas.
- **Preskočeni proizvodi** — proizvode koje sinhronizacija nije mogla da uveze, svaki sa razlogom i čiji je potez.

**Ne slažeš se sa odlukom?** Klikni **Zatraži još jedan pregled**. Možeš dodati kratku belešku za pregledača (do 500 znakova) — iskoristi je da objasniš šta je pregledač možda propustio. Tvoja žalba ide u redovni red za pregled i bićeš obavešten o rezultatu. Da red ostane fer, istu stvar možeš ponovo žaliti tek posle nekoliko dana.

Ako je odbijena cela tvoja *kategorija*, njeni proizvodi se sklanjaju sa tržišta zajedno, i zajedno se vraćaju ako se odluka preokrene — ne moraš ništa po proizvodu.

![Stranica Problemi](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-issues.png)

## Premeštanje proizvoda na drugo tržište

Prodaješ na opštem tržištu nešto što zapravo pripada moto tržištu (ili obrnuto)? Samo promeni oznaku u svojoj prodavnici:

1. U WooCommerce-u skloni oznaku starog tržišta i dodaj oznaku drugog tržišta.
2. Na sledećoj sinhronizaciji proizvod se pojavljuje u sekciji premeštanja na tvojoj stranici **Problemi**.
3. Izaberi mu kategoriju **na novom tržištu** i pošalji premeštanje — premeštanje se pregleda kao novi proizvod.
4. Tvoj živi oglas **ostaje živ** na starom tržištu sve vreme. Ništa ne nestaje dok čekaš.
5. Kada premeštanje bude odobreno, objavljuješ ga kao svaki odobreni proizvod (Spremno za sinhronizaciju ili automatsko objavljivanje). Oglas se seli — sa svojim ocenama, omiljenima i porukama.

Jedna stvar se menja: veb adresa oglasa, jer sada živi na drugom tržištu. Stari linkovi ka njemu prestaju da rade. Ako ipak ne želiš premeštanje, vrati staru oznaku — gotovo.

## Oznake: sva pravila

Oznaka je tvoj volan. Evo šta svaka promena oznake radi, u jednoj tabeli:

| Ti uradiš ovo u svojoj prodavnici | Ovo se desi na Oglasinu |
| --- | --- |
| Dodaš svoju oznaku proizvodu | Pojavljuje se na **Novi proizvodi** i čeka da ga pošalješ na pregled |
| Skloniš oznaku sa živog oglasa | Oglas odmah odlazi oflajn. Ništa se ne briše — tvoj proizvod, tvoja odluka |
| Vratiš oznaku | Oglas se vraća onlajn na sledećoj sinhronizaciji |
| Zameniš jednu svoju oznaku drugom za *isto* tržište | Ništa se ne menja |
| Proizvod nosi više oznaka za isto tržište | U redu je — bilo koja se računa |
| Promeniš oznaku u oznaku *drugog* tržišta | Proizvod ide kroz premeštanje ([vidi gore](#premeštanje-proizvoda-na-drugo-tržište)) |
| Dodaš *dodatnu* oznaku drugog tržišta na živi oglas | Oglas ostaje gde jeste i dalje se ažurira, ali dobijaš stavku na **Problemi** — skloni dodatnu oznaku da se očisti |
| Daš *novom* proizvodu oznake oba tržišta | Čeka na **Novi proizvodi** označen "ispravi oznaku" — ne može da se pošalje dok ne ostane jedno tržište |
| Obrišeš proizvod iz WooCommerce-a u potpunosti | Briše se i njegov Oglasino oglas. Ako ga kasnije ponovo napraviš u prodavnici, kreće ispočetka kao nov proizvod |

## Pauziranje ili zatvaranje veze

**Pauza** (na stranici Veza) potpuno zaustavlja sinhronizaciju — ništa se ne ažurira, ništa se ne otkriva — dok je ne nastaviš. Tvoji oglasi ostaju kakvi jesu. Koristi je za odmor ili radove na prodavnici.

Ako tvoji pristupni podaci prestanu da rade (na primer ključ je obrisan u WooCommerce-u), veza se sama pauzira i kaže ti — unesi ključeve ponovo i ponovi proveru da nastaviš.

**Zatvaranje veze** završava sve. Pošto su tvoji oglasi važni, zatvaranje uvek pita šta da bude sa njima — biraš jedno od tri:

- **Zadrži moje oglase** — ostaju na Oglasinu i postaju obični oglasi koje sam menjaš, više nisu vezani za prodavnicu.
- **Deaktiviraj moje oglase** — sakriveni su i odvezani; kasnije ih možeš ponovo aktivirati i menjati.
- **Obriši moje oglase** — uklanjaju se sa Oglasina i njihove fotografije se brišu.

Zatvaranje se potvrđuje ukucavanjem tražene reči — nije nešto što se desi slučajno.

## Ograničenja i pravila

Sve na jednom mestu, bez iznenađenja:

- **Dozvola API ključa:** uvek **Read**. Oglasino nikada ne piše u tvoju prodavnicu.
- **Adresa prodavnice:** mora počinjati sa `https://`.
- **Jedno tržište po proizvodu.** Oznake proizvoda određuju njegovo tržište, i može imati samo jedno.
- **Interval sinhronizacije:** minimum 60 minuta; podrazumevano na svakih 6 sati.
- **Ručna sinhronizacija:** jednom na sat.
- **Ponovni pokušaj preskočenih proizvoda:** do 10 proizvoda na sat.
- **Ograničenje broja proizvoda:** obično ga nema. Oglasino može postaviti gornju granicu koliko proizvoda veza sme da uveze; ako se granica odnosi na tebe, prikazana je na tvojoj stranici Veza, a proizvodi preko nje se pojavljuju među preskočenima.
- **Beleška uz žalbu:** do 500 znakova (i nije obavezna).
- **Imena i opisi:** predugački se automatski skraćuju da stanu u format oglasa — imena na 80 znakova, opisi na 2000.
- **Izmene filtera:** bez pregleda, ali važi velikodušno dnevno ograničenje.
- **Valuta prodavnice:** valuta tvoje prodavnice mora biti neka koju tržište podržava — reći ćemo ti pri povezivanju ako nije.

## Treba ti pomoć?

Piši nam na **support@oglasino.com** — reci nam adresu svoje prodavnice i šta si pokušavao, pa ćemo to rešiti zajedno.
