<!--
PREDLOŽAK — README završnog projekta na kolegiju Programsko inženjerstvo FER-a.
Kopirajte ovu datoteku u README.md u repozitoriju svojeg projekta. Zamijenite
svaku uputu u uglatim zagradama činjenicama o svojem projektu, uklonite sve
komentare s uputama i ogledne <details> blokove te prije predaje izbrišite ovu
napomenu. Nemojte kopirati nastavni primjer kao rezultat svojeg projekta.
-->

# [TradeIt]

**Najam predmeta i opreme od ljudi u blizini.** TradeIt povezuje vlasnike predmeta s osobama kojima su oni privremeno potrebni te objedinjuje pronalazak, dogovor najma, evidenciju stanja i korisničku podršku.

**Projekt na kolegiju:** Ovu je aplikaciju razvio studentski tim u sklopu kolegija [Programsko inženjerstvo](https://www.fer.unizg.hr/predmet/proinz) na Fakultetu elektrotehnike i računarstva Sveučilišta u Zagrebu (FER).

## Opis aplikacije

Osobi kojoj jednom treba grafički kalkulator, alat ili kamera kupnja može biti nepotrebna, a pronalazak najmodavca zahtijeva dogovor na više mjesta. TradeIt predlaže katalog najma s cijenama i raspoloživosti, dogovorom između korisnika te fotografijama pri preuzimanju i povratu. Očekivana korist je lakša ponovna uporaba predmeta; ušteda vremena, novca ili utjecaj na okoliš još nisu mjereni.

**Ključne funkcionalnosti**

- Mogućnost objavljivanja objekta ili usluge za najam
- Mogućnost pregleda objava
- Mogućnost iznajmljivanja traženog predmeta ili usluge

Za potpuni opseg, zahtjeve, oblikovanje i dokaze ispitivanja pogledajte [docs](docs/Home.md).

<a id="deployment"></a>

## Postavljanje (engl. deployment)

<!-- UPUTA: Ovaj odjeljak opisuje već postavljenu aplikaciju koju se  može otvoriti i isprobati bez lokalnog pokretanja izvornog koda.
Za Iteraciju 1 i Završni pregled navedite konkretne podatke. Provjerite vodi li URL na javno dostupnu pokrenutu aplikaciju i radi li navedeni tijek uporabe. Nikada ne objavljujte lozinke ni pristupne tokene. -->

**Javno dostupna aplikacija:** [Javni URL]

**Isprobajte:** [Jedna ili dvije kratke radnje koje pokazuju funkcionalan korisnički tijek.]

**Demonstracija:** [Objasnite kako dobiti potreban ograničeni pristup ako je prijava obavezna; u suprotnom napišite „Korisnički račun nije potreban.” Ovdje ne objavljujte lozinke ni pristupne tokene.]

**Ograničenja:** [Kratko navedite ograničenja postavljene inačice ili postavite poveznicu na jedinstveno mjerodavno mjesto u dokumentaciji s poznatim problemima.]

[Vodič za postavljanje i pokretanje](docs/6-Postavljanje-instalacija-i-konfiguracija.md) opisuje smještaj aplikacije (engl. hosting) koji tim stvarno koristi. Tim može koristiti Render ili drugu platformu koju ste dogovorili s asistentom/demonstratorom.

<a id="quick-start"></a>

## Brzi početak / instalacija

<!-- Obavezno od Demo 1 nadalje. Zamijenite mjesta za unos naredbama koje je drugi član tima uspješno provjerio nakon čistog kloniranja repozitorija. Detaljne upute za administraciju držite u projektnoj dokumentaciji u direktoriju docs/. -->

**Preduvjeti:** [Navedite potrebno izvršno okruženje (engl. runtime) i verzija, upravitelj paketa (engl. package manager), baza podataka ili vanjska usluga ako je nužna.]

```bash
git clone [repository URL]
cd [repository directory]
[install dependencies]
[run the application]
```

**Adresa:** [Stvarna adresa koju aplikacija ispiše nakon pokretanja.]

**Konfiguracija:** [Navedite potrebne varijable okruženja (engl. environment variables) ili uputite na sigurnu datoteku `.env.example`; objasnite gdje se dobivaju vrijednosti. Nikada ne stavljajte stvarne pristupne podatke u ovu datoteku, primjer konfiguracije, snimke zaslona, zapise ni zapise promjena (engl. commits).]

[Dodajte kratak korak provjere, primjerice koja se stranica treba otvoriti ili koja naredba pokreće osnovnu provjeru.] Za detaljno postavljanje pogledajte [projektnu dokumentaciju](docs/Home.md).

## Tehnologije

| Tehnologija ili alat               | Uloga                                                  | Status i razlog                                                              |
| ---------------------------------- | ------------------------------------------------------ | ---------------------------------------------------------------------------- |
| HTML5, CSS, JavaScript             | Zasloni, stilovi, navigacija i lokalne interakcije     | Planirani klijentski dio; raniji dizajn još nije prenesen u ovaj repozitorij |
| Node.js i npm                      | Izvođenje oglednog poslužitelja i naredbi iz predloška | Postojeći npm testovi samo ispisuju poruke; jsdom testovi nisu u ovom ZIP-u  |
| Python + FastAPI                   | Planirani HTTP API i poslovna pravila                  | Prijedlog za raspravu; API još nije implementiran                            |
| PostgreSQL                         | Planirana zajednička pohrana i integritet rezervacija  | Prijedlog; shema i migracije još nisu primijenjene                           |
| SQLAlchemy + Alembic               | Planirano preslikavanje modela i migracije             | Uvesti uz prvi vertikalni tijek API-ja                                       |
| OAuth/OIDC, Google Maps, AI servis | Planirane prijava, lokacija i provjera oglasa          | Vanjske integracije još nisu povezane; pružatelje i troškovnik potvrditi     |
| GitHub + GitHub Actions            | Verzije, pregled promjena i automatizirane provjere    | Repozitorij je naveden; workflow je predložak bez stvarne testne provjere    |

<a id="team-members"></a>

## Članovi tima

| Član            | Oznaka | Glavna uloga ili doprinos      | Prvi konkretan zadatak                                            |
| --------------- | ------ | ------------------------------ | ----------------------------------------------------------------- |
| Adam Winkler    | R1     | Frontend i UI                  | Povezati katalog s budućim API-jem; provjeriti prikaz na mobitelu |
| Leon Zorko      | R2     | Dokumentacija i koordinacija   | Potvrditi zahtjeve, održavati issues i stvarne zapisnike          |
| Patrik Šinko    | R3     | Baza podataka                  | Model korisnika, oglasa i rezervacija te početne migracije        |
| Pavao Knez      | R4     | Autentikacija i AI             | OIDC prijava, serverske ovlasti; zatim AI provjera oglasa         |
| Viktor Lazić    | R5     | Vanjske usluge                 | Pohrana fotografija i integracija lokacije                        |
| Lukas Davorija  | R6     | API i integracija              | Katalog, ponuda cijene i zahtjev za najam                         |
| Matej Miličević | R7     | Deploy, testiranje i fullstack | CI, razvojna okolina i prvo postavljanje                          |

## Doprinos projektu

Za praćenje zadataka navedena je Jira ploča ispod. GitHub sadrži izvorni kod i dokumentaciju. Predloženo je povezivati promjene sa zadacima i provesti pregled drugog člana prije spajanja; stvarni ritam i pravila tim tek treba evidentirati u [pregledu aktivnosti](docs/CONTRIBUTING.md).

Poveznica na Jiru: https://trade-it.atlassian.net/jira/software/projects/SCRUM/summary

<a id="license"></a>

**Status licence:** Nije dodjeljena licenca koja dopušta javnu ponovnu uporabu.

<a id="ai-usage"></a>

## Uporaba umjetne inteligencije [![AI Usage: Disclosed](https://img.shields.io/badge/AI%20Usage-Disclosed-blue.svg)](https://www.fer.unizg.hr/_download/repository/Policy%20on%20the%20appropriate%20use%20of%20artificial%20intelligence%20at%20the%20faculty%20of%20electrical%20engineering%20and%20computing%5B1%5D.pdf)

Ovaj projekt slijedi FER-ova [pravila o primjerenoj uporabi umjetne inteligencije](https://www.fer.unizg.hr/_download/repository/Policy%20on%20the%20appropriate%20use%20of%20artificial%20intelligence%20at%20the%20faculty%20of%20electrical%20engineering%20and%20computing%5B1%5D.pdf).

**Izjava:** [Navedite jesu li korišteni alati umjetne inteligencije. Ako jesu, navedite alate i njihove glavne namjene te objasnite kako je tim pregledao nastali kod ili tekst i kako može objasniti vlastiti doprinos. Ako nisu korišteni, to jasno navedite. U alate umjetne inteligencije nemojte unositi privatne podatke, pristupne podatke ni tuđe zaštićene materijale.]

[Ako je za ovaj projekt potreban detaljniji zapis uporabe umjetne inteligencije, postavite poveznicu na njegovo jedinstveno mjerodavno mjesto u dokumentaciji.]

<a id="code-of-conduct-and-support"></a>

## Kodeks ponašanja i podrška [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)

Od članova tima očekuje se pridržavanje **Kodeksa ponašanja studenata** Fakulteta elektrotehnike i računarstva Sveučilišta u Zagrebu, pravila timskog rada na kolegiju i [Etičkog kodeksa IEEE-a](https://www.ieee.org/about/corporate/governance/p7-8.html). [Postavite poveznicu na `CODE_OF_CONDUCT.md` ako se ta datoteka koristi u vašem repozitoriju.]

---

Struktura dokumentacije prilagođena je predlošku kolegija Programsko inženjerstvo FER-a autora [Vlade Sruka](https://www.fer.unizg.hr/vlado.sruk), licenciranom pod [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). Aplikaciju i njezin sadržaj izradio je gore navedeni studentski tim.
