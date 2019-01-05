# How can we create our own Spring Framework by following IOC

All frameworks in java uses the core building blocks offered by the Java language itself such as reflection plus another practice called the bytecode enhancing. Otherwise they heavily rely on the Java Enterprise edition technologies like Servlet and Filters. Without them being around, I had worked in projects where we ourselves wrote our own framework involving servlets and filters. However, our framework were not that advanced to handle IOC. So if we know the advanced design choices / requirements supported a framework like Spring, and we have deep expertise in the Java and Java Enterprise edition, we can build our own Spring Framework. One thing to keep in mind, though. Large open source frameworks like Spring is not the creation of a single person. Spring Framework has different modules and each module has several people contributing to the design and code.

Two things are cited very frequently in Spring Framework discussion and they are the # Dependency # Injection or DI and # Inversion of # Control or IOC. The secret of understanding the meaning of them is being really good with our English knowledge. The secret of understanding off all Information Technology, not just Spring,  is being good at English language and applying that knowledge in understanding technology. Now, lets consider DI or Dependency Injection. It is indeed a plain English phrase consisting of two words. The first word is Dependency and it means some object living or non living , that needs another object for birth, survival and proper functioning. As living human beings, we can say we have a dependency on Oxygen. I have a dependency on my morning coffee. Fish has a dependency on water. Plants have a dependency on Carbon DI Oxide to perform photosynthesis to make food etc. Life on earth has a dependency on the Sun. The example of dependencies experienced by us in the universe are plenty. 

Now, let us come to the second word, which is injection. It is another English word I came to know when I was a little child. When I used get a fever , some Doctor used that dreaded word to put a middle in my arms and called the painful process an injection. Coming back to the nature itself, nature uses plants to inject oxygen into the atmosphere which we then breathe. Nature also injects sunlight, water, soil, river, land into our living environment. We as living beings have not created any of the objects such as oxygen we need for living. Someone else injects them into the environment for us to use. 

As you may have noticed I have not used technology much till this point in the discussion. I did that because to prepare a context. Spring Framework borrows heavily from these natural environmental English language words / phrases and uses them for our benefit. It is naive to ignore the English meaning of technical terms when we try to understand technology. We can imagine objects living their life within the Java VM are very much like an animal living and being on earth. However, before Spring Framework existed, java application objects used to create their dependent object all by their own. This is similar to imagining I create my own oxygen to breathe, you do so for your own, Fish creates water, Cow creates grass, Tigers giving birth to deer before eating them and so on. So objects creating their own dependencies is not a natural concept but an artificial one. What is an example of an Object dependency? If we write a program to access and read data from a MySQL database our program will need a MySQL connection. If our program is used by a lot of people, we will need a pool of connection to MySQL. This MySQL connection / pool of connection is an object our data accessing program depends on. Without Spring , our program will create its own MySQL connection. With Spring, the framework itself will create these dependent objects like mother nature does for us and inject the MySQL connection to our program. 

# What is the advantage?

Say humans has a dependency of Oxygen. Oxygen is available in atmosphere on land and in water. However, our lungs cannot access the oxygen available from water. Fish can. So we fulfill our oxygen dependency by taking an oxygen tank with us during scuba diving under water. That oxygen tank is again not created by us but given or injected to us by the diving company. So we can fulfill the dependency requirement in multiple flexible ways if we are open to accept objects from outside environment. That is where dependency injection bring flexibility. Say  now that our program is ready and we need to test it. The MySQL DBA however is vacationing in Florida and will not return until next week. We can however, go ahead and tell Spring to inject a memory held Database connection like H2 and proceed with testing. If our program had hard coded the MySQL driver manager connection creation on startup instead of Spring injecting it to our program, our program would he hard dependent on the DBA returning from Florida and won't be able to test till then.

The next most important English term is Inversion of Control. It is another English phrase that starts with Inversion. What do we get when we invert the fraction 1/3? We get 3/1 or 3. So Inversion is the process of flipping (turning an object upside down) an object. When our program creates all its dependent objects, we say it has full control and all the lack of flexibility that comes with it. When Spring Framework takes the control away from out program, creates the dependent objects and injects them to our program, we call it Inversion of Control or IOC. As I said, the better we understand English language terms and phrases , the better we will understand information technology.

All that being said, not all program have the same dependency. Tigers can eat raw meat. Humans (most of them) have to cook meat before they are eaten. Some humans do not eat meat and call themselves vegetarians. Similarly, some program may access MySQL while others may access Oracle. Some other may access ActiveMQ or RabbitMQ. Some programs may need Jackson JSON processor or others may need Google's GSON. A REST Controller may need a Service while that Service may need a Data Access Object Repository. All these different dependencies need to be specified to Spring in some way. We have multiple ways of doing so in Spring. We can use old XML but it still works. We can also use Java configuration or we can use annotations. Spring reads these XML, annotations or java config and creates objects on our behalf and injects them to our program. 

# How does Apache Tomcat Processes Requests from multiple users?

# Answer 

Servlet containers like Tomcat / Jetty have a pool / collection of threads say 200. These pool of threads is created when the container starts. When individual user's request is received by the server, it picks a thread from that pool and that single thread is actually working only for that single user, waiting on IO, doing CPU processing etc. When the processing is complete, it is this thread that sends the user's response to the user and goes back to the pool to serve another user'

This model has some limitation when a lot of traffic comes to the server and the available threads are exhausted. Normally it is solved by creating a pool of the servlet container itself like 10 Tomcat server and putting them behind a load balancer. User first reach their LoadBalancer and the LB distributes the traffic to the pool of Tomcats.

