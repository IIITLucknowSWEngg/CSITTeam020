# Software Requirements Specification (SRS) for OYO Competitor

## 1. Introduction

### 1.1 Purpose
This SRS document outlines the functional and non-functional requirements for the OYO hotel booking system. It aligns closely with the user needs outlined in the URD, ensuring efficient development, testing, and stakeholder satisfaction.

### 1.2 Scope
The OYO allows customers to search and book hotel rooms while enabling hotel managers to manage inventory, bookings, and customer interactions. Key features include secure payments, real-time updates, notifications, and reporting. The document follows the cross-referenced URD to maintain consistency.

### 1.3 Definitions, Acronyms, and Abbreviations
- **URD**: User Requirements Document  
- **SRS**: Software Requirements Specification  
- **API**: Application Programming Interface  
- **NFR**: Non-Functional Requirement  
- **PCI DSS**: Payment Card Industry Data Security Standard  
- **GDPR**: General Data Protection Regulation  

### 1.4 References
- IEEE Std 830-1998 for SRS  
- SWEBOK v3.0  
- Cross-Reference Matrix  
- OYO User Requirements Document  

---

## 2. Overall Description

### 2.1 Product Perspective
The OYO system is a web-based and mobile application integrating third-party services (e.g., payment gateways, mapping tools) for seamless room bookings, payment processing, and inventory management.

### 2.2 Product Features
- **User Authentication and Management**: Secure user registration and login.  
- **Room Search and Filtering**: Search by location, dates, price, and amenities.  
- **Booking and Reservation Management**: Real-time room availability and booking.  
- **Payment Gateway Integration**: Secure, PCI DSS-compliant payment processing.  
- **Communication Interfaces**: Notifications for booking confirmations and updates.  
- **Room Listings and Descriptions**: Detailed hotel and room information.  

### 2.3 User Classes and Characteristics
- **Guests**: Simplified search, booking, and secure payment features.  
- **Hotel Managers**: Tools for managing room inventory, pricing, and customer interactions.  
- **Admins**: Platform oversight, reporting, and compliance.  
- **System Architects**: Ensuring scalability and secure data handling.  

### 2.4 Operating Environment
- Modern web browsers (Chrome, Safari, Firefox).  
- Mobile platforms (iOS, Android).  
- Backend hosted on scalable cloud infrastructure.  

### 2.5 Design and Implementation Constraints
- Adherence to PCI DSS and GDPR standards.  
- Scalable to handle peak loads (e.g., holidays).  
- Compatibility with various screen sizes and resolutions.  

### 2.6 Assumptions and Dependencies
- Stable internet access for all users.  
- Reliable integration with payment gateways and APIs.  
- Accurate room details provided by hotel managers.  

---

## 3. System Features

### 3.1 User Authentication and Management
- **Description**: Users can securely register, log in, and manage their accounts.  
- **Requirements**:  
  - Email and phone verification using OTP (URD 4.1).  
  - Password recovery via email or SMS.  
  - Single Sign-On (SSO) via Google and Facebook.  

### 3.2 Room Search and Filtering
- **Description**: Customers can search for rooms based on location, dates, and filters.  
- **Requirements**:  
  - Advanced search by price range, amenities, and ratings (URD 4.2).  
  - Predictive search suggestions and sort options.  

### 3.3 Booking and Reservation Management
- **Description**: Real-time room availability and booking.  
- **Requirements**:  
  - Step-by-step booking process (URD 4.3).  
  - Manage bookings, including modifications and cancellations.  
  - Notifications for booking confirmations.  

### 3.4 Payment Gateway Integration
- **Description**: Customers can securely pay for their bookings.  
- **Requirements**:  
  - Integration with PCI DSS-compliant gateways (URD 4.3).  
  - Support for multiple payment methods (credit card, UPI, wallets).  
  - Refund processing for cancellations.  

### 3.5 Room Listings and Descriptions
- **Description**: Hotel managers can create and manage detailed room listings.  
- **Requirements**:  
  - Photos, descriptions, and amenities for each room (URD 4.4).  
  - Seasonal pricing and availability adjustments.  

