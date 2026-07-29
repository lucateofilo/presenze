# Presenze

PWA single-file per il tracciamento presenze personale. Gira interamente nel browser, nessun server, nessun account.

**[→ Apri l'app](https://lucateofilo.github.io/presenze/)**

---

## Funzionalità

**Timbratura**
- Pulsante ENTRA / ESCI con selezione sito (B / N)
- Banner "in corso" con orario di avvio
- Timbratura manuale dal registro (aggiunta / modifica / eliminazione con undo)

**Registro**
- Statistiche giornaliere, settimanali e mensili
- Calendario mensile con ore per ogni giorno
- Dettaglio giorno: modifica orari, sito, note, stato pagamento

**Pagamenti**
- Metodo 1 — a ore (soglia ore standard + straordinari)
- Metodo 2 — a giornata fissa
- Modal pagamento con selezione delle giornate da saldare

**Diario**
- Note personali per data
- Lista cronologica con anteprima della prima riga
- Banner promemoria backup settimanale

**Export**
- Un solo file Excel con due fogli: Presenze + Diario
- Libreria SheetJS caricata solo al momento dell'export

---

## Stack

- HTML + CSS + JS vanilla, tutto in un singolo `index.html`
- `localStorage` per la persistenza dei dati
- [SheetJS](https://sheetjs.com/) (CDN lazy) per l'export Excel
- GitHub Pages per il deploy

---

## Dati locali

Tutto rimane sul dispositivo. Nessun dato viene inviato a server esterni.

| Chiave localStorage | Contenuto |
|---|---|
| `pr_records` | Array timbrature |
| `pr_stato` | Timbratura in corso |
| `pr_cfg` | Impostazioni pagamento |
| `pr_diary` | Note del diario |
| `pr_diary_export` | Timestamp ultimo backup |

---

## Installazione su telefono

Apri `https://lucateofilo.github.io/presenze/` da Safari (iOS) o Chrome (Android) e usa "Aggiungi a schermata Home".
