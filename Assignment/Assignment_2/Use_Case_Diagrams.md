## 1. Viewer Use Case Diagram
![image](https://github.com/user-attachments/assets/3bc8fe00-7313-4e0b-a6a3-d643efb256f5)

```
@startuml
' Use Case Diagram for Viewer (User) of OYO Application

actor "Viewer" as viewer

package "OYO Application (User)" {
    usecase "Search Hotels" as UC_Search
    usecase "View Hotel Details" as UC_View_Details
    usecase "Book a Room" as UC_Book
    usecase "Cancel Booking" as UC_Cancel
    usecase "Rate/Review Hotel" as UC_Review
    usecase "Manage Account" as UC_Account
    usecase "View Booking History" as UC_History
    usecase "Apply Offers/Promotions" as UC_Offers
}

' Viewer interactions
viewer --> UC_Search
viewer --> UC_View_Details
viewer --> UC_Book
viewer --> UC_Cancel
viewer --> UC_Review
viewer --> UC_Account
viewer --> UC_History
viewer --> UC_Offers

@enduml
```

---

## 2. Admin Use Case Diagram
![image](https://github.com/user-attachments/assets/6693245b-7800-4bfa-aa4e-7dda29723392)

```
@startuml
' Use Case Diagram for Admin of OYO Application

actor "Admin" as admin

package "OYO Application (Admin)" {
    usecase "Manage Properties" as UC_Manage_Properties
    usecase "Manage Users" as UC_Manage_Users
    usecase "Manage Bookings" as UC_Manage_Bookings
    usecase "View Analytics" as UC_Analytics
    usecase "Manage Payments" as UC_Manage_Payments
    usecase "Update Offers/Promotions" as UC_Manage_Offers
}

' Admin interactions
admin --> UC_Manage_Properties
admin --> UC_Manage_Users
admin --> UC_Manage_Bookings
admin --> UC_Analytics
admin --> UC_Manage_Payments
admin --> UC_Manage_Offers

@enduml
```

---
