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

# Answer

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


# What are the OAuth2 Grant Type and How they Work

# Answer

# 0. What is OAuth2 

A Specification i.e. website, PDF document created by representatives of large technology corporations like Google, Facebook, Microsoft, IBM, Salesforce, Amazon, Oracle and others. I am not sure if Apple took part as well. First they created OAuth1 and like Tech Companies always do followed the principle "Experts are the people who Complicate Simple Things". OAuth2 followed with simplifying the process. 

# 0. What service does OAuth2 provide

Authentication and Authorization. Authentication deals with verifying the user is the person trying to login and not a remote impersonted friend from far away countries. Authorization is the process of verifying that the authenticated user has permission to execute a service / perform a task. For example, I may have the permission to view some sales reports in an internal company website but my manager only has the permission to make the numbers look acceptable i.e. change the report for bosses higher up.

# 0. What is an OAuth2 Implementation

Some of these companies who took part in creation of the specification i.e. PDF Document, implemented their own OAuth2 service. For example, when you visit www.slideshare.com , if gives you an opportunity to login using your LinkedIn userid and password as if LinkedIn does a lot to protect / secure your username and password (It probably does now after an embarrassing  data breach six/seven yeacrs back) . That is your first introduction to OAuth2 without really knowing what goes underneath. 

# 1. OAuth2 Roles

	## A. Resource Owner : User
	## B. Resource Server : Google Mail / Gmail / BestBuy Product API, Your Company's Checkout REST API
	## C. Authorization Server : The Server issuing Access Token i.e. Facebook / Google
	## D. Client i.e. Browser based SPAs, Server Side Spring Boot / NodeJS Client, Machines, 
	
# 2. OAuth2 has different type of Grant Type because there are different types of use cases. There are lots of bullets but none of them silver colred.

# 3. Authorization Code Grant 

	A. This is for the type of third party applications that wants to leverage 
	Facebook / Google to provide authentication / authorization services instead 
	of providing their own , risking legal suites in case of hacking.
	
	B. These type of clients start with first registering themselves 
	with the Authorization Service Provider such as FaceBook
	
	C. When these applications, register they get two things among others
	
		I. A Client Identifier
		II. A Client Secret
		
	D. Registration is an one time activity and do not needs to 
	happen every-time the client uses the Auth Service
	
	E. As these types of clients need to keep a pair client identifier and the 
	client secret they typically runs in the server as browse javascript clients cannot keep secrets
	
	F. The clients in this grant type make two calls 
	
		I. First call to get an Auth Code from the Auth Server
		II. The second call using the Auth Code received from the first call, 
		gets the client their actual access token. The access token is short lived 
		i.e. 15 minutes not 15 years.
		III. Finally clients make the actual service call i.e. get your friend list 
		from Facebook , using the access token
		IV. From time to time, client also make another call to the Auth Server 
		to refresh the access token

	G. Following are the parameters that the client sends for the auth code call i.e. first call HTTP GET
		
		I. response_type with the value code
		II. client_id with the client identifier
		III. redirect_uri : When the call to the auth server completes with success . 
		failure where should the Auth server redirect the client to
		IV. scope - Read Contacts, Add Contacts, Get Products, Add Product etc.
		V. state with a CSRF token - Croos Site Request Forgery (CSRF) Optinoal 
		but highly recommended to protect against all the gentlemen out there in the Internet
		
		
	H. When the Auth Server determines that the call paramaters sent in the above 
	call are all valid, it send an auth code with the CSRF token back to the client reditect_uri
	
	I. The client should match the value of the CSRF token sent 
	back by the Auth Server with the one it originally sent to the Auth Server<
	
	
	J. Now that the client has the Auth Code, it needs the access token and for that 
	it will make a second call HTTP POST with the following paramaters
	
		I. grant_type with the value of authorization_code
		II. client_id with the client identifier
		III. client_secret with the client secret
		IV. redirect_uri with the same redirect URI the user was redirect back to
		V. code with the authorization code received from the first call
		
	K. Finally the Auth Server responds to the second call with the following
	
		I. token_type with the value Bearer
		II. expires_in integer for the TTL value
		III. access_token the access token itself
		IV. refresh_token to renew the access token 
		
	L. Now the client is ready to make the actual resource data call to serve its userbase. 
	It sends the access token as a paramater with this call.
	
	M. The client also sets a timer to get notified a little before the access 
	token goes to expires and goes to heaven. In that timer event, the client 
	may decide to make the call to the Auth Server with the refresh 
	token to get a new access token
	
	
