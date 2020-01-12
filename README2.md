#### Resumen Ejecutuvo

El objetivo de este proyecto es ampliar la funcionalidad de un proyecto educativo llamado decide, que consiste en una plataforma de voto electrónico. Este proyecto tiene el fin de poder acercar al alumno a trabajar con proyecto que se podrán encontrar en un futuro cercano cuando desempeñe su actividad laboral, así como tratar de enseñar al alumno los métodos básicos de gestión de incidencias y código fuente que se llevan a cabo durante un proyecto software. Para más información acerca del proyecto Decide consulte la siguiente página: https://github.com/decide-moltres/decide

### Alcance del proyecto

Para llevar a cabo este aprendizaje en concreto se nos ha asignado uno de los submódulos que forma Decide.
En concreto en este grupo hemos desarrollado en módulo de votación implementado, funcionalidad que se exigía en el pliego de la asignatura, así como funcionalidad extra que nos han pedido otros grupos que tenían otros submódulos de Decide, que deseaban hacer operaciones con el submódulo voting. Esta funcionalidad se caracteriza por implementar las elecciones de primarias, senado y presidenciales, así como ofrecer una API Rest de Voting y Political Parties para que el resto e los módulos puedan usar toda la información a través de la consulta de una url.

### Tecnologías empleadas

En proyecto se ha seguido desarrollándose en las tecnologías en los que fueron creados en un principio, por lo que para el desarrollo hemos continuado usando Python en su versión 3.6, en el framework Django, y como base de datos hemos usado Postgres. También hemos empleado otras tecnologías como Travis, Heroku, Codacy, que se explican en el apartado tattal


## Indicadores del proyecto



