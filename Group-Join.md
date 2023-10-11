## 1. Contare quanti iscritti ci sono stati ogni anno

SELECT COUNT(\*) AS `iscritti`, YEAR ( `enrolment_date` ) AS `anno_iscrizione`
FROM `students`
GROUP BY `anno_iscrizione`;

## 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT COUNT(\*) AS `insegnanti`,`office_address` AS `ufficio`
FROM `teachers`
GROUP BY `ufficio`;

## 3. Calcolare la media dei voti di ogni appello d'esame

SELECT AVG(`vote`) AS `media`
FROM `exam_student`
GROUP BY `exam_id`;

## 4. Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT COUNT(\*) AS `corsi_di_laurea`, `department_id` AS `dipartimento`
FROM `degrees`
GROUP BY `dipartimento`;

## 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT `students`.`name`, `students`.`surname`,`students`.`date_of_birth`,`students`.`fiscal_code`,`students`.`enrolment_date`
FROM `students`
JOIN `degrees`
ON `students`.degree_id = `degrees`.id
WHERE `degrees`.name = "corso di laurea in economia";

## 2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento diNeuroscienze

## 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

## 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cuisono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

## 5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

## 6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
