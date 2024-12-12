# Software Requirements Specification (SRS) for OYO Competitor

## 1. Introduction

### 1.1 Purpose
This SRS document outlines the functional and non-functional requirements for the OYO hotel booking system. It aligns closely with the user needs outlined in the URD, ensuring efficient development, testing, and stakeholder satisfaction.

### 1.2 Scope
The OYO clone allows customers to search and book hotel rooms while enabling hotel managers to manage inventory, bookings, and customer interactions. Key features include secure payments, real-time updates, notifications, and reporting. The document follows the cross-referenced URD to maintain consistency.

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
  - Email and phone verification using OTP (URD 3.1).
  - Password recovery via email or SMS.
  - Single Sign-On (SSO) via Google and Facebook.

### 3.2 Room Search and Filtering
- **Description**: Customers can search for rooms based on location, dates, and filters.
- **Requirements**:
  - Advanced search by price range, amenities, and ratings (URD 3.2).
  - Predictive search suggestions and sort options.

### 3.3 Booking and Reservation Management
- **Description**: Real-time room availability and booking.
- **Requirements**:
  - Step-by-step booking process (URD 3.3).
  - Manage bookings, including modifications and cancellations.
  - Notifications for booking confirmations.

### 3.4 Payment Gateway Integration
- **Description**: Customers can securely pay for their bookings.
- **Requirements**:
  - Integration with PCI DSS-compliant gateways (URD 3.4).
  - Support for multiple payment methods (credit card, UPI, wallets).
  - Refund processing for cancellations.

### 3.5 Room Listings and Descriptions
- **Description**: Hotel managers can create and manage detailed room listings.
- **Requirements**:
  - Photos, descriptions, and amenities for each room (URD 3.2).
  - Seasonal pricing and availability adjustments.

---

## 4. External Interface Requirements

### 4.1 User Interfaces
- Intuitive, responsive design for web and mobile.
- Accessibility features per WCAG 2.1.

### 4.2 Communication Interfaces
- **Description**: Notifications for important user updates.
- **Requirements**:
  - SMS and email notifications for confirmations and reminders (URD 3.5).
  - HTTPS for secure data transmission.

### 4.3 Software Interfaces
- Integration with third-party APIs (e.g., Stripe, Google Maps).
- API for real-time room availability (URD 3.6).

---

## 5. Non-Functional Requirements (NFRs)

### 5.1 Performance Requirements
- Response time <2 seconds.
- Support for 100,000 concurrent users.

### 5.2 Security Requirements
- Data encryption using TLS and AES-256 (URD 4.2).
- Two-factor authentication for user accounts.

### 5.3 Availability and Reliability
- 99.9% uptime using redundant cloud servers.

### 5.4 System Scalability
- Horizontal scaling for handling increased traffic (URD 4.3).

### 5.5 User Interface and Usability
- Compliance with WCAG 2.1 for accessibility (URD 4.1).
- User-friendly navigation for search and booking.

---

## 6. Other Requirements

### 6.1 Localization
- Region-specific content and language support (URD 4.4).

### 6.2 Ethical Considerations
- Transparency in cancellation and refund policies.
- Mechanisms for reporting inappropriate behavior.

---
## 7. Appendices

- **Appendix A:** Diagrams (System Architecture, Use Case Diagrams)  
- **Appendix B:** [Cross Reference Matrix(https://github.com/IIITLucknowSWEngg/CSITTeam020/blob/main/Assignment/Assignment_2/crossReferenceMatrix.md) 
---

### ABUSE CASE DIAGRAM
![Abuse Case Diagram](https://github.com/user-attachments/assets/77b92713-a86a-4e54-97c7-2dabc33c9418](https://camo.githubusercontent.com/6ede82767ac317e2084810f28897b74875c0cc493362421b66145ee750162250/68747470733a2f2f7777772e706c616e74746578742e636f6d2f6170692f706c616e74756d6c2f706e672f564c4c44527a696d3342715279377947536a65456d5678317133486a7147426a616971686931724c6375737273394f58715573774e707a485f6739616a76535756376f71674354372d79415944445a4c4c50676149474e464135304265717562596138506f353766586241656930396e2d377147557273747534396a6e355269645a65424f595f5470764d49396f446838696b53695a6a3463505f315a463644614c74484c543357656d4b5a66314d5236484134524b526757776e4b6864486452784c3570766d47475431346c444a753356314c637844646b4c3043794f4f5153537462724469632d74756c7866655f5f4e71736e374e3831333359746358686a7662323435626b4c386b67454f62466c78426969777a6f566e5a764d326652456539465a4737424e71634b756a413070346a49302d654d46504e6d3757764558693839654d476269623851456a5568776f6c637639315a584a566f33347538564e516d7a4d6e3248653274417a7a67616a6768746c5653386e76576e43543654625867655f7631384f76366a73336d7047695f4e664f7031666d5644394f534e6930797a4f747543585237355f5731426d66557850566876594846473572444c7661584c684a684b4453494e4f452d5f43436f506d6b6b576e6b6952346456675379374735637565564a453644385a6f365561365f47414c62654e75774b36534348755a79537853567374685248324548644657486e5a7a436346475a5f46412d32554e5f47636332313230646c5f4439745261746a644e4b5f71384b4d43756c49356665455044303048704c6b4d4c6a70654d57746338736f367745316e6a534c732d704e5166323362726f4c30765971394f4275485148417a414f596d695730686844337541754a47794579795756696a4a5457685061646564484c486257514132306c37663464756e5946497765656a515335414254466e565051434b3938717555467131454f634479794f63595374334a42716f63396f645855755a757a6a63554b4442684368435972394a4149755f7232575a7843717850574833746a4c584d5a6474723767306668325675645f306d3030)



# Error Case Diagram

<img width="630" alt="error_case" src="https://github.com/user-attachments/assets/c576679c-3c14-4726-bc97-d6941b2d3f87](https://github.com/IIITLucknowSWEngg/CSITTeam020/blob/main/Assignment/Assignment_2/Error_Case_Diagram.png">

## Chatgpt prompt
Create a Software Requirements Specification (SRS) outline for a platform that connects service providers with customers.
