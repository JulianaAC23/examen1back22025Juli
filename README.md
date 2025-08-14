# 📌 Nombre del Proyecto

## 📝 Descripción del Proyecto
Este proyecto es para corregir y estructurar adecuadamente
una aplicación básica de Spring Boot, centrada en la capa de modelos, y establecer
correctamente la conexión a una base de datos relacional denominada develop_db.

---

## 🛠️ Errores Corregidos
Listado de errores encontrados en el proyecto y cómo fueron solucionados.

| Nº | Error detectado       | Causa                                                         | Solución aplicada                                                                                                                                               |
|----|-----------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | Error en Gradle       | Falta el arcrhivo `pom.xml` donde se manejan las dependencias | Se cambió la herramienta Gradle por Maven. Primero agregué las dependencias en pom.xml y luego Add as Maven Project y al final sincronicé el proyecto con Maven |
| 2  | @I                    | Esta anotación no existe                                      | Se cambió @I, por @Id, la cual es la correcta                                                                                                                   |
| 3  | @Ge                   | Anotación incorrecta                                          | Se cambió @Ge, por @GenerateValue, la cual es la correcta                                                                                                       |
| 4  | strategy = IDENTITY   | Esta para generar valores automáticos esta incompleta         | La anotación completa es @GenerateValue(strategy = GenerationType.IDENTITY)                                                                                     |
| 5  | private String nombre | Las variables tienen que terminar con ";"                     | Se añade punto y coma al final: private String nombre;                                                                                                          |
| 6  | @JoinColumn(....);    | Las anotaciones NO deben terminar con ";"                     | Se quita el punto y coma al final de esta anotación: @JoinColumn(....)                                                                                          |
| 7  | ...                   | ...                                                           | ...                                                                                                                                                             |



---

## 🔌 Guía de Conexión a la Base de Datos
Pasos para configurar la conexión a la base de datos (ej. MySQL, PostgreSQL, etc.).

1. **Instalar la base de datos** (indicar versión recomendada).
2. **Crear la base de datos**:
   ```sql
   CREATE DATABASE nombre_bd;


## 📝 Recomendaciones 