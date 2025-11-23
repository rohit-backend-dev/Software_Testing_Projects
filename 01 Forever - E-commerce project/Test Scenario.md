# **Test Scenario Document – Forever E-Commerce Website**

**Project:** Forever E-Commerce Website
**Document:** Test Scenarios
**Version:** 1.0
**Prepared By:** QA
**Date:** 23-11-2025

---

# **1. User Registration – Test Scenarios**

1. Check if the registration page opens properly with all required fields.
2. Register using valid details and confirm that an account is created.
3.Try registering with an already registered email/mobile number and check the correct error message.
4. Verify validation messages for empty mandatory fields.
5. Check invalid email formats (missing @, missing .com, special characters, long email).
6. Verify password policy (minimum length, uppercase, lowercase, number, special character).
7. Enter an invalid mobile number (less digits, more digits, symbols).
8. Check password field masking and show/hide toggle.
9. Verify OTP is received on email/mobile.
10. Enter a wrong OTP and verify the error message.
11.Enter expired OTP and verify the flow.
12. Verify that OTP resend works.
13. After successful registration, verify the user is moved to the login page.

---

# **2. Login – Test Scenarios**

1. Login with correct email/mobile and password.
2. Try logging in with wrong credentials and check the error message.
3. Check validation for empty login fields.
4. Test login using OTP (if available).
5. Test Forgot Password flow with a registered email/mobile.
6. Test Forgot Password with an unregistered email/mobile.
7. Verify account lock after multiple wrong attempts (if implemented).
8. Login using the newly created account.
9. After login, verify the user lands on the home page.
10. Verify logout works properly.

---

# **3. Home Page – Test Scenarios**

1. Check if the home page loads completely without UI issues.
2. Check if the banner slider works (auto and manual slide).
3. Verify that category cards/icons open the correct pages.
4. Check if the search bar is visible and working.
5. Verify that featured or trending products load properly.
6. Check if top navigation links (Men, Women, Electronics, etc.) work.
7. Check that footer links open the correct pages.

---

# **4. Product Search – Test Scenarios**

1. Search with a correct product name and verify relevant results.
2. Search with partial keywords and check if suggestions appear.
3. Search with a misspelled keyword and verify closest matching results.
4. Search with random text and verify “No results found”.
5. Verify recent searches appear for logged-in users (if implemented).
6. Check if search suggestions match the typed text.

---

# **5. Categories & Filters – Test Scenarios**

1. Open any category and verify the products belong to that category.
2. Apply price filters and verify results update correctly.
3. Apply size/color filters (if available).
4. Apply brand filter and verify accuracy.
5. Use sorting options like Price Low→High, High→Low.
6. Apply multiple filters together and check combined results.
7. Remove one filter and verify results update.
8. Use “Clear All” to reset filters.

---

# **6. Product Listing Page (PLP) – Test Scenarios**

1. Check if all products load with image, price, and name.
2. Verify discount labels and tags are shown properly.
3. Click the wishlist icon and verify the item is added.
4. Verify pagination or infinite scroll works.
5. Verify clicking a product opens the product detail page.
6. Check if out-of-stock products show proper labels.

---

# **7. Product Detail Page (PDP) – Test Scenarios**

1. Check if product details like name, price, description load correctly.
2. Verify product images load and can be viewed/zoomed.
3. Select different sizes or colors and verify selection works.
4. Check Add to Cart button.
5. Check Add to Wishlist button.
6. Verify price and discount calculations.
7. Check delivery availability using pincode.
8. Verify user reviews and ratings are displayed.
9. Check related products section.

---

# **8. Add to Cart – Test Scenarios**

1. Add a product to the cart from the PDP.
2. Add a product to the cart from the PLP.
3. Increase and decrease the quantity and check price update.
4. Remove the product from the cart.
5. Check if cart total is calculated correctly.
6. Verify cart data remains after logout and login.
7. Apply coupon codes and check correct responses for valid/invalid codes.
8. Check if delivery charges are added (if applicable).

---

# **9. Wishlist – Test Scenarios**

1. Add product to wishlist.
2. Remove product from wishlist.
3. Check if wishlist persists after logout/login.
4. Move product from wishlist to cart.
5. Check if price and stock changes reflect on wishlist items.

---

# **10. Checkout – Test Scenarios**

1. Go to checkout from the cart.
2. Check if order summary displays correct product details.
3. Choose an existing address and continue.
4. Add a new address from checkout.
5. Check delivery charges or free delivery message.
6. Apply discount code (if supported).
7. Verify user cannot proceed without selecting an address.

---

# **11. Address Management – Test Scenarios**

1. Add a new address with valid inputs.
2. Verify validation for pincode, phone number, and required fields.
3. Edit an existing address.
4. Delete an address.
5. Mark an address as default.

---

# **12. Payment – Test Scenarios (Dummy Data)**

1. Check if payment options load (Card, UPI, Wallets, COD).
2. Make payment with a valid dummy card.
3. Try invalid card details and check error messages.
4. Try expired card details.
5. Test incorrect UPI ID.
6. Cancel the payment and verify the user returns to checkout.
7. Check payment timeout handling.
8. Verify order confirmation only appears after successful payment.
9. Verify COD option is available only for eligible addresses/products.

---

# **13. Order Summary – Test Scenarios**

1. Check order details like product name, price, address, and payment type.
2. Verify order ID is generated.
3. Check invoice download or print option.
4. Check links like “Continue Shopping” or “Go to My Orders”.

---

# **14. Order Tracking – Test Scenarios**

1. Check if the order appears in My Orders after successful payment.
2. Verify order statuses update correctly:

   * Placed
   * Packed
   * Shipped
   * Out for Delivery
   * Delivered
3. Check if tracking link opens the correct tracking page.
4. Try cancelling the order before it is shipped.
5. Verify refund starts for cancelled prepaid orders.
7. Verify reorder option for past orders.



---
