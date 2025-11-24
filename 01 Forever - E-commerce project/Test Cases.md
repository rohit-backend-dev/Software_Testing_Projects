# **Forever E-Commerce Test Cases**

*Note: “Actual Result” and “Comments” columns are to be filled during test execution.*

---

## **1. User Registration**

| Test Case ID | Test Case Title                     | Module       | Priority | Test Data                                                                                          | Steps                                                       | Expected Result                                                                     | Actual Result | Comments |
| ------------ | ----------------------------------- | ------------ | -------- | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------- | -------- |
| TC_REG_001   | Verify registration page loads      | Registration | High     | -                                                                                                  | 1. Navigate to registration page                            | Registration page opens with all fields                                             |               |          |
| TC_REG_002   | Register with valid details         | Registration | High     | Email: [testuser@gmail.com](mailto:testuser@gmail.com)<br>Password: Test@123<br>Mobile: 9876543210 | 1. Enter valid email, password, mobile<br>2. Click Register | Account created and redirected to login page                                        |               |          |
| TC_REG_003   | Register with existing email/mobile | Registration | High     | Email: [existing@test.com](mailto:existing@test.com)<br>Mobile: 9876543210                         | 1. Enter existing email or mobile<br>2. Click Register      | Error message: "Email/Mobile already exists"                                        |               |          |
| TC_REG_004   | Validate empty mandatory fields     | Registration | Medium   | Leave all fields blank                                                                             | 1. Click Register                                           | Validation messages shown                                                           |               |          |
| TC_REG_005   | Invalid email format                | Registration | Medium   | Email: testuser.com                                                                                | 1. Enter invalid email<br>2. Click Register                 | Validation message: "Enter valid email"                                             |               |          |
| TC_REG_006   | Verify password policy              | Registration | High     | Password: test                                                                                     | 1. Enter weak password<br>2. Click Register                 | Error message: "Password must contain min 8 chars, uppercase, number, special char" |               |          |
| TC_REG_007   | Invalid mobile number               | Registration | Medium   | Mobile: 123                                                                                        | 1. Enter invalid mobile<br>2. Click Register                | Error message: "Enter valid mobile number"                                          |               |          |
| TC_REG_008   | Verify OTP received                 | Registration | High     | Valid email/mobile                                                                                 | 1. Complete registration<br>2. Check OTP on email/mobile    | OTP received                                                                        |               |          |
| TC_REG_009   | Wrong OTP                           | Registration | High     | OTP: 0000                                                                                          | 1. Enter incorrect OTP<br>2. Click Verify                   | Error message: "Invalid OTP"                                                        |               |          |
| TC_REG_010   | Expired OTP                         | Registration | Medium   | OTP expired                                                                                        | 1. Wait for OTP to expire<br>2. Enter OTP                   | Message: "OTP expired, request new OTP"                                             |               |          |
| TC_REG_011   | OTP resend functionality            | Registration | Medium   | Valid email/mobile                                                                                 | 1. Click Resend OTP                                         | New OTP received successfully                                                       |               |          |
| TC_REG_012   | Successful registration redirect    | Registration | High     | Valid data                                                                                         | 1. Complete registration                                    | Redirected to login page                                                            |               |          |

---

## **2. Login**

| Test Case ID | Test Case Title                      | Module | Priority | Test Data                                                                     | Steps                                                       | Expected Result                           | Actual Result | Comments |
| ------------ | ------------------------------------ | ------ | -------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------- | ------------- | -------- |
| TC_LOGIN_001 | Login with valid credentials         | Login  | High     | Email: [testuser@gmail.com](mailto:testuser@gmail.com)<br>Password: Test@123  | 1. Enter email and password<br>2. Click Login               | User logged in and navigated to Home Page |               |          |
| TC_LOGIN_002 | Login with invalid credentials       | Login  | High     | Email: [testuser@gmail.com](mailto:testuser@gmail.com)<br>Password: WrongPass | 1. Enter email/password<br>2. Click Login                   | Error message: "Invalid credentials"      |               |          |
| TC_LOGIN_003 | Empty login fields validation        | Login  | Medium   | Leave fields blank                                                            | 1. Click Login                                              | Validation messages shown                 |               |          |
| TC_LOGIN_004 | Login via OTP                        | Login  | Medium   | Registered mobile/email                                                       | 1. Click "Login via OTP"<br>2. Enter OTP<br>3. Click Verify | User logged in successfully               |               |          |
| TC_LOGIN_005 | Forgot Password – registered         | Login  | Medium   | Registered email                                                              | 1. Click Forgot Password<br>2. Enter email<br>3. Submit     | Password reset email sent                 |               |          |
| TC_LOGIN_006 | Forgot Password – unregistered       | Login  | Medium   | Unregistered email                                                            | 1. Enter email<br>2. Submit                                 | Error message: "Email not found"          |               |          |
| TC_LOGIN_007 | Account lock after multiple attempts | Login  | High     | Wrong credentials                                                             | 1. Enter wrong password 5 times                             | Account locked message displayed          |               |          |
| TC_LOGIN_008 | Logout verification                  | Login  | High     | Logged-in user                                                                | 1. Click Logout                                             | User logged out, redirected to login page |               |          |

