# FrameDiary

## Miembros del grupo L1-DFAM-10

1. Arias Jiménez, Paula
2. Márquez Villalba, Alejandro
3. Parraga Delgado, Hugo


## 1. Introducción al problema

La empresa FrameDiary busca desarrollar el ocio y la cultura, para lograr una gestión de biblioteca de películas. Una de sus actividades principales es hacer que los usuarios, mediante una red social, puedan registrar, valorar y organizar las películas que ven, compartir sus críticas y seguir a otros espectadores.

Sin este proyecto, los usuarios registran ahora mismo sus películas y reseñas sin ningún tipo de organización, ya sea en documentos de texto o en notas, lo que impide actualizar la información automáticamente. Esto supone un problema para los espectadores que quieran saber cuántas películas han visto, consultar qué películas han visto otros usuarios o cuándo se escribió una reseña.

Estos son algunos ejemplos que muestran la necesidad del sistema:

- Un usuario quiere saber qué comentarios han hecho sus amigos sobre las películas que ha visto.
- Un espectador quiere ver películas similares a las que ya ha visto.

El nuevo sistema debe ser fácil de usar. Debe permitir a los usuarios llevar al día lo que han visto, comentarios y listas de forma detallada, ofreciendo herramientas de interacción social, como seguir a otros usuarios y consultar sus críticas y recomendaciones.

Con este sistema, los usuarios podrán gestionar mejor sus películas de manera más organizada, planificar películas futuras, hacer críticas y consultar las reseñas de otros usuarios.


## 2. Glosario de términos


| **TÉRMINO** | **DESCRIPCIÓN** |
|---|---|
| **Diary** | Histórico donde se registran las películas vistas de forma cronológica (como un diario personal). |
| **Review** | Opinión o evaluación personal que un usuario deja sobre una película, generalmente acompañada de una puntuación. |
| **WatchList** | Permite organizar las películas pendientes de ver. |
| **Like** | Es una función en redes sociales que permite a los usuarios expresar aprobación, interés o apoyo por un contenido. |
| **Label** | Etiqueta asignada a un dato almacenado en un repositorio (por ejemplo, género, tema o idioma original de una película). |
| **Follower** | Usuario que tiene la posibilidad de ver tu actividad y tus reviews. |
| **Recomendación** | Sugerencias basadas en lo popular de esta semana, las novedades de tus seguidos y los gustos del usuario. |


## 3. Visión general del sistema

La idea del proyecto es la siguiente: promover el cine entre los usuarios mediante recomendaciones y críticas de otros espectadores.

### 3.1. Requisitos generales

**OBJ-001: Gestión de películas**

El programa debe almacenar las películas añadidas por el administrador en la base de datos y mostrarlas a los usuarios.

**OBJ-002: Gestión de directores**

El programa debe almacenar información del director, en concreto su nombre y apellidos, su fecha de nacimiento y su filmografía.

**OBJ-003: Gestión de usuarios**

El programa debe implementar funciones para la gestión de usuarios y la interacción entre ellos.

**OBJ-004: Gestión del diario**

El programa debe registrar por fecha las películas vistas por los usuarios para lograr una organización precisa del recuento de películas.

**OBJ-005: Gestión de reviews**

El programa debe almacenar y mostrar a los usuarios las reseñas de las películas.

**OBJ-006: Gestión de recomendaciones**

El programa debe recomendar películas en base a la popularidad, la actividad de los usuarios seguidos, los favoritos del usuario y la distancia entre películas, que se calcula conforme a los labels y directores en común.

### 3.2. Usuarios del sistema
- **Espectador:** persona que utiliza la app para registrar las películas que ha visto, quiere ver o está viendo. Puede dejar reseñas, calificaciones y comentarios. Sigue a otros espectadores con gustos similares.
- **Administrador:** persona que utiliza la app para gestionar las películas en la base de datos.
## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Dar películas de alta

**Como** administrador

**Quiero** añadir películas a la base de datos de la aplicación

**Para** que estén disponibles para las diversas funciones de la aplicación.

**Pruebas de aceptación**

- Se registra una película, se pide un listado de películas y aparece la película nueva.
- Se intenta dar de alta una película con título, director y año de estreno ya registrados y se recibe un mensaje de error.

#### R.F.02. Modificar datos de las películas

**Como** administrador

**Quiero** que los datos de las películas sean modificables

**Para** poder arreglar cualquier error en los datos almacenados de estas.

**Pruebas de aceptación**

