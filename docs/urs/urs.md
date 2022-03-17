
### User Requirements Specification Document
##### DIBRIS – Università di Genova. Scuola Politecnica, Software Engineering Course 80154


**VERSION : X.X**

**Authors**  
XXXX
YYYY

**REVISION HISTORY**

| Version    | Date        | Authors      | Notes        |
| ----------- | ----------- | ----------- | ----------- |
| X.X |  | |  |

# Table of Contents

1. [Introduction](#p1)
	1. [Scope](#sp1.1)
	2. [Definitios and Acronym](#sp1.2) 
	3. [References](#sp1.3)
2. [Project](#p2)
	1. [Context and Motivation](#sp2.1)
	2. [Project Objectives](#sp2.2)
3. [Requirement](#p3)
 	1. [Stakeholders](#sp3.1)
 	2. [Functional Requirements](#sp3.2)
 	3. [Non-Functional Requirements](#sp3.3)
  
  

<a name="p1"></a>

## 1. Introduzione

<a name="sp1.1"></a>

### 1.1 Scope

Il documento in atto viene redatto al fine di *definire* i requisiti e gli obiettivi di un software di testing per BBS. Il quale verrà implementato durante il corso di Ingegneria del Software. Il documento verrà consulatato sia dagli sviluppatori, in corso d'opera, come riferiemento principale per i requisiti del sistema, che dagli utenti del sistema per capirne il fuzinamento. 

<a name="sp1.2"></a>

### 1.2 Definitios and Acronym


| Acronym				| Definition | 
| ------------------------------------- | ----------- | 
| NBA                                   | Non deterministic Buchi Automata |

<a name="sp1.3"></a>

### 1.3 References 

<a name="paragraph2"></a>

## 2. Descrizione generale del sistema

Il test del software è il processo di identificazione della correttezza e della qualità dei programmi software. 
Nel nostro caso, ossia Black Box Testing, il test viene eseguito senza conoscere la struttura interna del programma.
Il tester è a conoscenza di ciò che il software dovrebbe fare ma non è a conoscenza di come lo fa. Ad esempio, il tester è consapevole che un particolare input restituisce un determinato output invariabile, ma non è a conoscenza di come il software produce l'output in primo luogo.
I test vengono generati a partire dalle specifiche del software.

<a name="subparagraph5"></a>

### 2.1 Contesto e motivazioni 

I test possono essere eseguiti in molti modi diversi, per esempio se un software prende in input un numero intero all'interno di un certo range, si potrebbe testare l'intero range di numeri oppure solamente i valori agli estremi dell'intervallo.
Scrivere test manualmente richiede molto tempo, sono possibili errori anche in fase di testing.
Si stima che la metà del costo di sviluppo software sia dedicato al testing, essendo una delle fasi più importanti: rilasciare un software con errori al proprio interno potrebbe causare problemi di gravità proporzionata allo scopo del software stesso (es. nei sistemi safety-critical le conseguenze di un errore potrebbe essere anche la perdita di vite umane). 
Implementando test Black Box si avrà  la sicurezza di aver dato il massimo nella ricerca degli errori all'interno del sistema.

<a name="subparagraph6"></a>

### 2.2 Obiettivo del progetto

L’obiettivo é quello di sviluppare un software per la generazione di test automatici per sistemi reattivi, cioé sistemi ai quali applicando un input questi forniscono una risposta. 
Si sfrutta la rappresentazione NBA per la descrizione delle specifiche del sistema, la logica Booleana per poter generare dei test e le tecniche di ragionamento per la loro correttezza, con lo scopo di fornire uno strumento di verifica della risposta dei BBS, con elevata affidabilità.

<a name="subparagraph7"></a>

### 2.3 Utenti

Individuati 2 gruppi principali:
* Tester di sistemi reattivi
	* Queste figure utilizzano il software nell'ambito dei sistemi reattivi alla ricerca di errori negli stessi. Hanno necessità di testare software Black Box per verificare che questi rispettino le specifiche date, con una certa confidenza. 
* Analisti software per il RSDD
	* Il paradigma di sviluppo RSDD ha lo scopo di costruire un sistema a partire dai requisiti da soddisfare. Figure come quelle degli analisti software lo seguono, generando test su test per verificare che i sistemi che stanno costruendo soddisfino tutti i requisiti. Questi utenti hanno quindi l’esigenza di generare test per verificare se i sistemi che vogliono utilizzare rispettano determinati requisiti e con quale grado di fiducia.

<a name="paragraph3"></a>

## 3. User Requirement

In questa sezione descriveremo i requisiti dell’applicazione lato utente, assegnando ad ognuno un’id e una priorità seguendo la tabella sotto.
	
| Priorità | Significato | 
| --------------- | ----------- | 
| M | **Mandatory:** Requisito obbligatorio |
| D | **Desiderable:** Requisito che dovrebbe essere inserito nel sistema, a meno che il costo per implementarla non sia troppo alto.|
| O | **Optional:** Una funzionalità marcata con O può essere inserita nel sistema, a discrezione del manager del progetto. Ad esempio se il tempo di sviluppo è minore di quello previsto oppure se il costo per implementarla non è troppo alto. |
| E | **future Enhancement:** Questo requisito viene lasciato per la prossima release. |


**Requisiti funzionali**

| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 1.0 | **Input #1**: il sistema prende in input un numero intero rappresentante la lunghezza massima del test (Kmax). |M|
| 1.1 | **Input #2**: il sistema prende in input un numero intero rappresentante la lunghezza minima del test (Kmin). |M|
| 1.2 | **Input #3**: il sistema prende in input un numero intero rappresentante l'incremento della lunghezza del test (Step). |M|
| 1.3 |	**Input #4**: il sistema prende in input uno o più NBA. |M|
| 1.4 |	**Input #5**: il sistema prende in input un numero intero da 1 a N (numero massimo), che indica l'obiettivo da raggiungere. |M|
| 1.5 |	**Input #6**: l'NBA in input è descritto in formato DOT. |M|
| 1.6 |	**Input #7**: deve essere presente l'insieme dei nomi delle variabili del BBS. |M|
| 1.7 | **Input #8:** l'utente può selezionare la directory di salvataggio dell'output. |M|
| 1.8 | **Input #9:** formato formula in uscita DIMACS e/o SMT |M|
| 1.9 | **Input #10:** il sistema prende in input un tempo limite (Timeout (in secondi)) per la generazione del test. |M|
| 1.10 | **Output #1** il sistema prevede un timeout di default (in secondi) se non inserito dall'utente. |M|
| 1.11 | **Output #2**: il sistema fornisce in output una formula booleana che è SAT quando tutti i percorsi selezionati soddisfano il goal selezionato a lunghezza K. |M|
| 1.12 | **Output #3**: il sistema restituisce in output un test. |M|
| 1.13 | **Output #4**: formula booleana, il cui formato è selezionato dall'utente tramite interfaccia di input. |M|
| 1.14 | **Output #6**: nel caso in cui il sistema non riesca a generare un test entro il timeout, deve essere segnalato all'utente. |M|
| 1.15 | **Interfaccia:** deve essere presente un interfaccia GUI |M|
| 1.16 | **Interfaccia:** deve essere presente un interfaccia CLI che prende in input il file JSON. |M|
| 1.17 | **Ripetibilità del test:** date sempre le stesse condizioni di sistema (gruppo di automi, lunghezza di K, timeout e obbiettivi),questo deve generare sempre lo stesso test.  |M|
| 1.18 | **Visualizzazione del percorso:** l’utente può vedere a schermata il percorso che l’automa di Buchi esegue, attraverso il cambio di colore dei rami e dei nodi. |O|
| 1.19 | **Compilazione:** il sistema deve essere compilabile da linea di comando. |M|
 

**Requisiti non funzionali**

| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 2.0 | **Fruibilità del software:** il software di testing dovrebbe essere eseguibile sia da Windows che da Linux. |M|
| 2.1 | **Utilizzo esterno:** il software deve essere disponibile anche a terze parti. |M|
| 2.2 | **Libreria:** il sistema deve essere fruibuile da altri utenti come libreria. |M|
| 2.3 | **Importazione:** deve essere possibile importare il sistema in una ide comune (come Eclipse). |M|
