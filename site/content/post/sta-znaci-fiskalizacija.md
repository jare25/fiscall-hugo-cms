---
title: Elektronska fiskalizacija
date: 2020-12-27T22:58:00.921Z
description: Prema novim pravilima, svaki poreski obveznik koji je obavezan da
  izdaje račune i vrši proces fiskalizacije, obavezan je po zakonu da
  fiskalizuje sve račune za gotovinske i bezgotovinske transakcije.
image: img/hphone.png
---
Fiskalizacija znači da se svi izdati računi, kako gotovinski tako i bezgotovinski, evidentiraju u bazi podataka Poreske uprave. Fiskalizacija računa se vrši fiskalnim servisom koji je odgovoran za komunikaciju između poreskih obveznika, koji izdaju račune i Poreske uprave, koja obrađuje primljene poruke.

### **Ko su obveznici fiskalizacije?**

Obveznik fiskalizacije je:

1. fizičko lice koje je obveznik poreza na dohodak i obveznik je izdavanja računa za isporuku proizvoda, odnosno usluga
2. pravno lice koje je obveznik poreza na dobit u skladu sa zakonom kojim se uređuje porez na dobit pravnih lica i koje je obveznik izdavanja računa za isporuku proizvoda, odnosno usluga
3. poreski obveznik koji ostvaruje promet od prodaje roba ili usluga putem samonaplatnih uređaja (automata), a koji nije u obavezi izdavanja računa u skladu sa zakonom kojim se uređuje porez na dodatu vrijednost.

Obveznikom fiskalizacije ne smatraju se obveznici koji ostvaruju promet od:

1. prodaje karata ili žetona u linijskom putničkom saobraćaju i naplate prtljaga
2. prodaje poljoprivrednih proizvoda na pijačnim tezgama i ostalim otvorenim prostorima na kojima je omogućena prodaja na otvorenom, proizvedenih na sopstvenom poljoprivrednom gazdinstvu
3. otkupa poljoprivrednih proizvoda od strane obveznika poreza na dodatu vrijednost kod poljoprivrednih proizvođača
4. univerzalnih poštanskih usluga
5. pružanja bankarskih usluga i usluga osiguranja i reosiguranja
6. uplata za učestvovanje u igrama na sreću i zabavnim igrama
7. prodaje roba u avionima na letovima nacionalnog avio prevoznika.

### **Obaveze poreskih obveznika?**

Obveznici fiskalizacije, dužni su da nabave nove moderne elektronske naplatne uređaje (ENU) i da ih registruju kod Poreske uprave.

Pored toga, svi elektronski naplatni uređaji (ENU) će morati elektronski da se povežu sa PU, što će zahtijevati njihovu promjenu ili nadogradnju.

### **Kako sve funkcioniše?**

Proces razmjene podataka počinje kada operator treba da na elektronskom naplatnom uređaju (ENU) izda račun klijentu. Nakon što operator popuni sve elemente računa i na osnovu toga izračunava Identifikacioni kod obveznika fiskalizacije (IKOF) u skladu sa algoritmom opisanim u Pravilniku.

Poslije toga, on priprema XML poruku sa zahtjevom i elektronski potpisuje pomoću privatnog ključa aplikacionog certifikata koji je registrovani davalac usluge (CA) izdao poreskom obvezniku za potrebe fiskalizacije.

Sistem Poreske uprave dobija potpisanu XML poruku i verifikuje digitalni potpis i strukturu XML poruke. Ako je poruka prošla validaciju, pohranjuje se u bazi podataka fiskalizovanih računa (kao podatak i poruka u punom XML formatu).

Kada se XML poruka pohrani, Centralni informacioni sistem Poreske uprave (CIS) kroz fiskalni servis kreira odgovor sa jedinstvenim identifikacionim kodom računa (JIKR). Odgovor se potpisuje digitalnim certifikatom Poreske uprave i šalje elektronskom naplatnom uređaju (ENU) poreskog obveznika. Nakon što ENU dobije odgovor Poreske uprave, poreski obveznik je dužan da odmah odštampa gotovinski račun sa JIKR dobijenim od Poreske uprave i da odštampani račun preda ili dostavi klijentu.

### **Kad nije obveznik PDV-a**

U slučajevima kada poreski obveznik nije u sistemu PDVa, on može da kreira i fiskalizuje svoje gotovinske račune koristeći samouslužni EFI portal (SEP) Poreske uprave.

U toj situaciji on ne mora da posjeduje elektronski naplatni uređaj (ENU), već samo kompjuter ili tablet ili pametni telefon koji će koristiti da ostvari pristup SEP-u putem internet veze. Poreski obveznik će moći da ostvari pristup SEPu koristeći digitalni certifikat koji mu je izdalo Registrovani CA ili druge definisane načine autentifikacije.

Kada CIS kreira kod za poslovni prostor i kod za operatora, ti kodovi se čuvaju u bazi podataka na korisničkom nalogu poreskog obveznika na SEPu. Nakon toga, on može da kreira novi račun na SEP-u tako što odabere tu opciju na meniju SEP-a. Biće kreiran model pojednostavljenog računa sa unaprijed popunjenim postojećim podacima iz Registra poreskih obveznika koji vodi Poreska uprava. Poreski obveznik će morati da unese sve druge obavezne elemente podataka, u skladu sa shemom. Kada popuni podatke, potvrđuje ih i šalje servisu za fiskalizaciju (u SEPu). Kada se završi proces fiskalizacije, podaci će se sačuvati u bazi podataka a CIS će kreirati odgovor sa JIKR. Taj odgovor će biti potpisan digitalnim certifikatom Poreske uprave i poslat poreskom obvezniku i automatski sačuvan na kreiranom računu i u folderu fiskalizovanih računa na njegovom korisničkom nalogu u SEP-u. Nakon što se dobije odgovor, poreski obveznik mora odštampati gotovinski račun sa JIKR i taj račun dati klijentu ili poslati na njegov mejl, uz njegovu saglasnost u određenim situacijama propisanim zakonom.