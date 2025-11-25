
# **OpenCart – Detailed Test Cases (Aligned With Default Features)**

---

# **1. User Registration**

> **OpenCart default registration fields:**

| Test Case ID   | Title                         | Module       | Priority | Test Data                                                                                                                             | Steps                                                                            | Expected Result                                             | Actual | Comments |
| -------------- | ----------------------------- | ------------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ----------------------------------------------------------- | ------ | -------- |
| **TC_REG_001** | Load Registration Page        | Registration | High     | –                                                                                                                                     | 1. Go to *My Account → Register*.                                                | Registration page loads with all input fields.              | –      | –        |
| **TC_REG_002** | Valid User Registration       | Registration | High     | First Name: John<br>Last Name: Doe<br>Email: [test123@gmail.com](mailto:test123@gmail.com)<br>Phone: 9876543210<br>Password: Test@123 | 1. Fill all mandatory fields.<br>2. Accept Privacy Policy.<br>3. Click Continue. | Account created and redirected to success page.             | –      | –        |
| **TC_REG_003** | Register Using Existing Email | Registration | High     | Existing Email: [demo@user.com](mailto:demo@user.com)                                                                                 | 1. Enter an already registered email.<br>2. Submit form.                         | Warning: **"E-Mail Address is already registered!"**        | –      | –        |
| **TC_REG_004** | Mandatory Field Validation    | Registration | Medium   | –                                                                                                                                     | 1. Leave fields blank.<br>2. Click Continue.                                     | Field-level validation messages appear.                     | –      | –        |
| **TC_REG_005** | Invalid Email Format          | Registration | Medium   | Email: abc.com                                                                                                                        | 1. Enter invalid email.<br>2. Submit.                                            | Error: **"E-Mail Address does not appear to be valid!"**    | –      | –        |
| **TC_REG_006** | Password & Confirm Mismatch   | Registration | High     | Password: Test123<br>Confirm: Test124                                                                                                 | 1. Enter mismatching passwords.<br>2. Submit.                                    | Error: **"Password confirmation does not match password!"** | –      | –        |
| **TC_REG_007** | Telephone Field Validation    | Registration | Medium   | Phone: blank or less than 3 digits                                                                                                    | 1. Enter invalid telephone.<br>2. Submit.                                        | Error: **"Telephone must be between 3 and 32 characters!"** | –      | –        |
| **TC_REG_008** | Privacy Policy Not Selected   | Registration | High     | –                                                                                                                                     | 1. Fill all fields.<br>2. Do not check Privacy Policy.<br>3. Submit.             | Error: **"You must agree to the Privacy Policy!"**          | –      | –        |

---

# **2. Login – Test Cases**

| Test Case ID     | Title                   | Module | Priority | Test Data                         | Steps                                                  | Expected Result                                                    | Actual | Comments |
| ---------------- | ----------------------- | ------ | -------- | --------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------------ | ------ | -------- |
| **TC_LOGIN_001** | Load Login Page         | Login  | High     | –                                 | 1. Go to *My Account → Login*.                         | Login page loads correctly.                                        | –      | –        |
| **TC_LOGIN_002** | Valid Login             | Login  | High     | Valid registered email & password | 1. Enter credentials.<br>2. Click Login.               | User redirected to account dashboard.                              | –      | –        |
| **TC_LOGIN_003** | Invalid Login           | Login  | High     | Incorrect password                | 1. Enter invalid credentials.<br>2. Submit login form. | Error: **"Warning: No match for E-Mail Address and/or Password."** | –      | –        |
| **TC_LOGIN_004** | Empty Fields Validation | Login  | Medium   | –                                 | 1. Click Login without entering anything.              | Validation warning displayed.                                      | –      | –        |

---

# **3. Product Search – Test Cases**

| Test Case ID      | Title                     | Module | Priority | Test Data        | Steps                                    | Expected Result                                                    | Actual | Comments |
| ----------------- | ------------------------- | ------ | -------- | ---------------- | ---------------------------------------- | ------------------------------------------------------------------ | ------ | -------- |
| **TC_SEARCH_001** | Search with Valid Keyword | Search | High     | Keyword: iPhone  | 1. Enter “iPhone”.<br>2. Click Search.   | Matching products displayed.                                       | –      | –        |
| **TC_SEARCH_002** | Search with No Results    | Search | Medium   | Keyword: zxq123  | 1. Search invalid term.                  | **"There is no product that matches the search criteria."** shown. | –      | –        |
| **TC_SEARCH_003** | Partial Keyword Search    | Search | Medium   | Keyword: “lap”   | 1. Enter partial term.<br>2. Search.     | Relevant suggestions appear.                                       | –      | –        |
| **TC_SEARCH_004** | Search Within Category    | Search | Medium   | Category: Phones | 1. Choose category filter.<br>2. Search. | Results filtered by selected category.                             | –      | –        |

---

# **4. Product Details Page (PDP)**

| Test Case ID   | Title              | Module | Priority | Steps                              | Expected Result                              | Actual | Comments |
| -------------- | ------------------ | ------ | -------- | ---------------------------------- | -------------------------------------------- | ------ | -------- |
| **TC_PDP_001** | Load PDP           | PDP    | High     | 1. Open product from listing.      | Name, price, images, availability displayed. | –      | –        |
| **TC_PDP_002** | Image Preview      | PDP    | Medium   | 1. Switch product image thumbnail. | Main image updates accordingly.              | –      | –        |
| **TC_PDP_003** | Add to Cart        | PDP    | High     | 1. Click Add to Cart.              | Success: product added to cart.              | –      | –        |
| **TC_PDP_004** | Out of Stock Check | PDP    | Medium   | 1. Open out-of-stock product.      | Add to Cart disabled or not allowed.         | –      | –        |

