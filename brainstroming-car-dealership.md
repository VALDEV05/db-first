<!-- Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario -->
<!-- fonte da cui ho preso spunto autoscout24 -->

# Concessionario
# (Table) Auto Usate

<!-- Nome colonna | tipo di dato | attributi -->

- id | BIGINT | PRIMARY_KEY - AUTO_INCREMENT (NOT NULL / UNIQUE)
    <!-- Deve essere un numero unico che aumenta in modo automatico, nel caso quell'elemento venisse rimosso perderemmo l'utilità di quell'id. Necessario per la creazione della tabella del databese. -->
- marca_auto | VARCHAR(70) - NOT NULL
    <!-- È una stringa di massimo 70 caratteri, necessari per la ricerca della autovettura. Contenente il nome della marca dell' auto. -->
- modello_auto | VARCHAR(40) - NULL 
    <!-- È una stringa di massimo 40 caratteri, non necessaria. Contenente il modello dell' auto. -->
- versione | VARCHAR(40) - NULL 
    <!-- È una stringa di massimo 40 caratteri, non necessaria. Contenente la versione dell' auto. -->
- anno_immatricolazione | YEAR(YYYY) - NOT NULL
    <!-- È un numero di 4 cifre, l'anno. Anno in cui la macchina è stata immatricolata. Obbligatiori.  -->
- potenza_motore | SMALLINT - NULL
    <!-- È un numero che va da 0 - 65'535. Indica la potenza del motore.-->
- neopatentati | TINYINT (TRUE/FALSE | 1/0) -  DEFAULT(1) - NULL
    <!-- È un numero che va da 0 - 255, ovvero da 0/1. Quindi è come se restituisse un valore booleano (true/false) che indica se la macchina è per neopatentati.-->
- carburante | VARCHAR(30) - NULL (Benzina, Gasolio, GPL, Metano, Elettricità, Ibrida)
    <!-- Stringa di 30 caratteri, indica l'alimentazione della macchiana. -->
- kilometraggio | MEDIUMINT - DEFAULT(0) - NOT NULL
    <!-- È un numero che va da 0 - 16'777'215. Indica i km percorsi.-->
- tipo_cambio | VARCHAR(30) - NULL (automatico, manuale, semiautomatico)
    <!-- Stringa di 30 caratteri, indica la tipologia di cambio della macchina. Ho considerato 30 caratteri perchè la tipologia con cambio semiautomatico arriva a 27 caratteri. semi-automatic trasmission -->
- condizione_veicolo (nouvo, usato, KM0, aziendale, epoca, dimostrativo) | VARCHAR(15) - NOT NULL
    <!-- Stringa di 15 caratteri, indica la tipologia di cambio della macchina. -->
- numero_proprietari | TINYINT - NOT NULL  
    <!-- È un numero che va da 0 - 255. Quindi è perfetto per indicare il numero dei precedenti proprietari.-->
- descrizione_auto | TEXT - NOT NULL
    <!-- Contiene fino a 65535 caratteri - è usato ad esempio per le descrizioni prodotto-->
- colore | VARCHAR(15) - NULL
    <!-- Stringa di 15 caratteri, indica il colore della macchina. -->
- prezzo | FLOAT(9,2) - NOT NULL
    <!-- Indica un numero con la virgola di massimo 9 cifre con 2 cifre dopo la virgola. Ho messo 9 cifre pensando a macchine che costano fino a 9'999'999,99 milioni. -->
- sconto | TINYINT (TRUE/FALSE | 1/0) -  DEFAULT(1)
<!-- Potendo restituire un valore booleano, indica se lo sconto è presente o meno. -->
- immagine_auto | VARCHAR(255) - NULL
<!-- Stringa di 255 caratteri, indica il link o il percorso file per accedere all'immagine. -->
- numero_porte | TINYINT - NULL (2/3 - 4/5 - 6/7) 
<!-- Indica il numero di porte che ha quella macchina -->
- posti_disponibili | TINYINT - NULL (1/2 - 4/5 - 6/7) 
<!-- Indica il numero di posti che ha quella macchina -->
- (?) consumi_carburante | FLOAT(4,2) - NULL
<!-- numero che di solito sta intrno a ~20,5 l. Quindi come struttura dati ho utilizzato un float che ha 4 cifre, con due cifre dopo la virgola.-->
- (?) equipaggiamenti | TEXT - NULL
    <!-- Contiene fino a 65535 caratteri - è usato ad esempio per le descrizioni prodotto-->
