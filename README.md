# db-university

1.Selezionare tutti gli insegnanti:

SELECT * FROM `teachers`;

------------------------------------------------------

2.Seleziona tutti gli studenti il cui nome inizia per E:

SELECT * FROM `students` WHERE name LIKE "E%";

------------------------------------------------------

2.Seleziona tutti gli studenti il cui nome finisce per E:

SELECT * FROM `students` WHERE name LIKE "%E";

------------------------------------------------------

2.Seleziona tutti gli studenti il cui nome ha all' interno una E:

SELECT * FROM `students` WHERE name LIKE "%E%";

------------------------------------------------------

3.Seleziona tutti gli studenti che si sono iscritti nel 2021: 

SELECT * FROM `students` WHERE `enrolment_date` LIKE "2021%";

------------------------------------------------------

3.Seleziona tutti gli studenti che si sono iscritti nel mese di Giugno: 

SELECT * FROM `students` WHERE `enrolment_date` LIKE "%-06-%";

------------------------------------------------------

4.Seleziona tutti gli insegnanti che non hanno un numero di telefono: 

SELECT * FROM `teachers` WHERE `phone` IS NULL;

------------------------------------------------------

4.Seleziona SOLO gli insegnanti che hanno un numero di telefono: 

SELECT * FROM `teachers` WHERE `phone` IS NOT NULL;

------------------------------------------------------

5.Seleziona tutti gli appelli di esame dei mesi di giugno e luglio 2020;

SELECT * FROM `exams` WHERE `date` LIKE "2020-06-%" OR `date` LIKE "2020-07-%";

------------------------------------------------------

5.Seleziona il totale degli studenti:

SELECT COUNT(`id`) FROM `students`;

------------------------------------------------------

6.Seleziona tutti i voti degli studenti in ordine descrescente:

SELECT * FROM `exam_student` ORDER BY `vote` DESC;

------------------------------------------------------

7.Seleziona tutti i voti degli studenti in ordine crescente: 

SELECT * FROM `exam_student` ORDER BY `vote` ASC;

------------------------------------------------------

8.Fai la media di tutti i voti degli studenti:

SELECT AVG(`vote`) FROM `exam_student`;

------------------------------------------------------