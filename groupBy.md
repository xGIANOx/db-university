## (1) Contare quanti iscritti ci sono stati ogni anno

# SELECT YEAR(enrolment_date) as 'enrolment_year'
# COUNT(*) as total_students 
# FROM students 
# GROUP BY enrolment_year;

## (2) Contare gli insegnanti che hanno l'ufficio nello stesso edificio

# SELECT COUNT(*) as 'total_teachers', office_address 
# FROM teachers 
# GROUP BY office_address

## (3) Calcolare la media dei voti di ogni appello d'esame

# SELECT exam_id, AVG(vote) as average_vote 
# FROM exam_student 
# GROUP BY exam_id

## (4) Contare quanti corsi di laurea ci sono per ogni dipartimento
 
