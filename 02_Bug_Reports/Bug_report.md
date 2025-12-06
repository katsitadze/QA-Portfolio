# Bug Reports - QA Manual Tester Portfolio

## BUG_001: No voice options available for text-to-speech in AI Audio
**Priority:** High  
**Status:** Open  
**Type:** Functional Bug  
 
**Environment:** Desktop: Dell Intel i5-4210U / Windows 10 Pro / Chrome 140.0.7339.210 (64-bit)  

**Reproducibility:** 100%  

**Precondition:** User is logged in and on the Chat page with a stable internet connection  

**Steps to Reproduce:**  
1. Open TEST.ai  
2. Click on “AI Audio” in the navigation menu  
3. Type any text into the text area  
4. Click on the “Generate Audio” button  
5. Click on the “Select a voice” button  
6. Enter any search term in the “Search library voices” input field (e.g., "what", "test", "voice")  
7. Observe that no voices are found  

**Actual Result:**  
- No voice options appear at all  
- Searching for different keywords returns zero results  
- User cannot select a voice, making text-to-speech generation impossible  

**Expected Result:**  
- Available voice options should be displayed  
- Searching for a keyword should return at least one matching voice  
- User should be able to select a voice before generating audio  

---

## BUG_002: Left and right sidebar menu icons are not aligned symmetrically
**Priority:** Medium  
**Status:** Open  
**Type:** UI/Visual Bug  
**Environment:** Desktop: Dell Intel i5-4210U / Windows 10 Pro / Chrome 140.0.7339.210 (64-bit)   

**Reproducibility:** 100%  
**Precondition:** User is authorized and on the Chat page  

**Steps to Reproduce:**  
1. Open test.ai  
2. Navigate to the Edit Image section  
3. Observe the header section displaying “Welcome back,..”  
4. Check the left and right sidebar menu icons  

**Actual Result:**  
- Icons are not aligned horizontally  
- One icon appears slightly lower or mispositioned  
- Header looks visually unbalanced  

**Expected Result:**  
- Icons should be horizontally aligned and visually symmetrical  
- Equal spacing from the edges of the screen  

---

## BUG_003: Phone number field allows more digits than allowed
**Priority:** High  
**Status:** Open  
**Type:** Validation Bug  

**Environment:** Desktop: Dell Intel i5-4210U / Windows 10 Pro / Chrome 140.0.7339.210 (64-bit)   
**Reproducibility:** 100%  
**Precondition:** User is logged in and has a free plan  

**Steps to Reproduce:**  
1. Open website https://test.ai/  
2. Click on profile avatar  
3. Tap on “Subscription”  
4. Choose a plan  
5. Tap on “Subscription Now”  
6. Go to Billing page  
7. Click on “Update Subscription”  
8. Choose plan and tap “Select”  
9. Click “Continue”  
10. Click “Confirm”  
11. Fill all fields  
12. Type a long phone number in the phone field  

**Actual Result:**  
- Phone field allows unlimited digits  
- User can enter invalid, very long numbers  

**Expected Result:**  
- Phone number field should limit the number of digits  
- User cannot type more digits than allowed  

---


## BUG_004: Prompt Helper overlaps additional section
**Priority:** High  
**Status:** Open  
**Type:** UI/UX Bug  

**Environment:** Desktop: Dell Intel i5-4210U / Windows 10 Pro / Chrome 140.0.7339.210 (64-bit)   
**Reproducibility:** 100%  
**Precondition:** User is in the chat  

**Steps to Reproduce:**  
1. Press the Prompt button in chat  
2. Click any action in the Prompt Helper (Translate, Explain, etc.)  

**Actual Result:**  
- Additional section appears, but partially or fully hidden by prompt panel  

**Expected Result:**  
- Additional section should appear fully visible, not overlapped  

---

## BUG_005: AI Language search does not filter after first letter
**Priority:** High  
**Status:** Open  
**Type:** Functional Bug   

**Environment:** Desktop: Dell Intel i5-4210U / Windows 10 Pro / Chrome 140.0.7339.210 (64-bit)   
**Reproducibility:** 100%  
**Precondition:** User is in the chat  

**Steps to Reproduce:**  
1. Click “AI Language” on the right side of chat  
2. Type one letter in search field, e.g., “S”  

**Actual Result:** Languages are not filtered after typing first letter  

**Expected Result:** Only languages starting with the typed letter should appear  

---

# BUG_006: Main Page Text Does Not Update After Changing Language Level (Without Refresh)

**Severity:** Medium  
**Priority:** High  
**Status:** Open  
**Type:** Functional Bug  

## Environment
- **Device:** Desktop — Dell Intel i5-4210U  
- **OS:** Windows 10 Pro  
- **Browser:** Chrome 140.0.7339.210 (64-bit)

## Reproducibility
100%

## Precondition
User is logged into their account.

---

## Steps to Reproduce
1. Log in and navigate to your account settings.  
2. Go to the **Main Page**.  
3. Scroll to the bottom-right corner and open the **Change Level** component.  
4. Change the language level (e.g., A2 → B1).

---

## Actual Result
- The text on the Main Page **does not update automatically**.  
- Content is refreshed only after performing a **manual page reload** (F5).

## Expected Result
- Main Page text should **update instantly and dynamically** according to the selected language level, **without requiring a refresh**.

---


# BUG_007: Password Reset Email Not Received

**Severity:** High  
**Priority:** High  
**Status:** Open  
**Type:** Functional Bug  

**Environment:** Desktop: Dell Intel i5-4210U / Windows 10 Pro / Chrome 140.0.7339.210 (64-bit)   


## Reproducibility
100%

## Precondition
User is registered in the system.

---

## Steps to Reproduce
1. Open **test.ge**  
2. Click the **“Sign in”** button in the top menu  
3. In the **Sign In modal**, click **“Forgot your password?”**  
4. Enter email: **testmail@gmail.com**  
5. Click **“Send reset link”**

---

## Actual Result
- A message appears:  
  *“If this email address has been registered in our shop, you will receive a link to reset your password at testmail@gmail.com”*  
- **No password reset email is received** in the user’s inbox.

---

## Expected Result
- The same confirmation message should be shown.  
- **User should receive a password reset link** at the provided email address.

---



