# Exemplu de problema (predictia preturilor jocurilor de pe platforma Steam)

## Enunt
Implementati un model de AI pentru a prezice preturile din jocurile de pe Steam avand la dispozitie un set de antrenare `dataset_train.csv` si unul pe care trebuie sa faceti doar predictia`dataset_eval.csv`.

Setul de date contine urmatoarele campuri avand semnificatiile:

- `Name`: nume aplicație
- `AppID`: identificatorul jocului
- `Metacritic score`: nota medie a jocului de pe platforma de recenzii Metacritic
- `Genres`: o lista separata prin virgule conținând tag-uri referitoare la tipul de joc
- `Publishers`: numele producatorilor
- `Estimated Owners`: de forma min – max, insemnand asteptarile (producatorilor jocului) minime si maxime de jocuri vandute
- `Negatives`: numarul de dislike-uri
- `Positives`: numarul de like-uri
- `Recommendations`: cate persoane recomanda acest joc

## Note despre setul de date:

- Câmpul-ținta este „Price”. Date fiind celelalte feature-uri, scopul este de a prezice „Price”. Setul de date de evaluare vizibil pentru candidați nu conține acest câmp, însă el este necesar platformei de evaluare. Metrica de evaluare folosita este MAE (media sumei diferentelor in modul dintre output-ul predictiei voastre si cea corecta).
- Câmpul Genres, fiind o lista, trebuie transformat in date numerice într-un fel sau altul pentru a putea fi folosit in algoritmii de ML.
- Asemănător pentru câmpul Estimated Owners
- Unele câmpuri pot fi inutile in predicția campului-tinta. Incercati sa analizati datele si sa selectați doar ce este nevoie sau ar putea explica predictia.

## Cerinte

**P1 (40p**). Incarcati setul de date de antrenare si scrieți un fișier output_1.csv in care sa aveți header-ul:

"Samples,Average Price,Average Owners,Unique Genres”

- Samples: numarul de linii de input din setul de date de antrenare, folosit in scop de verificare locala
- Average Price: pretul mediul pentru toate produsele din setul de date
- Average Owners: pentru campurile din coloana Estimated Owners de forma min – max, extrageti media tutor valorilor considerand pentru fiecare linie int ((min + max) / 2).
- Unique Genres: numarul unic de tag-uri existet in dataset pentru toata coloana Genres

Fiecare din cele 4 componente valoreaza 10p.

**P2 (60p)** Implementati un model de AI si rulați predicția pentru fiecare rând din dataset_eval.csv.

Output-ul trebuie sa fie un fișier output_2.csv cu o singura coloana numita „Price”.
