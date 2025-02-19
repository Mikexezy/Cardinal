---
connections:
  - "[[Salvatore che non se la fida di informatica]]"
source:
  - Prof. Michele Pernaci
---
#### Lezione

Step 1. creiamo il nostro database
```sql
CREATE DATABASE prova;
USE prova;
```

Step 2. aggiungiamo le nostre tabelle
```sql
CREATE TABLE mike(
	ID INT AUTO_INCREMENT PRIMARY KEY
	Nome VARCHAR(15) NOT NULL
	Cognome VARCHAR(15) NOT NULL
	Email VARCHAR(100) UNIQUE NOT NULL,
    DataNascita DATE
);

CREATE TABLE ciccio(
	ID INT AUTO_INCREMENT PRIMARY KEY
	Nome VARCHAR(15) NOT NULL
	Cognome VARCHAR(15) NOT NULL
);

CREATE TABLE ryze(
	ID INT AUTO_INCREMENT PRIMARY KEY
	Nome VARCHAR(15) NOT NULL
	Cognome VARCHAR(15) NOT NULL
);
```

Step 3. Popoliamo le nostre tabelle
```sql
INSERT INTO ciccio(Nome, Cognome) VALUES ("Francesco", "La Piana");
INSERT INTO ciccio(Nome, Cognome) VALUES ("Luca", "La Piana");
UPDATE ciccio SET Nome = "Andrea" WHERE Cognome = "Petrantoni";
```

Step 4. Eliminare qualcosa
```sql
DELETE FROM ciccio; 
TRUNCATE ciccio;

DELETE FROM ciccio WHERE cognome = "La Piana";

DROP TABLE ciccio; 
DROP TABLE IF EXISTS ciccio; 

DROP DATABASE prova;
```

Step 5. Interroghiamo il database
```sql
SELECT ciccio.Cognome
FROM ciccio 
WHERE ciccio.Nome = "Luca"

SELECT *
FROM ciccio 
GROUP BY ciccio.Cognome

SELECT *
FROM ciccio 
WHERE ciccio.Nome IN("Davide", "Elia", "Carlo")
```

Step 6. Foreign Key
```sql
CREATE TABLE Clienti (

    id INT PRIMARY KEY,

    nome VARCHAR(100),

    email VARCHAR(100)

);

CREATE TABLE Ordini (

    id INT PRIMARY KEY,

    data_ordine DATE,

    customer_id INT,

    FOREIGN KEY (customer_id) REFERENCES Clienti(id)

);
```

Step 7. Foreign Key in caso di associazione N:N
```sql
CREATE TABLE Studenti (
    id INT PRIMARY KEY,
    nome VARCHAR(100)
);

CREATE TABLE Corsi (
    id INT PRIMARY KEY,
    nome_corso VARCHAR(100)
);

CREATE TABLE Studenti_Corsi (
    studente_id INT,
    corso_id INT,
    FOREIGN KEY (studente_id) REFERENCES Studenti(id) ON DELETE CASCADE,
    FOREIGN KEY (corso_id) REFERENCES Corsi(id) ON DELETE CASCADE,
    PRIMARY KEY (studente_id, corso_id)
);
```