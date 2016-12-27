# Trabajo realizado
- Se ha añadido una nueva dependencia al proyecto. Esta dependencia es el conector MySql, que sera necesaria en tiempo de compilacion

# Introduccion a Maven
### Creación de un nuevo proyecto
Para crear un proyecto maven tenemos que escribir en consola lo siguiente: 

```mvn -B archetype:generate -DgroupId=com.egc.app -DartifactId=mavenproyect```

### Comandos básicos
Lo compandos que podemos ejecutar en maven son los siguientes:

```mvn compile``` – compila el proyecto y deja el resultado en target/classes

```mvn test``` – compila los test y los ejecuta

```mvn package``` – empaqueta el proyecto y lo dejará en taget/autentiaNegocio-1.0-SNAPSHOT.jar

```mvn install``` – guarda el proyecto en el repositorio

```mvn clean``` – borra el directorio de salida (target)
### Scopes
El scope sirve para indicar el alcance de nuestra dependencia. Hay 6 tipos:

```compile``` - es la que tenemos por defecto sino especificamos scope. Indica que la dependencia es necesaria para compilar. La dependencia además se propaga en los proyectos dependientes.

```provided``` - Es como la anterior, pero esperas que el contenedor ya tenga esa libreria. Un claro ejemplo es cuando desplegamos en un servidor de aplicaciones, que por defecto, tiene bastantes librerías que utilizaremos en el proyecto, así que no necesitamos desplegar la dependencia.

```runtime``` - La dependencia es necesaria en tiempo de ejecución pero no es necesaria para compilar.

```test``` - La dependencia es solo para testing que es una de las fases de compilación con maven. JUnit es un claro ejemplo de esto.

```system``` - Es como provided pero tienes que incluir la dependencia explicitamente. Maven no buscará este artefacto en tu repositorio local. Habrá que especificar la ruta de la dependencia mediante la etiqueta <systemPath>

```import``` - este solo se usa en la sección dependencyManagement. Lo explicaré en otro artículo sobre transitividad de dependencias.

