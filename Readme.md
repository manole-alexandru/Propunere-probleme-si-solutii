In acest folder gasiti un ghidaj tehnic si cod refolosibil **pentru cei care doresc sa propuna probleme pentru Olimpiada de AI**.

# Problema
Documentul [Problema.md](Problema.md) contine un exemplu de problema. Structura generala a unei probleme este in [Sablon_problema.md](Sablon_problema.md), iar cateva sfaturi utile se gasesc in [Recomandari.md](Recomandari.md).

# Solutii
Folderul [Solutii](Solutii) contine 2 posibile solutii - pentru incepatori si avansati.
    
# Set de date
Pregatirea unui set de date este descrisa in folderul [Dataset si evaluator/Dataset](Dataset%20si%20evaluator/Dataset). Acolo gasiti un notebook cu pasii realizati pentru curatarea unui dataset public, transformarea lui si obtinerea a 3 seturi de date:
- `dataset_train`: folosit pentru antrenare
- `dataset_eval`: folosit pentru predictie de catre candidati (acestia nu cunosc ground-truth-ul valorilor de iesire)
- `dataset_eval_t`: la fel ca mai sus, ascuns candidatilor, contine si campurile pentru evaluare.
Nota: Fiecare candidat primeste primele doua seturi (vedeti folderul fiecaruia) si scoate ca output fisierele cerute in formatul cerut de enuntul problemei.

# Evaluator (pentru comisia de evaluare)
Notebook-ul de evaluare [Dataset si evaluator/Evaluator.ipynb](Dataset%20si%20evaluator/Evaluator.ipynb) contine cod reutilizabil care compara rezultatele candidatilor si genereaza ca iesire un tabel sortat dupa scoruri si detalierea rezultatelor.
