### Contare quanti iscritti ci sono stati ogni anno

```SQL
SELECT COUNT(*) AS `new_students_number`, YEAR(`enrolment_date`) AS `enrolment_year`
FROM `students`
GROUP BY `enrolment_year`
```

### Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```SQL
SELECT COUNT(*) AS `teachers_number`, `office_address` AS `office_location`
FROM `teachers`
GROUP BY `office_address`
```

### Calcolare la media dei voti di ogni appello d'esame

```SQL
SELECT `exam_id`, AVG(`vote`) AS 'average_vote'
FROM `exam_student`
GROUP BY `exam_id`
```