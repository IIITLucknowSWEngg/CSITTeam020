**Feature: User Registration**

| **Test ID**    | **TC-REG-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that a user can successfully register with valid information. |
| **Precondition** | User is on the registration page.                           |
| **Steps**      | 1. The user enters valid information (name, email, password). <br> 2. The user submits the registration form. |
| **Expected Result** | The user should be successfully registered. <br> The user should be redirected to the login page. |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const registrationPage = require('../pages/registrationPage');

describe('OYO User Registration', function() {
  it('should register user successfully', function() {
    registrationPage.open();
    registrationPage.fillRegistrationForm('John Doe', 'john@example.com', 'password123');
    registrationPage.submitForm();
    expect(registrationPage.getSuccessMessage()).to.equal('Registration successful');
    expect(browser.getUrl()).to.include('/login');
  });
});
```

---

**Feature: User Login**

| **Test ID**    | **TC-LOG-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that a user can successfully log in with valid credentials. |
| **Precondition** | User is on the login page.                                  |
| **Steps**      | 1. The user enters valid credentials (email, password). <br> 2. The user submits the login form. |
| **Expected Result** | The user should be successfully logged in. <br> The user should be redirected to the dashboard. |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const loginPage = require('../pages/loginPage');

describe('OYO User Login', function() {
  it('should login user successfully', function() {
    loginPage.open();
    loginPage.enterCredentials('john@example.com', 'password123');
    loginPage.submitLogin();
    expect(loginPage.getWelcomeMessage()).to.include('Welcome, John Doe');
    expect(browser.getUrl()).to.include('/dashboard');
  });
});
```

---

**Feature: Room Booking**

| **Test ID**    | **TC-RB-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that the user can successfully book a room.           |
| **Precondition** | User is logged in and on the room booking page.             |
| **Steps**      | 1. The user enters valid check-in and check-out dates. <br> 2. The user selects a room and payment method. <br> 3. The user submits the booking. |
| **Expected Result** | The room should be successfully booked. <br> The user should receive a confirmation message. |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const bookingPage = require('../pages/bookingPage');

describe('OYO Room Booking', function() {
  it('should book a room successfully', function() {
    bookingPage.open();
    bookingPage.enterBookingDetails('2024-12-15', '2024-12-20');
    bookingPage.selectRoom('Deluxe Room');
    bookingPage.selectPaymentMethod('Credit Card');
    bookingPage.submitBooking();
    expect(bookingPage.getConfirmationMessage()).to.equal('Room booked successfully');
    expect(browser.getUrl()).to.include('/booking-details');
  });
});
```

---

**Feature: Payment Processing**

| **Test ID**    | **TC-PP-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that the user can successfully complete payment for a booking. |
| **Precondition** | User has a booking pending payment.                         |
| **Steps**      | 1. The user selects a payment method and enters payment details. <br> 2. The user submits the payment. |
| **Expected Result** | The payment should be processed successfully. <br> The user should receive a payment confirmation. |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const paymentPage = require('../pages/paymentPage');

describe('OYO Payment Processing', function() {
  it('should process payment successfully', function() {
    paymentPage.open();
    paymentPage.enterPaymentDetails('1234 5678 9012 3456', '12/25', '123');
    paymentPage.submitPayment();
    expect(paymentPage.getPaymentConfirmation()).to.equal('Payment successful');
    expect(browser.getUrl()).to.include('/payment-confirmation');
  });
});
```

---

**Feature: Booking Status Update**

| **Test ID**    | **TC-BSU-001**                                              |
|----------------|-------------------------------------------------------------|
| **Description**| Verify that the user can view the current status of their booking. |
| **Precondition** | User has a confirmed booking.                               |
| **Steps**      | 1. The user navigates to the booking status page. <br> 2. The user checks the current status of the booking. |
| **Expected Result** | The user should see the current status of their booking (e.g., "Confirmed", "Checked-in"). |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const bookingStatusPage = require('../pages/bookingStatusPage');

describe('OYO Booking Status Update', function() {
  it('should show the correct booking status', function() {
    bookingStatusPage.open();
    bookingStatusPage.checkStatus();
    expect(bookingStatusPage.getStatus()).to.equal('Confirmed');
  });
});
```

---

**Feature: User Profile Management**

| **Test ID**    | **TC-UPM-001**                                               |
|----------------|--------------------------------------------------------------|
| **Description**| Verify that the user can successfully update their profile. |
| **Precondition** | User is logged in.                                          |
| **Steps**      | 1. The user navigates to the profile page. <br> 2. The user updates their profile information (name, email). <br> 3. The user saves the changes. |
| **Expected Result** | The profile should be updated successfully. |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const profilePage = require('../pages/profilePage');

describe('OYO User Profile Management', function() {
  it('should update user profile successfully', function() {
    profilePage.open();
    profilePage.updateProfile('John Updated', 'johnupdated@example.com');
    expect(profilePage.getSuccessMessage()).to.equal('Profile updated successfully');
  });
});
```

---

**Feature: Room Check-Out**

| **Test ID**    | **TC-RCO-001**                                               |
|----------------|-------------------------------------------------------------|
| **Description**| Verify that the user can successfully check out after their stay. |
| **Precondition** | User has completed their stay.                             |
| **Steps**      | 1. The user completes the check-out process.                 |
| **Expected Result** | The user should receive a payment receipt and booking completion message. |
| **Status**     | Pending/Pass/Fail                                            |

```javascript
const chai = require('chai');
const expect = chai.expect;
const checkOutPage = require('../pages/checkOutPage');

// Test for OYO Room Check-Out
describe('OYO Room Check-Out', function() {
  it('should complete check-out process successfully', function() {
    checkOutPage.open();
    checkOutPage.completeCheckOut();
    expect(checkOutPage.getCompletionMessage()).to.equal('Check-out successful. Thank you for staying with OYO.');
    expect(checkOutPage.getReceipt()).to.include('Payment successfully processed');
  });
});



