# Kako da povežeš svoju WooCommerce prodavnicu sa Oglasinom

Imaš veb prodavnicu. Oglasino može automatski da prikazuje tvoje proizvode kao oglase. Podesiš jednom, i poslije toga se cijene, fotografije i zalihe ažuriraju same.

Ovaj vodič te vodi kroz sve, korak po korak. Ne treba ti nikakvo tehničko znanje — ako umiješ da koristiš WooCommerce admin stranicu, umiješ i ovo.

Ako negdje zapneš, piši nam: **support@oglasino.com**.

## Sadržaj

- [Šta je uvoz prodavnice?](#šta-je-uvoz-prodavnice)
- [Prije nego što počneš](#prije-nego-što-počneš)
- [Brzi početak](#brzi-početak)
- [Korak 1: Pripremi svoju WooCommerce prodavnicu](#korak-1-pripremi-svoju-woocommerce-prodavnicu)
- [Korak 2: Poveži prodavnicu na Oglasinu](#korak-2-poveži-prodavnicu-na-oglasinu)
- [Korak 3: Pregled](#korak-3-pregled)
- [Korak 4: Objavi svoje proizvode](#korak-4-objavi-svoje-proizvode)
- [Kako radi sinhronizacija](#kako-radi-sinhronizacija)
- [Dodavanje novih proizvoda kasnije](#dodavanje-novih-proizvoda-kasnije)
- [Upravljanje oglasima](#upravljanje-oglasima)
- [Promjena kategorije](#promjena-kategorije)
- [Filteri](#filteri)
- [Kada nešto bude odbijeno](#kada-nešto-bude-odbijeno)
- [Premještanje proizvoda na drugo tržište](#premještanje-proizvoda-na-drugo-tržište)
- [Oznake: sva pravila](#oznake-sva-pravila)
- [Pauziranje ili zatvaranje veze](#pauziranje-ili-zatvaranje-veze)
- [Ograničenja i pravila](#ograničenja-i-pravila)
- [Treba ti pomoć?](#treba-ti-pomoć)

## Šta je uvoz prodavnice?

Uvoz prodavnice povezuje tvoju WooCommerce prodavnicu sa Oglasinom. Evo cijele ideje u četiri rečenice:

1. U svojoj prodavnici staviš **oznaku** (malu etiketu) na svaki proizvod koji želiš na Oglasinu.
2. Oglasino pročita te proizvode iz tvoje prodavnice i napravi oglase od njih.
3. Od tada Oglasino redovno provjerava tvoju prodavnicu. Ako promijeniš cijenu ili fotografiju, ili se proizvod rasproda, oglas se ažurira sam.
4. Nikada više ne moraš da unosiš proizvode ručno.

Dvije važne stvari prije nego što počneš:

- **Oglasino može samo da čita tvoju prodavnicu. Nikada ne može da je mijenja.** Napravićeš poseban ključ koji dozvoljava samo čitanje ("Read"). Ništa što mi radimo ne može da dirne tvoju prodavnicu.
- **Ništa se ne pojavljuje na Oglasinu bez tvoje dozvole.** Novi proizvodi prvo prolaze kratak pregled kod našeg tima, a i poslije odobrenja *ti* odlučuješ kada idu uživo. Nema iznenađenja.

## Prije nego što počneš

Treba ti:

- WooCommerce (WordPress) prodavnica koja je onlajn.
- Admin pristup toj prodavnici (moraš moći da otvoriš njen Dashboard).
- Oko 15–20 minuta.
- Okvirna ideja koje proizvode želiš na Oglasinu — sve, ili samo neke.

To je sve. Spreman? Krećemo.

## Brzi početak

Cio proces, u jednoj listi. Svaki korak je detaljno objašnjen niže.

1. U WooCommerce-u napravi oznaku (na primjer `oglasino`).
2. Stavi tu oznaku na svaki proizvod koji želiš na Oglasinu.
3. U WooCommerce-u napravi API ključ sa **Read** dozvolom. Kopiraj oba ključa koja dobiješ.
4. Na Oglasinu otvori svoju kontrolnu tablu i idi na **Prodavnica**. Izaberi **WooCommerce**.
5. Unesi adresu prodavnice i nalijepi oba ključa.
6. Izaberi na koje tržište idu tvoji proizvodi i upiši svoju oznaku.
7. Poveži kategorije svoje prodavnice sa Oglasino kategorijama i podesi filtere.
8. Klikni **Pošalji na pregled** i sačekaj — naš tim sve provjerava.
9. Kada se pregled završi, dobijaš obavještenje. Idi na **Spremno za sinhronizaciju** i objavi odobrene proizvode.

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
2. Štikliraj kućicu pored svakog proizvoda koji želiš na Oglasinu. (Možeš štiklirati kućicu na samom vrhu da izabereš cijelu stranicu.)
3. U padajućem meniju **Bulk edit** iznad liste izaberi **Edit**, pa klikni **Apply**.

![Biranje proizvoda za grupno označavanje](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-bulk-tag-select.png)

4. Iznad proizvoda se otvara panel. Nađi polje **Tags**, upiši svoju oznaku (`oglasino`) i klikni **Update**.

![Upisivanje oznake u panelu za grupno mijenjanje](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-bulk-tag-apply.png)

To je to — ti proizvodi su sada označeni za Oglasino.

Za označavanje jednog proizvoda (na primjer novog koji dodaš sljedećeg mjeseca): otvori proizvod za izmjenu, nađi kutiju **Product tags** sa desne strane, upiši oznaku i ažuriraj proizvod.

![Označavanje jednog proizvoda](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-product-tag-single.png)

### Napravi API ključ

API ključ je kao posebna lozinka. On dozvoljava Oglasinu da *pročita* proizvode iz tvoje prodavnice. Napravićeš ga samo sa **Read** dozvolom — to znači da Oglasino može da gleda, ali nikada ne može ništa da mijenja ili briše u tvojoj prodavnici.

Ključ dolazi u dva dijela: **Consumer key** i **Consumer secret**. Kopiraćeš oba i nalijepiti ih u Oglasino u Koraku 2.

1. U WordPress admin meniju idi na **WooCommerce → Settings**.
2. Otvori karticu **Advanced**.
3. Klikni **REST API keys**.
4. Klikni **Add key**.

![Gdje se pravi API ključ](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-rest-api-page.png)

5. Popuni formu:
   - **Description:** upiši `Oglasino` (da znaš čemu ključ služi).
   - **User:** izaberi svoj admin nalog.
   - **Permissions:** izaberi **Read**. Ne "Read/Write" — samo **Read**. To je garancija da Oglasino nikada ne može da mijenja tvoju prodavnicu.
6. Klikni **Generate API key**.

![Popunjavanje forme za ključ](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/woo-api-key-form.png)

7. Sljedeća stranica prikazuje tvoja dva ključa: **Consumer key** (počinje sa `ck_`) i **Consumer secret** (počinje sa `cs_`). **Kopiraj oba odmah** — nalijepi ih negdje na sigurno, na primjer u bilješku na računaru.

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

- **URL prodavnice** — adresa tvoje prodavnice, počinje sa `https://`. Na primjer `https://tvojaprodavnica.com`.
- **Consumer ključ** — nalijepi `ck_...` ključ koji si kopirao u Koraku 1.
- **Consumer tajna** — nalijepi `cs_...` ključ.

Polja za ključeve sakrivaju ono što kucaš, kao polja za lozinku. Klikni na ikonicu oka ako želiš da provjeriš šta si nalijepio.

Ispod polja, na ovom koraku su i prekidači tvoje veze. Sve ih možeš promijeniti i kasnije, tako da ne moraš sada da lomiš glavu:

- **Automatski aktiviraj uvezene proizvode** — uključeno: proizvodi postaju vidljivi čim se uvezu. Isključeno: i dalje se sinhronizuju, ali ostaju sakriveni dok ih sam ne aktiviraš. (Nije isto što i Pauza — Pauza u potpunosti zaustavlja sinhronizaciju.)
- **Automatsko objavljivanje poslije prve provjere** i **Automatsko objavljivanje poslije kasnijih provjera** — da li odobreni proizvodi idu uživo sami poslije pregleda, ili čekaju tebe. Detaljno objašnjeno u [Koraku 4](#korak-4-objavi-svoje-proizvode).
- **Interval sinhronizacije (minuti)** — koliko često provjeravamo promjene u tvojoj prodavnici. Počinje na 360 (na svakih 6 sati); minimum je 60.

![Unošenje adrese prodavnice i ključeva](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-credentials.png)

Kada nastaviš, Oglasino se povezuje sa tvojom prodavnicom i sve provjerava — vidjećeš poruku o provjeri. Ako nešto ne valja, dobijaš jasnu poruku. Dvije najčešće:

- *"Prodavnica je odbila tvoje API ključeve."* — Provjeri da si nalijepio oba ključa u cijelosti i da ključ ima **Read** dozvolu.
- *"Ne možemo da pristupimo tvojoj prodavnici."* — Provjeri adresu i da li je tvoj sajt zaista onlajn.

### Sajtovi i oznake

Oglasino ima više od jednog tržišta — opšte tržište i moto tržište. Na ovom koraku biraš **gdje idu tvoji proizvodi** i **koja ih oznaka označava**.

1. Štikliraj tržište (ili tržišta) na kojima želiš da objavljuješ.
2. Za svako od njih upiši oznaku iz Koraka 1 u polje **Oznake proizvoda**.

Pravilo je jednostavno: uvoze se samo proizvodi sa nekom od ovih oznaka, i **jedan proizvod može pripadati samo jednom tržištu**. Ako prodaješ na oba tržišta, koristi različitu oznaku za svako (na primjer `oglasino` za jedno, `oglasino-moto` za drugo) — i svakom proizvodu daj samo jednu od njih.

Za jedno tržište možeš unijeti više oznaka, odvojenih zarezom. Bilo koja od njih se računa.

![Biranje tržišta i unošenje oznake](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-sites-tags.png)

### Povezivanje kategorija

Sada Oglasino čita tvoje označene proizvode i grupiše ih po kategorijama *tvoje* prodavnice. Za svaku tvoju kategoriju kažeš kojoj **Oglasino kategoriji** ti proizvodi pripadaju. To se zove mapiranje. Primjer: tvoja kategorija "Zimske čarape" → Oglasino kategorija "Čarape".

Da bude brže, Oglasino predlaže najbliže poklapanje za svaku tvoju kategoriju — vidjećeš oznaku **Predloženo**. Predlog možeš prihvatiti, promijeniti, ili ostaviti kategoriju nepovezanu (nepovezano samo znači da ti proizvodi neće dobiti kategoriju iz mapiranja — postavljaš ih jedan po jedan).

- Kategorija koju izabereš za sekciju važi za **svaki proizvod u toj sekciji**...
- ...osim ako otvoriš proizvod i daš mu **njegovu sopstvenu** kategoriju. Sopstveni izbor proizvoda uvijek pobjeđuje.

**Nijesi siguran koja kategorija odgovara?** Izaberi najbolju procjenu i nastavi dalje. Naš tim provjerava svaki proizvod tokom pregleda i ispravlja kategorije gdje treba. Ovdje ne možeš "pogriješiti" ni na koji štetan način.

Svaki proizvod mora imati kategoriju prije nego što pošalješ — čarobnjak ti prikazuje koliko ih još nema.

![Povezivanje tvojih kategorija sa Oglasino kategorijama](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-mapping.png)

### Filteri

Filteri su sitni detalji kojima kupci sužavaju pretragu — stvari kao stanje (novo ili korišćeno) i isporuka. Oglasi sa dobrim filterima se češće pronalaze, pa ovaj korak vrijedi jedan minut.

Vrijednosti filtera podešavaš **jednom po sekciji**, i svaki proizvod u toj sekciji ih koristi. Kao i kod kategorija, pojedinačni proizvod može imati svoje vrijednosti — otvori proizvod, klikni **Izmijeni filtere** i promijeni šta ti treba. Vrijednost koju sam podesiš na proizvodu nosi oznaku da je izmijenjena, i uvijek se možeš vratiti na vrijednosti sekcije.

Dvije posebne stvari:

- Filter označen sa **Obavezno** mora imati vrijednost prije slanja. (Za početak je to *stanje* — novo ili korišćeno.)
- Filter *dostupnosti* se vodi automatski iz zaliha tvoje prodavnice. Njega nikada ne podešavaš.

![Podešavanje filtera sekcije](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-filters.png)

![Dijalog filtera proizvoda](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-product-filters.png)

### Pregledaj i pošalji

Posljednji korak prikazuje pregled svega: tvoja prodavnica, tržište, oznaka, broj proizvoda, kategorije. Još jedna stvar koju treba da znaš, otvoreno:

> Kada pošalješ, tvoji proizvodi idu našem timu na pregled. Ništa se ne pojavljuje na sajtu dok ne bude odobreno.

Dobro je znati i: fotografije proizvoda dolaze direktno iz tvoje prodavnice i biće prikazane na Oglasinu.

Zadovoljan pregledom? Klikni **Pošalji na pregled**.

![Završni pregled](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-wizard-review.png)

## Korak 3: Pregled

Kada pošalješ, tvoja veza prikazuje **Čeka pregled**. Evo šta to znači, iskreno i u cijelosti:

- Naš tim gleda svaki proizvod koji si poslao — imena, fotografije, kategorije — i svaki odobrava, ili odbija uz kratko objašnjenje. Ako si negdje izabrao pogrešnu kategoriju, mi je jednostavno ispravimo.
- **Dok je pregled otvoren, ta runda je zaključana.** Ne možeš mijenjati te proizvode i ne vidiš odluke dok se donose. To je namjerno: sve odluke stižu **odjednom**, kada se pregled završi, pa dobijaš jedan jasan rezultat umjesto zbunjujućeg kapanja.
- Tvoja prodavnica sve vrijeme normalno radi, naravno — pregled se tiče samo onoga što je na Oglasinu.

Kada se pregled završi, dobijaš obavještenje (u aplikaciji i mejlom). Onda:

- **Odobreni proizvodi** su spremni za objavu — vidi sljedeći korak.
- **Odbijeni proizvodi** (ako ih ima) se pojavljuju na tvojoj stranici **Problemi**, svaki sa razlogom. Možeš popraviti stvari ili zatražiti novi pregled — vidi [Kada nešto bude odbijeno](#kada-nešto-bude-odbijeno).

![Dok tvoj pregled traje](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-pending-review.png)

## Korak 4: Objavi svoje proizvode

Evo pravila koje Oglasino nikada ne krši: **oglas nikada ne ide uživo bez tvog pristanka.** Odobrenje našeg tima nije objavljivanje — *ti* objavljuješ (ili uključiš prekidač koji objavljuje za tebe; oba su tvoja odluka).

Otvori **Spremno za sinhronizaciju**. Tu čeka svaki odobreni, još neobjavljeni proizvod.

- Objavi jedan proizvod, štikliraj više njih pa klikni **Objavi izabrano**, ili klikni **Objavi sve**.
- Objavljeni proizvod postaje živ oglas na tržištu, vidljiv kupcima.
- Povremeno je neki red onemogućen uz napomenu — taj proizvod čeka na nešto (na primjer promjenu kategorije koja je još na pregledu). Blokiran je samo taj red; sve ostalo može.

![Objavljivanje sa stranice Spremno za sinhronizaciju](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-ready-for-sync.png)

**Ne želiš da klikćeš svaki put?** Dva prekidača iz Koraka 2 to rješavaju:

- **Automatsko objavljivanje poslije prve provjere** — kada se tvoj prvi pregled završi, odobreni proizvodi odmah idu uživo.
- **Automatsko objavljivanje poslije kasnijih provjera** — isto, za svaki pregled poslije prvog.

Sa oba isključena, sve uvijek čeka tebe na stranici Spremno za sinhronizaciju. A treći prekidač, **Automatski aktiviraj uvezene proizvode**, odlučuje kako proizvodi stižu: uključeno — postaju vidljivi čim se uvezu; isključeno — sinhronizuju se, ali ostaju sakriveni dok ih sam ne aktiviraš.

Sva tri su tvoj izbor, i možeš ih promijeniti bilo kada na stranici **Veza**.

![Prekidači tvoje veze](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-connection-settings.png)

## Kako radi sinhronizacija

Kada se tvoj prvi pregled završi, veza postaje **Aktivno** i Oglasino počinje redovno da provjerava tvoju prodavnicu. "Sinhronizacija" je samo ta provjera.

**Šta se automatski ažurira na tvojim živim oglasima:**

- Promjene cijena.
- Promjene imena, opisa i fotografija.
- Zalihe: proizvod koji se rasproda automatski se skida sa sajta; kada se vrati na zalihe, vraća se i oglas. (Ovo nikada ne gazi tvoje odluke — proizvod koji si sakrio ostaje sakriven.)
- Novi označeni proizvodi se *otkrivaju* — pojavljuju se na tvojoj stranici **Novi proizvodi** i čekaju tebe. Vidi [Dodavanje novih proizvoda kasnije](#dodavanje-novih-proizvoda-kasnije).

**Šta se NIKADA ne dešava automatski:**

- Objavljivanje novog oglasa. Novi proizvodi uvijek idu kroz pregled, pa kroz Spremno za sinhronizaciju (ili tvoj prekidač automatskog objavljivanja). Uvijek.

**Tempo i kontrola:**

- Koliko često provjeravamo određuje **Interval sinhronizacije** na tvojoj stranici Veza. Podrazumijevano je na svakih 6 sati; minimum je 60 minuta.
- Ne možeš da čekaš? Klikni dugme za trenutnu sinhronizaciju na stranici Veza. (Jednom na sat.)
- Stranica Veza uvijek prikazuje tvoju **Posljednju sinhronizaciju**: kada je bila, šta je uradila (koliko je napravljeno / ažurirano / uklonjeno) i koje je proizvode preskočila, sa razlogom.

Ako sinhronizacija preskoči proizvod, razlog ti kaže čiji je potez: nešto što se popravlja u tvojoj prodavnici, privremeni problem koji se sam ponovi, ili nešto na našoj strani gdje ti ne moraš ništa.

## Dodavanje novih proizvoda kasnije

Ovo je svakodnevna rutina, i kratka je:

1. U WooCommerce-u stavi svoju oznaku na novi proizvod. To je jedino što radiš u prodavnici.
2. Na sljedećoj sinhronizaciji proizvod se pojavljuje na tvojoj stranici **Novi proizvodi** na Oglasinu.
3. Obično već ima kategoriju (iz tvog mapiranja). Promijeni je ako želiš, ili izaberi ako nedostaje — proizvod ne može da se pošalje bez kategorije.
4. Podesi mu filtere ako treba (obavezni filteri moraju imati vrijednost).
5. Štikliraj proizvode i klikni **Pošalji izabrano**.
6. Grupa ide na pregled. Kada se završi, dobijaš obavještenje, a odobreni proizvodi stižu na **Spremno za sinhronizaciju** kao i obično.

Proizvodi koji još ne mogu da se pošalju su istaknuti sa razlogom na samom redu — najčešće "prvo izaberi kategoriju" ili problem sa oznakom (vidi [Oznake: sva pravila](#oznake-sva-pravila)).

![Novi proizvodi te čekaju](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-new-products.png)

## Upravljanje oglasima

**Proizvodi prodavnice** prikazuju svaki živi oglas koji je došao iz tvoje prodavnice. Otvori bilo koji proizvod da vidiš njegove akcije: pregledaj oglas, pogledaj ga u svojoj prodavnici, zatraži promjenu kategorije, ili izmijeni njegove filtere.

![Akcije jednog proizvoda](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-product-actions.png)

Sa ove stranice možeš:

- Otvoriti bilo koji oglas i vidjeti ga kao što ga vide kupci.
- **Sakriti oglas.** Sakrivanje ga skida sa sajta za kupce, ali on sve vrijeme prima ažuriranja iz tvoje prodavnice (cijena, zalihe, fotografije). Kada ga poželiš nazad, prikaži ga ponovo — sljedeća sinhronizacija ga vraća onlajn. Sakrivanje je po oglasu i potpuno povratno.
- **Zatražiti promjenu kategorije** za proizvod — vidi sljedeću sekciju.

Dobro je znati: oglasi uvezeni iz tvoje prodavnice su *vođeni tvojom prodavnicom*. Proizvod mijenjaš u WooCommerce-u — ne na Oglasinu — i promjene stižu na sljedećoj sinhronizaciji. To i jeste cijela poenta: jedno mjesto za mijenjanje.

![Tvoji živi oglasi iz prodavnice](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-shop-products.png)

## Promjena kategorije

Kategorije su jedina stvar koja ide kroz pregled čak i kada je proizvod već živ — kategorija odlučuje gdje te kupci pronalaze, pa naš tim potvrđuje promjene. Dvije vrste:

**Promjena kategorije jednog proizvoda.** Na stranici **Proizvodi prodavnice** otvori proizvod i klikni **Zatraži promjenu kategorije**. Izaberi novu kategoriju, podesi filtere za nju, i izaberi šta se dešava dok zahtjev čeka:

- **Sakrij do odluke** — oglas se sklanja dok se pregled ne završi.
- **Ostavi aktivno** — oglas ostaje živ pod trenutnom kategorijom dok se pregled ne završi.

Zatim **Pošalji zahtjev za promjenu**. Ako bude odobren, promjena se primjenjuje automatski i proizvod ide (ili ostaje) uživo. Ako bude odbijen, sve ostaje tačno kako je bilo, a razlog ćeš naći na stranici **Problemi**. Dok zahtjev čeka, taj proizvod je označen kao na pregledu i njegovo dugme za promjenu je onemogućeno — jedan otvoren zahtjev po proizvodu.

**Promjena podrazumijevane kategorije mapiranja.** Stranica **Mapiranja kategorija** prikazuje svaku kategoriju tvoje prodavnice i njenu podrazumijevanu Oglasino kategoriju — onu koju nasljeđuju budući proizvodi.

- Red bez podrazumijevane kategorije ima dugme za njeno postavljanje. Prvo postavljanje važi samo za buduće proizvode — i prolazi kratak pregled.
- Red sa postojećom ima **Promijeni podrazumijevanu kategoriju**. Kada takva promjena bude odobrena, ažuriraju se i proizvodi koji već koriste tu podrazumijevanu kategoriju. Proizvodi kojima si dao sopstvenu kategoriju se nikada ne diraju.
- Podrazumijevana kategorija koju je naš tim potvrdio nosi oznaku **Potvrđeno**.

Dok je pregled koji uključuje neko mapiranje otvoren, njegova dugmad su onemogućena uz kratko objašnjenje — nikada sklonjena, samo čekaju.

![Tvoja mapiranja kategorija](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-category-mappings.png)

## Filteri

Sve iz koraka sa filterima nastavlja da radi i poslije pokretanja, a filtere možeš mijenjati bilo kada — **izmjene filtera ne idu na pregled**.

- **Filteri sekcije:** na stranici **Mapiranja kategorija** svaka sekcija ima dugme **Filteri sekcije**. Vrijednosti koje tu sačuvaš važe za svaki proizvod u sekciji — osim za proizvode gdje si podesio sopstvene vrijednosti.
- **Filteri proizvoda:** na stranicama **Proizvodi prodavnice** (i **Novi proizvodi**) otvori proizvod i izmijeni njegove filtere da podesiš vrijednosti samo za njega. Tvoje sopstvene vrijednosti su označene kao izmijenjene; uvijek ih možeš vratiti pod kontrolu sekcije.
- **Obavezni** filteri uvijek moraju imati vrijednost — obaveznu vrijednost možeš promijeniti, ali je ne možeš ostaviti praznu.
- Filter *dostupnosti* je automatski (prati zalihe tvoje prodavnice) i ne može se mijenjati.

Jedna iskrena napomena: pošto izmjene filtera preskaču pregled, postoji dnevno ograničenje koliko ih možeš napraviti. Velikodušno je — primijetićeš ga samo ako nešto na tvojoj strani poludi i ispali hiljade izmjena.

![Mijenjanje filtera jedne sekcije](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-filter-popup.png)

## Kada nešto bude odbijeno

Ponekad naš tim odbije proizvod ili kategoriju. To nije kraj ničega — evo kako radi.

Sve što traži tvoju pažnju živi na jednoj stranici: **Problemi**. Tu ćeš naći:

- **Odbijeno pregledom** — odbijene proizvode, svaki sa razlogom pregledača. Proizvodi odbijeni zajedno kao grupa dijele jedan razlog.
- **Odbijene promjene kategorija** — sa dugmetom da zatražiš promjenu ponovo ako želiš još jedan pokušaj.
- **Odbijena premještanja** — vidi [sekciju o premještanju](#premještanje-proizvoda-na-drugo-tržište).
- **Dodatne oznake tržišta** — žive proizvode koji nose oznaku za drugo tržište. Skloni dodatnu oznaku u svojoj prodavnici i ovo se samo čisti. U međuvremenu možeš sakriti oglas.
- **Preskočeni proizvodi** — proizvode koje sinhronizacija nije mogla da uveze, svaki sa razlogom i čiji je potez.

**Ne slažeš se sa odlukom?** Klikni **Zatraži još jedan pregled**. Možeš dodati kratku bilješku za pregledača (do 500 znakova) — iskoristi je da objasniš šta je pregledač možda propustio. Tvoja žalba ide u redovni red za pregled i bićeš obaviješten o rezultatu. Da red ostane fer, istu stvar možeš ponovo žaliti tek poslije nekoliko dana.

Ako je odbijena cijela tvoja *kategorija*, njeni proizvodi se sklanjaju sa tržišta zajedno, i zajedno se vraćaju ako se odluka preokrene — ne moraš ništa po proizvodu.

![Stranica Problemi](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/sr/app-issues.png)

## Premještanje proizvoda na drugo tržište

Prodaješ na opštem tržištu nešto što zapravo pripada moto tržištu (ili obrnuto)? Samo promijeni oznaku u svojoj prodavnici:

1. U WooCommerce-u skloni oznaku starog tržišta i dodaj oznaku drugog tržišta.
2. Na sljedećoj sinhronizaciji proizvod se pojavljuje u sekciji premještanja na tvojoj stranici **Problemi**.
3. Izaberi mu kategoriju **na novom tržištu** i pošalji premještanje — premještanje se pregleda kao novi proizvod.
4. Tvoj živi oglas **ostaje živ** na starom tržištu sve vrijeme. Ništa ne nestaje dok čekaš.
5. Kada premještanje bude odobreno, objavljuješ ga kao svaki odobreni proizvod (Spremno za sinhronizaciju ili automatsko objavljivanje). Oglas se seli — sa svojim ocjenama, omiljenima i porukama.

Jedna stvar se mijenja: veb adresa oglasa, jer sada živi na drugom tržištu. Stari linkovi ka njemu prestaju da rade. Ako ipak ne želiš premještanje, vrati staru oznaku — gotovo.

## Oznake: sva pravila

Oznaka je tvoj volan. Evo šta svaka promjena oznake radi, u jednoj tabeli:

| Ti uradiš ovo u svojoj prodavnici | Ovo se desi na Oglasinu |
| --- | --- |
| Dodaš svoju oznaku proizvodu | Pojavljuje se na **Novi proizvodi** i čeka da ga pošalješ na pregled |
| Skloniš oznaku sa živog oglasa | Oglas odmah odlazi oflajn. Ništa se ne briše — tvoj proizvod, tvoja odluka |
| Vratiš oznaku | Oglas se vraća onlajn na sljedećoj sinhronizaciji |
| Zamijeniš jednu svoju oznaku drugom za *isto* tržište | Ništa se ne mijenja |
| Proizvod nosi više oznaka za isto tržište | U redu je — bilo koja se računa |
| Promijeniš oznaku u oznaku *drugog* tržišta | Proizvod ide kroz premještanje ([vidi gore](#premještanje-proizvoda-na-drugo-tržište)) |
| Dodaš *dodatnu* oznaku drugog tržišta na živi oglas | Oglas ostaje gdje jeste i dalje se ažurira, ali dobijaš stavku na **Problemi** — skloni dodatnu oznaku da se očisti |
| Daš *novom* proizvodu oznake oba tržišta | Čeka na **Novi proizvodi** označen "ispravi oznaku" — ne može da se pošalje dok ne ostane jedno tržište |
| Obrišeš proizvod iz WooCommerce-a u potpunosti | Briše se i njegov Oglasino oglas. Ako ga kasnije ponovo napraviš u prodavnici, kreće ispočetka kao nov proizvod |

## Pauziranje ili zatvaranje veze

**Pauza** (na stranici Veza) potpuno zaustavlja sinhronizaciju — ništa se ne ažurira, ništa se ne otkriva — dok je ne nastaviš. Tvoji oglasi ostaju kakvi jesu. Koristi je za odmor ili radove na prodavnici.

Ako tvoji pristupni podaci prestanu da rade (na primjer ključ je obrisan u WooCommerce-u), veza se sama pauzira i kaže ti — unesi ključeve ponovo i ponovi provjeru da nastaviš.

**Zatvaranje veze** završava sve. Pošto su tvoji oglasi važni, zatvaranje uvijek pita šta da bude sa njima — biraš jedno od tri:

- **Zadrži moje oglase** — ostaju na Oglasinu i postaju obični oglasi koje sam mijenjaš, više nijesu vezani za prodavnicu.
- **Deaktiviraj moje oglase** — sakriveni su i odvezani; kasnije ih možeš ponovo aktivirati i mijenjati.
- **Obriši moje oglase** — uklanjaju se sa Oglasina i njihove fotografije se brišu.

Zatvaranje se potvrđuje ukucavanjem tražene riječi — nije nešto što se desi slučajno.

## Ograničenja i pravila

Sve na jednom mjestu, bez iznenađenja:

- **Dozvola API ključa:** uvijek **Read**. Oglasino nikada ne piše u tvoju prodavnicu.
- **Adresa prodavnice:** mora počinjati sa `https://`.
- **Jedno tržište po proizvodu.** Oznake proizvoda određuju njegovo tržište, i može imati samo jedno.
- **Interval sinhronizacije:** minimum 60 minuta; podrazumijevano na svakih 6 sati.
- **Ručna sinhronizacija:** jednom na sat.
- **Ponovni pokušaj preskočenih proizvoda:** do 10 proizvoda na sat.
- **Ograničenje broja proizvoda:** obično ga nema. Oglasino može postaviti gornju granicu koliko proizvoda veza smije da uveze; ako se granica odnosi na tebe, prikazana je na tvojoj stranici Veza, a proizvodi preko nje se pojavljuju među preskočenima.
- **Bilješka uz žalbu:** do 500 znakova (i nije obavezna).
- **Imena i opisi:** predugački se automatski skraćuju da stanu u format oglasa — imena na 80 znakova, opisi na 2000.
- **Izmjene filtera:** bez pregleda, ali važi velikodušno dnevno ograničenje.
- **Valuta prodavnice:** valuta tvoje prodavnice mora biti neka koju tržište podržava — reći ćemo ti pri povezivanju ako nije.

## Treba ti pomoć?

Piši nam na **support@oglasino.com** — reci nam adresu svoje prodavnice i šta si pokušavao, pa ćemo to riješiti zajedno.
