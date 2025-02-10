# Continut
Acest folder contine un ghidaj tehnic si posibil cod re-folosibil pentru:

# Problema
Documentul sablon si exemplu de problema contine un sablon de problema, un exemplu de problema, ajustarea unui set de date, pregatirea unui evaluator, sfaturi utile si simulari

# Solutii
Folderul Solutii_Problema contine 2 posibile solutii, pentru incepatori si avansati
    
# Set de date (pentru comisie)
Pentru pregatirea unui set de date, expunem in Comisie_PregatireProblema/Dataset un notebook cu pasii realizati pentru curatarea unui dataset public, transformarea lui si obtinerea a 3 seturi de date:
- dataset_train: folosit pentru antrenare
- dataset_eval: folosit pentru predictie de catre candidati (acestia nu cunosc ground-truth-ul valorilor de iesire)
- dataset_eval_t: la fel ca mai sus, ascuns candidatilor, contine si campurile pentru evaluare.

Fiecare candidat primeste primele doua seturi (vedeti folderele fiecaruia) si scoate ca output fisierele in formatul cerut de enuntul problemei.

# Evaluator (pentru comisie)
Notebook-ul de evaluare contine cod reutilizabil care compara rezultatele candidatilor si genereaza ca iesire un tabel sortat dupa scoruri si detalierea rezultatelor.
