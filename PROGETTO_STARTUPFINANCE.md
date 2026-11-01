# startupfinance - progetto: hub di idee, imprenditori e startup in fase iniziale

Repo `cialdecompatibili-netizen/startupfinance`, cartella `C:\Users\mirco\Desktop\repository\startupfinance`. Clone di mistraltemplate1 (guida tecnica in `CLAUDE.md`). Il tema crypto e' stato tolto e vive in `cryptomagazine`.

## Idea (da Mirco, 1/11/2026)
Non e' solo un blog: e' un **ecosistema** con tre livelli collegati.

1. **Blog di startup**: guide, storie di imprenditori, casi reali, come si parte e come si scala.
2. **Blog di finanza**: come si finanzia una startup (bootstrapping, business angel, venture capital, crowdfunding, bandi), numeri, regole, rischi.
3. **Le startup che vogliamo realizzare noi**: uno spazio dedicato dove presentiamo le idee/progetti in costruzione, collegati ai due blog.

Sopra questi tre livelli ci sono **due percorsi di azione** per chi arriva sul sito:
- **Bottone "Investitore"**: per chi vuole sostenere o finanziare le startup.
- **Bottone "Candidati"**: per chi vuole entrare nel progetto (imprenditore, sviluppatore, collaboratore, socio).

Obiettivo: un **hub** dove idee, imprenditori, startup in fase iniziale e investitori si incontrano. Il blog porta traffico e credibilita', le startup sono il prodotto, i due bottoni sono la conversione.

## Logica del sito
```
Lettore -> blog (startup + finanza) -> scopre le startup del progetto -> sceglie: investire oppure candidarsi
```
Ogni articolo, quando pertinente, rimanda alla startup collegata e ai due bottoni. Ogni startup ha la sua pagina con stato, team, obiettivo, cosa cerca e i due bottoni.

## Menu (proposta, da confermare)
Voci principali in `_data/navigation.yml`, tendine in `_data/sottomenu.yml` (chiave = `title` identico):

- **Blog** > Startup / Finanza / Storie di imprenditori
- **Le nostre startup** > elenco (una pagina per startup) / come le scegliamo
- **Investitori** (pagina dedicata con modulo)
- **Candidati** (pagina dedicata con modulo)
- **Chi siamo**
- **Contatti**

I due bottoni **Investitore** e **Candidati** devono essere sempre visibili (header o fascia fissa), distinti dal resto del menu, e portare ognuno a una pagina con spiegazione chiara + modulo. Il contatto passa da `contact_endpoint` (vedi `docs/RICETTE.md`).

## Struttura contenuti prevista
- Categorie articoli: `Startup`, `Finanza`, `Storie` (+ lingua EN con `ref:` collegato).
- Pagine: `startup/` (elenco) e una pagina per ogni startup, `investitori`, `candidati`.
- Home a blocchi (`_data/blocks_home.json`): hero con i due bottoni, ultimi articoli, startup in evidenza, come funziona, contatti. Fascia numeri solo se ci sono dati veri con fonte.

## Regole editoriali
- Dati e cifre solo verificati, sempre con la fonte (come in cryptomagazine); niente numeri inventati.
- Finanza: contenuti informativi, non consulenza. Nessuna promessa di rendimento.
- Pagina investitori: niente sollecitazione al pubblico risparmio ne' rendimenti garantiti. Prima di pubblicare i testi su raccolta di capitale va verificato il quadro normativo (da fare).
- Terminologia chiara, senza gergo inutile; IT + EN.
- Design: niente bordi laterali colorati; kit blocchi del template.

## Stato (1/11/2026)
Fatto: home, Servizi e Chi siamo con testi reali IT+EN, tema crypto rimosso.
Da fare, in ordine:
1. Decidere nomi e struttura del menu (sezione sopra) e aggiornare `navigation.yml` / `sottomenu.yml`.
2. Pagine `investitori` e `candidati` con modulo.
3. Sezione "Le nostre startup" + prima pagina startup (serve sapere quale).
4. Primi 2-3 articoli veri (startup + finanza) IT+EN, verificati sulle fonti.
5. Home: hero con i due bottoni, card ultimo articolo.
6. Pulizia pagine del template non usate (negozio, carrello, ordine) se non servono.

## Da decidere con Mirco
- Quali startup presentare per prime e che stato hanno (idea, in sviluppo, attiva).
- Cosa chiede il modulo investitore e quello candidati (campi, dove arrivano le email).
- Nome definitivo del sito/brand.