# What is the difference between Aggregation and Composition in Object Oriented Programming

# Answer

All things that are Information Technology are present so vividly in real life, that we may do well to understand the English meaning of the term and look for real life examples. The word compose is present in the music industry since hundreds of years before it came to programming as composition. In the music industry, a music director composes songs from lyrics, notes, beats and instrument players. So when several smaller objects / things are combined together to form one object i.e. song, we say that song is composed of lyrics, notes, beats and other things.

Similarly in Object Oriented programming, which obviously came from life experiences of the creators, not the other way round, composition means using smaller things to make something bigger. So when we are using @Autowired for a Service class instance inside a Controller, we are making the controller using a service instance. We can also say the song has lyrics in real life, the controller has a service attribute in programming, A Cow has four legs in real life, the Cow class consists of an array of Leg objects etc.

Aggregation is about hierarchy / inheritance. Human children has their outer and inner organs which is composition. However, how these organs look and work may have been "aggregated" from the genes of their parents and grandparents. A Tiger inherits his Lung from his parent Tiger and Tigress, a Fish inherits his / her gills from his / her parent Fish, Mukesh inherited his wealth partly from Dhirubhai. Aggregation is all about summation as well. We add up genes from parents / grandparents on each side and arrive at a certain child . Similarly, rich parents of a certain child contribute their own money which is then "aggregated" in the child's wealth.

In programming, when we give birth to children by "extending" a parent class we call it aggregation. We extend an Animal class to create Tigers, Cows etc. But as the teeth of a Tiger is different from that of a Cow, we compose of different kinds of teeth in Tigers and Cows.

# How do we secure microservices

# Answer

Here is an working git repository for securing Microservices using an Angular 6 front end

https://github.com/binitdatta/rollingstone-spring-security

Take a look.

If you want to learn more about the theory , I can recommend a book called Spring Security Third edition from Pactpub.com. Look into Chapter 9 and Chapter 17 and you can ask question here if something is not clear from the book chapters.

# How does Spring Cloud Remote Config Client Work? Do they make a single or multiple calls to get properties

# Answer

You can check this out https://www.udemy.com/practical-world-java-spring-microservices/

As I showed the config service testing with a web browser that makes a HTTP call, the config client also makes the same call with the same argument and gets all properties in the same call. There are multiple ways to configure clients about changes on remote properties. First of all, some properties like database username and password etc, will not make sense for them get refreshed after start. The Spring Data JPA is configured to create the datasource, transaction and connection pool objects at the start. So some properties do need restarts irrespective of whether they are coming from local file or fetched remotely. Other properties such as message or error messages, internationalization properties etc, can be configured to either be refreshed manually or pragmatically . There is yet another way using spring-cloud-bus to send events to config clients whenever properties change on the remote server. This is the best setup as this will not need any manual handling.

# Shall we create a common project for all the Model / Domain objects shared by Microservices and let each Microservice have their own copy

# Answer.

We can certainly have all common model objects pulled together into a common utility java library , build it and push it as a jar to an internal Artifactory. A lot companies I know uses this method through an internally hosted Artifactory. All dependent applications can just have the repository configured and  have the common jar as a dependency. The con is less flexibility. When one of the Microservices needs an additional fields, every other service also has to change. The solution is if one application needs changes, it should use a local DTO and keep the common model object unchanged. As this is a tutorial, I did not go through the ARtifactory process as it would be a distraction from teaching Micro services.

# Shall we use Java 8 Optional Type in API Return types

# Anser

Optional is a Java 8 feature and while we can surely use it for internal operations, using it as return values may have some consequences if a java 7 or lower client is used to access the API. However, people who are still using java 7 or lower, should upgrade sooner than later now that Java is coming with a new version every six months.

# Why should we design out applications using interfaces

# Answer

Using interfaces everywhere makes our application flexible. Using a service interface for injecting services to controllers gives us an opportunity to have multiple different implementations and change the dependency injection either through spring profiles or very little code change. Like if we have two implementations of one service interface and each are annotated with @Service annotation, either we can comment out one implementation and spring will pick the other or we can use Qualifiers if we want both. Spring Profile also is a great help.

# What are Transactions?

# Answer

Transactions are implicit when we are dealing with one single record insert / delete and update etc. We do not need transaction in these situations as if that one statement fails, the consistency of the database won;t be impacted. When dealing with more than one record such as a account transfer involving at least two account, one from which we withdraw money and another to which we deposit money, transactions are needed. Why? As we are having two separate update statements for updating the two accounts, if one succeeds and the other fails, the database will be inconsistent. In such situation as we need to tell the database that both operations either fail or succeed together we create an boundary to tell the DB to treat them as a single transaction and monitor their success or failure together. It is very much lik the english meaning of the word transaction. When we buy things in the market, we pay money and the shop-owner give us the product. If we either do not pay for the product or we pay and the shop-owner does not give the product, the transaction between us and the shop-owner will be clean and there will be disputes.

Transactions in the technical world is just a common sense based implementation of the real world version.

# What is BOM in Java Maven Applications

# Answer

In general the BOM term came from the manufacturing world and it stands for Bill of Materials. It is a short form for listing all the spare parts of making a larger object like a Car. A BOM for a Car would include an engine, four tires, windows, rood and the rest of the items that make a car. In Maven / Gradle, we have situation where we need to control the versions of multiple dependencies centrally. So we define one dependenyManagement element and control the dependency version from there. All the other dependency then do not have to include a version element. For example, if you look into the pom.xml or build.gradle we are using in the project repositories, we have a dependencyManagement element for Spring Cloud and we include a version. Once we do that, all other actual dependencies like eureka or hystrix can be specified without a version.


