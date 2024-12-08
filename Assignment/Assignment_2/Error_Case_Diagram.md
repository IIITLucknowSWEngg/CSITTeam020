# Error Case Diagram


![Error Case Diagram](<https://github.com/IIITLucknowSWEngg/CSITTeam020/blob/main/Assignment/Assignment_2/Error_Case_Diagram.png>)
 
 ```

@startuml
title Error Case Diagram - OYO Competitor

actor "Customer" as customer
actor "Hotel Manager" as hotelManager
actor "Support Agent" as supportAgent

' Main System Use Cases
usecase "Search Rooms" as UC_SearchRooms
usecase "Book Room" as UC_BookRoom
usecase "Make Payment" as UC_Payment
usecase "Manage Listings" as UC_ManageListings
usecase "View Booking Details" as UC_ViewBookings
usecase "Assist Customer" as UC_AssistCustomer

' Error Cases for Customer
usecase "(Room Not Available)" as Error_RoomNotAvailable
usecase "(Payment Failed)" as Error_PaymentFailed
usecase "(Search Error)" as Error_Search
usecase "(Booking Cancellation Error)" as Error_CancellationError

' Error Cases for Hotel Manager
usecase "(Listing Creation Failed)" as Error_ListingCreation
usecase "(Update Room Details Failed)" as Error_UpdateDetails
usecase "(Overbooking Error)" as Error_Overbooking

' Error Cases for Support Agent
usecase "(Customer Assistance Error)" as Error_Assistance

' Relationships for Customer
customer --> UC_SearchRooms : "Search for Rooms"
customer --> UC_BookRoom : "Book a Room"
customer --> UC_Payment : "Make Payment"
customer --> UC_ViewBookings : "View Booking History"

UC_SearchRooms --> Error_Search : "If search query fails"
UC_SearchRooms --> Error_RoomNotAvailable : "If no rooms match criteria"
UC_BookRoom --> Error_RoomNotAvailable : "If room is no longer available"
UC_BookRoom --> Error_CancellationError : "If cancellation fails"
UC_Payment --> Error_PaymentFailed : "If payment is declined"

' Relationships for Hotel Manager
hotelManager --> UC_ManageListings : "Create/Update Listings"
hotelManager --> UC_ViewBookings : "View Bookings"

UC_ManageListings --> Error_ListingCreation : "If listing creation fails"
UC_ManageListings --> Error_UpdateDetails : "If updating room details fails"
UC_ManageListings --> Error_Overbooking : "If multiple bookings conflict"

' Relationships for Support Agent
supportAgent --> UC_AssistCustomer : "Handle Customer Queries"
UC_AssistCustomer --> Error_Assistance : "If unable to resolve issues"

@enduml



 ```
