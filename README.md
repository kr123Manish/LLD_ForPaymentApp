
# Low-Level Design of Payment Apps

This article outlines a Low-Level Design (LLD) approach for Payment Apps, with the aim of building and discussing a suitable design. The project involves creating an LLD for Payment Apps, and the approach to be taken will depend on whether the system is already known or not.

If you already know about the system, the recommended approach is to align your understanding with the expectations of the client. However, if you are not familiar with the project, the following steps are suggested:

## Step 0 

- Identify the classes, entities, and components.
- Determine whether a schema is necessary.
- Consider how the system will be interacted with, such as through Rest API, Command Line Interface, or Hard coded which run automatically.

## Step 1
- Discuss and classify the requirements in detail.
- Suggest ideas and ask generic questions.
- Identify the core features and minimums of 5 to 8.
- Visualize the system for each feature and consider edge cases and future requirements.

## Requirements for Payment Apps.
- SignUp
    - Email -> Password
    - Phone -> OTP

- Login 
    - Email -> Password
    - Phone -> OTP

- Add profile details and do KYC.
    - Name
    - Phone No.
    - PAN
    - Aadhar
    - Bank details
        - Account Number
        - IFC Code
        - Branch Name
        - Account Holder Name
- Send Money to others with following methods.
    - |-> UPI Id
    - |-> Phone Number
    - |-> Bank Account
    - |-> QR Code

**Note:** Our system suppord payment with phone Number and bank account. Not with UPI Id and QR code because first focus on MVP (Mininmal viable product).

- Source of Payment.
    - Debit / Credit card.
    - UPI.

- See Payment History.
    - Pagination.
        - 10 transaction on each page.
        - Most recent first.
    - How do you handle transactions.
        - We want to allow retrives.
        - We will allow multiple transactions.
    - If sender and reciver has any payment and any transaction fails we will cancell the whole process and rollback.

**Note:** Here we use the concept of automicity in which either complete whole thing or don't do any things.

## Step 2
- Use case Diagram
<img scr=""></img>
## Step 3
- Class Diagram
    - entities
    - Relationships between entities
    - Enum
    - Interfaces
    - Design pattern used.



