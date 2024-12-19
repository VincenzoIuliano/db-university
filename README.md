### Selezionare tutti gli studenti nati nel 1990 

```SQL
SELECT *
FROM `students`
WHERE YEAR(`date_of_birth`) = 1990
```
### Selezionare tutti i corsi che valgono più di 10 crediti 

```SQL
SELECT *
FROM `courses`
WHERE `cfu` > 10
```

### Selezionare tutti gli studenti che hanno più di 30 anni

```SQL
SELECT *, TIMESTAMPDIFF(YEAR, `date_of_birth`,CURDATE()) AS `anni`
FROM `students`
WHERE TIMESTAMPDIFF( YEAR, `date_of_birth`, CURDATE()) > 30
```

### Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea

```SQL
SELECT *
FROM `courses`
WHERE `period` = 'I semestre' AND `year` = 1
```

### Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020

```SQL
SELECT *
FROM `exams`
WHERE `date` = '2020-06-20' AND hour(hour) >= 14
```

### Selezionare tutti i corsi di laurea magistrale

```SQL
SELECT *
FROM `degrees`
WHERE `level` = 'magistrale'
```

### Da quanti dipartimenti è composta l'università?

```SQL
SELECT count(*)
FROM `departments`
```

### Quanti sono gli insegnanti che non hanno un numero di telefono?

```SQL
SELECT count(*)
FROM `teachers`
WHERE `phone` IS NOT NULL
```

