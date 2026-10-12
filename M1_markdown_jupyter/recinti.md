# Guida ai recinti annidati

Un recinto è una riga di almeno tre apici inversi che apre o chiude un blocco di codice. Per mostrare un recinto dentro un altro, quello esterno deve usare più apici di quello interno.

## Primo esempio: un blocco normale

Il lettore vedrà un riquadro con codice Java colorato.

```java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
```

## Secondo esempio: il sorgente di un blocco

Il lettore vedrà un riquadro che contiene, come testo, anche le righe con gli apici inversi del blocco Java. Il recinto esterno ha quattro apici, quello interno tre.

````markdown
```java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
```
````

## Terzo esempio: tre livelli

Il lettore vedrà un riquadro che contiene un recinto da quattro apici, a sua volta contenente il recinto da tre con il codice Java. Ogni livello esterno usa un apice in più.

`````markdown
````markdown
```java
System.out.println("Ciao");
```
````
`````