# 4. Implicit grant is for Browser based JavaScript Single , Double, Tripple or Multiple Page Applications for which the entire world including all Hackers can see the JavaScript Code and constants like client identifier and client secret being used.

	A. As these type of open to the world applications, cannot keep and use a client 
	identifier and client secret, they do not involve the call to first get an Auth Code
	
	B. Theses clients make a SINGLE call to the Auth Server and get their access token directly.
	
	C. Following paramaters are sent to the Auth Server by the user agent (browser) 
	based JavaScript Applications
	
		I. response_type with the value token. NOTE THE DIFFERENCE HERE. 
		Auth Flow sends this as "code" not token
		II. client_id with the client identifier
		III. redirect_uri : When the call to the auth server completes with success . 
		failure where should the Auth server redirect the client to
		IV. scope - Read Contacts, Add Contacts, Get Products, Add Product etc.
		V. state with a CSRF token - Croos Site Request Forgery (CSRF) Optinoal 
		but highly recommended to protect against all the gentlemen out there in the Internet
		
	D. Finally the Auth Server responds to the second call with the following
	
		I. token_type with the value Bearer
		II. expires_in integer for the TTL value
		III. access_token the access token itself
	E. This Implicit Grant does not return a refresh token because the browser has 
	no means of keeping it private
	
	F. Now the JavaScript can make actual functional calls to the resource server 
	using the access token it received from the Auth Server.
	
	E. When the Resource Server gets a call from its clients, it validates the access t
	oken with the Aiuth Server and when the validation goes well, it responds data to the clients.
	
# 5. Resource owner credentials grant or Resource owner Password credentials grant

	A. This is the weakest of all the OAuth2 flows.
	
	B. This is one way of integrating your legacy applications with OAuth2
	
	C. This is applicable when the company that owns the Resource Server also 
	owns the Clients. Clients can be Web Apps, native mobile apps or JavaScript Apps
	
	D. The client first asks a username and password from the resource owner
	
	E. The client then sends a POST request to the Auth Server along with the following
	
		I. grant_type with the value password
		II. client_id with the the client’s ID
		III. client_secret with the client’s secret
		IV. scope with a space-delimited list of requested scope permissions.
		V. username with the user’s username
		VI. password with the user’s password
	
	D. The Auth Server validates the username and password and responds with
	
		I. token_type with the value Bearer
		II. expires_in with an integer representing the TTL of the access token
		III. access_token the access token itself
		IV. refresh_token a refresh token that can be used to acquire a new access token 
		when the original expires
		
# 6. Client credentials grant

	A. This grant type of ideal for IoT devices or any other client machines that needs to access some servers.
	
	B. As all the machines can use one permission and a specific user's permission is 
	not required, this is rhe simplest of all OAuth2 flows like
	
	C. Machines send a POST request with the following
	
		I. grant_type with the value client_credentials
		II. client_id with the the client’s ID
		III. client_secret with the client’s secret
		IV. scope with a space-delimited list of requested scope permissions.
		
	D. The Auth Server responds with the following
	
		I. token_type with the value Bearer
		II. expires_in with an integer representing the TTL of the access token
		III. access_token the access token itself

# 7. Summary

	A. Third party Server Side Applications from Startups / reluctant / unwilling to 
	invest in Authorization Service - Use Auth Code Grant Type
	
	B. Third party Client Side JavaScript Applications from Startups reluctant / unwilling 
	to invest in Authorization Service - Use Implicit Code Grant Type
	
	C. Legacy Applications that owns the Client Application as well - Use Resource Owner Password Grant Type
	
	D. Do not have a Heart, consider yourself a Machine - Use Client Credentials Grant Type
	
# How does Spring Security be implemented in Microservices. 

Microservices may need Authentication and Authorization features. Spring Boot is the Michael Jordan of Microservices. If you are lucky, you have implemented your Microservices in Spring Boot as Spring Boot has the most number of supporting libraries (over 40) for Microservices. Spring Security is one of those highly popular libraries even though it is quite old. Spring Security has kept an excellent pace with time and provides an excellent implementation for all the OAuth2 grant type / flows. We may also need API Security based on Json Web Token (JWT) and again Spring Security goes a long way to keep you secured there. Here is an example that shows how to integrate an angular 6 client with Spring Boot 2 REST API. https://github.com/binitdatta/rollingstone-spring-security. I worked on this POC with another highly talented engineer called Rohan Grover and forked it to do some UI enhancement which is pending. 

