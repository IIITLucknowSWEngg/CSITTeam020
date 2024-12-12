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

### i) Customer Features
### a) Booking a Hotel
![booking_a_hotel](https://github.com/user-attachments/assets/921ee62c-b86b-4d10-8f5b-adf5e5e130c1)

```
@startuml
title Customer Features - Booking a Hotel

actor Customer as customer
entity "OYO Web/Mobile App" as app
control "Booking Service" as bookingService
database "Booking Database" as bookingDb
database "Hotel Inventory System" as inventorySystem

customer -> app : Searches hotels
app -> bookingService : Sends search request
bookingService -> inventorySystem : Retrieves available hotels
inventorySystem --> bookingService : Sends available hotel data
bookingService --> app : Sends search results
customer -> app : Selects a hotel and books it
app -> bookingService : Sends booking request
bookingService -> bookingDb : Stores booking details
bookingService --> app : Confirms booking

@enduml
```

### b) Reviewing a Stay
![managing_hotels](https://github.com/user-attachments/assets/ba31ed19-ac5a-4f11-90e2-32b930872471)


```
@startuml
title Customer Features - Reviewing a Stay

actor Customer as customer
entity "OYO Web/Mobile App" as app
control "Review Service" as reviewService
database "Review Database" as reviewDb

customer -> app : Selects a past stay
app -> reviewService : Submits review and rating
reviewService -> reviewDb : Stores review data
reviewService --> app : Confirms review submission

@enduml
```

### ii) Admin Features
![reviewing_a_stay](https://github.com/user-attachments/assets/f0538108-8bff-429d-95db-665905846edf)

```
@startuml
title Admin Features - Managing Hotels

actor Admin as admin
entity "OYO Admin Portal" as portal
control "Hotel Management Service" as hotelService
database "Hotel Database" as hotelDb

admin -> portal : Logs in to admin portal
portal -> hotelService : Sends login credentials
hotelService --> portal : Confirms login

admin -> portal : Adds/updates hotel details
portal -> hotelService : Sends hotel details
hotelService -> hotelDb : Updates hotel database
hotelService --> portal : Confirms update

admin -> portal : Views hotel inventory
portal -> hotelService : Requests inventory data
hotelService -> hotelDb : Retrieves inventory details
hotelService --> portal : Sends inventory data

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

