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

#### R.F.14. Seguir usuarios


**Como** espectador


**Quiero** que sea posible dar "follow" a otros usuarios


**Para** que sea posible la interacción entre usuarios y que en el "feed" me salgan películas populares entre otros usuarios.


**Pruebas de aceptación**


- Al seguir a un usuario, en el listado de usuarios seguidos aparece el nuevo usuario.
- En la lista de seguidores de este usuario aparecerá el nuevo seguidor.
- Al intentar seguir a un usuario que no existe o a un usuario que ya seguías se lanza un mensaje de error.


#### R.F.15. Dejar de seguir usuarios


**Como** espectador


**Quiero** dejar de seguir usuarios si no me interesan sus reseñas


**Para** no ver sus actualizaciones en mi feed.


**Pruebas de aceptación**


- Al dejar de seguir a un usuario, en el listado de usuarios seguidos dejará de aparecer dicho usuario.
- En la lista de seguidores de este usuario dejará de aparecer el antiguo seguidor.
- Al intentar dejar de seguir a un usuario que no existe o a un usuario que no seguías se lanza un mensaje de error.


#### R.F.16. Crear "review"


**Como** espectador


**Quiero** poder dar una valoración en forma de estrellas de entre 0.5 y 5 y poder dejar un comentario


**Para** dar mi opinión sobre las películas que voy viendo.


**Pruebas de aceptación**


- Al crear una "review" se pide un listado de "reviews" de dicha película y aparecerá la nueva.
- Si se intenta crear una "review" de una película que no existe, se mandará un mensaje de error.


#### R.F.17. Modificar "review"


**Como** espectador


**Quiero** poder modificar la valoración dada a una película o el comentario sobre la obra vista


**Para** mantener actualizadas mis reseñas sobre lo que pienso de las películas que voy viendo.


**Pruebas de aceptación**


- Al modificar una reseña de una película, en el listado de reseñas de dicha película aparecerá la reseña modificada.
- Al intentar modificar la reseña de una película dejando vacíos los datos se dará un mensaje de error.


#### R.F.18. Eliminar "review"


**Como** espectador


**Quiero** eliminar una "review"


**Para** que esta no salga en mi "Diary".


**Pruebas de aceptación**


- La "review" eliminada aparecerá como eliminada en el listado de reviews de la película.
- Si se intenta eliminar una "review" de una película a la cual no hemos hecho "review", el sistema mandará un mensaje de error.


#### R.F.19. Dar "like" a una "review"


**Como** espectador


**Quiero** mostrar mi nivel de acuerdo dando "like" a otra "review"


**Para** que esta tenga más peso sobre otras reseñas con menos "likes".


**Pruebas de aceptación**


- Al dar un "like" a una "review", en el listado de usuarios a los que les ha gustado la reseña aparecerá el like que hemos dado.
- Al intentar dar "like" a una "review" a la que ya le he dado like se mostrará un mensaje de error.


#### R.F.20. Añadir película a favoritos


**Como** espectador


**Quiero** tener una lista de películas favoritas


**Para** que estas sean las primeras que salgan en mi perfil.


**Pruebas de aceptación**


- Al añadir una película a favoritos, se mostrará en nuestro listado de películas favoritas.
- Al intentar añadir a favoritos una película que ya tengo en favoritos, se mostrará un mensaje de error.


#### R.F.21. Eliminar película de favoritos


**Como** espectador


**Quiero** que las películas que ya no considere favoritas puedan ser eliminadas de la lista


**Para** que la información y mis gustos estén actualizados.


**Pruebas de aceptación**


- Al eliminar una película de favoritos, en el listado de películas favoritas esa película aparecerá como eliminada.
- Al intentar eliminar de favoritos una película que no teníamos en favoritos, el sistema mostrará un mensaje de error.


#### R.F.22. Añadir película a mi "WatchList"


**Como** espectador


**Quiero** añadir las películas que tenga pensado ver


**Para** tenerlas todas organizadas en el mismo sitio a la hora de buscar qué ver en cines o plataformas.


**Pruebas de aceptación**


- Al añadir una película a mi "WatchList", esta se mostrará en nuestro listado de películas deseadas.
- Al intentar añadir a mi "WatchList" una película que ya tengo, el sistema envía un mensaje de error.


#### R.F.23. Eliminar película de mi "WatchList"


**Como** espectador


**Quiero** borrar de mi lista las películas que ya he visto o que ya no me interesan


**Para** no confundirme y no volver a ver una película que ya conozco.


**Pruebas de aceptación**


- Al eliminar la película de mi "WatchList", en el listado de películas deseadas no aparecerá dicha película.
- Al intentar eliminar de mi "WatchList" una película que no estaba en ella, se mostrará en pantalla un mensaje de error.


#### R.F.24. Añadir película a mi "Diary"


**Como** espectador


**Quiero** añadir las películas que haya visto


**Para** tenerlas todas organizadas en el mismo sitio a la hora de ver mi historial de visionado.


**Pruebas de aceptación**


- Al añadir una película a mi "Diary", esta se mostrará en nuestro listado de películas vistas.
- Al intentar añadir a mi "Diary" una película que ya tengo, el sistema envía un mensaje de error.


#### R.F.25. Eliminar película de mi "Diary"


**Como** espectador


**Quiero** borrar de mi diario películas que haya añadido por error


**Para** evitar confusiones y que la lista sea realista.


**Pruebas de aceptación**


- Al eliminar la película de mi "Diary", en el listado de películas vistas no aparecerá dicha película.
- Al intentar eliminar de mi "Diary" una película que no estaba en él, se mostrará en pantalla un mensaje de error.


#### R.F.26. Recomendaciones automáticas