NOTE: If you are not lucky and have not chosen Spring Boot (all the other guys are just REST APIs and nothing else and that includes DOT NET, NodeJS, PHP and any other language / framework under the sun. However, with DOT NET we can use the https://steeltoe.io/ to get the benefits.), you can create a wrapper Proxy API in Spring Boot to provide security. 

# Does internal Microservice to Microservice calls require authentication

Think about a huge house with 20 rooms. Imagine each room as a Microservice. Only the front door Microservice i.e. Main Gate, needs security, right? Rooms inside the house do not. Microservice REST APIs are very similar. Security or not, our clients should never ever be forced to call hundreds of separate Microservices. Never. We should instead create an API Gateway on our own implementing Spring Cloud Zuul or Spring Cloud API Gateway or we can use a Vendor's implementation of API Gateway like Amazon, Azure, Google, APIGEE and others. It is at that API Gateway layer your clients will be authenticated. For custom implementations, we can imagine the Spring Cloud Zuul / API Gateway implementing Spring Security. Individual Microservices better be exposed only through the API Gateway like our inner rooms of the large house.

# What does it mean being Cloud Native

# Answer

Cloud Native is a term that we keep hearing repeatedly these days irrespective of our (technical / non-technical) roles in the IT industry. I feel the secret of an apparently confusing and cryptic technical term is to understand the English meaning of the term(s). Imagine being a plant on planet earth. The basic nature of the plant is to generate food through photosynthesis using Sunlight and Chlorophyll. The plant does this on sunny days and surprisingly the plant does the same on Cloudy days. So the plant does not to need to see the Sun in order feed itself. 

Now, let us draw a parallel between the plant and the applications that we deploy. In the past, our application always needed to directly see hardware and system software. Without hardware and system software (like OS, Application Container like Tomcat etc) being made available to them, they simply won't run. That is not how nature works though. Our applications needed to run even if they cannot see where the hardware and system software are coming from. Like a plant does not care where the sunlight is coming from, (from a clear sky or a cloudy one), it generates food. Our application should be able to run whether they are running on physical hardware, virtualized hardware (when physical hardware is shared between multiple Operating Systems), or if they are coming from something else like a Docker Container (more on that later). Why this is so? Because our applications have no direct love for direct hardware. All it needs is a layer to make system calls for memory, disk, networking and CPU. If these system resource calls can be intercepted by whatever intermediate layer (hardware device drivers, software Hypervisor, docker engine etc.), our application won't care and run smoothly. This is exactly the Cloud providers internally and in public cloud leverage to help us migrate our applications to Cloud. They isolate our applications from physical hardware, buy physical hardware on massive and cheap scale, share the physical hardware among all customers. The model is centuries old. Imagine you and your neighbor having your on electricity generation plant vs getting electricity from the utility company. If we can share physical electricity generation hardware for energy, we can do the same for our software applications.

Now, let us come to the second term which is native. English language comes to the rescue again. If someone is a native of Mexico or China, he/she is natively capable of speaking Spanish and Chinese respectively. Now imagine the Cloud as a country in the Internet. The Cloud country has a language of its own which says

A. The machines (CPU, Memory, IO) that power me can stop working anytime. They are cheap and commodity hardware and that is why so affordable.
B. The disks that provide storage are as vulnerable.

What these native properties of the Cloud country means is that applications running on Cloud should expect underlying resource failure. Say a Web Application is running on premise and is deployed to expensive IBM hardware. The application code directly hard codes the log file location to generate application logs. When this application is migrated to the Cloud, the knowledge of this hardcoded disk path location is bad for the application as the cloud is not guaranteed to provide 24/7 availability of any hard dependency. 

Another popular grammer that the Cloud language expects application to know, is being stateless. Being the opposite is bad even on non cloudy sunny days. Why the cloud dislikes stateful applications? Because of the same vulnerable and cheap hardware powering the cloud again. If between multiple calls of a stateful application, the hardware on which the app is running decides to take a vacation i.e. stop working, then the application team would be restless even if they are not stateless. Short term memory loss and dementia are bad for humans but they are good for Cloud applications. Applications, targeted for Cloud deployment, should not remember anything between calls to be Cloud Native.

Like I mentioned two here, being Cloud native means we (our applications) learn the grammer of the language spoken in the Cloud country. So teaching the language spoken in the Cloud country to our applications before they are migrated to the Cloud is known as the process of being Cloud Native. Cloud Native Experts are skilled to lecture elaborately to customers about what Cloud Native means but this is the underlying truth. Once we know them clearly, we can work better with experts . 

# Data Persistance in Microservice  : Standalone Database or a Shared one, Which one is best?

# Answer

The super short answer is that it depends. The idea of Microservices was coined by noted Computer Scientist Martin Fowler (https://martinfowler.com/articles/microservices.html#CharacteristicsOfAMicroserviceArchitecture). Fowler proposes that each Microservice has its own dedicated database. Since then, the idea of a dedicated database for each Microservice has been written about in hundreds of related books, blogs , official Wiki pages from early adapter companies.

Apart from Mr. Fowler, the other significant contribution towards the Microservices architecture came from the company Netflix. Not only they invested and later open sourced a significant number libraries implementing the Microservice ecosystem, their success using the Microservices architecture were keenly observed by CIOs across multiple business verticals. 

One aspect that has to be noted about the practical Microservice role model i.e. Netflix is that the company was new and a startup (not anymore). They had a free had, did not have to deal with decades old legacy systems to deploy new systems in production. That single fact gave them significant momentum in creating a Microservice based system. As with all of us, we follow other people success more than we understand their challenges, situation or the same of our own.

When we try to repeat the same Microservice success story in Banks, Insurance, Healthcare, Manufacturing and other major business verticals that are decades if not centuries old, we face a significantly different challenge. Let us try to understand these challenges using an example.

How legacy companies such as Banks, Insurance and Healthcare are different from the types of Netflix is that they have invested millions of dollars over the years in building a very complex Enterprise Date Warehouse, ETL systems, Master Data Management (MDM) products etc. In such interconnected companies, the output of one applications is frequently the input of another. These companies also have budget limitations from from money and time perspectives. When Netflix decides to have a single dedicated database for each of its Microservices, that is easy because there are hardly any downstream system they would break by that decision. When a large bank tries to apply the same design criteria with a say 15 millon dollar and within next 8 months budget to convert one monolithic application into Microservices Architecture, they come quickly to the unpleasant reality that this decision breaks their EDW and ETL process and they may need another 30 million to replace the EDW datasources apart from the huge impact on their business users of those EDW / BI systems. Architects who would readily suggest the Netflix architecture for a legacy Bank, Healthcare and Insurance company are probably not aware the enterprise legacy bottlenecks and the impact on his/her decision on them.

However, the Microservices architecture even if it can be applied 80 percent in a legacy company without following the dedicate database dictat, delivers a huge gain in efficiency few large companies can and should ignore. The original pain that gave birth to the Microservices architecture are 

# A. The long time it takes to deploy monolithic application. 

# B. The other idea that drove the Microservice movement is one small error in one part of a large monolithic application impacting other healthy parts.

Seeing from these two aspects, the Microservice migration projects in any type of company is a business driven project not  technology driven one, even though a lot of people understand Microservice projects solely from the technology used. That is a mistake, though. Even after using the best breed of technologies used, if the organization does not realize faster time to market with new features deployment and strict resource boundaries protecting good services from bad ones, the entire project may do little to realize the business objectives.

The solution is to take a middle path. Microservice migration projects that converts large monolithic applications into smaller services following the right sized API boundaries delivers huge gains to the business organization even if they use a single shared database but lives no impact on other downstream systems. The projct may remain on time and cost budget and may actually encourage the CIO to commission the project rather than discarding it when presented with the added complexities of converting the downstream EDS systems along with the target system. 

At the same time, legacy organizations, may do well to work actively from moving away (at their own pace) from legacy EDW systems to modern loosely coupled real time streaming based analytics, Big Data and NoSQL platfroms to reduce the impact of changing an upstream system on the downstream ones.

As we may realize that there are lots of bullets but none of them, colored "silver" which tells us that the "Netflix" story may not be entirely applicable to a 100 years old Bank, even though large parts of it could be.

