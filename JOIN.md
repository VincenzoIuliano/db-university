### Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

```SQL
SELECT `degrees`.`name`, `students`.*
FROM `degrees`
JOIN `students`
ON `degrees`.`id` = `students`.`degree_id`
WHERE `degrees`.`name` = 'Corso di Laurea in Biologia'
```