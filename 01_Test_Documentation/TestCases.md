# QA Manual Tester Portfolio - Test Cases

## TC_253: Verify correct and secure redirection to "X" bank payment page

**Module:** Checkout / Payment  
**Test Objective:** Ensure that the redirection link (**approval_url**) returned from "X" bank works correctly and securely redirects the user to the bank’s payment page. The Redirect URL should start with a secure protocol (`https://`).  

**Preconditions:**  
- User is on the Checkout page  
- User has at least one product in the cart  
- Shipping address and delivery time are provided  
- Payment method selected is "X" bank  

**Test Steps:**  
1. On the Checkout page, click the "გადახდა" (Pay) button  
2. Open the order details in the admin panel  
3. In the API return data, find `"rel": "approval_url"`  
4. Open the `"uri"` link  
5. Verify that the URL starts with `https://`  
6. Verify that the `payid` in the URL matches the transaction identifier  

**Expected Result:**  
- The link opens without errors  
- User is redirected to the "X" bank payment page  
- Redirect URL starts with secure protocol (`https://`)  
- The `payid` in the URL matches the transaction ID  

**Severity:** High  
**Test Type:** Positive

---

## TC_256: Verify expiration of payment link

**Module:** Checkout / Payment  
**Test Objective:** Ensure that the payment link (**approval_url**) becomes **inactive after the specified time** (expirationMinutes=5) to prevent payment using old or canceled sessions.  

**Preconditions:**  
- User is on the Checkout page  
- Payment method selected is "X" bank  
- Response includes `"expirationMinutes": 5`  

**Test Steps:**  
1. On the Checkout page, click the “გადახდა” (Pay) button and start the payment process  
2. Verify the `expirationMinutes` field in the response  
3. Open the `approval_url` in the browser  
4. Wait for the specified expiration time (5 minutes)  
5. Try to open the `approval_url` again  

**Expected Result:**  
- The payment link becomes inactive after 5 minutes  
- User receives a “Session expired” message or a similar notification  

**Severity:** High  
**Test Type:** Positive

---

## TC_296: Verify correct linking of payId and merchantPaymentID

**Module:** Orders / Payment  
**Test Objective:** Ensure that the `payid` returned by the bank correctly links to the existing Order ID (`merchantPaymentID`) in our system and is reflected in Order details.  

**Preconditions:**  
- Payment has been performed (Order ID is created)  

**Test Steps:**  
1. In the admin panel, navigate to "TBC new ტრანზაქციები" and locate the Order ID  
2. Click "View"  
3. Verify the `merchantPaymentId` matches the Order ID  
4. Verify the `payid` matches the transaction identifier  
5. Check that no duplicate entry is created in Order History  

**Expected Result:**  
- `merchantPaymentId` matches the Order ID  
- `payid` matches the transaction identifier  
- No duplicate entries exist in Order History  

**Severity:** High  
**Test Type:** Positive

---

## TC_297: Verify user cannot change email without current password

**Module:** User Profile / Security  
**Test Objective:** Ensure that a user cannot change their email address on the 'Profile' page without providing the current password.  

**Preconditions:**  
- User is logged in  
- User’s email is not changed  

**Test Steps:**  
1. Click on the Profile icon in the header  
2. In the dropdown menu, select 'Information'  
3. Delete the existing email from the field  
4. Enter a new email address  
5. Click the "Save" button  

**Expected Result:**  
- Email cannot be changed without entering the current password  

**Severity:** Low  
**Test Type:** Negative

