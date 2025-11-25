# OpenCart Test Scenarios

## 1. User Registration

1. Verify new user can open the registration page from the "My Account" menu.
2. Verify user can register with valid mandatory details.
3. Verify error messages when submitting the form with missing mandatory fields.
4. Verify system prevents registration with an already registered email.
5. Verify user receives a success confirmation after completing registration.

## 2. User Login

1. Verify login page loads correctly from the "My Account" menu.
2. Verify login succeeds with valid credentials.
3. Verify login fails with invalid credentials.
4. Verify error message appears for empty username/password submission.
5. Verify user is redirected to account dashboard after login.

## 3. Product Search

1. Verify search returns relevant products for valid keywords.
2. Verify search results show accurate product information.
3. Verify search with partial keywords returns appropriate suggestions/results.
4. Verify system behavior when no products match the search.
5. Verify filters can be applied on search results.

## 4. Product Details Page

1. Verify product detail page loads with correct image, title, price, and description.
2. Verify user can switch between multiple product images.
3. Verify quantity box accepts only valid numeric inputs.
4. Verify "Add to Cart" and "Add to Wishlist" are displayed and functional.

## 5. Cart Operations

1. Verify product can be added to cart from product listing.
2. Verify cart updates when quantity is changed.
3. Verify item removal works correctly.
4. Verify price and total calculations are correct.
5. Verify cart persists after page refresh or navigation.

## 6. Wishlist

1. Verify user can add products to wishlist.
2. Verify wishlist items display correctly.
3. Verify wishlist items can be moved to cart.
4. Verify wishlist is cleared properly.

## 7. Checkout

1. Verify user can start checkout from the cart.
2. Verify guest checkout and registered user checkout flows.
3. Verify address fields accept valid input and validate incorrect values.
4. Verify order review displays correct items, prices, and totals.
5. Verify order can be placed using test/dummy payment.

## 8. Order History

1. Verify order history shows recently placed orders.
2. Verify order details view displays correct information.
3. Verify user can reorder existing items.

## 9. Admin Panel – Product Management

1. Verify admin can log in to the backend.
2. Verify admin can view the products list.
3. Verify a new product can be added with valid data.
4. Verify existing product details can be edited.
5. Verify admin can enable/disable products.

## 10. Admin Panel – Order Management

1. Verify admin can view new orders.
2. Verify order statuses can be updated.
3. Verify invoice generation function works correctly.

## 11. UI & Compatibility

1. Verify layout consistency across Chrome, Firefox, and Edge.
2. Verify responsiveness on mobile viewport.
3. Verify all major elements render properly without UI shifts.

## 12. General Scenarios

1. Verify breadcrumb navigation works across pages.
2. Verify site search and navigation remain functional after login/logout.
3. Verify error pages (404, invalid routes) display correctly.
4. Verify security validations like logout expiry and protected pages.
