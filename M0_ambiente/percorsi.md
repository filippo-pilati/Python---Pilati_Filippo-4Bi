# MODULO 0 Esercizio 2

## Compiti di Informatica (Come moversi tra i file)

Per prima cosa mi sposto nell’unità C, perché Git CMD possa aprirsi in un altro disco:

Z:\>C:

Ora entro nella cartella Users, che contiene tutti gli utenti del computer:

C:\>cd Users

Entro nel mio utente:

C:\Users>cd filippo.pilati

Entro nei Documenti:

C:\Users\filippo.pilati>cd Documents

Creo la cartella dell’esercizio:

C:\Users\filippo.pilati\Documents>mkdir esercizio-percorsi

Entro nella cartella appena creata:

C:\Users\filippo.pilati\Documents>cd esercizio-percorsi

Creo le due cartelle richieste: dati e risultati

C:\Users\filippo.pilati\Documents\esercizio-percorsi>mkdir dati
C:\Users\filippo.pilati\Documents\esercizio-percorsi>mkdir risultati

Entro nella cartella dati:

C:\Users\filippo.pilati\Documents\esercizio-percorsi>cd dati

Torno indietro alla cartella principale dell’esercizio:

C:\Users\filippo.pilati\Documents\esercizio-percorsi\dati>cd ..

Infine entro nella cartella risultati:

C:\Users\filippo.pilati\Documents\esercizio-percorsi>cd risultati

Per poter usare il comando Get-Location si deve essere in powershell e non cmd:

C:\Users\filippo.pilati\Documents\esercizio-percorsi\risultati>powershell Windows PowerShell Copyright (C) Microsoft Corporation. 

Tutti i diritti riservati.

Installa la versione più recente di PowerShell per nuove funzionalità e miglioramenti. https://aka.ms/PSWindows

Ora posso usare il comando:
PS C:\Users\filippo.pilati\Documents\esercizio-percorsi\risultati> Get-Location

Path
----
C:\Users\filippo.pilati\Documents\esercizio-percorsi\risultati