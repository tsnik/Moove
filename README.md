# Moove

1. Получение всех имен и фамилий людей в определенном кабинете  
SELECT first_name, last_name FROM Persons WHERE room=42
2. Добавление нового телефона сотруднику  
INSERT INTO Numbers (person_id, phone) VALUES (1, '+79166965456')
3. Получение списка телефонов всех сотрудников определенной должности в одном из отделов  
SELECT first_name, last_name, phone FROM Persons JOIN Numbers on person_id=Persons.id WHERE position = 'Intern' and department='R&D'
4. Добавление нового сотрудника  
INSERT INTO Persons (first_name, last_name, email, department, position, room) VALUES ('Vasya', 'Pupkin', 'vasya.pupkin@example.com', 'R&D', 'Intern', 42)
5. Перемещение сотрудника в другой отдел со сменой комнаты  
UPDATE Persons SET department='IT', room=43 WHERE id=1

Решено было использовать две таблицы, так как у каждого сотрудника может быть несколько телефонов. Все остальные поля единичные, поэтому их можно оставить в таблице сотрудников.