### 3.6 Reviews and Ratings
- **Description**: Users can provide reviews and ratings for their stays.  
- **Requirements**:  
  - Guests can rate and review properties after their stay (URD 4.5).  
  - Property owners can respond to reviews to enhance credibility.  
  - Display aggregate ratings and top reviews on property listings.  

### 3.7 Analytics and Insights
- **Description**: Provide actionable insights for admins and hotel managers.  
- **Requirements**:  
  - Generate reports on bookings, revenue, and customer satisfaction (URD 4.6).  
  - Real-time dashboards for tracking property performance and trends.  
  - Recommendations for pricing and inventory adjustments based on analytics.  

---

## 4. External Interface Requirements

### 4.1 User Interfaces
- Intuitive, responsive design for web and mobile.  
- Accessibility features per WCAG 2.1.  

### 4.2 Communication Interfaces
- **Description**: Notifications for important user updates.  
- **Requirements**:  
  - SMS and email notifications for confirmations and reminders
  - HTTPS for secure data transmission.  

### 4.3 Software Interfaces
- Integration with third-party APIs (e.g., Stripe, Google Maps).  
- API for real-time room availability  

---

## 5. Non-Functional Requirements (NFRs)

### 5.1 Performance Requirements
- Response time <2 seconds.  
- Support for 100,000 concurrent users.  

### 5.2 Security Requirements
- Data encryption using TLS and AES-256 (URD 5.2).  
- Two-factor authentication for user accounts.  

### 5.3 Availability and Reliability
- 99.9% uptime using redundant cloud servers.  

### 5.4 System Scalability
- Horizontal scaling for handling increased traffic (URD 5.1).  

### 5.5 User Interface and Usability
- Compliance with WCAG 2.1 for accessibility  .
- User-friendly navigation for search and booking.  

---

## 6. Other Requirements

### 6.1 Localization
- Region-specific content and language support .  

### 6.2 Ethical Considerations
- Transparency in cancellation and refund policies.  
- Mechanisms for reporting inappropriate behavior.  

---

## 7. Appendices

- **Appendix A:** Diagrams (System Architecture, Use Case Diagrams)  
- **Appendix B:** [Cross Reference Matrix](https://github.com/IIITLucknowSWEngg/CSITTeam020/blob/main/Assignment/Assignment_2/crossReferenceMatrix.md)  

---
## Appendix A: Use Case Diagram
---
## Happy Path Diagram
Below is the Use Case Diagram for the happy path of the Oyo clone application. It illustrates the primary actors (Guest, Host, and Admin) and their interactions with the system for key processes like User Registration, Room Booking, Payment Processing, Reviews, and Property Management.

The diagram details the step-by-step flow for each interaction, representing the standard sequence of actions without any exception handling (happy path):

## Actors:
  - User: A person who uses the platform to search for and book rooms.
  - Admin: A system administrator responsible for managing platform operations, such as approving/rejecting listings and generating reports.
  - Hotel Partner: A hotel or property owner who lists and manages their properties on the platform.


This diagram highlights the fundamental interactions and processes that enable seamless room booking and management for both guests and hosts within the Oyo system.


![usecase](https://github.com/user-attachments/assets/0e764235-8369-40e3-aade-ced367dc3671)





---

### ABUSE CASE DIAGRAM

## Actors:

  - Attacker: Engages in sophisticated exploits, such as SQL injection, Cross-Site Scripting (XSS), or phishing attempts, which lead to trust loss and data breaches.
  - Malicious Host: Posts unauthorized property listings, generates fake reviews to manipulate rankings, or engages in payment fraud.
  - Fraudulent User: Creates fake bookings, abuses shared credentials, or performs automated actions that lead to revenue loss.
  - Bot Network: Exploits APIs, scrapes property metadata, floods the system with irrelevant content, or causes performance degradation.

![abusecase](https://github.com/user-attachments/assets/c00378f7-1dc5-4c5f-b233-a37779cfb132)


# Error Case Diagram
![Error_Case_Diagram](https://github.com/user-attachments/assets/7ab40919-5830-45c8-a7ab-907e61be8258)



## Chatgpt prompt
Create a Software Requirements Specification (SRS) outline for a platform that connects service providers with customers.
