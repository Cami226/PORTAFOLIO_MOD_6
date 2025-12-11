# PORTAFOLIO_MOD_6



M6_Evaluación de portafolio[Actividad Evaluada]

Evaluación del módulo
Contexto del Proyecto

Formas parte del equipo de desarrollo de un sistema interno para una empresa que gestiona capacitaciones de personal. Se te ha encargado desarrollar una aplicación web en Spring Boot que permita:

Registrar cursos de capacitación

Gestionar instructores y empleados inscritos

Permitir autenticación y autorización con roles de usuario (admin y empleado)

Exponer servicios REST para integrar con otros sistemas internos

Administrar el proyecto utilizando un gestor como Trello, Jira o GitHub Projects


Requerimientos de la Aplicación

Panel de administración para gestionar cursos y asignar instructores

Panel de empleado para ver los cursos disponibles e inscribirse

Login con autenticación por rol (Spring Security)

Servicios REST para:

Consultar cursos disponibles

Registrar empleados a cursos

Acceso restringido a los endpoints según el rol

Administración del ciclo de vida del proyecto con tareas y sprints


Instrucciones

1. Gestión del ciclo de vida del proyecto con un gestor de tareas

Crea un tablero en Trello, Jira o GitHub Projects.

Agrega columnas como: Backlog, To Do, In Progress, Done

Define tareas para cada funcionalidad del proyecto.

Asigna tareas por roles y agrupa por etapas (planificación, desarrollo, pruebas, despliegue).

Toma capturas del tablero en diferentes momentos del avance.

2. Implementación con Spring Boot y Spring MVC

Inicializa el proyecto con Spring Initializr (usa Maven o Gradle).

Agrega las dependencias necesarias: spring-boot-starter-web, spring-boot-starter-data-jpa, spring-boot-starter-security, spring-boot-starter-thymeleaf (opcional).

Implementa controladores que gestionen vistas con Spring MVC:

/admin/cursos: Vista para gestionar cursos

/empleado/cursos: Vista para ver cursos disponibles

3. Capa de acceso a datos (Spring Data JPA)

Crea entidades: Curso, Empleado, Instructor, Inscripcion

Crea interfaces de repositorio extendiendo JpaRepository

Usa base de datos H2, PostgreSQL o MySQL

Asegúrate de aplicar relaciones entre entidades (OneToMany, ManyToOne, etc.)

4. Seguridad con Spring Security

Implementa sistema de login con usuarios y roles: ADMIN, EMPLEADO

Protege rutas:

Rutas /admin/** accesibles solo para ADMIN

Rutas /empleado/** accesibles para usuarios autenticados con rol EMPLEADO

Configura WebSecurityConfigurerAdapter (o SecurityFilterChain si usas Spring Security 6+)

5. Servicios REST para interoperabilidad

Expón endpoints REST para:

GET /api/cursos: Devuelve el listado de cursos disponibles

POST /api/inscripciones: Registra a un empleado en un curso

Configura el controlador REST (@RestController)

Asegura los endpoints con JWT o Basic Auth

Usa @CrossOrigin si deseas permitir peticiones desde clientes externos


Producto Esperado

Proyecto completo en Spring Boot con:

Controladores Web y REST

Repositorios JPA

Seguridad implementada

Tablero con tareas en gestor de proyecto

Base de datos con relaciones funcionando

Rutas protegidas por roles

Documentación con:

Diagrama de clases

Diagrama del flujo de navegación

Evidencia del uso del gestor de proyecto

Instrucciones para ejecutar el proyecto (README.md)
