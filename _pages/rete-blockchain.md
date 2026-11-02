---
layout: single
title: "Rete blockchain: una rete tipo TRON, costruita su software già esistente"
permalink: /startup/rete-blockchain/
ref: rete-blockchain
author_profile: false
seo_description: "Idea in studio: una rete blockchain per pagamenti e startup crypto, ispirata a TRON ma costruita partendo da software con licenze permissive."
---

<p class="hub-lead"><span class="hub-tag">Idea in studio</span> Una rete blockchain nostra, pensata per pagamenti veloci a costo basso e per ospitare le startup di questo sito. Prendiamo spunto da TRON, ma non partiamo da zero e non copiamo a caso: partiamo da software già pronto con licenze semplici.</p>

## Cosa fa TRON (e cosa ci interessa)
Secondo la documentazione ufficiale, TRON usa un sistema a **delegated proof of stake**: chi possiede TRX li blocca, ottiene potere di voto e vota i **27 Super Representative**, che producono i blocchi a turno. Gli smart contract girano su una macchina virtuale compatibile con quella di Ethereum (TVM). Le risorse non si pagano solo a commissione: esistono **Bandwidth** (per i trasferimenti) ed **Energy** (per i contratti), che si ottengono bloccando token oppure bruciandoli al momento.

Da qui prendiamo tre idee:
1. **Pochi validatori noti che si alternano**: veloce e prevedibile, meno decentralizzato di Bitcoin o Ethereum.
2. **Compatibilità con gli strumenti di Ethereum**: wallet, librerie e contratti già esistenti funzionano.
3. **Risorse a quota**: chi usa poco la rete paga poco o niente, chi la usa molto blocca valore. Utile per i pagamenti.

## Il nodo licenze: perché non copiamo TRON
Il codice di TRON (java-tron) è pubblico ma sotto **LGPLv3**. Si può usare, però le modifiche al codice coperto dalla licenza vanno rese pubbliche alle stesse condizioni, con obblighi su avvisi e licenza. Per un progetto che vuole poi vendere servizi e tenere qualcosa di proprietario è un vincolo da capire bene. Anche il nome e il marchio TRON non sono nostri: non si usano. Wikipedia riporta inoltre una contestazione sul rispetto della LGPL da parte del progetto TRON verso EthereumJ: motivo in più per non costruire sopra una base dalla storia di licenze discussa senza una verifica legale.

## Quattro strade, dalla più semplice alla più complessa
| Strada | Cosa si prende | Licenza | Verifica |
|---|---|---|---|
| **A. Rete EVM su Reth** | Nodo Ethereum scritto in Rust, modulare, usabile come libreria | Apache-2.0 e MIT (permissive) | Confermata sul repository |
| **B. Rete con Cosmos SDK e CometBFT** | Blockchain con validatori a rotazione, simile a TRON per idea | Apache-2.0 (a quanto risulta) | Da verificare sul repository |
| **C. Fork di go-ethereum** | Il nodo Ethereum più diffuso | Libreria LGPL, programmi GPL (a quanto risulta) | Da verificare: licenze con obblighi |
| **D. Fork di java-tron** | La vera rete TRON | LGPLv3 | Confermata sul repository |

Come regola: **Apache-2.0 e MIT** sono le più comode (si può anche chiudere il proprio codice, mantenendo avvisi e licenza). **LGPL e GPL** impongono di pubblicare le modifiche. Alcuni progetti usano poi licenze "business source" che limitano l'uso commerciale: prima di adottare qualsiasi codice, si legge il file LICENSE della versione che si usa.

## Cosa proponiamo
**Strada A come prima scelta.** Una rete compatibile con Ethereum costruita su Reth, con pochi validatori a rotazione come TRON, e le risorse a quota solo se servono. Motivi: licenze permissive, strumenti già pronti, nessun bisogno di scrivere un nodo da zero. La strada B resta l'alternativa se ci serve una rete con regole molto personalizzate.

## Come procediamo, a fasi
1. **Rete di prova locale**: avviamo un nodo e pochi validatori sul nostro computer, nessun valore reale.
2. **Rete di prova pubblica** con 3-5 validatori scelti da noi, per i primi test di pagamento.
3. **Registro e pagamenti dei nostri progetti**: usiamo la rete per [Registro immutabile]({{ '/startup/registro-immutabile/' | relative_url }}) e [Rete fisica]({{ '/startup/rete-fisica/' | relative_url }}).
4. **Apertura ad altri validatori e sviluppatori**, solo dopo audit di sicurezza e parere legale.

## Cosa può offrire la rete
- Pagamenti e trasferimenti di stablecoin a costo ridotto.
- Spazio per le startup crypto di questo sito: contratti, registri e prove con data certa.
- Strumenti per sviluppatori: documentazione, wallet e faucet di prova.
- Servizi per chi vuole lanciare la propria app senza gestire un nodo.

## Come potremmo guadagnare
Commissioni sui servizi che costruiamo sopra la rete, abbonamenti per chi usa il registro e i pagamenti, assistenza a chi vuole avviare una sua rete. Prezzi non definiti. Nessun token da vendere per partire.

## Rischi e regole da verificare
- **Sicurezza**: una blockchain gestisce valore reale. Servono audit esterni e un periodo di prova lungo prima di aprirla.
- **Licenze**: parere di un avvocato esperto di software libero sulla combinazione finale di componenti.
- **Token e vendita**: emettere o vendere un token può rientrare in regole come MiCA e in quelle italiane. Per ora non si emette niente.
- **Antiriciclaggio**: reti veloci e a basso costo attirano anche usi illeciti; servono regole chiare e collaborazione con le autorità. Vedi gli [articoli di Crypto Magazine](https://cialdecompatibili-netizen.github.io/cryptomagazine/blog/) su come i flussi illeciti passano da un servizio all'altro.
- **Concorrenza**: esistono già molte reti simili. La nostra possibile differenza è un uso preciso (registri e pagamenti per piccole imprese italiane), non essere "un'altra TRON".

## Stato
Idea in studio: nessuna rete attiva, nessun token in vendita e nessuna promessa di rendimento. Se vuoi entrare con tempo o capitale, leggi la pagina [Investi]({{ '/investi/' | relative_url }}).

<p><a class="hub-btn hub-btn--a" href="{{ '/investi/?startup=rete-blockchain' | relative_url }}">Investi</a> <a class="hub-btn hub-btn--o" href="{{ '/lavora-con-noi/?startup=rete-blockchain' | relative_url }}">Candidati</a></p>
