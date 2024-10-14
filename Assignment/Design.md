# Design documentation of OYO Booking System

## 1. Introduction

The OYO hotel booking system is a web-based application that will enable customers to search and book hotel rooms
online. The system will provide an easy-to-use interface for users to search for hotels based on their preferred
location, budget, and other criteria. The system will also provide hotel managers with an easy way to manage their room
inventory, bookings, and customer information.
This design document outlines the key aspects of the system, including its design principles and activity diagrams.

## 2. System Architecture

The OYO application follows a client-server architecture model. Clients can be web-based interfaces. It sends requests
to the server for various operations such as hotel search, room booking, reservation management, and billing. The server
component handles the business logic and processes the requests received from the client. the client and server
communicate with each other over a network using standardized protocols, such as HTTP or TCP/IP.
Presentation Layer: It includes web-based interfaces, mobile applications, and other client-side components. And
communicates with the application layer to retrieve and display information to the users.
Application Layer: The application layer contains the core business logic and functionality of the OYO Hotel Management
System. It handles user requests, processes data, and performs operations such as hotel search, booking management,
reservation management, and billing.
Data Access Layer: It provides the necessary functions of the OYO application to access and manipulate data with help of
SQL queries. It includes tables, schemas, and relationships that represent entities such as hotels, rooms, guests,
reservations, and billing information. The database stores and manages the persistent data required for the OYO Hotel
Management System.
Integration Components: This includes interfaces with payment gateways, third-party APIs for hotel inventory and
availability, and other external systems. Integration components facilitate seamless integration and synchronization of
data between the OYO system and external entities.

## 3. Implementation details of OYO booking System:

The OYO booking system is implemented using Java, JavaScript, and Python. It follows a microservices architecture, with
Spring Boot and Django for the backend. The frontend uses HTML5, CSS3, and frameworks Angular.js. Data is stored in a
relational database like MySQL. RESTful APIs and message queues enable communication between components. Security
measures, CI/CD pipelines, and monitoring tools are incorporated. Cloud services may be utilized for scalability and
cost optimization.

## 4. Functional Requirements:

User Registration: Allow users to register accounts with the system. It stores user details, including name, contact
information, and login credentials.
Hotel Search and Booking: Provide a search functionality for users to find available hotels based on location, dates,
and other filters. Allow users to select a room from the available options and proceed with the booking process. And
also calculate and display the total cost of the booking, including taxes and additional charges.
Reservation Management: Manage hotel room reservations, scheduling dates and canceling bookings. Ensure real-time
availability updates to prevent double bookings. Handle special requests and preferences, such as room upgrades or
specific amenities.
Guest Management: Facilitate the check-in and check-out processes for guests. Capture guest details, including
identification information, contact information, and payment preferences. Maintain a record of guest history and
preferences for personalized service.
Billing and Invoicing: Generate accurate invoices for guests based on their bookings, including room charges, additional
services, and applicable taxes. Provide multiple payment options, such as cash, credit/debit cards, and mobile wallets.
Generate receipts and maintain a transaction history for accounting purposes.
Reporting and Analytics: Generate reports on hotel occupancy, revenue, guest reviews and statistics. Provide insights
and analytics to aid in decision-making and revenue optimization. Support customizable reports based on various
parameters, such as date ranges and hotel locations.

## 5. Non-Functional Requirements:

Performance: OYO ensures fast response times for user interactions, even with a large volume of concurrent users.
Optimize database queries and utilize caching mechanisms for efficient data retrieval. Conduct performance testing to
validate system scalability and responsiveness.
Usability: Design an intuitive and user-friendly interface for both hotel staff and guests. Provide clear instructions
and feedback to guide users through various processes. Support multiple languages and accessibility standards to cater
to diverse user requirements.
Security: Implement strong encryption algorithms to protect sensitive user data during transmission and storage. Employ
secure authentication and authorization mechanisms to control access to system functionalities and data. Regularly apply
security patches and updates to address vulnerabilities and ensure system integrity.
Reliability: Ensure high system availability to minimize downtime and disruptions. Implement data backup and recovery
mechanisms to prevent data loss in case of system failures. Monitor system performance and implement proactive measures
to prevent potential issues.
Scalability: Design the system to handle a growing number of hotels, rooms, and bookings without compromising
performance. Utilize scalable infrastructure and technologies that can accommodate future growth and increased user
load. Implement horizontal scaling strategies to distribute the system load across multiple servers.
Maintainability: Develop clean and modular code adhering to coding best practices and design patterns. Provide
comprehensive documentation to assist in system maintenance, troubleshooting, and future enhancements.
Ensuring it meets the functional needs of the users and satisfies the non-functional aspects essential for a successful
and efficient system.

