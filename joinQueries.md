## (1) Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

# SELECT students.name, students.surname, students.registration_number 
# FROM students 
# JOIN degrees ON students.degree_id = degrees.id
# WHERE degrees.name = 'Corso di Laurea in Economia';

## (2) Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

# SELECT degrees.name AS degree_name, degrees.level, degrees.address, departments.name AS department_name 
# FROM degrees 
# JOIN departments ON degrees.department_id = departments.id 
# WHERE degrees.level = 'magistrale' AND departments.name = 'Dipartimento di Neuroscienze';

## (3) Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

# SELECT courses.name 
# FROM course_teacher 
# JOIN courses ON course_teacher.course_id = courses.id 
# JOIN teachers ON course_teacher.teacher_id = teachers.id 
# WHERE teachers.id = 44;

## (4) Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

# SELECT  students.name AS student_name, students.surname, students.registration_number, departments.name AS department_name,   departments.address AS department_address, departments.head_of_departmentdegrees.name AS degree_name, degrees.level AS degree_level, degrees.address AS degree_address, 
# FROM students 
# JOIN degrees ON students.degree_id = degrees.id 
# JOIN departments ON degrees.department_id = departments.id 
# ORDER BY students.surname, students.name;

## (5) Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

# SELECT degrees.name AS degree_name, courses.name AS course_name, teachers.name AS teacher_name, teachers.surname 
# FROM course_teacher JOIN courses ON course_teacher.course_id = courses.id 
# JOIN degrees ON courses.degree_id = degrees.id
# JOIN teachers ON course_teacher.teacher_id = teachers.id 

## (6) Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica

# SELECT teachers.id as 'teachers_id', teachers.name as 'teachers_name', teachers.surname, departments.name as 'department_name' 
# FROM teachers 
# JOIN course_teacher ON teachers.id = course_teacher.teacher_id 
# JOIN courses ON course_teacher.course_id = courses.id 
# JOIN degrees ON courses.degree_id = degrees.id 
# JOIN departments ON degrees.department_id = departments.id 
# WHERE departments.id = 5;