Miembro del equipo  | Horas | Commits | LoC | Test | Issues | Incremento |
------------- | ------------- | ------------- | ------------- | ------------- | ------------- |  ------------- | 
[Pérez Barrera, Juan Luis](https://github.com/juanluisperez1) | -- | 10 | ZZ | 6 | 7 | Creación API Political Party 
[Aguza Barragán, Jose Manuel](https://github.com/Aguza5) | -- | 27 | YY | 5 | 14 | Creación de las Primary Elections 
[Ripoll Torejón, Pablo](https://github.com/PabloRT98) | -- | 24 | YY | ZZ | 10 | Creación de las Senate Elections 
[García Limones, Raúl](https://github.com/raugarlim) | -- | 19 | YY | 5 | 9 | Creación de las Presidenciales Elections y métedo de API de voting 
[Castro Cachero, Álvaro Juan](https://github.com/alvcascac) | -- | 7 | YY | 4 | 9 | Tipo de votación other, que incluyes repuestas yes/no auto generadas
**TOTAL** | --  | 90 | tYY | 20 | 49 | Implementación de las votaciones estipuladas en el pliego, añadiendo también una API para accerder a las votaciones 

  _**Anotación** en este apartado no hemos incluido las horas que cada miembro ha invertido en el proyecto puesto que consideramos que todos los miembros del equipo hemos invertido la misma cantidad de tiempo en cada una de las tareas que teniamos asignadas_
  
La tabla contiene la información de cada miembro del proyecto y el total de la siguiente forma: 
  * Commits: solo contar los commits hechos por miembros del equipo, no lo commits previos
  * LoC (líneas de código): solo contar las líneas producidas por el equipo y no las que ya existían o las que se producen al incluir código de terceros
  * Test: solo contar los test realizados por el equipo nuevos
  * Issues: solo contar las issues gestionadas dentro del proyecto y que hayan sido gestionadas por el equipo
  * Incremento: principal incremento funcional del que se ha hecho cargo el miembro del proyecto

### Integración con otros equipos

En este apartado citamos todos los equipos con los que hemos realizado la integración, cabe destacar que un principio intentamos realizar la integración continua con todos los módulos, pero por falta de comunicación, así como falta de la realización de nuestras peticiones, por su parte, no hemos podido integranos con el módulo de censo 

* Cabina(https://github.com/decide-moltres/decide-cabina-angular): Nos han realizado peticiones de una API para obtener las votaciones dado el id de un usuario parar ello le hemos facilitado una API para que pudieran ir probando  su desarrollo para ello desplegamos una versión del módulo voting en heroku en el cual se podía realizar llamdas a la API REST para hacer consultas consulta de los datos almacenados en Decide

* Visualización(https://github.com/decide-moltres/decide-visualizacion): Nos proporcionan los cambios en el repositorio general y nos intregamos con ellos a través de pull request

* Autenticación(https://github.com/decide-moltres/decide-Auth): Les hemos rrealizado unas series de peticiones, que nos han resuleto y nos las han commiteado directametne  anuestro repositorio puesto que eran imprecimdibles para seguir con el desarrollo de nuestro proyecto




#### Visión global del proceso de desarrollo 

En el siguiente apartado se dará una visión de los procesos seguidos durante el transcurso del proyecto.

Cabe destacar primer que nuestro grupo en este caso Moltres, esta organizado de la siguiente forma, contamos con una organización en Github en la cual nos encontramos todos los miembros del equipo Moltres. 

En esta organización cada subgrupo dentro del equipo Moltres posee un repositorio, en el cual implementan incrementos funcionales de cada submódulo del proyecto Decide. Junto a esto también apreciamos un repositorio decide a parte, en el cual se tiene como proyecto base para realizar la fusión de todas las funcionalidades y realizar la integración continua.

En nuestro caso, tenemos un repositorio al cual denominamos Voting, donde desarrollamos incrementos funcionales del submódulo Voting.

 
A la hora de realizar un cambio, podemos destacar tres tipos de cambios, incremento de funcionalidad en nuestro módulo que no necesita de cambios en otros módulos, incremento funcional que requiere de otros incremento funcionales de otro módulo en cuestión, por ejemplo, en nuestro caso un cambio así sería el siguiente, el equipo de cabina nos pide al módulo votación que hagamos una pequeña llamada a la API en la cual nos devuelva un usuario dada una votación y el último tipo de cambio, sería un incremento funcional que necesita de cambios en otro submódulo de Decide, pero este submódulo no está asignado a nadie.

Todos los cambios comparten la misma fase inicial que consiste en una pequeña reunión entre los miembros del equipo para discutir la funcionalidad a implementar, y decidir si esa tarea se realiza o no, en el caso de que el incremento funcional requiera de varios módulos se realiza una pequeña reunión en todos los miembros de ambos y se decide si  se aprueba el cambio.

A continuación describimos las características de los diferentes cambios

*Incremento de funcionalidad en nuestro módulo que no necesita de cambios en otros módulos

* Comenzaremos primero creando una issue en nuestro tablero de Github de nuestro repositorio de equipo, siguiendo las plantillas y convecciones estipuladas en el apartado Gestión de Incidencias y Gestión del Código Fuente. Una vez creada esa issue no se le puede asignar a ningún miembro del equipo y deberá ser aceptada por otro miembro del equipo, con el fin de poder verificar que la funcionalidad es una tarea asumible y tratar de evitar posibles errores futuros. Una vez la issue se encuentra en la columna de accepted ahí ya se le puede asignar a un miembro para esa tarea y que este comience a trabajar en ella. Cuando comience a trabajar en ella el miembro en cuestión deberá pasarla a la columna del tablero started, donde se encuentran las issues asociadas a tareas que han comenzado. 

Una vez el miembro tiene su tarea asignada, lo primero es estudiar si es una funcionalidad muy grande que va a requerir de la creación de una nueva rama en este caso la denominaremos featureXXX donde XXX es un nombre identificativo de la issue creada, (cabe resaltar que estas ramas se crean a partir de la rama develop, no de la rama master) o simplemente es un pequeño incremento funcional que se puede desarrollar en una de las ramas ya creadas. Una vez elegida ya la rama, el desarrollador realiza los cambios que requieran ese incremento funcional, mientras se realizan cambios pequeños que aporten en todo momento una versión correcta del proyecto el desarrollador podrá hacer commit según la guía de commits, utilizando las plantillas y asociándolas a la issue correspondiente, una vez que este finalice su tarea hará un push para reflejar sus cambios en el repositorio en remoto. Tras haber realizado el cambio la issue deberá ser traslada a la columna fixed, para posteriormente ser verificada por otro desarrollador y pasarla verified y cerrarla. En caso de que esa rama no requiera más cambios este desarrollador la fusionará con develop para llegar constatar sus cambios en la versión del proyecto de develop. Cuando encontremos en develop una versión estable del proyecto y todas a las ramas estén mergeadas y todo funcione correctamente se realizará un merge de la rama develop con la rama master. Para verificar este proceso de mergeo, se utilizan las herramientas de travis y codacy destacando que estas herramientas solo se utilizan en las ramas develop y master, una vez que hagamos un push a la rama de develop travis comenzará a hacer una build en la que instalará todas las dependencias del proyecto, correrá todos los test que aparecen en el proyecto así como realiza un coverage y se lo pasará a herramienta codacy para el posterior análisis del código.  Si este procedimiento ha realizado una build correcta... Finalmente, al mergear la rama develop con master se realizará el mismo procedimiento de Codacy y travis añadiéndole además el despliegue automatizado en heroku de la versión de master, además de esto cada push a la rama master se le asocia una reléase con el fin de tener un historial de versiones diferentes del módulo Voting siempre disponible. En el caso de que este no de una build verde se analizará el código en busca de los posibles errores, creando las issues que se considere necesarias para arreglar ese fallo hasta conseguir que este saque la build verde y poder seguir con el procedimiento normal. Una vez que tenemos la versión en la rama master y su etiqueta reléase asociada de manera estable, la mergeamos al repositorio común para poder tener integrados todos los módulos del proyecto Decide


*Incremento funcional que requiere de otros incrementos funcionales de otro módulo en cuestión.
 	
El procedimiento es exactamente al anterior excepto por pequeñas variaciones, entre ellas son el tablero donde se crea la issue en lugar de ser el nuestro personal es el tablero creado en el poyecto general de Decide, es entonces creamos la issues en el tablero en cuestión el equipo afectado decidirá si implentar la petición de cambio o no, en el caso de que decida implementar la petición este pasará esa issue a accepted, y seguirá con el procedimiento citado anteriormente.
En el caso de que no la acepte el equipo que propuso esa issue tendrá dos opciones implementar el cambio por si mismo, es decir tocar en ambos módulos el mismo equipo desarrollo, siguiendo la estrategia que encontramos más arriba, o finalmente descartar ese cambiar y no realizar la funcionalidad prevista.

A este matiz, se suma de que para que los grupos dispongan de esa funcionalidad existen dos maneras la citada anteriormente en la que el grupo que ha realizado la funcionalidad extra crea en el repositorio común a la que llama igual que su módulo y sube ahí la versión del proyecto con el cambio y os del módulo que la necesiten simplemente la mergean en su rama o bien también cabe la posibilidad de que esta parte sea muy necesaria y se vean los grupo involucrados a realizar un commit directamente al repositorio individual de cada submódulo.


*Incremento funcional que requiere de otros incrementos funcionales de otro módulo en cuestión, pero el grupo no está presente.

En este procedimiento de cambio cabe remarcar de a pesar de que influyan dos módulos diferentes, al no existir un equipo encargado de un submódulo, el cambio deberá ser realizado por el módulo que haya realizado esa petición de cambio. Siguiendo así los pasos estipulados en el primer punto de está sección


* Incremento funcional

El cambio de votación que vamos a proponer es añadir un nuevo tipo de votación al módulo de votación.


1º Se crea la issue correspondiente a esa tarea y la coloca en la columna new. La issue al ser una issue que añadirá nuevas características al sistema deberá usar la plantilla feat y rellenar los diferentes campos que aparecen al seleccionar la plantilla.

2º Una vez esa issue esta en new, otro del miembro del equipo la pasará a la columna accepted si considerá que le cambio es apropiado, con el fin de que autorizar a realizar esa tarea.

4º Seguido a esto el desarrollador se asignará a la tarea y podrá moverla a la parte de started cuando este decida ponerse a trabajar en la issue en cuestión

5º El paso siguiente sería elegir la ramas, en nuestro repositorio, las ramas se crean en función de las issues épicas y esta últimas a su vez referencian también a una o varias issues, en nuestro caso la tarea de añadir un nuevo tipo de voting referenciaría a 



 
 