**Como** espectador


**Quiero** que el sistema me recomiende películas en base a mis favoritas


**Para** tener una mayor variedad de películas que ver.


**Pruebas de aceptación**


- Una película de Christopher Nolan con respecto a otra película de Christopher Nolan tendrá 10 puntos.
- Una película de Christopher Nolan con respecto a una película de Greta Gerwig tendrá 0 puntos.
- Si la película "Interstellar" tiene 8 etiquetas en común con la película "Ad Astra", tendrá 16 puntos.
- Si "Interstellar" tiene 0 etiquetas en común con "Amélie", tendrá 0 puntos.


#### 4.1.1. Requisitos de información


#### R.I.01. Datos de usuario


El sistema almacena los datos de los distintos usuarios para gestionar la aplicación:


- Correo electrónico
- Contraseña
- Nombre
- Foto de perfil
- Biografía
- "WatchList"
- "Diary": una lista que mostrará las películas que el usuario ha registrado como vistas
- Lista de favoritos
- Seguidores y seguidos


**Pruebas de aceptación:**


- Se registra un usuario nuevo, se pide un listado de usuarios y aparece el usuario nuevo.
- Se modifican los datos de usuario, se pide un listado de usuarios y aparece el usuario con los datos modificados.
- Se elimina un usuario, se pide un listado de usuarios y aparece el usuario como eliminado.
- Se intenta registrar un usuario con un correo electrónico ya registrado y se recibe un mensaje de error.
- No se permiten registros ni modificaciones que dejen sin valor los datos de nombre, correo electrónico o contraseña.


#### R.I.02. Datos de películas


Guardamos los siguientes datos de las películas:


- Título
- Director
- Póster
- Sinopsis
- "Labels" (géneros y temas)
- Duración (en minutos)
- Idioma original (como label)
- Fecha de estreno


**Pruebas de aceptación:**


- Se registra una película nueva, se pide un listado de películas y aparece la película nueva.
- Se modifican los datos de la película, se pide un listado de películas y aparece la película con los datos modificados.
- Se elimina una película, se pide un listado de películas y aparece la película como eliminada.
- Se intenta registrar una película con el mismo título, director y año de estreno que otra ya registrada y se recibe un mensaje de error.
- No se permiten registros ni modificaciones que dejen sin valor algún dato.


#### R.I.03. Datos de director


El sistema almacena de cada director:


- Nombre
- Foto
- Breve biografía
- Fecha de nacimiento
- Su filmografía


**Pruebas de aceptación:**


- Se registra un director nuevo, se pide un listado de directores y aparece el director nuevo.
- Se modifican los datos del director, se pide un listado de directores y aparece el director con los datos modificados.
- Se elimina un director, se pide un listado de directores y aparece el director como eliminado.
- Se intenta registrar un director ya registrado y se recibe un mensaje de error.
- No se permiten registros ni modificaciones que dejen sin valor algún dato.


#### R.I.04. Datos de "reviews"


De cada reseña guardamos:


- Película
- Usuario
- Puntuación
- Comentario
- Fecha de publicación


**Pruebas de aceptación:**


- Se registra una reseña nueva, se pide un listado de reseñas y aparece la reseña nueva.
- Se modifican los datos de la reseña, se pide un listado de reseñas y aparece la reseña con los datos modificados.
- Se elimina una reseña, se pide un listado de reseñas y aparece la reseña como eliminada.
- Se intenta registrar una reseña ya registrada y se recibe un mensaje de error.
- No se permiten registros ni modificaciones que dejen sin valor algún dato.


#### 4.1.2. Reglas de negocio


#### R.N.01. Restricción de auto-seguimiento


Un usuario no puede seguirse a sí mismo.


#### R.N.02. Validación de puntuación de la review


El valor de la puntuación debe estar entre 0.5 y 5 estrellas.


#### R.N.03. Restricción del "like"


No se puede dar "like" a una "review" más de una vez.


#### R.N.04. Solo se puede hacer una "review" de una película que esté registrada en el "Diary"


Para poder hacerle una reseña a la película, es necesario haberla visto primero.


#### R.N.05. Una película solo puede tener asociados 8 labels como máximo


Por facilidad para el espectador, para tener de una forma más visible de qué va dicha película.


#### R.N.06. Cálculo de distancia entre películas


La distancia entre películas será calculada en base a 10 puntos si coincide el director (si tenemos 3 películas del mismo director, nos sumaría 30 puntos) y 2 puntos por cada etiqueta que tenga en común con las películas de la lista de favoritos. Se mostrarán las 10 películas que más puntos tengan con respecto a los favoritos del usuario.


#### 4.2. Mapa de historias de usuario (opcional)


#### 4.3. Requisitos no funcionales (opcional)


#### R.N.F.01. Usabilidad


La aplicación debe ser fácil de usar para que los usuarios puedan utilizarla de forma intuitiva.


#### R.N.F.02. Rendimiento


Se espera que la aplicación funcione de forma fluida y que los tiempos de espera sean mínimos.


#### R.N.F.03. Seguridad


Se garantiza la seguridad y protección de los datos de los usuarios.


#### R.N.F.04. Portabilidad


El sistema estará disponible para teléfonos y tablets, y habrá una opción web para usar en ordenadores y portátiles.


#### R.N.F.05. Escalabilidad


La aplicación soportará grandes aumentos y descensos de usuarios.


#### R.N.F.06. Mantenibilidad


El código debe ser claro y abierto para facilitar la sostenibilidad de la aplicación.


#### R.N.F.07. Datos en la nube


Los datos se guardarán en la nube para ser accesibles con facilidad desde distintos dispositivos.

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