---

## **3. Home Page**

| Test Case ID | Test Case Title              | Module | Priority | Test Data      | Steps                                  | Expected Result                          | Actual Result | Comments |
| ------------ | ---------------------------- | ------ | -------- | -------------- | -------------------------------------- | ---------------------------------------- | ------------- | -------- |
| TC_HOME_001  | Home page loads correctly    | Home   | High     | -              | 1. Navigate to Home page               | Page loads with UI intact                |               |          |
| TC_HOME_002  | Banner slider auto/manual    | Home   | Medium   | -              | 1. Observe slider<br>2. Click arrows   | Slides change automatically and manually |               |          |
| TC_HOME_003  | Category cards navigation    | Home   | Medium   | -              | 1. Click category card                 | Correct category page opens              |               |          |
| TC_HOME_004  | Search bar visibility        | Home   | Medium   | -              | 1. Check search bar                    | Search bar visible and functional        |               |          |
| TC_HOME_005  | Featured/trending products   | Home   | Medium   | -              | 1. Observe products section            | Products load correctly                  |               |          |
| TC_HOME_006  | Top navigation links         | Home   | Medium   | -              | 1. Click links Men/Women/Electronics   | Pages open correctly                     |               |          |
| TC_HOME_007  | Footer links                 | Home   | Medium   | -              | 1. Click footer links                  | Correct pages open                       |               |          |
| TC_HOME_008  | Personalized recommendations | Home   | Medium   | Logged-in user | 1. Login<br>2. Observe recommendations | Recommendations shown based on user      |               |          |

---

## **4. Product Search**

| Test Case ID  | Test Case Title          | Module | Priority | Test Data                | Steps                                              | Expected Result                            | Actual Result | Comments |
| ------------- | ------------------------ | ------ | -------- | ------------------------ | -------------------------------------------------- | ------------------------------------------ | ------------- | -------- |
| TC_SEARCH_001 | Search exact product     | Search | High     | Product: "T-shirt"       | 1. Enter product name<br>2. Click Search           | Relevant results displayed                 |               |          |
| TC_SEARCH_002 | Partial keyword search   | Search | Medium   | Product: "T-sh"          | 1. Enter partial keyword<br>2. Observe suggestions | Suggestions appear correctly               |               |          |
| TC_SEARCH_003 | Misspelled keyword       | Search | Medium   | Product: "T-shrit"       | 1. Enter misspelled text<br>2. Click Search        | Closest matching results shown             |               |          |
| TC_SEARCH_004 | Random text search       | Search | Low      | Product: "xyzabc"        | 1. Enter random text<br>2. Click Search            | Message: "No results found"                |               |          |
| TC_SEARCH_005 | Recent searches          | Search | Medium   | Logged-in user           | 1. Search products<br>2. Check recent searches     | Recent searches appear                     |               |          |
| TC_SEARCH_006 | Search suggestions match | Search | Medium   | Partial text             | 1. Type text in search bar                         | Suggestions match typed text               |               |          |
| TC_SEARCH_007 | Click search suggestion  | Search | Medium   | Suggestion from dropdown | 1. Click suggestion                                | Navigated to correct product/category page |               |          |

---

## **5. Categories & Filters**

