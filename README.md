# Proyecto Maven

Para crear un proyecto maven tenemos que escribir en consola lo siguiente: 

```mvn -B archetype:generate -DgroupId=com.egc.app -DartifactId=mavenproyect```

Lo compandos que podemos ejecutar en maven son los siguientes:

```mvn compile``` – compila el proyecto y deja el resultado en target/classes

```mvn test``` – compila los test y los ejecuta

```mvn package``` – empaqueta el proyecto y lo dejará en taget/autentiaNegocio-1.0-SNAPSHOT.jar

```mvn install``` – guarda el proyecto en el repositorio

```mvn clean``` – borra el directorio de salida (target)
