<!-- Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario -->
<!-- fonte da cui ho preso spunto autoscout24 -->

# Concessionario
# (Table) Auto Usate

<!-- Nome colonna | tipo di dato | attributi -->

- id | BIGINT | PRIMARY_KEY - AUTO_INCREMENT (NOT NULL / UNIQUE) --> valori di default
- Marca auto | VARCHAR(70) - NOT NULL
- nome modello auto | VARCHAR(40) - NULL 
- versione | VARCHAR(40) - NULL 
- anno di immatricolazione |  DATE(YYYY-MM-GG) - NOT NULL
- potenza (cilindrata motore) | MEDIUMINT - NULL
- se è per neopatentati | TINYINT (TRUE/FALSE | 1/0) -  DEFAULT(1) - NULL
- carburante | VARCHAR(30) - NULL (Benzina, Gasolio, GPL, Metano, Elettricità, Ibrida)
- kilometraggio | MEDIUMINT - DEFAULT(0) - NOT NULL
- tipo di cambio | VARCHAR(30) - NULL (automatico, manuale, semiautomatico)
- Condizione veicolo (nouvo, usato, KM0, aziendale, epoca, dimostrativo) | VARCHAR(15) - NOT NULL
- numero proprietari | SMALL - NOT NULL  
- descrizione auto | TEXT - NOT NULL
- colore | VARCHAR(25) - NULL
- prezzo | FLOAT(9,2) - NOT NULL
- sconto | TINYINT (TRUE/FALSE | 1/0) -  DEFAULT(1)
- immagine auto | VARCHAR(255) - NULL
- numero di porte | SMALL - NULL (2/3 - 4/5 - 6/7) 
- posti disponibili | SMALL - NULL (1/2 - 4/5 - 6/7) 
- (?) consumi_carburante | FLOAT(4,2) - NULL
- (?) equipaggiamenti | TEXT - NULL

SEMI-AUTOMATIC TRANSMISSION