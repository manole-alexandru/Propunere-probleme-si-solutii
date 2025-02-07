# Overview
    Acest folder contine un ghidaj tehnic si posibil cod re-folosibil pentru:
        * Comisie: propunera unei probleme, ajustarea unui dataset, pregatirea unui evaluator, sfaturi utile in urma unor iteratii succesive in simularea unei propuneri si simulari (vezi documentul Sablon...docx)
        * Candidati: solutiile posibile a doi studenti, unul incepator si unul avasat, in folderul OutputCandidati.
    

# Dataset
    In vederea pregatirii unui dataset, expunem in Comisie_PregatireProblema/Dataset un notebook cu pasii realizati in vederea curatarii unui dataset public, transformarea lui, si obtinerea a 3 seturi de date:
        * dataset_train: folosit la antrenare
        * dataset_eval: folosit pentru predictie de catre candidati (acestia nu cunosc ground-truth-ul valorilor de iesire).
        * dataset_eval_t: la fel ca mai sus, ascuns candidatilor, contine si campurile pentru evaluare.

    Fiecare candidat primeste primele doua seturi (vedeti folderele fiecaruia) si scoate ca output fisierele in formatul cerut de enuntul problemei.

# Evaluator
    Notebook-ul de evaluare este contine cod reutilizabil care compara rezultatele candidatilor si scoate ca iesire un tabel sortat dupa scoruri si detalierea rezultatelor.