| Test Case ID | Test Case Title         | Module               | Priority | Test Data                                 | Steps                      | Expected Result                     | Actual Result | Comments |
| ------------ | ----------------------- | -------------------- | -------- | ----------------------------------------- | -------------------------- | ----------------------------------- | ------------- | -------- |
| TC_CAT_001   | Open category page      | Categories & Filters | High     | Category: Men                             | 1. Click on category       | Correct products displayed          |               |          |
| TC_CAT_002   | Apply price filter      | Categories & Filters | Medium   | Price: 500–1000                           | 1. Select price range      | Filtered products shown             |               |          |
| TC_CAT_003   | Apply size/color filter | Categories & Filters | Medium   | Size: M<br>Color: Red                     | 1. Select size and color   | Filtered results match criteria     |               |          |
| TC_CAT_004   | Apply brand filter      | Categories & Filters | Medium   | Brand: Nike                               | 1. Select brand            | Products displayed belong to brand  |               |          |
| TC_CAT_005   | Use sorting options     | Categories & Filters | Medium   | Sort: Price Low→High                      | 1. Select sorting option   | Products sorted correctly           |               |          |
| TC_CAT_006   | Apply multiple filters  | Categories & Filters | Medium   | Size: M<br>Brand: Nike<br>Price: 500–1000 | 1. Select multiple filters | Combined filtered results displayed |               |          |
| TC_CAT_007   | Remove one filter       | Categories & Filters | Medium   | Remove brand                              | 1. Remove a filter         | Results updated correctly           |               |          |
| TC_CAT_008   | Clear all filters       | Categories & Filters | Medium   | Multiple filters applied                  | 1. Click Clear All         | All filters reset                   |               |          |

---

## **6. Product Listing Page (PLP)**

| Test Case ID | Test Case Title            | Module | Priority | Test Data            | Steps                             | Expected Result                          | Actual Result | Comments |
| ------------ | -------------------------- | ------ | -------- | -------------------- | --------------------------------- | ---------------------------------------- | ------------- | -------- |
| TC_PLP_001   | Verify products load       | PLP    | High     | -                    | 1. Open PLP                       | Products display with image, name, price |               |          |
| TC_PLP_002   | Discount labels            | PLP    | Medium   | -                    | 1. Check product labels           | Discount labels visible correctly        |               |          |
| TC_PLP_003   | Add to wishlist            | PLP    | Medium   | -                    | 1. Click wishlist icon            | Product added to wishlist                |               |          |
| TC_PLP_004   | Pagination/infinite scroll | PLP    | Medium   | -                    | 1. Scroll down or click next page | Products load correctly                  |               |          |
| TC_PLP_005   | Open PDP from PLP          | PLP    | High     | -                    | 1. Click product                  | Product detail page opens                |               |          |
| TC_PLP_006   | Out-of-stock product       | PLP    | Medium   | Out-of-stock product | 1. Observe product label          | "Out of stock" label displayed           |               |          |
| TC_PLP_007   | Sponsored products         | PLP    | Low      | Sponsored product    | 1. Observe PLP                    | Sponsored product visible                |               |          |

---

## **7. Product Detail Page (PDP)**

| Test Case ID | Test Case Title            | Module | Priority | Test Data             | Steps                         | Expected Result                  | Actual Result | Comments |
| ------------ | -------------------------- | ------ | -------- | --------------------- | ----------------------------- | -------------------------------- | ------------- | -------- |
| TC_PDP_001   | Product details load       | PDP    | High     | -                     | 1. Open PDP                   | Name, price, description visible |               |          |
| TC_PDP_002   | Product images             | PDP    | Medium   | -                     | 1. Click image<br>2. Zoom     | Image loads and zoom works       |               |          |
| TC_PDP_003   | Select size/color          | PDP    | Medium   | Size: M<br>Color: Red | 1. Select options             | Selected attributes updated      |               |          |
| TC_PDP_004   | Add to Cart                | PDP    | High     | -                     | 1. Click Add to Cart          | Product added to cart            |               |          |
| TC_PDP_005   | Add to Wishlist            | PDP    | Medium   | -                     | 1. Click wishlist icon        | Product added to wishlist        |               |          |
| TC_PDP_006   | Price & discount check     | PDP    | High     | -                     | 1. Observe price & discount   | Correct calculation displayed    |               |          |
| TC_PDP_007   | Check delivery via pincode | PDP    | Medium   | Pincode: 110001       | 1. Enter pincode              | Delivery availability shown      |               |          |
| TC_PDP_008   | Reviews & ratings          | PDP    | Medium   | -                     | 1. Scroll to reviews          | Reviews & ratings displayed      |               |          |
| TC_PDP_009   | Related products           | PDP    | Low      | -                     | 1. Scroll to related products | Related products shown           |               |          |

---

## **8. Add to Cart**

