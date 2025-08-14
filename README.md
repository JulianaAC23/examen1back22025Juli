# 📌 Examen 1 Backend2 

## 📝 Descripción del Proyecto
Este proyecto es para corregir y estructurar adecuadamente
una aplicación básica de Spring Boot, centrada en la capa de modelos, y establecer
correctamente la conexión a una base de datos relacional denominada develop_db.

---

## 🛠️ Errores Corregidos
Listado de errores encontrados en el proyecto y cómo fueron solucionados.

| Nº | Error detectado                                              | Causa                                                                        | Solución aplicada                                                                                                                                              |
|----|--------------------------------------------------------------|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | Error en Gradle (Clase Curso)                                | Falta el arcrhivo `pom.xml` donde se manejan las dependencias                | Se cambió la herramienta Gradle por Maven. Primero agregué las dependencias en pom.xml y luego Add as Maven Project y al final sincronicé el proyecto con Maven |
| 2  | @I (Clase Curso)                                             | Esta anotación no existe                                                     | Se cambió @I, por @Id, la cual es la correcta                                                                                                                  |
| 3  | @Ge (Clase Curso)                                            | Anotación incorrecta                                                         | Se cambió @Ge, por @GenerateValue, la cual es la correcta                                                                                                      |
| 4  | strategy = IDENTITY (Clase Curso)                            | Esta anotación para generar valores automáticos esta incompleta              | La anotación completa es @GenerateValue(strategy = GenerationType.IDENTITY)                                                                                    |
| 5  | private String nombre (Clase Curso)                          | Las variables tienen que terminar con ";"                                    | Se añade punto y coma al final: private String nombre;                                                                                                         |
| 6  | @JoinColumn(....); (Clase Curso)                             | Las anotaciones NO deben terminar con ";"                                    | Se quita el punto y coma al final de esta anotación: @JoinColumn(....)                                                                                         |
| 7  | Docente docente (Clase Curso)                                | Le hace falta el tipo y el punto y coma al final                             | Se corrige por: private Docente docente;                                                                                                                       |
| 8  | this.id = id; - this.nombre = nombre; (Clase Curso)          | Le hace falta los métodos Getter y Setter                                    | Se agregan los métodos Getter y Setter con la herramienta Generate -> Getter and Setter a: id, nombre y docente;                                               |
| 9  | @Entit (Clase Docente)                                       | Esta anotación esta incompleta                                               | Se corrige por la anotación correcta @Entity                                                                                                                   |
| 10 | No hay @Id (Clase Docente)                                   | Esta anotación hace falta para la clave primaria                             | Se añade la anotación @Id encima de @GenerateValue(...)                                                                                                        |
| 11 | No hay constructores vacios (Clase Docente)                  | Esto es buena práctica para que JPA pueda instanciarla                       | Se añaden los constructores vacios                                                                                                                             |
| 12 | Faltan algunos Getter y Setter en los campos (Clase Docente) | Los Getter y Setter están incompletos                                        | Se añaden los Getter y Setter faltantes                                                                                                                        |
| 13 | @Entit (Clase Usuario)                                       | Esta anotación esta incompleta                                               | Se corrige la anotación correcta: @Entity                                                                                                                      |
| 14 | strategy = GenerationType. (Clase Usuario)                   | Esta parte esta incompleta, le falta especificar el tipo                     | Se completa por: strategy = GenerationType.IDENTITY al ser clave primaria                                                                                      |
| 15 | @Colun (Clase Usuario)                                       | Esta anotación esta escrita de forma incorrecta en tres sitios               | Se escribe de forma correcta en los tres sitios: @Column                                                                                                       |
| 16 | private String contraseña; (Clase Usuario)                   | Falta de mapeo en la columna contraseña, por buena práctica por la letra "ñ" | Se mapea con @Column(name = "contraseña")...                                                                                                                   |
| 17 | this.id = id; this.nombre = nombre;.... (Clase Usuario)      | Faltan los Getter y Setter                                                   | Se agregan los métodos Getter y Setter con la herramienta Generate -> Getter and Setter                                                                        |
| 18 | TipoUsuario (Clase Usuario)                                  | Este enum aun no existe                                                      | Se crea la clase Enum donde están los tipos de usuarios: Estudiante, Docente y Familiar                                                                        |
| 19 | @Table(name = usuarios) (Clase Usuario)                      | Todas las tablas(clases u entidades) deben ser singulares                    | @Table(name = usuario)                                                                       |



---

## 🔌 Guía de Conexión a la Base de Datos
Pasos para configurar la conexión a la base de datos local con MySQL.

1. **Iniciar MySQL en XAMPP** 
2. **En XAMPP dirigirte a phpmyadmin por medio del bóton 'Admin'**
3. **En phpmyadmin irte a 'Nueva' base de datos en la columna izquierda**
4. **Ponerle el nombre a la base de datos en este caso: develop_db y darle al botón Crear**
5. **Configurar la base de datos en 'application.properties'**
   Poner el username: root, este es el que maneja MySQL por defecto
   Poner password: (vacia) ya que no se tiene una
   poner la url con el nombre de la base de datos
6. **Ejecutamos la aplicación para crear la columnas en la base de datos**
7. **Cuando se termine de ejecutar veremos este mensaje al final en la consola 'Started Examen1Back2Application in 8.485 seconds (process running for 9.663)'**
8. **Vamos a phpmyadmin, actualizamos la páginas y veremos que nuestras columnas: 'curso, docente y usuario' , ya están creadas** 
   


## 📝 Recomendaciones 
Este plantilla se realizó con ayuda de Inteligencia Artificial.