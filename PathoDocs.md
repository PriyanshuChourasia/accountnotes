# Patho Docs

## Service Booking System

### Flow Diagram

```
[Patient Registration] [Already registered]
                                  |
                          [Tests Selection]  
                                  |
                  [Self Requested] [Doctor Prescribed]
                                  |
             [Slot] [if multiple branch give location selection ]
                                  |
                        [Payment Mode Selection]
                                  |
                         [Payment Confirmation]
                                  |
                        [Test Processing in Lab]
                                  |
                          [Report Generation]
                                  |
                    [Report ready to access by customer]
```

### Booking Channels

Patients can book services through the following modes:

* On-Premise Booking
* Online Booking

### Patient Type

When booking, the patient can fall into one of the following categories:

* Already registered Patient - Add a new test or booking or appointment into their account & Search can be done by Patient ID
* New Patient - First time visitor have to complete Registration with minimum details and rest of the details can be filled on their profile section of the site.

### Appointment / Booking Scenarios

A. Regular Appointment

* Patient books a **general appointment** (doctor consultation or health check-up).
* Tests may be prescribed after consultation.

B. Walk-in with Prescription

* Patient arrives with a **doctor's prescription** mentioning test names.
* Staff uploads/scans the document or selects equivalent tests from system catalog.
* Booking created for those tests.

C. Self-requested  (No Prescription Needed)

* Some tests (like blood sugar, cholesterol, vitamin levels, routine blood panel, pregnancy test, eye checkup, etc.) do ​**not require prescription**​.
* Patient can directly choose these tests from the catalog.

### Booking Flow for Patients

a. For new Patients

* Patient provides minimum details like (name,age,gender,contact)
* Uploads / mentions referral (if prescribed by a doctor)
* Select tests/services
* Confirms slot datetime
* Payment (This can be done in two parts one is that advance payment and rest will be paid after test and this can also be done conditionally)
* Registration Completed (Patient ID generated and Booking ID generated)

b. For Already registered Patient

* Search by Patient id or Booking Id
* Goes into the Patient account
* Create a new appointment there with information required
* Generate new booking ID on same patient ID
* Payment method will be same either in two parts or full payment

### Report Generation Process

Every test has some time duration which can be 1 day or 4 hours any which will be mentioned in the bill and even it will help in report publishing to user's account.

1. Test Completion
   * Patient has given sample
   * Test data and publish output to the lab
2. Test data entry to system
3. Report formatting

if payement === pending
show payment pending on the report view section
PDF or any means of document will not generate untill unless the payment is done

if payment != pending
Patient can view report and even can download

