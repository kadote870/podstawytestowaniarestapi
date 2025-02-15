# Task 05 - Trello

* Utwórz kolekcję o nazwie **Task 05**,
* Utwórz nową kolekcję środowiska

> 💡 Przed przystąpieniem do pracy zaplanuj utworzenie zmiennych środowiskowych tak, aby w przyszłości uniknąć problemów
> przy testowaniu dwóch różnych instancji środowiska testowego np. DEV, QA i PROD

* Utwórz API Key oraz Token do
  Trello ([link](https://trello.com/power-ups/admin)) ([tutorial](../trello/generate-key-token.md))
* Utwórz zapytanie tworzące nową tablicę o nazwie
  task_4_board ([Create a Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post))

> * 💡Podczas pracy implemetuj zmienne środowiskowe zamiast prawdziwych tokenów
> * 💡Sprawdzaj wszystkie tworzone requesty do api pomagając sobie przy użyciu 'Save Response' i 'Path Variable'

* Utwórz zapytanie pobierające listę wszystkich list dla
  task_4_board ([Get Lists on a Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-lists-get))
* Utwórz zapytanie tworzące nową listę o nazwie task_4_list dla tablicy
  task_4_board ([Create a List on a Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-lists-post))
* Utwórz zapytanie pobierające listę wszystkich kart dla listy
  task_4_list ([Get Cards in a List](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-cards-get))
* Utwórz zapytanie tworzące nową kartę o nazwie task_4_card dla listy
  task_4_list ([Create a new Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-post))
* Utwórz zapytanie dodające opis task_4_card_description do karty
  task_4_card ([Update a Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-put))
* Utwórz zapytanie usuwające kartę
  task_4_card ([Delete a Card](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-delete))
* Utwórz zapytanie usuwające
  tablicę ([Delete a Board](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-delete))

# Następny rozdział: [Task 06 - Variables](06-task-variables.md)