### Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

```SQL
SELECT `degrees`.`name`, `students`.*
FROM `degrees`
JOIN `students`
ON `degrees`.`id` = `students`.`degree_id`
WHERE `degrees`.`name` = 'Corso di Laurea in Biologia'
```

### Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

```SQL
SELECT `degrees`.`name` , `degrees`.`level`
FROM `departments`
JOIN `degrees`
ON `degrees`.`department_id` = `departments`.`id`
WHERE `degrees`.`level` = 'Magistrale' AND `departments`.`name` = 'Dipartimento di Neuroscienze'
```