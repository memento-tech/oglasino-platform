# Kak podklyuchit vash magazin WooCommerce k Oglasino

U vas est internet-magazin. Oglasino mozhet avtomaticheski pokazyvat vashi tovary kak obyavleniya. Vy nastraivaete odin raz, i posle etogo tseny, foto i nalichie obnovlyayutsya sami.

Eto rukovodstvo provedet vas cherez vse, shag za shagom. Nikakikh tekhnicheskikh znaniy ne nuzhno — esli vy umeete polzovatsya admin-panelyu WooCommerce, vy spravites i s etim.

Esli gde-to zastryanete, napishite nam: **support@oglasino.com**.

## Soderzhanie

- [Kak podklyuchit vash magazin WooCommerce k Oglasino](#kak-podklyuchit-vash-magazin-woocommerce-k-oglasino)
  - [Soderzhanie](#soderzhanie)
  - [Chto takoe import magazina?](#chto-takoe-import-magazina)
  - [Pered nachalom](#pered-nachalom)
  - [Bystryy start](#bystryy-start)
  - [Shag 1: Podgotovte vash magazin WooCommerce](#shag-1-podgotovte-vash-magazin-woocommerce)
    - [Sozdayte teg](#sozdayte-teg)
    - [Postavte teg na tovary](#postavte-teg-na-tovary)
    - [Sozdayte API-klyuch](#sozdayte-api-klyuch)
  - [Shag 2: Podklyuchite magazin na Oglasino](#shag-2-podklyuchite-magazin-na-oglasino)
    - [Vyberite platformu](#vyberite-platformu)
    - [Podklyuchite vash magazin](#podklyuchite-vash-magazin)
    - [Sayty i tegi](#sayty-i-tegi)
    - [Sopostavlenie kategoriy](#sopostavlenie-kategoriy)
    - [Filtry](#filtry)
    - [Proverte i otpravte](#proverte-i-otpravte)
  - [Shag 3: Proverka](#shag-3-proverka)
  - [Shag 4: Opublikuyte vashi tovary](#shag-4-opublikuyte-vashi-tovary)
  - [Kak rabotaet sinkhronizatsiya](#kak-rabotaet-sinkhronizatsiya)
  - [Dobavlenie novykh tovarov pozzhe](#dobavlenie-novykh-tovarov-pozzhe)
  - [Upravlenie obyavleniyami](#upravlenie-obyavleniyami)
  - [Smena kategorii](#smena-kategorii)
  - [Filtry](#filtry-1)
  - [Esli chto-to otkloneno](#esli-chto-to-otkloneno)
  - [Perenos tovara na drugoy marketpleys](#perenos-tovara-na-drugoy-marketpleys)
  - [Tegi: vse pravila](#tegi-vse-pravila)
  - [Pauza ili zakrytie podklyucheniya](#pauza-ili-zakrytie-podklyucheniya)
  - [Limity i pravila](#limity-i-pravila)
  - [Nuzhna pomoshch?](#nuzhna-pomoshch)

## Chto takoe import magazina?

Import magazina soedinyaet vash magazin WooCommerce s Oglasino. Vot vsya ideya v chetyrekh predlozheniyakh:

1. V svoem magazine vy stavite **teg** (malenkuyu metku) na kazhdyy tovar, kotoryy khotite videt na Oglasino.
2. Oglasino schityvaet eti tovary iz vashego magazina i sozdaet iz nikh obyavleniya.
3. S etogo momenta Oglasino regulyarno proveryaet vash magazin. Esli vy pomenyali tsenu ili foto, ili tovar raskuplen, obyavlenie obnovlyaetsya samo.
4. Vam bolshe nikogda ne nuzhno vvodit tovary vruchnuyu.

Dve vazhnye veshchi pered nachalom:

- **Oglasino mozhet tolko chitat vash magazin. Izmenit ego ono ne mozhet nikogda.** Vy sozdadite spetsialnyy klyuch tolko dlya chteniya ("Read"). Nichto iz togo, chto my delaem, ne mozhet tronut vash magazin.
- **Nichto ne poyavlyaetsya na Oglasino bez vashego razresheniya.** Novye tovary snachala prokhodyat korotkuyu proverku u nashey komandy, i dazhe posle odobreniya _vy_ reshaete, kogda oni vykhodyat v prodazhu. Nikakikh syurprizov.

## Pered nachalom

Vam nuzhny:

- Magazin WooCommerce (WordPress), kotoryy rabotaet onlayn.
- Admin-dostup k etomu magazinu (vy dolzhny umet otkryt ego Dashboard).
- Okolo 15–20 minut.
- Primernoe ponimanie, kakie tovary vy khotite na Oglasino — vse ili tolko chast.

Eto vse. Gotovy? Poekhali.

## Bystryy start

Ves protsess odnim spiskom. Kazhdyy shag podrobno obyasnen nizhe.

1. V WooCommerce sozdayte teg (naprimer `oglasino`).
2. Postavte etot teg na kazhdyy tovar, kotoryy khotite na Oglasino.
3. V WooCommerce sozdayte API-klyuch s razresheniem **Read**. Skopiruyte oba klyucha, kotorye on vydast.
4. Na Oglasino otkroyte vashu panel i pereydite v razdel **Magazin**. Vyberite **WooCommerce**.
5. Vvedite adres magazina i vstavte oba klyucha.
6. Vyberite, na kakoy marketpleys idut vashi tovary, i vvedite vash teg.
7. Sopostavte kategorii vashego magazina s kategoriyami Oglasino i nastroyte filtry.
8. Nazhmite **Otpravit na proverku** i podozhdite — nasha komanda vse proverit.
9. Kogda proverka zavershitsya, vy poluchite uvedomlenie. Pereydite v **Gotovo k sinkhronizatsii** i opublikuyte odobrennye tovary.

Gotovo. S etogo momenta vash magazin i Oglasino ostayutsya sinkhronizirovannymi avtomaticheski.

## Shag 1: Podgotovte vash magazin WooCommerce

Vse v etom shage proiskhodit v **admin-paneli WooCommerce** — ne na Oglasino.

### Sozdayte teg

Teg — eto prosto metka. Im vy govorite Oglasino "khochu _etot_ tovar na Oglasino" — importiruyutsya tolko tovary s tegom. Vse ostalnoe v vashem magazine ignoriruetsya.

1. V admin-menyu WordPress pereydite v **Products → Tags**.
2. V pole **Name** vvedite teg, kotoryy budete ispolzovat dlya Oglasino. `oglasino` — khoroshiy prostoy variant, no imya vybiraete vy. Zapomnite ego, ono ponadobitsya pozzhe.
3. Nazhmite **Add new tag**.
4. Vash novyy teg poyavitsya v spiske sprava.

![Sozdanie tega v WooCommerce](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-product-tags-page.png)

### Postavte teg na tovary

Teper otmette tovary, kotorye khotite na Oglasino. Bystree vsego — pometit srazu mnogo tovarov:

1. Pereydite v **Products → All Products**.
2. Otmette galochkoy kazhdyy tovar, kotoryy khotite na Oglasino. (Mozhno otmetit galochku na samom verkhu, chtoby vybrat vsyu stranitsu.)
3. V vypadayushchem menyu **Bulk edit** nad spiskom vyberite **Edit** i nazhmite **Apply**.

![Vybor tovarov dlya massovogo tegirovaniya](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-bulk-tag-select.png)

4. Nad tovarami otkroetsya panel. Naydite pole **Tags**, vvedite vash teg (`oglasino`) i nazhmite **Update**.

![Vvod tega v paneli massovogo redaktirovaniya](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-bulk-tag-apply.png)

Vot i vse — eti tovary teper otmecheny dlya Oglasino.

Chtoby pometit odin tovar (naprimer novyy, kotoryy vy dobavite v sleduyushchem mesyatse): otkroyte tovar dlya redaktirovaniya, naydite blok **Product tags** sprava, vvedite teg i obnovite tovar.

![Tegirovanie odnogo tovara](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-product-tag-single.png)

### Sozdayte API-klyuch

API-klyuch — eto kak spetsialnyy parol. On pozvolyaet Oglasino _chitat_ tovary iz vashego magazina. Vy sozdadite ego tolko s razresheniem **Read** — eto znachit, chto Oglasino mozhet smotret, no nikogda ne mozhet nichego izmenit ili udalit v vashem magazine.

Klyuch sostoit iz dvukh chastey: **Consumer key** i **Consumer secret**. Vy skopiruete oba i vstavite ikh v Oglasino na Shage 2.

1. V admin-menyu WordPress pereydite v **WooCommerce → Settings**.
2. Otkroyte vkladku **Advanced**.
3. Nazhmite **REST API keys**.
4. Nazhmite **Add key**.

![Gde sozdaetsya API-klyuch](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-rest-api-page.png)

5. Zapolnite formu:
   - **Description:** vvedite `Oglasino` (chtoby pomnit, dlya chego etot klyuch).
   - **User:** vyberite vash admin-akkaunt.
   - **Permissions:** vyberite **Read**. Ne "Read/Write" — tolko **Read**. Imenno eto garantiruet, chto Oglasino nikogda ne smozhet izmenit vash magazin.
6. Nazhmite **Generate API key**.

![Zapolnenie formy klyucha](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-api-key-form.png)

7. Sleduyushchaya stranitsa pokazhet vashi dva klyucha: **Consumer key** (nachinaetsya s `ck_`) i **Consumer secret** (nachinaetsya s `cs_`). **Skopiruyte oba pryamo seychas** — sokhranite ikh v nadezhnom meste, naprimer v zametke na kompyutere.

**Vazhno:** WooCommerce pokazyvaet sekretnyy klyuch **tolko odin raz**. Esli vy uydete so stranitsy, ne skopirovav ego, vernut ego nelzya — pridetsya udalit klyuch i sozdat novyy. Ne katastrofa, no khlopotno. Poetomu: kopiruyte oba srazu.

![Srazu skopiruyte oba klyucha](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/woo-api-key-generated.png)

Vash magazin gotov. Teper — na Oglasino.

## Shag 2: Podklyuchite magazin na Oglasino

Voydite na Oglasino i otkroyte vashu panel. V menyu vy naydete razdel **Magazin** — eto tsentr vsego, o chem eto rukovodstvo. Vnutri: **Podklyuchenie**, **Tovary magazina**, **Novye tovary**, **Gotovo k sinkhronizatsii**, **Sopostavleniya kategoriy** i **Problemy**. Ne volnuytes, chto eto vse znachit — rukovodstvo obyasnit kazhdyy razdel.

Otkroyte **Podklyuchenie**. Zapustitsya korotkiy master nastroyki. Vy mozhete ostanovitsya i vernutsya v lyuboy moment; nichego ne stanet okonchatelnym, poka vy v kontse ne nazhmete **Otpravit na proverku**. Esli khotite nachat zanovo, nazhmite **Otmenit chernovik** — dannye dostupa k magazinu iz otmenennogo chernovika nikogda ne sokhranyayutsya.

### Vyberite platformu

Vyberite **WooCommerce**.

![Vybor WooCommerce](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-shop-platform.png)

### Podklyuchite vash magazin

Tri polya:

- **URL magazina** — adres vashego magazina, nachinaetsya s `https://`. Naprimer `https://vashmagazin.com`.
- **Consumer key** — vstavte klyuch `ck_...`, kotoryy vy skopirovali na Shage 1.
- **Consumer secret** — vstavte klyuch `cs_...`.

Polya klyuchey skryvayut to, chto vy vvodite, kak polya parolya. Nazhmite na ikonku glaza, esli khotite proverit, chto vy vstavili.

Pod polyami na etom shage nakhodyatsya i pereklyuchateli vashego podklyucheniya. Vse ikh mozhno pomenyat pozzhe, tak chto ne lomayte golovu seychas:

- **Avtomaticheski aktivirovat importirovannye tovary** — vklyucheno: tovary stanovyatsya vidimymi srazu posle importa. Vyklyucheno: oni prodolzhayut sinkhronizirovatsya, no ostayutsya skrytymi, poka vy sami ikh ne aktiviruete. (Eto ne to zhe samoe, chto Pauza — Pauza polnostyu ostanavlivaet sinkhronizatsiyu.)
- **Avtopublikatsiya posle pervoy proverki** i **Avtopublikatsiya posle sleduyushchikh proverok** — vykhodyat li odobrennye tovary v prodazhu sami posle proverki ili zhdut vas. Podrobno v [Shage 4](#shag-4-opublikuyte-vashi-tovary).
- **Interval sinkhronizatsii (minuty)** — kak chasto my proveryaem izmeneniya v vashem magazine. Nachinaetsya s 360 (kazhdye 6 chasov); minimum — 60.

![Vvod adresa magazina i klyuchey](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-wizard-credentials.png)

Kogda vy prodolzhite, Oglasino podklyuchitsya k vashemu magazinu i vse proverit — vy uvidite soobshchenie o proverke. Esli chto-to ne tak, vy poluchite ponyatnoe soobshchenie. Dva samykh chastykh:

- _"Magazin otklonil vashi API-klyuchi."_ — Proverte, chto vy vstavili oba klyucha polnostyu i chto u klyucha razreshenie **Read**.
- _"My ne mozhem svyazatsya s vashim magazinom."_ — Proverte adres i to, chto vash sayt deystvitelno rabotaet.

### Sayty i tegi

U Oglasino bolshe odnogo marketpleysa — obshchiy marketpleys i moto-marketpleys. Na etom shage vy vybiraete, **kuda idut vashi tovary** i **kakoy teg ikh otmechaet**.

1. Otmette marketpleys (ili marketpleysy), gde khotite publikovatsya.
2. Dlya kazhdogo vvedite teg iz Shaga 1 v pole **Tegi tovarov**.

Pravilo prostoe: importiruyutsya tolko tovary s odnim iz etikh tegov, i **odin tovar mozhet prinadlezhat tolko odnomu marketpleysu**. Esli vy prodaete na oboikh, ispolzuyte raznye tegi (naprimer `oglasino` dlya odnogo i `oglasino-moto` dlya drugogo) — i davayte kazhdomu tovaru tolko odin iz nikh.

Dlya odnogo marketpleysa mozhno vvesti neskolko tegov cherez zapyatuyu. Schitaetsya lyuboy iz nikh.

![Vybor marketpleysa i vvod tega](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-wizard-sites-tags.png)

### Sopostavlenie kategoriy

Teper Oglasino schityvaet vashi tovary s tegom i gruppiruet ikh po kategoriyam _vashego_ magazina. Dlya kazhdoy vashey kategorii vy govorite, k kakoy **kategorii Oglasino** eti tovary otnosyatsya. Eto nazyvaetsya sopostavleniem. Primer: vasha kategoriya "Zimnie noski" → kategoriya Oglasino "Noski".

Chtoby bylo bystree, Oglasino predlagaet blizhayshee sovpadenie dlya kazhdoy vashey kategorii — vy uvidite metku **Predlozheno**. Predlozhenie mozhno prinyat, pomenyat ili ostavit kategoriyu nesopostavlennoy (eto prosto znachit, chto ee tovary ne poluchat kategoriyu iz sopostavleniya — vy zadadite ikh po odnomu).

- Kategoriya, kotoruyu vy vybrali dlya sektsii, deystvuet na **kazhdyy tovar v etoy sektsii**...
- ...esli tolko vy ne otkroete tovar i ne dadite emu **ego sobstvennuyu** kategoriyu. Sobstvennyy vybor tovara vsegda pobezhdaet.

**Ne uvereny, kakaya kategoriya podkhodit?** Vyberite luchshiy variant i idite dalshe. Nasha komanda proveryaet kazhdyy tovar vo vremya proverki i ispravlyaet kategorii, gde nuzhno. Zdes nelzya "oshibitsya" tak, chtoby eto navredilo.

U kazhdogo tovara dolzhna byt kategoriya do otpravki — master pokazyvaet, u skolkikh tovarov ee eshche net.

![Sopostavlenie vashikh kategoriy s kategoriyami Oglasino](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-wizard-mapping.png)

### Filtry

Filtry — eto melkie detali, po kotorym pokupateli suzhayut poisk: sostoyanie (novyy ili b/u), dostavka i tak dalee. Obyavleniya s khoroshimi filtrami nakhodyat chashche, tak chto etot shag stoit odnoy minuty.

Znacheniya filtrov vy zadaete **odin raz na sektsiyu**, i kazhdyy tovar v etoy sektsii ikh ispolzuet. Kak i s kategoriyami, otdelnyy tovar mozhet imet svoi znacheniya — otkroyte tovar, otkroyte ego filtry i pomenyayte, chto nuzhno. Znachenie, kotoroe vy zadali samomu tovaru, pomechaetsya kak izmenennoe, i vsegda mozhno vernutsya k znacheniyam sektsii.

Dve osobye veshchi:

- Filtr s metkoy **Obyazatelno** dolzhen imet znachenie do otpravki. (Vnachale eto _sostoyanie_ — novyy ili b/u.)
- Filtr _nalichiya_ vedetsya avtomaticheski po ostatkam vashego magazina. Ego vy nikogda ne zadaete.

![Nastroyka filtrov sektsii](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-wizard-filters.png)

![Dialog filtrov tovara](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-wizard-product-filters.png)

### Proverte i otpravte

Posledniy shag pokazyvaet svodku vsego: vash magazin, marketpleys, teg, skolko tovarov, kategorii. Eshche odna veshch, kotoruyu nuzhno znat, otkryto:

> Posle otpravki vashi tovary idut nashey komande na proverku. Nichto ne poyavitsya na sayte, poka ne budet odobreno.

Polezno znat i eto: foto tovarov berutsya pryamo iz vashego magazina i budut pokazany na Oglasino.

Dovolny svodkoy? Nazhmite **Otpravit na proverku**.

![Itogovaya svodka](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-wizard-review.png)

## Shag 3: Proverka

Posle otpravki vashe podklyuchenie pokazyvaet **Ozhidaet proverki**. Vot chto eto znachit, chestno i polnostyu:

- Nasha komanda smotrit kazhdyy otpravlennyy tovar — nazvaniya, foto, kategorii — i kazhdyy odobryaet ili otklonyaet s korotkim obyasneniem. Esli vy gde-to vybrali ne tu kategoriyu, my prosto ee ispravim.
- **Poka proverka otkryta, eta partiya zablokirovana.** Vy ne mozhete redaktirovat eti tovary i ne vidite resheniya po khodu. Eto sdelano spetsialno: vse resheniya prikhodyat **srazu**, kogda proverka zavershena, — odin ponyatnyy rezultat vmesto sbivayushchego s tolku ruchya.
- Vash magazin vse eto vremya rabotaet kak obychno — proverka kasaetsya tolko togo, chto na Oglasino.

Kogda proverka zavershitsya, vy poluchite uvedomlenie (v prilozhenii i po pochte). Dalee:

- **Odobrennye tovary** gotovy k publikatsii — smotrite sleduyushchiy shag.
- **Otklonennye tovary** (esli takie est) poyavyatsya na vashey stranitse **Problemy**, kazhdyy s prichinoy. Mozhno ispravit ili zaprosit eshche odnu proverku — smotrite [Esli chto-to otkloneno](#esli-chto-to-otkloneno).

![Poka idet vasha proverka](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-pending-review.png)

## Shag 4: Opublikuyte vashi tovary

Vot pravilo, kotoroe Oglasino ne narushaet nikogda: **obyavlenie nikogda ne vykhodit v prodazhu bez vashego soglasiya.** Odobrenie nashey komandy — eto ne publikatsiya. Publikuete _vy_ (ili vklyuchaete pereklyuchatel, kotoryy publikuet za vas; oba varianta — vashe reshenie).

Otkroyte **Gotovo k sinkhronizatsii**. Zdes zhdet kazhdyy odobrennyy, eshche ne opublikovannyy tovar.

- Opublikuyte odin tovar, otmette neskolko i nazhmite **Opublikovat vybrannoe**, ili nazhmite **Opublikovat vse**.
- Opublikovannyy tovar stanovitsya zhivym obyavleniem na marketpleyse, vidimym pokupatelyam.
- Inogda stroka otklyuchena s primechaniem — etot tovar chego-to zhdet (naprimer, smeny kategorii, kotoraya eshche na proverke). Zablokirovana tolko eta stroka; vse ostalnoe mozhno.

![Publikatsiya so stranitsy Gotovo k sinkhronizatsii](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-ready-for-sync.png)

**Ne khotite nazhimat kazhdyy raz?** Dva pereklyuchatelya iz Shaga 2 eto reshayut:

- **Avtopublikatsiya posle pervoy proverki** — kogda vasha pervaya proverka zavershitsya, odobrennye tovary srazu vykhodyat v prodazhu.
- **Avtopublikatsiya posle sleduyushchikh proverok** — to zhe samoe dlya kazhdoy proverki posle pervoy.

Esli oba vyklyucheny, vse vsegda zhdet vas na stranitse Gotovo k sinkhronizatsii. A tretiy pereklyuchatel, **Avtomaticheski aktivirovat importirovannye tovary**, reshaet, kak tovary prikhodyat: vklyucheno — oni stanovyatsya vidimymi srazu posle importa; vyklyucheno — oni sinkhroniziruyutsya, no ostayutsya skrytymi, poka vy sami ikh ne aktiviruete.

Vse tri — vash vybor, i ikh mozhno pomenyat v lyuboy moment na stranitse **Podklyuchenie**.

![Pereklyuchateli vashego podklyucheniya](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-connection-settings.png)

## Kak rabotaet sinkhronizatsiya

Kogda vasha pervaya proverka zavershena, podklyuchenie stanovitsya **Aktivno**, i Oglasino nachinaet regulyarno proveryat vash magazin. "Sinkhronizatsiya" — eto prosto takaya proverka.

**Chto obnovlyaetsya avtomaticheski na vashikh zhivykh obyavleniyakh:**

- Izmeneniya tsen.
- Izmeneniya nazvaniya, opisaniya i foto.
- Nalichie: raskuplennyy tovar avtomaticheski snimaetsya s prodazhi; kogda on snova v nalichii, obyavlenie vozvrashchaetsya. (Eto nikogda ne otmenyaet vashi resheniya — tovar, kotoryy vy skryli, ostaetsya skrytym.)
- Novye tovary s tegom _obnaruzhivayutsya_ — oni poyavlyayutsya na vashey stranitse **Novye tovary** i zhdut vas. Smotrite [Dobavlenie novykh tovarov pozzhe](#dobavlenie-novykh-tovarov-pozzhe).

**Chto NIKOGDA ne proiskhodit avtomaticheski:**

- Publikatsiya novogo obyavleniya. Novye tovary vsegda prokhodyat proverku, a potom Gotovo k sinkhronizatsii (ili vash pereklyuchatel avtopublikatsii). Vsegda.

**Temp i kontrol:**

- Kak chasto my proveryaem, opredelyaet **Interval sinkhronizatsii** na vashey stranitse Podklyuchenie. Po umolchaniyu — kazhdye 6 chasov; minimum — 60 minut.
- Ne terpitsya? Nazhmite knopku momentalnoy sinkhronizatsii na stranitse Podklyuchenie. (Raz v chas.)
- Stranitsa Podklyuchenie vsegda pokazyvaet vashu **poslednyuyu sinkhronizatsiyu**: kogda ona byla, chto sdelala (skolko sozdano / obnovleno / ubrano) i kakie tovary propustila, s prichinoy.

Esli sinkhronizatsiya propustila tovar, prichina govorit, chey eto khod: chto-to nuzhno popravit v vashem magazine, vremennaya problema, kotoraya povtoritsya sama, ili chto-to na nashey storone, gde vam nichego delat ne nuzhno.

## Dobavlenie novykh tovarov pozzhe

Eto ezhednevnaya rutina, i ona korotkaya:

1. V WooCommerce postavte vash teg na novyy tovar. Eto edinstvennoe, chto vy delaete v magazine.
2. Pri sleduyushchey sinkhronizatsii tovar poyavitsya na vashey stranitse **Novye tovary** na Oglasino.
3. Obychno u nego uzhe est kategoriya (iz vashego sopostavleniya). Pomenyayte, esli khotite, ili vyberite, esli ee net — tovar nelzya otpravit bez kategorii.
4. Nastroyte emu filtry, esli nuzhno (obyazatelnye filtry dolzhny imet znachenie).
5. Otmette tovary i nazhmite **Otpravit vybrannoe**.
6. Partiya idet na proverku. Kogda ona zavershitsya, vy poluchite uvedomlenie, a odobrennye tovary popadut v **Gotovo k sinkhronizatsii** kak obychno.

Tovary, kotorye poka nelzya otpravit, vydeleny s prichinoy pryamo v stroke — chashche vsego "snachala vyberite kategoriyu" ili problema s tegom (smotrite [Tegi: vse pravila](#tegi-vse-pravila)).

![Novye tovary zhdut vas](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-new-products.png)

## Upravlenie obyavleniyami

**Tovary magazina** — eto kazhdoe zhivoe obyavlenie, prishedshee iz vashego magazina. Otkroyte lyuboy tovar, chtoby uvidet ego deystviya: posmotret obyavlenie, otkryt ego v vashem magazine, zaprosit smenu kategorii ili pomenyat ego filtry.

![Deystviya odnogo tovara](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-product-actions.png)

S etoy stranitsy vy mozhete:

- Otkryt lyuboe obyavlenie i uvidet ego glazami pokupateley.
- **Skryt obyavlenie.** Skrytie ubiraet ego s sayta dlya pokupateley, no ono vse vremya poluchaet obnovleniya iz vashego magazina (tsena, nalichie, foto). Kogda zakhotite vernut — pokazhite ego snova, i sleduyushchaya sinkhronizatsiya vernet ego onlayn. Skrytie deystvuet na odno obyavlenie i polnostyu obratimo.
- **Zaprosit smenu kategorii** dlya tovara — smotrite sleduyushchiy razdel.

Polezno znat: obyavleniya, importirovannye iz vashego magazina, _upravlyayutsya vashim magazinom_. Tovar vy menyaete v WooCommerce — ne na Oglasino — i izmeneniya prikhodyat pri sleduyushchey sinkhronizatsii. V etom i sut: odno mesto dlya redaktirovaniya.

![Vashi zhivye obyavleniya iz magazina](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-shop-products.png)

## Smena kategorii

Kategorii — edinstvennoe, chto prokhodit proverku dazhe kogda tovar uzhe v prodazhe: kategoriya opredelyaet, gde pokupateli vas nakhodyat, poetomu nasha komanda podtverzhdaet izmeneniya. Dva vida:

**Smena kategorii odnogo tovara.** Na stranitse **Tovary magazina** otkroyte tovar i nazhmite **Zaprosit smenu kategorii**. Vyberite novuyu kategoriyu, nastroyte dlya nee filtry i vyberite, chto proiskhodit, poka zapros zhdet:

- **Skryt do resheniya** — obyavlenie ubiraetsya, poka proverka ne zavershitsya.
- **Ostavit aktivnym** — obyavlenie ostaetsya v prodazhe v tekushchey kategorii, poka proverka ne zavershitsya.

Zatem **Otpravit zapros na smenu**. Esli ego odobryat, izmenenie primenitsya avtomaticheski, i tovar vyydet (ili ostanetsya) v prodazhe. Esli otklonyat — vse ostanetsya rovno kak bylo, a prichinu vy naydete na stranitse **Problemy**. Poka zapros zhdet, tovar pomechen kak na proverke, i ego knopka smeny otklyuchena — odin otkrytyy zapros na tovar.

**Smena kategorii po umolchaniyu u sopostavleniya.** Stranitsa **Sopostavleniya kategoriy** pokazyvaet kazhduyu kategoriyu vashego magazina i ee kategoriyu Oglasino po umolchaniyu — tu, kotoruyu nasleduyut budushchie tovary.

- U stroki bez kategorii po umolchaniyu est knopka, chtoby ee zadat. Pervoe zadanie deystvuet tolko na budushchie tovary — i prokhodit korotkuyu proverku.
- U stroki s sushchestvuyushchey est **Izmenit kategoriyu po umolchaniyu**. Kogda takoe izmenenie odobreno, obnovlyayutsya i tovary, uzhe ispolzuyushchie etu kategoriyu po umolchaniyu. Tovary, kotorym vy dali sobstvennuyu kategoriyu, ne trogayutsya nikogda.
- Kategoriya po umolchaniyu, podtverzhdennaya nashey komandoy, neset metku **Podtverzhdeno**.

Poka otkryta proverka, zatragivayushchaya sopostavlenie, ego knopki otklyucheny s korotkim obyasneniem — oni ne ischezayut, prosto zhdut.

![Vashi sopostavleniya kategoriy](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-category-mappings.png)

## Filtry

Vse iz shaga s filtrami prodolzhaet rabotat i posle zapuska, i filtry mozhno menyat v lyuboy moment — **izmeneniya filtrov ne prokhodyat proverku**.

- **Filtry razdela:** na stranitse **Sopostavleniya kategoriy** u kazhdoy sektsii est knopka **Filtry razdela**. Sokhranennye tam znacheniya deystvuyut na kazhdyy tovar sektsii — krome tovarov, gde vy zadali sobstvennye znacheniya.
- **Filtry tovara:** na stranitsakh **Tovary magazina** (i **Novye tovary**) otkroyte tovar i pomenyayte ego filtry, chtoby zadat znacheniya tolko dlya nego. Vashi sobstvennye znacheniya pomecheny kak izmenennye; ikh vsegda mozhno vernut pod kontrol sektsii.
- **Obyazatelnye** filtry vsegda dolzhny imet znachenie — obyazatelnoe znachenie mozhno pomenyat, no nelzya ostavit pustym.
- Filtr _nalichiya_ avtomaticheskiy (on sleduet za ostatkami vashego magazina), i ego menyat nelzya.

Odno chestnoe zamechanie: poskolku izmeneniya filtrov ne prokhodyat proverku, est dnevnoy limit na ikh kolichestvo. On shchedryy — vy zametite ego, tolko esli chto-to na vashey storone soydet s uma i vystrelit tysyachami izmeneniy.

![Redaktirovanie filtrov sektsii](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-filter-popup.png)

## Esli chto-to otkloneno

Inogda nasha komanda otklonyaet tovar ili kategoriyu. Eto ne konets — vot kak eto rabotaet.

Vse, chto trebuet vashego vnimaniya, zhivet na odnoy stranitse: **Problemy**. Tam vy naydete:

- **Otkloneno proverkoy** — otklonennye tovary, kazhdyy s prichinoy proveryayushchego. Tovary, otklonennye vmeste kak gruppa, delyat odnu prichinu.
- **Otklonennye smeny kategoriy** — s knopkoy zaprosit smenu snova, esli khotite eshche odnu popytku.
- **Otklonennye perenosy** — smotrite [razdel o perenose](#perenos-tovara-na-drugoy-marketpleys).
- **Lishnie tegi marketpleysov** — zhivye tovary s tegom drugogo marketpleysa. Uberite lishniy teg v magazine, i eto ochistitsya samo. Poka mozhno skryt obyavlenie.
- **Propushchennye tovary** — tovary, kotorye sinkhronizatsiya ne smogla importirovat, kazhdyy s prichinoy i s tem, chey eto khod.

**Ne soglasny s resheniem?** Nazhmite **Zaprosit eshche odnu proverku**. Mozhno dobavit korotkuyu zametku dlya proveryayushchego (do 500 znakov) — obyasnite v ney, chto proveryayushchiy mog upustit. Vasha apellyatsiya idet v obychnuyu ochered proverki, i vy poluchite uvedomlenie s rezultatom. Chtoby ochered ostavalas chestnoy, tu zhe veshch mozhno obzhalovat snova tolko cherez neskolko dney.

Esli otklonena tselaya vasha _kategoriya_, ee tovary snimayutsya s marketpleysa vmeste — i vmeste vozvrashchayutsya, esli reshenie otmenyat. Vam ne nuzhno nichego delat po kazhdomu tovaru.

![Stranitsa Problemy](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/ru/app-issues.png)

## Perenos tovara na drugoy marketpleys

Prodaete na obshchem marketpleyse to, chemu mesto na moto-marketpleyse (ili naoborot)? Prosto pomenyayte teg v magazine:

1. V WooCommerce uberite teg starogo marketpleysa i dobavte teg drugogo.
2. Pri sleduyushchey sinkhronizatsii tovar poyavitsya v razdele perenosov na vashey stranitse **Problemy**.
3. Vyberite emu kategoriyu **na novom marketpleyse** i otpravte perenos — perenos proveryaetsya kak novyy tovar.
4. Vashe zhivoe obyavlenie **ostaetsya v prodazhe** na starom marketpleyse vse eto vremya. Nichego ne ischezaet, poka vy zhdete.
5. Kogda perenos odobren, vy publikuete ego kak lyuboy odobrennyy tovar (Gotovo k sinkhronizatsii ili avtopublikatsiya). Obyavlenie pereezzhaet — so svoimi otzyvami, izbrannym i soobshcheniyami.

Menyaetsya odno: veb-adres obyavleniya, potomu chto ono teper zhivet na drugom marketpleyse. Starye ssylki na nego perestanut rabotat. Esli perenos vse-taki ne nuzhen — vernite staryy teg, i gotovo.

## Tegi: vse pravila

Teg — eto vash rul. Vot chto delaet kazhdoe izmenenie tega, odnoy tablitsey:

| Vy delaete eto v svoem magazine                                    | Eto proiskhodit na Oglasino                                                                                                       |
| ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| Dobavlyaete vash teg tovaru                                        | On poyavlyaetsya v **Novye tovary** i zhdet otpravki na proverku                                                                  |
| Ubiraete teg s zhivogo obyavleniya                                 | Obyavlenie srazu ukhodit oflayn. Nichego ne udalyaetsya — vash tovar, vashe reshenie                                              |
| Vozvrashchaete teg                                                 | Obyavlenie vozvrashchaetsya onlayn pri sleduyushchey sinkhronizatsii                                                              |
| Menyaete odin svoy teg na drugoy dlya _togo zhe_ marketpleysa      | Nichego ne menyaetsya                                                                                                             |
| Tovar neset neskolko tegov odnogo marketpleysa                     | Normalno — schitaetsya lyuboy iz nikh                                                                                             |
| Menyaete teg na teg _drugogo_ marketpleysa                         | Tovar idet cherez perenos ([smotrite vyshe](#perenos-tovara-na-drugoy-marketpleys))                                               |
| Dobavlyaete zhivomu obyavleniyu _lishniy_ teg drugogo marketpleysa | Obyavlenie ostaetsya na meste i obnovlyaetsya, no vy poluchaete zapis v **Problemy** — uberite lishniy teg, chtoby ochistit       |
| Daete _novomu_ tovaru tegi oboikh marketpleysov                    | On zhdet v **Novye tovary** s pometkoy "ispravte teg" — ego nelzya otpravit, poka ne ostanetsya odin marketpleys                  |
| Polnostyu udalyaete tovar iz WooCommerce                           | Ego obyavlenie na Oglasino tozhe udalyaetsya. Esli pozzhe vy sozdadite ego v magazine zanovo, on nachnet snachala kak novyy tovar |

## Pauza ili zakrytie podklyucheniya

**Pauza** (na stranitse Podklyuchenie) polnostyu ostanavlivaet sinkhronizatsiyu — nichego ne obnovlyaetsya, nichego ne obnaruzhivaetsya — poka vy ee ne snimete. Vashi obyavleniya ostayutsya kak est. Ispolzuyte ee dlya otpuska ili rabot v magazine.

Esli vashi dannye dostupa perestali rabotat (naprimer, klyuch udalen v WooCommerce), podklyuchenie samo stanovitsya na pauzu i soobshchaet vam — vvedite klyuchi zanovo i povtorite proverku, chtoby prodolzhit.

**Zakrytie podklyucheniya** zavershaet vse. Poskolku vashi obyavleniya vazhny, pri zakrytii vsegda sprashivaetsya, chto s nimi delat — vy vybiraete odno iz trekh:

- **Ostavit moi obyavleniya** — oni ostayutsya na Oglasino i stanovyatsya obychnymi obyavleniyami, kotorye vy redaktiruete sami; oni bolshe ne svyazany s magazinom.
- **Deaktivirovat moi obyavleniya** — oni skryty i otvyazany; pozzhe ikh mozhno snova aktivirovat i redaktirovat.
- **Udalit moi obyavleniya** — oni ubirayutsya s Oglasino, i ikh foto udalyayutsya.

Zakrytie podtverzhdaetsya vvodom zaproshennogo slova — sluchayno eto ne sdelat.

## Limity i pravila

Vse v odnom meste, bez syurprizov:

- **Razreshenie API-klyucha:** vsegda **Read**. Oglasino nikogda ne pishet v vash magazin.
- **Adres magazina:** dolzhen nachinatsya s `https://`.
- **Odin marketpleys na tovar.** Tegi tovara opredelyayut ego marketpleys, i on mozhet byt tolko odin.
- **Interval sinkhronizatsii:** minimum 60 minut; po umolchaniyu — kazhdye 6 chasov.
- **Ruchnaya sinkhronizatsiya:** raz v chas.
- **Povtor propushchennykh tovarov:** do 10 tovarov v chas.
- **Limit chisla tovarov:** obychno ego net. Oglasino mozhet zadat verkhnyuyu granitsu, skolko tovarov mozhet importirovat podklyuchenie; esli granitsa kasaetsya vas, ona pokazana na vashey stranitse Podklyuchenie, a tovary sverkh nee popadayut v propushchennye.
- **Zametka k apellyatsii:** do 500 znakov (i ona neobyazatelna).
- **Nazvaniya i opisaniya:** slishkom dlinnye avtomaticheski sokrashchayutsya pod format obyavleniya — nazvaniya do 80 znakov, opisaniya do 2000.
- **Izmeneniya filtrov:** bez proverki, no deystvuet shchedryy dnevnoy limit.
- **Valyuta magazina:** valyuta vashego magazina dolzhna podderzhivatsya marketpleysom — pri podklyuchenii my skazhem, esli eto ne tak.

## Nuzhna pomoshch?

Napishite nam na **support@oglasino.com** — ukazhite adres vashego magazina i chto vy pytalis sdelat, i my razberemsya vmeste s vami.
