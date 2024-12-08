# **User Requirements Document or System Definition Document for OYO**

# User Registration

| **Use-case:**                 | User Registration                                                                                                                                                              |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Primary actor:**            | Customer                                                                                                                                                                       |
| Goal in context:              | To onboard the user into the OYO portal                                                                                                                                        |
| Preconditions:                | The user must have access to the internet and a device with a web browser. The user must also have a valid email address and phone number.                                     |
| Trigger:                      | The user clicks on the "Sign Up" button on the OYO portal.                                                                                                                     |
| Scenario:                     |                                                                                                                                                                                |
| (i)                           | The user clicks on the "Sign Up" button on the OYO portal                                                                                                                      |
| (ii)                          | The user is redirected to the registration page.                                                                                                                               |
| (iii)                         | The user enters their name, email address, and phone number in the registration form.                                                                                          |
| (iv)                          | The user sets a password and confirms it.                                                                                                                                      |
| (v)                           | The user clicks on the "Register" button to submit the registration form.                                                                                                      |
| (vi)                          | The system sends a verification code to the user's email address and phone number.                                                                                             |
| (vii)                         | The user enters the verification code on the OYO portal.                                                                                                                       |
| (viii)                        | The system verifies the code and completes the registration process.                                                                                                           |
| (ix)                          | The user is logged in to the OYO portal.                                                                                                                                       |
| Expectations:                   |                                                                                                                                                                                |
| (i)                           | The user should be able to enter all the necessary details required for registration such as full name, email address, password, phone number, and other relevant information. |
| (ii)                          | The system should verify that the email address provided by the user is valid and unique, and that the password is strong enough to ensure account security.                   |
| (iii)                         | The user should be able to see clear and concise instructions for completing the registration process.                                                                         |
| (iv)                          | The system should notify the user in case any of the required fields are left empty or if the information provided is incorrect.                                               |
| (v)                           | The user should receive a confirmation email after successful registration.                                                                                                    |
| (vi)                          | The user should be able to log in to the portal using their registered email address and password.                                                                             |
| (vii)                         | The user should be able to edit their personal information after registration.                                                                                                 |
| (viii)                        | The user's personal information should be kept confidential and not shared with third parties.                                                                                 |
| (ix)                          | The registration process should be easy to use and understand for users of all technical abilities.                                                                            |
| (x)                           | The system should prevent the creation of fake or spam accounts by using email verification or captcha verification.                                                           |
| (xi)                          | The system should provide options for users to reset their password in case they forget it.                                                                                    |
| (xii)                         | The system should provide clear guidelines and feedback to the user in case there are any issues with the registration process.                                                |
| Priority:                     | High                                                                                                                                                                           |
| When available:               | The registration functionality should be available 24/7.                                                                                                                       |
| Frequency of use:             | This use case is expected to be used frequently by new users.                                                                                                                  |
| Channel to actor:             | The user can access the OYO portal using any device with a web browser.                                                                                                        |
| Secondary actors:             | The system, which is responsible for verifying the user's registration details and sending the verification code.                                                              |
| Channels to secondary actors: | The system should send the verification code to the user's email address and phone number                                                                                      |
| Open issues:                  | No open issues at this time                                                                                                                                                    |

# Booking Room on OYO Portal