---

# **5. Cart – Test Cases**

| Test Case ID    | Title               | Module | Priority | Steps                                   | Expected Result               | Actual | Comments |
| --------------- | ------------------- | ------ | -------- | --------------------------------------- | ----------------------------- | ------ | -------- |
| **TC_CART_001** | Add Product to Cart | Cart   | High     | Add from listing or PDP.                | Product appears in cart.      | –      | –        |
| **TC_CART_002** | Update Quantity     | Cart   | High     | 1. Change quantity.<br>2. Click Update. | Cart total updates correctly. | –      | –        |
| **TC_CART_003** | Remove Item         | Cart   | Medium   | 1. Click Remove (X).                    | Item removed from cart.       | –      | –        |
| **TC_CART_004** | Cart Retains Items  | Cart   | Medium   | 1. Add items.<br>2. Refresh page.       | Cart retains added items.     | –      | –        |

---

# **6. Checkout – Test Cases**

> **OpenCart supports:** Guest checkout, Return customer checkout, Different shipping address.

| Test Case ID  | Title                          | Module   | Priority | Steps                                                  | Expected Result                        | Actual | Comments |
| ------------- | ------------------------------ | -------- | -------- | ------------------------------------------------------ | -------------------------------------- | ------ | -------- |
| **TC_CO_001** | Load Checkout Page             | Checkout | High     | 1. Go to cart.<br>2. Click Checkout.                   | Checkout page opens with all sections. | –      | –        |
| **TC_CO_002** | Guest Checkout Flow            | Checkout | High     | 1. Select Guest Checkout.<br>2. Enter required fields. | Proceeds to next steps smoothly.       | –      | –        |
| **TC_CO_003** | Address Field Validation       | Checkout | High     | 1. Leave address blank.<br>2. Continue.                | Required field errors displayed.       | –      | –        |
| **TC_CO_004** | Place Order (Cash On Delivery) | Checkout | High     | 1. Enter all details.<br>2. Select COD.<br>3. Confirm. | Order placed successfully.             | –      | –        |

---

# **7. Wishlist – Test Cases**

| Test Case ID  | Title                   | Module   | Priority | Steps                                   | Expected Result           | Actual | Comments |
| ------------- | ----------------------- | -------- | -------- | --------------------------------------- | ------------------------- | ------ | -------- |
| **TC_WL_001** | Add to Wishlist         | Wishlist | Medium   | 1. Click heart icon on product.         | Item added to wishlist.   | –      | –        |
| **TC_WL_002** | Wishlist Requires Login | Wishlist | Medium   | 1. Try adding wishlist when logged out. | Redirected to login page. | –      | –        |
| **TC_WL_003** | Move to Cart            | Wishlist | Medium   | 1. Open wishlist.<br>2. Add to Cart.    | Product moved to cart.    | –      | –        |

---

# **8. Order History – Test Cases**

| Test Case ID  | Title                    | Module | Priority | Steps                                             | Expected Result                              | Actual | Comments |
| ------------- | ------------------------ | ------ | -------- | ------------------------------------------------- | -------------------------------------------- | ------ | -------- |
| **TC_OH_001** | View Order History       | Orders | Medium   | 1. Login.<br>2. Navigate to Orders.               | Past orders displayed correctly.             | –      | –        |
| **TC_OH_002** | View Order Details       | Orders | Medium   | 1. Open any order.                                | All details shown (products, price, status). | –      | –        |
| **TC_OH_003** | Guest Cannot View Orders | Orders | Medium   | 1. Logout.<br>2. Try visiting order history page. | Redirect to login page.                      | –      | –        |

---

# **9. Admin – Product Management**

| Test Case ID   | Title           | Module         | Priority | Steps                                  | Expected Result                 | Actual | Comments |
| -------------- | --------------- | -------------- | -------- | -------------------------------------- | ------------------------------- | ------ | -------- |
| **TC_ADP_001** | Add Product     | Admin Products | High     | 1. Login admin.<br>2. Add new product. | Product added successfully.     | –      | –        |
| **TC_ADP_002** | Edit Product    | Admin Products | Medium   | 1. Edit details of existing product.   | Changes saved.                  | –      | –        |
| **TC_ADP_003** | Disable Product | Admin Products | Medium   | 1. Set Status = Disabled.<br>2. Save.  | Product hidden from storefront. | –      | –        |

---

# **10. Admin – Order Management**

| Test Case ID   | Title               | Module       | Priority | Steps                                     | Expected Result              | Actual | Comments |
| -------------- | ------------------- | ------------ | -------- | ----------------------------------------- | ---------------------------- | ------ | -------- |
| **TC_ADO_001** | View All Orders     | Admin Orders | High     | 1. Login admin.<br>2. Navigate to Orders. | All orders listed correctly. | –      | –        |
| **TC_ADO_002** | Update Order Status | Admin Orders | High     | 1. Change status (Pending → Shipped).     | Status updated successfully. | –      | –        |
| **TC_ADO_003** | Generate Invoice    | Admin Orders | Medium   | 1. Open order.<br>2. Click Invoice.       | PDF invoice generated.       | –      | –        |

---

# **11. UI & Compatibility**

| Test Case ID  | Title                 | Module | Priority | Steps                               | Expected Result                | Actual | Comments |
| ------------- | --------------------- | ------ | -------- | ----------------------------------- | ------------------------------ | ------ | -------- |
| **TC_UI_001** | Cross-Browser Testing | UI     | Medium   | Open site in Chrome, Firefox, Edge. | UI consistent across browsers. | –      | –        |
| **TC_UI_002** | Mobile Responsiveness | UI     | Medium   | Test site in mobile view.           | Responsive layout works.       | –      | –        |

---

