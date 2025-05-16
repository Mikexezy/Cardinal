---
connections:
  - "[[Database]]"
  - "[[Apprendimento supervisionato]]"
source:
  - Prof. Manuela Musumeci
  - Prof. Fabio Capraro
---
Possibili entità: Attori, Recita, Film, Proiezioni, Sale

```Modello-Logico
Attori(CodAttore, Nome, AnnoNascita, Nazionalità)
Recite(CodAttore, CodFilm, ID)
Film(CodFilm, Titolo, AnnoProduzione, Nazionalità, Regista, Genere)
Proiezioni(CodProiezione, CodFilm, CodSala, Incasso, DataProiezione)
Sale(CodSala, Posti, Nome, Città)
```



# Query
---

Visualizzare il numero di sale per ogni città.
```sql
SELECT Città, count(CodSala)
FROM Sale
GROUP BY Città
```

---

Recuperare il numero di sale nella città di Pisa e che abbiano un numero di posti maggiore di 60.
```sql
SELECT count(CodSala)
FROM Sale
WHERE Città = "Pisa" AND Posti > 60
```

---

Per ogni film di fantascienza, recuperare il titolo e l'incasso totale di tutte le sue proiezioni successive all'1 Gennaio.
```sql
SELECT Titolo, SUM(Incasso) as IncassoTotale
FROM Film, Proiezioni
WHERE Film.CodFilm = Proiezioni.CodFilm 
AND Film.Genere = "Fantascienza" 
AND Proiezioni.DataProiezione > "01-01-2025"
GROUP BY Titolo
```
>[!Differenza fra HAVING e WHERE]
>Having viene applicato su tutto il gruppo precedentemente creato dal GROUP BY,
>mentre il WHERE viene applicato per ogni singolo record.

---

Recuperare i titoli dei film che non sono mai stati proiettati a Pisa.
```sql
SELECT Titolo
FROM Film,
WHERE Film.CodFilm NOT IN(
	SELECT Proiezioni.CodFilm
	FROM Proiezioni, Sale
	WHERE Proiezioni.CodSala = Sale.CodSala
	AND Sale.Città = "Pisa" 
)
```