| **Use Case**          | Booking a Room on the OYO Portal                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Primary Actor**      | Registered customer on the OYO portal.                                                                                     |
| **Goal**               | The customer wants to book a room for a specific date and location on the OYO portal.                                       |
| **Preconditions**      | The customer must be registered, logged in, and have a valid payment method linked to their account.                        |
| **Trigger**            | The customer clicks the "Book a Room" button on the OYO portal.                                                            |
| **Main Scenario**      |                                                                                                                            |
| 1.                    | The customer clicks "Book a Room."                                                                                          |
| 2.                    | They are redirected to the room booking page.                                                                               |
| 3.                    | The customer enters their desired location and stay dates.                                                                  |
| 4.                    | The system displays available rooms and their pricing.                                                                      |
| 5.                    | The customer selects a room and clicks "Book Now."                                                                          |
| 6.                    | The customer enters payment details and confirms the booking.                                                               |
| 7.                    | The system validates payment, confirms the booking, and sends a confirmation email to the customer.                         |
| **Expectations**       |                                                                                                                            |
| 1.                    | Users can search for rooms by location, check-in/check-out dates, and apply filters.                                         |
| 2.                    | Room details, photos, amenities, and user reviews are clearly displayed.                                                     |
| 3.                    | Users can seamlessly book a room by choosing dates and completing payment.                                                   |
| 4.                    | Payment validation and booking confirmation occur without issues.                                                            |
| 5.                    | A confirmation email is sent immediately upon successful booking.                                                            |
| 6.                    | Users can cancel bookings and receive refunds according to the cancellation policy.                                          |
| 7.                    | Cancellation policies, fees, and refund processes are clearly communicated.                                                  |
| 8.                    | Email notifications are sent if a booking request is approved or rejected.                                                   |
| 9.                    | A secure payment gateway is used to protect payment information.                                                             |
| 10.                   | Customer support is available for booking-related issues or queries.                                                         |
| **Priority**           | High                                                                                                                        |
| **Availability**       | Room booking functionality should be available 24/7.                                                                        |
| **Frequency of Use**   | Expected to be used frequently by customers seeking room bookings.                                                           |
| **Channel to Actor**   | The OYO portal, accessible on any web-enabled device.                                                                       |
| **Secondary Actor**    | The system, responsible for processing the booking and sending confirmation emails.                                          |
| **Channel to Secondary Actor** | Confirmation email sent to the customer’s registered email address.                                                  |
| **Open Issues**        | None                                                                                                                        |


# Registering a Room on OYO Portal

| **Use Case**          | Registering a Room on the OYO Portal                                                                                                  |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| **Primary Actor**      | Hotel partner registered on the OYO portal, looking to list their room.                                                              |
| **Goal**               | The hotel partner wants to register their room on the OYO portal so that it can be booked by customers.                              |
| **Preconditions**      | The hotel partner must be registered, logged in, and have all necessary details (location, size, amenities, availability, etc.)       |
| **Trigger**            | The hotel partner clicks the "List Your Room" button on the OYO portal.                                                              |
| **Main Scenario**      |                                                                                                                                      |
| 1.                    | The hotel partner clicks "List Your Room" on the portal.                                                                              |
| 2.                    | They are redirected to the room registration page.                                                                                    |
| 3.                    | The hotel partner enters details about the room (location, size, amenities, availability).                                            |
| 4.                    | Photos of the room are uploaded by the hotel partner.                                                                                 |
| 5.                    | The hotel partner sets the room's price and selects a payment method.                                                                 |
| 6.                    | They submit the registration form by clicking "List Your Room."                                                                       |
| 7.                    | The hotel partner verifies and approves the room listing.                                                                             |
| 8.                    | The room becomes available for booking by customers.                                                                                  |
| **Expectations**       |                                                                                                                                      |
| 1.                    | Hotel partners should be able to provide all necessary room details (location, size, amenities, availability).                         |
| 2.                    | Partners should be able to upload photos to highlight the room’s features.                                                            |
| 3.                    | The system allows setting the price and selecting a payment method for the room.                                                      |
| 4.                    | The system verifies the information and rejects incomplete or incorrect listings.                                                     |
| 5.                    | The system should approve listings promptly if all the details are correct.                                                           |
| 6.                    | Approved listings should be visible to customers on the OYO portal.                                                                   |
| 7.                    | Rooms should be bookable based on their set availability.                                                                             |
| 8.                    | The system should notify the partner via email when their room listing is approved or rejected.                                        |
| 9.                    | Hotel partners should be able to edit or delete their room listings if needed.                                                        |
| 10.                   | Clear feedback and guidelines should be provided if a room listing is rejected.                                                       |
| **Priority**           | High                                                                                                                                 |
| **Availability**       | Room registration functionality should be available 24/7.                                                                            |
| **Frequency of Use**   | Frequently used by hotel partners listing their rooms on the OYO portal.                                                             |
| **Channel to Actor**   | Hotel partners access the OYO portal via any web-enabled device.                                                                      |
| **Secondary Actor**    | The system, responsible for verifying and approving room listings.                                                                    |
| **Channel to Secondary Actor** | The system sends email notifications to the partner when their listing is approved or rejected.                                 |
| **Open Issues**        | Potential issues with verifying details (e.g., accuracy of room info, quality of photos). System should provide clear feedback if rejected. |


