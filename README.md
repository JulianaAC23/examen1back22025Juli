# 📌 Examen 1 Backend2 

## 📝 Descripción del Proyecto
Este proyecto es para corregir y estructurar adecuadamente
una aplicación básica de Spring Boot, centrada en la capa de modelos, y establecer
correctamente la conexión a una base de datos relacional denominada develop_db.

---

## 🛠️ Errores Corregidos
Listado de errores encontrados en el proyecto y cómo fueron solucionados.

| Nº | Error detectado                                              | Causa                                                                        | Solución aplicada                                                                                                                                      |
|----|--------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | Error en Gradle (Clase Curso)                                | Falta el arcrhivo `pom.xml` donde se manejan las dependencias                | Se cambió la herramienta Gradle por Maven. Primero agregué las dependencias en pom.xml y luego Add as Maven Project y al final sincronicé el proyecto con Maven |
| 2  | @I (Clase Curso)                                             | Esta anotación no existe                                                     | Se cambió @I, por @Id, la cual es la correcta                                                                                                          |
| 3  | @Ge (Clase Curso)                                            | Anotación incorrecta                                                         | Se cambió @Ge, por @GenerateValue, la cual es la correcta                                                                                              |
| 4  | strategy = IDENTITY (Clase Curso)                            | Esta anotación para generar valores automáticos esta incompleta              | La anotación completa es @GenerateValue(strategy = GenerationType.IDENTITY)                                                                            |
| 5  | private String nombre (Clase Curso)                          | Las variables tienen que terminar con ";"                                    | Se añade punto y coma al final: private String nombre;                                                                                                 |
| 6  | @JoinColumn(....); (Clase Curso)                             | Las anotaciones NO deben terminar con ";"                                    | Se quita el punto y coma al final de esta anotación: @JoinColumn(....)                                                                                 |
| 7  | Docente docente (Clase Curso)                                | Le hace falta el tipo y el punto y coma al final                             | Se corrige por: private Docente docente;                                                                                                               |
| 8  | this.id = id; - this.nombre = nombre; (Clase Curso)          | Le hace falta los métodos Getter y Setter                                    | Se agregan los métodos Getter y Setter con la herramienta Generate -> Getter and Setter a: id, nombre y docente;                                       |
| 9  | @Entit (Clase Docente)                                       | Esta anotación esta incompleta                                               | Se corrige por la anotación correcta @Entity                                                                                                           |
| 10 | No hay @Id (Clase Docente)                                   | Esta anotación hace falta para la clave primaria                             | Se añade la anotación @Id encima de @GenerateValue(...)                                                                                                |
| 11 | No hay constructores vacios (Clase Docente)                  | Esto es buena práctica para que JPA pueda instanciarla                       | Se añaden los constructores vacios                                                                                                                     |
| 12 | Faltan algunos Getter y Setter en los campos (Clase Docente) | Los Getter y Setter están incompletos                                        | Se añaden los Getter y Setter faltantes                                                                                                                |
| 13 | @Entit (Clase Usuario)                                       | Esta anotación esta incompleta                                               | Se corrige la anotación correcta: @Entity                                                                                                              |
| 14 | strategy = GenerationType. (Clase Usuario)                   | Esta parte esta incompleta, le falta especificar el tipo                     | Se completa por: strategy = GenerationType.IDENTITY al ser clave primaria                                                                              |
| 15 | @Colun (Clase Usuario)                                       | Esta anotación esta escrita de forma incorrecta en tres sitios               | Se escribe de forma correcta en los tres sitios: @Column                                                                                               |
| 16 | private String contraseña; (Clase Usuario)                   | Falta de mapeo en la columna contraseña, por buena práctica por la letra "ñ" | Se mapea con @Column(name = "contraseña")...                                                                                                           |
| 17 | this.id = id; this.nombre = nombre;.... (Clase Usuario)      | Faltan los Getter y Setter                                                   | Se agregan los métodos Getter y Setter con la herramienta Generate -> Getter and Setter                                                                                                                                                       |
| 18 |                                                              |                                                                              |                                                                                                                                                        |



---

## 🔌 Guía de Conexión a la Base de Datos
Pasos para configurar la conexión a la base de datos (ej. MySQL, PostgreSQL, etc.).

1. **Instalar la base de datos** (indicar versión recomendada).
2. **Crear la base de datos**:
   ```sql
   CREATE DATABASE nombre_bd;


## 📝 Recomendaciones 
Este plantilla se realizó con ayuda de Inteligencia Artificial.