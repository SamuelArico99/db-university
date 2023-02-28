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



ESERCIZIO DI OGGI

1. Selezionare tutti gli studenti nati nel 1990 (160)

SELECT * FROM `students` WHERE `date_of_birth` LIKE "1990%";

------------------------------------------------------

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

SELECT * FROM `courses` WHERE `cfu`> 10;

------------------------------------------------------

3. Selezionare tutti gli studenti che hanno più di 30 anni

SELECT * FROM `students` WHERE YEAR(CURRENT_DATE) - YEAR(date_of_birth) > 30;

-----------------------------------------------------

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)

SELECT * FROM `courses` WHERE `year` LIKE "1" AND `period` LIKE "I semestre";

-----------------------------------------------------

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)

SELECT * FROM exams WHERE date = '2020-06-20' AND hour > '14:00:00';

-----------------------------------------------------

6. Selezionare tutti i corsi di laurea magistrale (38)

SELECT * FROM `degrees` WHERE `level` LIKE "magistrale";

-----------------------------------------------------

7. Da quanti dipartimenti è composta l'università? (12)

SELECT COUNT(`id`) FROM `departments`;

-----------------------------------------------------

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

SELECT * FROM `teachers` WHERE `phone` IS NULL;

-----------------------------------------------------