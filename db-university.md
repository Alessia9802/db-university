<!-- Query con Group by -->
<!-- Contare quanti iscritti ci sono stati ogni anno -->

- SELECT COUNT(`id`) AS `iscrizioni`, YEAR(`enrolment_date`) AS `anno` FROM `students` GROUP BY `anno`;
<!-- Contare gli insegnanti che hanno l'ufficio nello stesso edificio -->

- SELECT `office_address`, `id` FROM `teachers` WHERE `office_address` = `office_address` GROUP BY `office_address`, `id`;

<!-- Calcolare la media dei voti di ogni appello d'esame -->

- SELECT COUNT(`exam_id`) AS `ESAMI`, AVG(vote) FROM `exam_student` GROUP BY `vote`;

<!-- Contare quanti corsi di laurea ci sono per ogni dipartimento -->

- SELECT COUNT(`name`) FROM `departments` GROUP BY `name`;

<!-- Query con Join -->
<!-- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia -->

- SELECT \* FROM `degrees` JOIN `students` ON students.id = degrees.students_id;
  <!-- Selezionare tutti i Corsi di Laurea del Dipartimento di Neuroscienze -->
  SELECT departments FROM `departments` WHERE `departments` = "Dipartimento di Neuroscenze";
  <!-- Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) -->
  <!-- Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome -->
  <!-- Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti -->
  <!-- Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54) -->
