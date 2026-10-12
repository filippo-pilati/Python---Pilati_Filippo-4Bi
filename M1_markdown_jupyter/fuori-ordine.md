# Notebook eseguito fuori ordine

## Ordine reale di esecuzione

Le celle sono state eseguite nell'ordine `[1]`, `[2]`, `[3]`, `[4]`, cioè: la cella con `iscritti = 22` (ultima nel file), poi quella con `aula` e `posti = 24` (prima nel file), poi la cella con `liberi` (terza), infine quella con `posti = posti - 2` (seconda). Lo si deduce dai numeri fra parentesi quadre, che crescono con l'ordine di esecuzione e non con la posizione nel file.

## Perché `[4]` mostra 22 e `[3]` ha calcolato con 24

La cella `[3]` è stata eseguita prima della `[4]`: in quel momento `posti` valeva ancora `24`, quindi `24 - 22 = 2`. Solo dopo la cella `[4]` ha sottratto 2 a `posti`, portandola a `22`. Il kernel conserva lo stato in memoria, per cui ogni cella vede i valori lasciati dalle celle eseguite prima di essa nel tempo.

## Output dopo Restart Kernel and Run All Cells

Le celle vengono eseguite dall'alto in basso. La seconda cella del file (`[4]`) funziona, la terza (`[3]`) si ferma con un errore e l'ultima cella (`[1]`) non viene eseguita affatto.

```text
Posti disponibili: 22
```

La cella con `print(aula, ...)` non stampa nulla perché genera un errore. La cella `iscritti = 22` non viene eseguita, quindi non stampa `Iscritti: 22`.

## La cella che produce errore

La cella che calcola `liberi` usa `iscritti`, che a kernel appena avviato non esiste ancora:

```text
NameError: name 'iscritti' is not defined
```

## Correzione

Basta spostare la cella con `iscritti = 22` e la sua `print` in cima al notebook, prima di tutte le altre. Dall'alto in basso l'output diventa:

```text
Iscritti: 22
Posti disponibili: 22
Laboratorio 3 - liberi: 0
```

Al posto di `liberi: 2` comparirà `liberi: 0`, perché ora `posti` vale `22` quando viene calcolata la differenza (`22 - 22`). Il `2` originale dipendeva dall'ordine di esecuzione accidentale, non dall'ordine di scrittura.