- Se modifican los datos de una película, se pide un listado de películas y aparece con los datos modificados.
- No se permiten modificaciones que dejen sin valor algún dato.

#### R.F.03. Eliminar películas de la base de datos

**Como** administrador

**Quiero** poder eliminar de la aplicación películas que hayan sido registradas por error y/o no existan

**Para** que la aplicación muestre películas reales que la gente pueda ver y no sea difícil de usar.

**Pruebas de aceptación**

- Se elimina una película, se pide un listado de películas y aparece la película como eliminada.
- No se puede eliminar una película no existente.

#### R.F.04. Consultar el listado de películas

**Como** espectador

**Quiero** ser capaz de consultar el listado de películas de la aplicación

**Para** ver los detalles y las "reviews" que contenga esa película.

**Pruebas de aceptación**

- Se muestra un listado con las películas registradas en el sistema.
- En caso de buscar una película que no exista, no aparecerá en el listado.

#### R.F.05. Dar directores de alta

**Como** administrador

**Quiero** dar directores de alta

**Para** añadir sus películas a la base de datos y que esté disponible una biografía de estos y su filmografía.

**Pruebas de aceptación**

- Al registrar un nuevo director se muestra un listado con los directores y aparece el nuevo director.
- Al intentar registrar un nuevo director que ya está registrado se crea un mensaje de error.

#### R.F.06. Editar directores

**Como** administrador

**Quiero** modificar datos de los directores

**Para** mantener la información actualizada.

**Pruebas de aceptación**

- Al modificar los datos de un director, en el listado aparecerá el director con los nuevos datos.
- Al intentar modificar los datos de un director y dejar en blanco alguno de ellos, el sistema mandará un mensaje de error.

#### R.F.07. Eliminar directores

**Como** administrador

**Quiero** poder dar de baja directores en la aplicación

**Para** asegurarme de que ningún director es dado de alta por error.

**Pruebas de aceptación**

- Al eliminar un director, en el listado de directores aparecerá dicho director como eliminado.
- Si se intenta eliminar un director que no existe, el sistema mandará un mensaje de error.

#### R.F.08. Consultar directores

**Como** usuario

**Quiero** ver el listado de directores registrados en la aplicación

**Para** ver la filmografía de cada uno.

**Pruebas de aceptación**

- Se mostrará un listado con los datos de cada director.
- En caso de querer buscar un director que no exista, no aparecerá en el listado.

#### R.F.09. Asignar película a director

**Como** administrador

**Quiero** asignar a un director las películas que se registran en la aplicación

**Para** que la película quede guardada entre las obras de este director.

**Pruebas de aceptación**

- Se mostrará un listado con la filmografía del director y aparecerá la nueva película asignada.
- En caso de intentar asignar a una película un director que no existe se mostrará un mensaje de error.
- En caso de intentar asignar una película que no existe a un director se mostrará un mensaje de error.

#### R.F.10. Creación de usuarios

**Como** espectador

**Quiero** poder darme de alta y crear una cuenta en la aplicación

**Para** contribuir a la comunidad cinéfila y poder dar "reviews" de las películas que veo.

**Pruebas de aceptación**

- Se registra un nuevo usuario, se pide un listado de espectadores y aparece el nuevo espectador.
- Al registrarse en la aplicación con un correo electrónico que ya está en uso, se mostrará un mensaje de error.

#### R.F.11. Modificar datos de usuario

**Como** espectador

**Quiero** modificar los datos de mi perfil

**Para** mantener actualizada mi información.

**Pruebas de aceptación**

- Se modifican los datos de un usuario, se pide un listado de usuarios y aparece el usuario con los datos modificados.
- La modificación no será registrada si se deja algún campo obligatorio vacío.

#### R.F.12. Eliminar usuario

**Como** espectador

**Quiero** poder darme de baja en la aplicación cuando ya no me interese

**Para** que mis datos personales no se guarden en la aplicación.

**Pruebas de aceptación**

- Cuando se da de baja un espectador, se pide un listado de usuarios y aparece como eliminado.
- Si intento eliminar una cuenta que no existe, se mostrará un mensaje de error.

#### R.F.13. Consultar usuarios

**Como** espectador

**Quiero** tener disponible un listado con los usuarios registrados

**Para** ver sus perfiles y su actividad de visionado.

**Pruebas de aceptación**

- Se muestra un listado con los usuarios registrados en la aplicación.
- Un usuario no registrado no aparecerá en el listado.

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


