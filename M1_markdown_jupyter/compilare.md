# Compilare ed eseguire il progetto Java

Queste istruzioni partono da un repository appena clonato. I sorgenti stanno in `src/`, i file compilati vanno in `bin/` e la classe con il metodo `main` si chiama `MediaVoti`.

## Procedura

1. Apri il terminale nella cartella del repository clonato.
2. Controlla che il JDK sia installato:
   - esegui `javac -version` per il compilatore;
   - esegui `java -version` per la macchina virtuale;
   - se uno dei due comandi non esiste, leggi la citazione in fondo alla pagina.
3. Crea la cartella `bin/` se non esiste:

   ```bash
   mkdir -p bin
   ```

4. Compila tutti i sorgenti di `src/` con l'opzione `-d bin`, che indica dove scrivere i file `.class`:

   ```bash
   javac -d bin src/*.java
   ```

5. Esegui la classe `MediaVoti` indicando a Java dove cercare le classi con l'opzione `-cp`:

   ```bash
   java -cp bin MediaVoti
   ```

## Se il JDK non è installato

> bash: javac: command not found

Installa il JDK 17, riapri il terminale e ripeti il passo 2.