# Seeking Support on OYO Portal

| **Use Case**          | Seeking Support from the OYO Portal                                                                                                |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Primary Actor**      | Registered User                                                                                                                    |
| **Goal**               | To receive assistance when facing issues while booking a room or registering a room on the OYO portal.                              |
| **Preconditions**      |                                                                                                                                   |
| 1.                    | The user is registered on the OYO portal.                                                                                           |
| 2.                    | The user is logged in to their account.                                                                                             |
| 3.                    | The user is attempting to book or register a room and is facing an issue.                                                           |
| **Trigger**            | The user clicks on the "Need Help?" or "Contact Support" button on the portal.                                                     |
| **Main Scenario**      |                                                                                                                                   |
| 1.                    | The system displays a contact form for the user to provide their name, email, phone number, and a brief description of the issue.    |
| 2.                    | The user fills out the form and submits it.                                                                                         |
| 3.                    | The system sends a confirmation email acknowledging receipt of the query and provides an estimated response time.                   |
| 4.                    | A support representative reviews the query and contacts the user via their preferred channel (email, phone, or chat).               |
| **Expectations**       |                                                                                                                                   |
| 1.                    | The "Need Help?" or "Contact Support" button should be easy to locate on the booking or registration page.                          |
| 2.                    | The contact form should be simple and user-friendly for query submission.                                                           |
| 3.                    | The system should provide an estimated response time upon form submission.                                                          |
| 4.                    | Support representatives should be knowledgeable and capable of providing effective assistance.                                      |
| 5.                    | If the issue cannot be resolved immediately, the representative informs the user of next steps and an estimated resolution time.     |
| 6.                    | The user should receive regular updates until the issue is resolved.                                                                |
| **Priority**           | High                                                                                                                               |
| **Availability**       | Support should be available 24/7.                                                                                                  |
| **Frequency of Use**   | As per the user's need.                                                                                                            |
| **Channel to Actor**   | Support is accessed via email, phone, or chat.                                                                                     |
| **Secondary Actor**    | Support Representative responsible for assisting users.                                                                            |
| **Channel to Secondary Actor** | Support communication occurs via email, phone, or chat.                                                                         |
| **Open Issues**        | The system should allow users to escalate their query if they are unsatisfied with the support received.                            |
                                  

# Receipt Download from OYO Portal

| **Use Case**          | Receipt Download from the OYO Portal                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Primary Actor**      | Registered User                                                                                                                    |
| **Goal**               | To obtain a receipt for the room booked on the OYO portal.                                                                        |
| **Preconditions**      |                                                                                                                                   |
| 1.                    | The user is registered on the OYO portal.                                                                                          |
| 2.                    | The user is logged in to their account.                                                                                            |
| 3.                    | The user has successfully booked a room on the OYO portal.                                                                        |
| **Trigger**            | The user clicks the "Get Receipt" or "Download Receipt" button on the booking confirmation page.                                  |
| **Main Scenario**      |                                                                                                                                   |
| 1.                    | The system displays a receipt for the room booking, including details like room type, booking dates, payment details, and taxes.   |
| 2.                    | The user can download the receipt in a printable or PDF format.                                                                   |
| 3.                    | If there are issues obtaining the receipt, the user can click "Need Help?" or "Contact Support" for assistance from the OYO team.  |
| **Expectations**       |                                                                                                                                   |
| 1.                    | The system should generate a clear and accurate receipt for the room booking.                                                    |
| 2.                    | The receipt should contain all relevant details, including room type, booking dates, payment details, and applicable taxes.        |
| 3.                    | The user should be able to easily download the receipt in a printable or PDF format.                                             |
| 4.                    | Users facing issues obtaining the receipt should be able to contact the OYO support team for assistance easily.                     |
| **Priority**           | Medium                                                                                                                             |
| **Availability**       | The receipt download functionality should be available 24/7.                                                                     |
| **Frequency of Use**   | As per the user's need.                                                                                                           |
| **Channel to Actor**   | Support is accessed via email, phone, or chat.                                                                                    |
| **Secondary Actor**    | Support Representative responsible for assisting users.                                                                          |
| **Channel to Secondary Actor** | Support communication occurs via email, phone, or chat.                                                                         |
| **Open Issues**        | None.                                                                                                                             |
