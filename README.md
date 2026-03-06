# udemy-microservices-springboot-docker-kubernetes-microservices-section7
### Create MySQL Docker images and containers
* Create the accountsdb database: 
`docker run -p 3306:3306 --name accountsdb -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=accountsdb -d mysql`<br>
* Create the loansdb database: 
`docker run -p 3307:3306 --name loansdb -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=loanssdb -d mysql`<br>
* Create the cardsdb database: 
`docker run -p 3308:3306 --name cardsdb -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=cardsdb -d mysql`<br>
* Install SQLectron and create three connections for the three databases created above. Start the configserver and three microservices, and check the tables created in the SQLectron. 
* Test the CRUD operations by using Postman. <br>
Example 1<br>
Name: CreateAccount <br>
Method: POST <br>
Url: http://localhost:8080/api/create <br>
RequestBody:
{
    "name": "Madan Reddy",
    "email": "tutor@eazybytes",
    "mobileNumber": "4354437687"
} <br> 
Example 2:
Name: CreateCard <br>
Method: POST <br>
Url: http://localhost:9000/api/create?mobileNumber=4354437687 <br>
Example 3: <br> 
Name: CreateLoan <br>
Method: POST <br>
Url: http://localhost:8090/api/create?mobileNumber=4354437687 <br>

