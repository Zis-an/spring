TO CREATE A SPRING PROJECT ( NOT A SPRING BOOT PROJECT )

NEW -> PROJECT -> MAVEN ARCHETYPE -> CATALOG (Internal) -> ARCHETYPE (org.apachemaven.archetypes:maven-achetype-quickstart)


* In the Spring there is no option/annotation called @Component.

* To get the IoC container in Spring, First of all, dependency has to be added in the pom.xml file. This dependency is available in Maven Repository Website -> Spring Context -> LTS Spring Context Dependency

* Then in IntelliJ IDEA, maven has to be reloaded in the pom.xml. In eclipse, it gets to be reload automatically (not sure).

* Have to make sure this Maven: org.springframework:spring-context:number.number.number gets to be installed inside External Libraries. Cause it will provide the object of ApplicationContext which stays inside the IoC container.

* Now the next thing is ApplicationContext is an interface. So, object of ApplicationContext can't be created. But as it is an interface, it has several classes which implements ApplicationContext and those classes can be used.



--------------------- Video 09 ---------------------

* Now the ApplicationContext's object need a xml file to make the object work so a xml file have to be created. Inside the resource folder this xml file will stay.

* How many beans are in the xml file, that many objects will be created inside IoC container.