| Test Case ID | Test Case Title                     | Module | Priority | Test Data       | Steps                               | Expected Result                 | Actual Result | Comments |
| ------------ | ----------------------------------- | ------ | -------- | --------------- | ----------------------------------- | ------------------------------- | ------------- | -------- |
| TC_CART_001  | Add product from PDP                | Cart   | High     | -               | 1. Open PDP<br>2. Click Add to Cart | Product added to cart           |               |          |
| TC_CART_002  | Add product from PLP                | Cart   | High     | -               | 1. Open PLP<br>2. Click Add to Cart | Product added to cart           |               |          |
| TC_CART_003  | Increase/decrease quantity          | Cart   | Medium   | -               | 1. Change quantity                  | Cart total updated              |               |          |
| TC_CART_004  | Remove product from cart            | Cart   | Medium   | -               | 1. Click Remove                     | Product removed, total updated  |               |          |
| TC_CART_005  | Cart persists after logout/login    | Cart   | Medium   | -               | 1. Logout & login                   | Cart retains products           |               |          |
| TC_CART_006  | Apply coupon codes                  | Cart   | Medium   | Coupon: TEST10  | 1. Enter coupon<br>2. Apply         | Discount applied or error shown |               |          |
| TC_CART_007  | Delivery charges                    | Cart   | Medium   | Pincode: 110001 | 1. Enter pincode                    | Delivery charges calculated     |               |          |
| TC_CART_008  | Out-of-stock product cannot proceed | Cart   | High     | -               | 1. Add out-of-stock product         | Prevent adding/checkout         |               |          |

---

## **9. Wishlist**

| Test Case ID | Test Case Title                      | Module   | Priority | Test Data | Steps                                        | Expected Result        | Actual Result | Comments |
| ------------ | ------------------------------------ | -------- | -------- | --------- | -------------------------------------------- | ---------------------- | ------------- | -------- |
| TC_WISH_001  | Add product to wishlist              | Wishlist | Medium   | -         | 1. Click wishlist icon                       | Product added          |               |          |
| TC_WISH_002  | Remove product from wishlist         | Wishlist | Medium   | -         | 1. Click remove                              | Product removed        |               |          |
| TC_WISH_003  | Wishlist persists after logout/login | Wishlist | Medium   | -         | 1. Logout & login                            | Wishlist retains items |               |          |
| TC_WISH_004  | Move product to cart                 | Wishlist | Medium   | -         | 1. Click move to cart                        | Product moved to cart  |               |          |
| TC_WISH_005  | Price/stock reflect changes          | Wishlist | Medium   | -         | 1. Observe wishlist after price/stock change | Updates reflected      |               |          |

---

## **10. Checkout**

| Test Case ID | Test Case Title                | Module   | Priority | Test Data         | Steps                                         | Expected Result                         | Actual Result | Comments |
| ------------ | ------------------------------ | -------- | -------- | ----------------- | --------------------------------------------- | --------------------------------------- | ------------- | -------- |
| TC_CHECK_001 | Go to checkout from cart       | Checkout | High     | -                 | 1. Open cart<br>2. Click Checkout             | Checkout page opens                     |               |          |
| TC_CHECK_002 | Verify order summary           | Checkout | High     | -                 | 1. Observe order summary                      | Product, price, quantity correct        |               |          |
| TC_CHECK_003 | Choose existing address        | Checkout | Medium   | Address: Existing | 1. Select address<br>2. Continue              | Address selected and checkout continues |               |          |
| TC_CHECK_004 | Add new address                | Checkout | Medium   | Address: New      | 1. Enter new address<br>2. Save               | New address saved and selected          |               |          |
| TC_CHECK_005 | Delivery charges/free delivery | Checkout | Medium   | Pincode: 110001   | 1. Enter pincode                              | Delivery charges or free delivery shown |               |          |
| TC_CHECK_006 | Apply discount code            | Checkout | Medium   | Coupon: TEST10    | 1. Enter coupon<br>2. Apply                   | Discount applied or error shown         |               |          |
| TC_CHECK_007 | Cannot proceed without address | Checkout | High     | -                 | 1. Do not select address<br>2. Click Continue | Error shown, cannot proceed             |               |          |

---

## **11. Address Management**

| Test Case ID | Test Case Title        | Module             | Priority | Test Data                  | Steps                                                     | Expected Result             | Actual Result | Comments |
| ------------ | ---------------------- | ------------------ | -------- | -------------------------- | --------------------------------------------------------- | --------------------------- | ------------- | -------- |
| TC_ADDR_001  | Add new address        | Address Management | Medium   | Address details            | 1. Click Add Address<br>2. Enter valid details<br>3. Save | Address saved               |               |          |
| TC_ADDR_002  | Validate pincode/phone | Address Management | Medium   | Pincode: 123<br>Phone: abc | 1. Enter invalid inputs<br>2. Save                        | Validation errors displayed |               |          |
| TC_ADDR_003  | Edit address           | Address Management | Medium   | Existing address           | 1. Click Edit<br>2. Update details<br>3. Save             | Updated address saved       |               |          |
| TC_ADDR_004  | Delete address         | Address Management | Medium   | Existing address           | 1. Click Delete<br>2. Confirm                             | Address removed             |               |          |
| TC_ADDR_005  | Mark as default        | Address Management | Medium   | Existing address           | 1. Select default option                                  | Address marked default      |               |          |

