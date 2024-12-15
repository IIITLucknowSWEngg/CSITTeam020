#   C4 Diagrams

 

# 1. Context diagram

A context diagram for an OYO booking system illustrates its interactions with external entities. The main system is
the "OYO Booking System," surrounded by entities such as "Customer," "Payment Gateway," "Hotel," and "Inventory System."
The arrows represent information flow between the main system and external entities. The diagram provides a high-level
view of the system's scope and relationships, facilitating understanding among stakeholders.
![the picture](./UML%20Diagrams/Context_Diagram.png)
```
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml

LAYOUT_TOP_DOWN()
title System Context Diagram - OYO Booking System

Person(customer, "Customer", "Searches, books, and manages hotel stays")
Person(hotelAdmin, "Hotel Admin", "Manages hotel details, room availability, and pricing")

System(oyoBookingSystem, "OYO Booking System", "Online platform for hotel reservations")

System_Ext(paymentGateway, "Payment Gateway", "Processes customer payments securely")
System_Ext(hotel, "Hotel", "Provides accommodations")
System_Ext(inventorySystem, "Inventory System", "Tracks room availability and pricing")
System_Ext(notificationService, "Notification Service", "Sends booking confirmations and alerts")
System_Ext(analytics, "Analytics", "Tracks user behavior and platform performance")
System_Ext(reviewSystem, "Review System", "Manages customer feedback and ratings")

Rel(customer, oyoBookingSystem, "Searches, books, and manages stays", "HTTPS")
Rel(hotelAdmin, oyoBookingSystem, "Manages hotel details and inventory", "HTTPS")
Rel(oyoBookingSystem, paymentGateway, "Processes payments", "API")
Rel(oyoBookingSystem, hotel, "Sends booking details", "API")
Rel(oyoBookingSystem, inventorySystem, "Syncs room availability and pricing", "API")
Rel(oyoBookingSystem, notificationService, "Sends booking confirmations", "SMTP")
Rel(oyoBookingSystem, analytics, "Tracks platform usage", "API")
Rel(oyoBookingSystem, reviewSystem, "Manages customer feedback", "API")
@enduml
```

---
# 2. Container diagram

A container diagram for an OYO booking system shows the software containers that make up the system. The main containers
are the "Web Frontend," "Booking Service," "Payment Service," and "Database." The "Web Browser" interacts with the "Web
Frontend" for user interaction. The "Booking Service" and "Payment Service" handle booking and payment processes. The "
Database" stores system data. The diagram illustrates the system's software architecture and component relationships.
![the picture](./UML%20Diagrams/Conatiner_Diagram.png)
```
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

skinparam {
    RectangleBackgroundColor #C08080
    RectangleBorderColor #A06060
    RectangleFontColor #FFFFFF
    ArrowColor #A06060
    ArrowThickness 2
    ArrowStyle dashed
}

LAYOUT_TOP_DOWN()
title Container Diagram - OYO Booking System

Person(customer, "Customer", "Searches, books, and manages hotel stays")
Person(hotelAdmin, "Hotel Admin", "Manages hotel details, room availability, and pricing")

System_Boundary(oyoBookingSystem, "OYO Booking System") {
    Container(webFrontend, "Web Frontend", "React", "Allows customers to search and book hotels")
    Container(bookingService, "Booking Service", "Node.js", "Handles hotel booking operations")
    Container(paymentService, "Payment Service", "Java", "Processes payments securely")
    Container(notificationService, "Notification Service", "Python", "Sends booking confirmations and notifications")
    Container(reviewService, "Review Service", "Ruby", "Manages customer feedback and ratings")

    ContainerDb(mainDatabase, "Database", "PostgreSQL", "Stores customer, booking, and hotel data")
}

System_Ext(paymentGateway, "Payment Gateway", "Processes customer payments securely")
System_Ext(hotel, "Hotel", "Provides accommodations")
System_Ext(inventorySystem, "Inventory System", "Tracks room availability and pricing")

Rel(customer, webFrontend, "Interacts with", "HTTPS")
Rel(hotelAdmin, oyoBookingSystem, "Manages hotel details and inventory", "HTTPS")
Rel(webFrontend, bookingService, "Handles booking requests", "HTTPS")
Rel(webFrontend, paymentService, "Processes payments", "HTTPS")
Rel(bookingService, mainDatabase, "Stores booking data", "JDBC")
Rel(paymentService, paymentGateway, "Processes payments", "API")
Rel(notificationService, mainDatabase, "Fetches booking data", "JDBC")
Rel(notificationService, customer, "Sends notifications", "SMTP")
Rel(bookingService, inventorySystem, "Updates room availability", "API")
@enduml
```


