SpringApplication.run -> Creates a container to run the application.

Spring has its own container inside JVM named IoC Container/Spring Container.

To create object using Spring Boot / To get the object from the Ioc Container -> 
* The type of the IoC container inside JVM is ApplicationContext.
*  run method from SpringApplication.run returns the object of ConfigurableApplicationContext.
* This ConfigurableApplicationContext class extends the interface named ApplicationContext.
* Which means the run method is returning the object of ApplicationContext.
*This means I already have the object which is coming from the run method.

To tell Spring to create object of a specific class :
On top of the class, which classes object is required,

@Component

This keyword has to be added to tell Spring framework to create the object of that class.



-------------------------- Another Video Starts --------------------------



Autowiring

Annotation: @Autowired

What this does is, it connects Dev class to the Laptop class. Dev is depended on Laptop class so when object of Dev class is being created, at the same time object of the Laptop class will be created too.

Scenario:

* If Dev class contains the Laptop classes private variable to create the object, this scenario is called "Field Injection". In this case, annotation @Autowired is mandatory.

* If Dev class contains a parameterized constructor which takes an object of the Laptop class as a parameter this is called "Constructor Injection". In this case, annotation @Autowired is optional.

* If Dev class contains a set method to set the object of the Laptop class it is called "Setter injection". In this case, annotation @Autowired is mandatory.



BY DEFAULT SPRING FRAMEWORK SEARCH FOR CLASSES LIKE LAPTOP CLASS (A CLASS WHO HAS SUB-ORDINATE[DEPENDENT] CLASS) BY TYPE. MEANS SPRING SEARCH FOR THE CLASS TYPE NOT FOR THE CLASS NAME.


Spring gets confused if there are more than one bean. To avoid this confusion, an annotation is required on top of the class name.

Annotation: @Primary

In any case, if the above annotation is not liked to be used there is another annotation. This annotation is required inside the class and if there is @Autowired annotation this annotation will be placed under it and it takes the class name but with a small letter.

Annotation: @Qualifier("laptop")