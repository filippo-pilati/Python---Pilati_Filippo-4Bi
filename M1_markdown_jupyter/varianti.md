# Le varianti di Markdown a confronto

## Tabella di confronto

| Costrutto                  | Markdown originale | CommonMark | GitHub Flavored Markdown |
|:---------------------------|:------------------:|:----------:|:------------------------:|
| Blocchi di codice recintati | No (solo rientro)  | Sì         | Sì                       |
| Tabelle                    | No                 | No         | Sì                       |
| Caselle di spunta          | No                 | No         | Sì                       |
| Testo barrato              | No                 | No         | Sì                       |
| Collegamenti automatici    | Solo con `<...>`   | Solo con `<...>` | Sì, anche senza parentesi |
| Note a piè di pagina       | No                 | No         | Sì (su GitHub)           |

## Esempi delle estensioni di GitHub

Caselle di spunta:

- [x] Creare il repository
- [x] Clonare il repository
- [ ] Scrivere il file `postazione.md`
- [ ] Scrivere il file `compilare.md`
- [ ] Controllare l'anteprima
- [ ] Fare il push

Testo barrato: la versione ~~Git 2.2x~~ è superata, si usa Git 2.4x.

Collegamento automatico: https://github.github.com/gfm/

## Quale variante usare

Per le consegne del corso conviene usare GitHub Flavored Markdown, perché i file vengono letti su GitHub e le consegne usano tabelle, caselle di spunta e diagrammi che CommonMark non definisce. GFM è un'estensione di CommonMark: ogni documento CommonMark valido resta valido, quindi non si perde nulla. Se questo stesso file viene aperto con uno strumento che implementa solo CommonMark, la tabella compare come righe di testo separate da barre verticali. Le caselle di spunta diventano normali voci di elenco con le parentesi quadre in vista, e il testo barrato mostra le tilde. L'indirizzo scritto per esteso resta testo non cliccabile. Le differenze nell'anteprima di Visual Studio Code vanno annotate qui dopo la prova.