---
# 3. Component diagram

### i) User Features
![User Features](https://www.planttext.com/api/plantuml/png/RPDDRjim48Nt0dI7WHR9AXVe8WXerOO1rp4aTD7bH1uxH2JI86adldrcI3aXs-v4plSUvqzFFg0BvscigtjOsEba3Pa0hSQZmmaEri5lJmwMXE7io8Cz01fu_lCSQGewM5TNTUNVj3cXQ8QRIn-k8u6Z8Q0vZYJKFVpy2EGCZj6shd1WFJHoQ03zV5iau-lgovB9DMpmUgFNHQmdTCChtC5IZ_mAzEGkUg28zik-O9MrdF6nO5I9xF0woSSA0xtZDIAxLO5qn0U6zXYqDOLPLvfjRT07FVpBRVk_72-QtZqNqJ5hZhuq5LVfJei1Nz0JDsS_VxBMsWassYTTgvAaLJbpgtkEgZ8QPtrBOKOMqK4UxMYC-VjNVUA7pm8_F3po6E07D6l3FUTv-gQk-4O2t7I9fBdmyg3Pmo7EneFZP3DKHV8NlZ7sadBCehkLH7VE3kIvQ3YbqMH45_Ky3z8N1bmnc8pRbfp9nfAx9RiDOJAB3MdArlE66iFBBSgwabAZibMYN5A85KkLiAU0UXIzIf1AKC-x_rrkXd6v6VRViYL3OHPTuJMd6ZljqWB5j9-u5V4l_mG0)

```
@startuml
' Component Diagram for User Features of an OYO Competitor

skinparam componentStyle rectangle

' External User
actor "User" as User

' Components
component "UI Layer" as UI
component "Search & Filter Service" as SFS
component "Booking Service" as BS
component "Payment Gateway" as PG
component "Recommendation Service" as RS
component "Notification Service" as NS
component "Reviews & Ratings Service" as RRS

' Databases
database "Room Listings DB" as RDB
database "Booking DB" as BDB
database "User Reviews DB" as CRDB

' Relationships
user --> UI : "Interacts"
UI --> SFS : "Searches and filters rooms"
UI --> BS : "Makes bookings"
UI --> PG : "Processes payments"
UI --> RS : "Receives recommendations"
UI --> NS : "Receives notifications"
UI --> RRS : "Leaves reviews"

' Database Connections
SFS --> RDB : "Fetches room details"
BS --> BDB : "Stores booking details"
PG --> BDB : "Processes payments"
RRS --> CRDB : "Stores reviews and ratings"

@enduml

```

### ii) Admin Features
![Admin Features](https://www.planttext.com/api/plantuml/png/TPD1R-CW48NlblmVHhdqLFNUGrLJDwSsbM9vfJrEx4c2QaC4atRpxtV0E36LUZBYVS1xp_3i6HsVnw4ixk35ZYTho33K6WyEHzXR1rK_QWDhGZuxyc3tW0O-_dx0oo1mMPI5_zJcX87lvXqQlWm4ZZf6SnWYTGUl_vYSmG6gZgqh2mmVMCK3Le0UC8mczkh5byLrryH2ZVwui-ZwkAggCsHhxGZlQF10OvXeo7tfZYAwVMyojlNaVcFR7wooLd8UViFL3xoIe1VMdS-eAeSsblLUTyZQcepRD5CDDJBkq9EqqATXIlYcFOiT3xMQejLgoSHaIMfpQGwIL1NKSDQMXcZ47_L9pei_0-xldwHWU9H0NKTUdApAGYR2lBGPXAaG3oxOwebH3mkepQ6p-5geAbTtaxK5K4NzZwPlkHvpfJTv4-M6JE_1BCeCoB8_kK_6o6qCKba4up50hMAollSFhxrc_r3JG3nd6LB5ibURLhHfHUeYnbbaLWbJ4zQUfFLRB937nkTKOUPWJTmThnMAvnkXScBUAeVQ78gkv7NfBysNsCIpD1HV-Ny0)

```
@startuml
' Component Diagram for Admin Features of an OYO Clone

skinparam componentStyle rectangle

' External Actor
actor "Admin" as admin

' Components
component "Admin Dashboard" as AD
component "Room Management Service" as RMS
component "User Management Service" as UMS
component "Booking Management Service" as BMS
component "Analytics Service" as AS
component "Notification Service" as NS

' Databases
database "Room Listings DB" as RDB
database "User DB" as UDB
database "Booking DB" as BDB

' Relationships
admin --> AD : "Accesses"
AD --> RMS : "Manages room details"
AD --> UMS : "Manages users"
AD --> BMS : "Manages bookings"
AD --> AS : "Views analytics"
AD --> NS : "Sends notifications"

' Database Connections
RMS --> RDB : "Adds/Edits/Deletes room listings"
UMS --> UDB : "Accesses user details"
BMS --> BDB : "Updates booking statuses"
AS --> RDB : "Fetches room data"
AS --> BDB : "Fetches booking data"
AS --> UDB : "Fetches user activity"

@enduml

```
---
# 4. Deployment diagram

A deployment diagram for the OYO Booking System illustrates the physical architecture of the system, showing how different components are deployed across nodes. The diagram includes key tiers such as the "Client Tier" with web and mobile apps, the "API Tier" with services like API Gateway and Booking Service, and the "Data Tier" with databases for user and booking data. Each node represents a physical or virtual machine, while connections show communication between components. This diagram provides a detailed view of the system's infrastructure, aiding developers and architects in understanding its deployment.
![deploymentdiagram](https://github.com/user-attachments/assets/8dffd558-18fc-4ba2-94dd-074d6c7f509c)
```
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Deployment.puml

LAYOUT_WITH_LEGEND()
title Deployment Diagram - OYO Booking System

Deployment_Node(client, "Client Tier", "User Devices") {
    Deployment_Node(browser, "Web Browser") {
        Container(web, "Web App", "React", "Allows users to search and book hotels")
    }
    Deployment_Node(mobile, "Mobile Device") {
        Container(app, "Mobile App", "React Native", "Provides hotel search and booking on the go")
    }
}

Deployment_Node(api, "API Tier", "AWS ECS/Kubernetes") {
    Deployment_Node(api_cluster, "API Cluster", "Load Balanced") {
        Container(api_gateway, "API Gateway", "Express.js", "Handles incoming requests and routing")
        Container(booking_service, "Booking Service", "Node.js", "Manages hotel bookings and availability")
        Container(auth_service, "Authentication Service", "OAuth2/OpenID", "Handles user authentication and sessions")
    }
    Deployment_Node(notification, "Notification Service") {
        Container(notification_service, "Notification Service", "Python", "Sends booking confirmations and alerts")
    }
}

Deployment_Node(data, "Data Tier", "AWS RDS/DynamoDB") {
    Deployment_Node(databases, "Database Cluster") {
        ContainerDb(user_db, "User Database", "Amazon RDS", "Stores user information")
        ContainerDb(booking_db, "Booking Database", "Amazon RDS", "Stores booking details and hotel availability")
    }
}

Deployment_Node(storage, "Storage Tier", "Global") {
    Deployment_Node(object_storage, "Object Storage") {
        Container(hotel_images, "Hotel Images", "Amazon S3", "Stores hotel images and related static assets")
    }
}

Deployment_Node(monitoring, "Monitoring and Security") {
    Container(logging, "Logging", "AWS CloudWatch", "Captures application logs for debugging and monitoring")
    Container(metrics, "Metrics", "Prometheus/Grafana", "Monitors system performance and usage")
    Container(security, "Web Application Firewall (WAF)", "AWS WAF", "Protects against malicious requests")
}

Rel(web, api_gateway, "Sends requests", "HTTPS")
Rel(app, api_gateway, "Sends requests", "HTTPS")
Rel(api_gateway, auth_service, "Authenticates users", "OAuth2")
Rel(api_gateway, booking_service, "Manages bookings", "REST")
Rel(booking_service, booking_db, "Reads/Writes", "SQL")
Rel(booking_service, user_db, "Reads/Writes", "SQL")
Rel(notification_service, booking_db, "Fetches booking details", "SQL")
Rel(notification_service, user_db, "Fetches user details", "SQL")
Rel(notification_service, client, "Sends notifications", "SMTP")

' Error Handling Relationships
Rel(api_gateway, logging, "Logs errors and invalid requests", "HTTPS")
Rel(api_gateway, security, "Protects against request floods and malicious inputs", "WAF Rules")
Rel(booking_service, logging, "Logs backend errors", "HTTPS")
@enduml
```

---

