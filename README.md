# compito_tpsi_4ainf

Realizzare un programma scritto in linguaggio C così composto:

1. `math.c`: contenente le definizioni delle seguenti funzioni
   * `int somma(int, int)` : esegue la somma tra due interi e restituisce il risultato [0.5 pt]
   * `int differenza(int, int)` : esegue la differenza tra due interi e restituisce il risultato [0.5 pt]
   * `int moltiplicazione(int, int)` : eseuge la moltiplicazoine tra due interi e restituisce il risultato [0.5 pt]
   * `flaot divisione(float, float)` : esegue la divisione tra due float e restituisce il risultato [0.5 pt]
2. `math.h`: contenente i prototipi (dichiarazioni) delle funzioni elencate sopra [0.25 pt]
3. `pow.c`: contenente la definizione della seguente funzione
   * int potenza(int base, int esponente): esegue l'operazione $base^{esponente}$ [2 pt]
4. `pow.h`: contenente il prototipo della funzione al punto 3 [0.25 pt]
5. `trace.h` contente una macro `TRACE()` che stampi con la funzione `printf()` il nome del file, il numero di riga e il nome della funzione in cui viene richiamata. [1 pt]
   * `__FILE__` : stampa il nome del file  (%s)
   * `__LINE__` : stampa il numero di riga (%d)
   * `__func__` : stampa il nome della funzione (%s)
6. `main.c` che attraverso un menu' (come quello mostrato sotto) chieda all'utente l'operazione da svolgere e gli operandi su cui applicare l'operazione e che stampi il risultato finale [1.5 pt]

   ```c
   + Somma
   * Moltiplicazione
   - Differenza
   / Divisione
   ^ Potenza
   # Logger
   ! Esci
   ```
   terminata l'operazione e stampato il risultato il programma deve tornare a mostrare il menu' ed aspettare nuovi comandi. Si termini il programma usando la voce di menu' `!`
8. Richiamare la macro `TRACE()` nella prima riga di ogni funzione (compreso il main) solo se la macro `DEBUG` è definita. Definire ls macro `DEBUG` attraverso l'opzione `-DDEBUG` a tempo di compilazione [0.5]
9. Definire all'interno del main (come variabili globali) i seguenti vettori che conterranno lo storico delle operazioni (+ - / * ^) degli operandi e dei risultati (l'elmento i-esimo di ogni vettore conterrà rispettivamente gli operandi l'operazione ed il risultato dell'i-esima iterazione del programma) [0.25]
    ```c
    #define BUF 10

    int operando1_[BUF] = {0};
    int operando2_[BUF] = {0};
    int risultato_[BUF] = {0};
    char operazione_[BUF] = {'\0'};
    ```
10. `logger.c`: contenente la definizione della seguente funzione `void logger(int iterazioni)` che stamperà tutte le operazioni, gli operandi ed i risultati delle iterazioni fino a quel momento eseguite. Per fare questo la funzione deve usare i vettori globali dichiarati al punto 9. [1 pt]
11. `logger.h`: contenente il prototipo della funzione al punto 10 [0.25 pt]
    
Realizzare un Makefile che compili e linki assieme tutti i file. **Un programma che non compila o senza Makefile non avrà la sufficienza**
