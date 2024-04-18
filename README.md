# plantilla-spring-boot
Exercises Use case. 
A travel company wants to have a hotel reservation system so that its clients can access it through a website. The client's data to make a reservation are: Name, email, paternal last name, tourist destination data, which is the city and name of the hotel, as well as the number of people in the room to be rented. The payment must also be established in the reservation, which It is only through a card, whose data is card name, balance, and card number. As a use case to guide you, use the following: “Reservation to Huatulco for two people at the Bahías Huatulco hotel, payment with a Banamex payroll card whose balance is 120,000 pesos in the name of Juan Carlos Campos whose email is rapidclimategmail.com.” Cost of the room for 2 people: 4000 pesos. Considering the above, develop the following.

1. With the help of Netbeans, create the necessary MySQL tables that have resulted from the analysis. Write the code to create the tables in the exam. VALUE 2 POINTS.
2. Using JPA, prepare the mapping of the tables. In the resulting entities (classes) implement the constructor that initializes the attributes of each entity. Write the code of the created constructors in the exam. VALUE 2 POINTS.
3. With the help of Hibernate, propose a DAO called DAOReration, which must have the following methods. to. A method called save that saves a reservation. Write the entire method code in the exam. VALUE 2 POINTS. 4. A method called findAll() that returns a generic array to all reservations. Write the entire reservation code on the exam. VALUE 1 POINT. c. A method called searchById(Integer id) that obtains a reservation based on the provided id. Write the code in the exam. VALUE 1 POINT. d. Create a Servlet that accepts the GET method and inside it invoke the reservation DAO and save from there the data given as a use case at the beginning of the exam. VALUE 2 POINTS.

Plantilla con Spring boot noviembre 2015
## Configuarcion inicial de las dependencias 
The first thing we need to do is configure and add the spring dependencies in the **pom.xml** file. You must add the following dependencies before closing the tag
```
<dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>io.spring.platform</groupId>
                <artifactId>platform-bom</artifactId>
                <version>1.0.1.RELEASE</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>

<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
</dependencies>
    <build>
        <resources>
            <resource>
                <directory>${basedir}/src/main/resources</directory>
                <includes>
                    <include>META-INF/**</include>
                    <include>public/**</include>
                    <include>**/*.properties</include>
                </includes>
            </resource>
        </resources>
    </build>
```