## 6. Design Principles:

OYO follows these design principles to ensure the effectiveness, scalability, and user satisfaction of its application.
Simplicity: OYO emphasizes simplicity in its design to provide a clean and intuitive user experience. The user
interfaces are designed to be easy to navigate, understand, and use, minimizing complexity and maximizing usability.
Modularity: OYO's design embraces modularity, breaking down the application into smaller, self-contained modules. This
allows for easier development, maintenance, and scalability by enabling teams to work independently on different modules
and components.
Responsiveness: OYO prioritizes responsiveness in its design to ensure a smooth and seamless user experience across
different devices and platforms. The application is designed to be responsive and adaptable, providing optimal
performance and usability regardless of the user's device or screen size.
Data-driven: OYO leverages data-driven design to enhance the user experience and optimize operations. User feedback,
analytics, and data insights are utilized to drive improvements in the application's functionality, user interfaces, and
overall performance.
Security: OYO places a strong emphasis on security in its design, ensuring that user data and transactions are
protected. Robust security measures, such as encryption, secure authentication, and data privacy controls, are
incorporated to safeguard user information and maintain trust.

## 7. Activity Diagram Flow:

### 1. User Registration:

- The activity starts with a user accessing the OYO website or mobile app.
- The user selects the registration option and provides the required information.
- The system validates the user's inputs and creates a new account for the user.
- Once the account is created, the activity ends.

### 2. Hotel Search and Booking:

- The activity starts with the user logging into their OYO account.
- The user enters the desired location, check-in/check-out dates, and other search criteria.
- The system retrieves available hotels matching the search criteria.
- The user selects a hotel from the list, views the details, and checks the availability of rooms.
- The user proceeds to book a room by providing necessary details and making payment.
- The system confirms the booking and generates a booking confirmation.
- The activity ends with the user receiving the confirmation.

### 3. Check-In Process:

- The activity starts when a guest arrives at the hotel.
- The guest provides their booking details to the hotel staff.
- The staff retrieves the guest's reservation information from the system.
- The staff verifies the guest's identity and collects any required additional information.
- The system updates the guest's check-in status and generates a room key or access code.
- The staff provides the room key or access code to the guest.
- The activity ends with the guest proceeding to their assigned room.

### 4. Guest Services:

- This activity represents various services provided to the guest during their stay.
- It includes activities such as room cleaning, room service, concierge assistance, etc.
- The guest can request these services through the OYO app or by contacting the hotel staff directly.
- The staff receives and processes the guest's service requests.
- The staff updates the status of each service request in the system.
- The activity continues until all requested services are provided.

### 5. Check-Out Process:

- The activity starts when the guest initiates the check-out process.
- The guest informs the hotel staff about their intention to check out.
- The staff retrieves the guest's reservation and verifies the room's condition.
- The staff collects any outstanding payments or additional charges.
- The system updates the guest's check-out status and finalizes the billing.
- The staff provides the guest with Iman invoice or receipt.
- The activity ends with the guest leaving the hotel.

## Flowchart for Oyo Booking System

![the picture](./UML%20Diagrams/Activity_Diagram.png)

## 8. Deployment and Maintenance:

Deployment : The OYO booking system is typically deployed in cloud environments, such as Amazon Web Services (AWS),
Microsoft Azure, or Google Cloud Platform (GCP). These cloud platforms provide scalability, flexibility, and high
availability for the OYO system.
Maintenance: The OYO technical team remotely performs maintenance tasks, including monitoring, software updates,
issue resolution, and user support, to ensure smooth system operation and enhance performance.

## 9. Conclusion:

The design of the OYO booking system incorporates key design principles and aims to deliver a reliable,
user-friendly, and scalable solution for efficient hotel management and seamless user experiences.
