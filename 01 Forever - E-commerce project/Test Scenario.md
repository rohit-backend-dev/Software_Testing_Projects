# **1. TEST SCENARIO – Forever E-Commerce Website**

**Application / Test Level:** Web Application – Functional, UI, Integration

---

## **1.1 Test Basis**

| Document                                            | Author | Date       | Version |
| --------------------------------------------------- | ------ | ---------- | ------- |
| Test Scenario Document – Forever E-Commerce Website | QA     | 23-11-2025 | 1.0     |

**Basis:**

* Business requirement documents (BRD)
* Functional specification documents (FSD)
* UI/UX design mockups
* Requirement Traceability Matrix (RTM)
* Previous release defects (if any)

---

## **1.2 The Requisites**

**To start the test execution the following matters need to be present:**

* Test environment accessible
* Test data for registration, login, product catalog, cart, payment
* Dummy payment gateway credentials
* Access to admin panel for backend checks (if applicable)

**Minimal system requirements:**

* Browser: Chrome, Firefox, Edge latest versions
* Internet speed: 2 Mbps or above
* Screen resolution: 1366x768 or higher
* Operating system: Windows 10+, MacOS, Linux

**System configuration:**

* Web server running the staging environment
* Database configured with test data
* API endpoints accessible for product, cart, order, payment
* Email and SMS OTP gateway configured

---

## **1.3 Product Risks (from MTP)**

1. Incorrect validation of mandatory fields during registration/login.
2. Search and filter may not return accurate or complete results.
3. Price calculation, discount, and coupon application errors in cart or checkout.
4. Payment gateway failure or timeout scenarios not handled properly.
5. Order status and tracking inconsistencies in My Orders section.

---

## **2. Test Scenarios**

### **2.1 User Registration**

**Test Basis:** BRD, FSD – Registration Module

**Scenarios:**

1. Check if the registration page opens with all required fields.
2. Register with valid email, mobile, and password; verify account creation.
3. Try registering with an already registered email/mobile; verify error message.
4. Validate empty mandatory fields.
5. Check invalid email formats.
6. Verify password policy compliance.
7. Enter invalid mobile numbers.
8. Verify OTP delivery to email/mobile.
9. Enter wrong OTP and verify error message.
10. Enter expired OTP and verify behavior.
11. Verify OTP resend functionality.
12. After successful registration, verify redirection to login page.

---

### **2.2 Login**

**Test Basis:** BRD, FSD – Login Module

**Scenarios:**

1. Login with valid credentials.
2. Login with invalid credentials; verify error messages.
3. Check empty field validation.
4. Test login via OTP (if implemented).
5. Test Forgot Password flow for registered users.
6. Test Forgot Password for unregistered users.
7. Verify account lock after multiple wrong attempts.
8. Login using newly created account.
9. Verify landing page post-login is Home Page.
10. Verify logout functionality.

---

### **2.3 Home Page**

**Test Basis:** BRD, FSD – Home Page

**Scenarios:**

1. Home page loads completely without UI issues.
2. Banner slider works (auto/manual).
3. Category cards/icons navigate correctly.
4. Search bar visible and functional.
5. Featured/trending products load properly.
6. Top navigation links functional.
7. Footer links functional.
8. Personalized recommendations for logged-in users.
9. Responsive layout on mobile, tablet, desktop.

---

### **2.4 Product Search**

**Test Basis:** FSD – Search Module

**Scenarios:**

1. Search with exact product name; verify results.
2. Search with partial keywords; check suggestions.
3. Search with misspelled keywords; verify closest matches.
4. Random text input shows “No results found”.
5. Recent searches visible for logged-in users.
6. Dropdown suggestions match typed text.
7. Clicking a suggestion navigates to correct product/category page.

---

### **2.5 Categories & Filters**

**Test Basis:** FSD – Category & Filter Module

**Scenarios:**

1. Open a category; verify correct products.
2. Apply price filters; verify results.
3. Apply size/color filters; verify results.
4. Apply brand filter; verify accuracy.
5. Use sorting options; verify order.
6. Apply multiple filters; verify combined results.
7. Remove one filter; verify updated results.
8. Use “Clear All” to reset filters.

---

### **2.6 Product Listing Page (PLP)**

**Test Basis:** FSD – PLP Module

**Scenarios:**

1. Products load with image, price, name.
2. Discount labels visible.
3. Wishlist icon adds item correctly.
4. Pagination or infinite scroll works.
5. Clicking a product opens PDP.
6. Out-of-stock products labeled.
7. Sponsored products displayed correctly.

---

### **2.7 Product Detail Page (PDP)**

**Test Basis:** FSD – PDP Module

**Scenarios:**

1. Product details (name, price, description) displayed.
2. Images load and zoom works.
3. Size/color selection works.
4. Add to Cart button functional.
5. Add to Wishlist button functional.
6. Price and discount calculation correct.
7. Check delivery availability via pincode.
8. Reviews and ratings displayed.
9. Related products section works.

---

### **2.8 Add to Cart**

**Test Basis:** FSD – Cart Module

**Scenarios:**

1. Add product to cart from PDP.
2. Add product to cart from PLP.
3. Increase/decrease quantity; verify total price.
4. Remove product from cart.
5. Cart total calculation correct.
6. Cart persists after logout/login.
7. Apply coupon codes; verify valid/invalid responses.
8. Delivery charges applied correctly.
9. Cannot proceed with out-of-stock items.

---

### **2.9 Wishlist**

**Test Basis:** FSD – Wishlist Module

**Scenarios:**

1. Add product to wishlist.
2. Remove product from wishlist.
3. Wishlist persists after logout/login.
4. Move product to cart.
5. Price/stock changes reflect in wishlist.

---

### **2.10 Checkout**

**Test Basis:** FSD – Checkout Module

**Scenarios:**

1. Checkout from cart.
2. Verify order summary details.
3. Select existing address; continue.
4. Add new address from checkout.
5. Delivery charges/free delivery message correct.
6. Apply discount codes.
7. Cannot proceed without selecting address.

---

### **2.11 Address Management**

**Test Basis:** FSD – Address Module

**Scenarios:**

1. Add new address with valid data.
2. Validate pincode, phone, required fields.
3. Edit existing address.
4. Delete address.
5. Mark address as default.

---

### **2.12 Payment (Dummy Data)**

**Test Basis:** FSD – Payment Module

**Scenarios:**

1. Payment options load (Card, UPI, Wallets, COD).
2. Payment with valid dummy card succeeds.
3. Invalid card details show errors.
4. Expired card test.
5. Incorrect UPI ID test.
6. Cancel payment returns user to checkout.
7. Payment timeout handling.
8. Order confirmation only after successful payment.
9. COD only for eligible addresses/products.

---

### **2.13 Order Summary**

**Test Basis:** FSD – Order Module

**Scenarios:**

1. Verify order details (product, price, address, payment).
2. Order ID generated correctly.
3. Invoice download/print works.
4. Links “Continue Shopping” / “Go to My Orders” functional.

---

### **2.14 Order Tracking**

**Test Basis:** FSD – Order Tracking Module

**Scenarios:**

1. Order appears in My Orders after payment.
2. Order statuses update correctly:
Verify order statuses update correctly:
     •  Placed
     •  Packed
     •  Shipped
     •  Out for Delivery
     •  Delivered
3. Tracking link opens courier page.
4. Cancel order before shipment.
5. Refund starts for prepaid cancellations.
6. Reorder option for past orders.