---

## **12. Payment (Dummy Data)**

| Test Case ID | Test Case Title                  | Module  | Priority | Test Data                    | Steps                           | Expected Result                     | Actual Result | Comments |
| ------------ | -------------------------------- | ------- | -------- | ---------------------------- | ------------------------------- | ----------------------------------- | ------------- | -------- |
| TC_PAY_001   | Payment options load             | Payment | High     | -                            | 1. Open payment page            | Card, UPI, Wallets, COD visible     |               |          |
| TC_PAY_002   | Valid card payment               | Payment | High     | Card: Valid dummy            | 1. Enter card details<br>2. Pay | Payment successful, order confirmed |               |          |
| TC_PAY_003   | Invalid card details             | Payment | High     | Card: Invalid                | 1. Enter invalid card<br>2. Pay | Error message displayed             |               |          |
| TC_PAY_004   | Expired card                     | Payment | Medium   | Card: Expired                | 1. Enter expired card<br>2. Pay | Error message displayed             |               |          |
| TC_PAY_005   | Incorrect UPI ID                 | Payment | Medium   | UPI: wrong@upi               | 1. Enter UPI ID<br>2. Pay       | Error message displayed             |               |          |
| TC_PAY_006   | Cancel payment                   | Payment | Medium   | -                            | 1. Click Cancel                 | Returns to checkout                 |               |          |
| TC_PAY_007   | Payment timeout handling         | Payment | Medium   | -                            | 1. Simulate timeout             | Proper error message                |               |          |
| TC_PAY_008   | Order confirmation after payment | Payment | High     | -                            | 1. Complete payment             | Order confirmation page appears     |               |          |
| TC_PAY_009   | COD availability                 | Payment | Medium   | COD eligible address/product | 1. Select COD                   | COD option available                |               |          |

---

## **13. Order Summary**

| Test Case ID     | Test Case Title            | Module        | Priority | Test Data | Steps                                      | Expected Result                          | Actual Result | Comments |
| ---------------- | -------------------------- | ------------- | -------- | --------- | ------------------------------------------ | ---------------------------------------- | ------------- | -------- |
| TC_ORDER_SUM_001 | Verify order details       | Order Summary | High     | -         | 1. Open order summary                      | Product, price, address, payment correct |               |          |
| TC_ORDER_SUM_002 | Verify order ID generation | Order Summary | High     | -         | 1. Place order                             | Unique order ID generated                |               |          |
| TC_ORDER_SUM_003 | Invoice download/print     | Order Summary | Medium   | -         | 1. Click download/print                    | Invoice downloaded or printed            |               |          |
| TC_ORDER_SUM_004 | Links functional           | Order Summary | Medium   | -         | 1. Click Continue Shopping/Go to My Orders | Navigates correctly                      |               |          |

---

## **14. Order Tracking**

| Test Case ID | Test Case Title                    | Module         | Priority | Test Data          | Steps                              | Expected Result                                                          | Actual Result | Comments |
| ------------ | ---------------------------------- | -------------- | -------- | ------------------ | ---------------------------------- | ------------------------------------------------------------------------ | ------------- | -------- |
| TC_TRACK_001 | Order appears in My Orders         | Order Tracking | High     | -                  | 1. Login<br>2. Check My Orders     | Order visible                                                            |               |          |
| TC_TRACK_002 | Verify order statuses              | Order Tracking | High     | -                  | 1. Track order                     | Status updates: Placed → Packed → Shipped → Out for Delivery → Delivered |               |          |
| TC_TRACK_003 | Tracking link                      | Order Tracking | Medium   | -                  | 1. Click tracking link             | Opens courier tracking page                                              |               |          |
| TC_TRACK_004 | Cancel order before shipment       | Order Tracking | Medium   | Pre-shipment order | 1. Click Cancel                    | Order cancelled                                                          |               |          |
| TC_TRACK_005 | Refund for prepaid cancelled order | Order Tracking | Medium   | Prepaid order      | 1. Cancel order<br>2. Check refund | Refund initiated                                                         |               |          |
| TC_TRACK_006 | Reorder past order                 | Order Tracking | Medium   | Previous order     | 1. Click Reorder                   | Products added to cart                                                   |               |          |

