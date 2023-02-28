# db-university

1.Selezionare tutti gli insegnanti:
SELECT * FROM `teachers`;

2.Seleziona tutti gli studenti il cui nome inizia per E:
SELECT * FROM `students` WHERE name LIKE "E%";

2.Seleziona tutti gli studenti il cui nome finisce per E:
SELECT * FROM `students` WHERE name LIKE "%E";

2.Seleziona tutti gli studenti il cui nome ha all' interno una E:
SELECT * FROM `students` WHERE name LIKE "%E%";