# **Test Plan – Forever Web Application**

**Project:** Forever E-Commerce Website
**Document Type:** Test Plan
**Version:** 1.0
**Prepared By:** QA
**Date:** 23-11-2025

---

## **1. Introduction**

This test plan explains how the Forever e-commerce website will be tested. The goal is to check all important shopping features such as sign-up, login, searching products, adding items to the cart, placing an order, and viewing order details. The document also covers the scope of testing, the approach, environment details, and the list of items we will deliver at the end of testing.

---

## **2. Objectives**

* Ensure all main features on the Forever website work as expected.
* Verify that users can browse products, add them to cart, and successfully complete the checkout process.
* Identify defects early and share them with the development team.
* Check basic UI elements like buttons, labels, navigation, and layout consistency across browsers.

---

## **3. Scope**

### **In Scope**

* Functional testing of all user-facing modules
* UI and basic usability checks
* Smoke testing and regression testing
* Cross-browser checks (Chrome, Edge, Firefox)
* Payment flow using dummy card details
* Order tracking flow

### **Out of Scope**

* Performance/load testing
* API or backend-level testing
* Security testing (advanced tools)

---

## **4. Test Approach**

Testing will be carried out manually using the requirement documents and user stories.
Smoke tests will run after each new build to ensure major features are working.
Detailed regression tests will be executed before release.
All issues will be logged with screenshots, steps to reproduce, severity, and priority.
Retesting will be performed once fixes are provided.

---

## **5. Entry Criteria**

* All requirements are shared and finalized.
* Test environment is available.
* Test cases are written and reviewed.

### **Exit Criteria**

* All planned test cases are executed.
* No critical or high-severity defects remain open.
* Test summary report is prepared and reviewed.

---

## **6. Test Environment**

* **Operating System:** Windows 10/11
* **Browsers:** Chrome, Edge, Firefox (latest versions)
* **Test URL:** Staging / UAT website
* **Integrations:** Dummy Payment Gateway, Email OTP, SMS OTP

---

## **7. Tools Used**

(As part of manual QA, only essential tools are listed)

* **Test Case Documentation:** Excel / Google Sheets
* **Bug Tracking:** JIRA
* **Browser Tools:** Chrome DevTools
* **Documentation:** Google Docs / MS Word
* **Screenshots & Evidence:** Lightshot / Snipping Tool

---

## **8. Modules Covered**

* User Registration
* Login
* Home Page
* Product Search
* Categories & Filters
* Product Listing Page
* Product Detail Page
* Add to Cart
* Wishlist
* Checkout
* Address Management
* Payment (dummy cards)
* Order Summary
* Order Tracking

---

## **9. Test Data**

* Valid and invalid email IDs
* Strong/weak passwords
* Mobile numbers (valid/invalid)
* Sample product keywords
* Multiple delivery addresses
* Dummy payment card numbers
* Valid and expired coupon codes

---

## **10. Deliverables**

* Test Plan
* Test Cases
* Test Execution Sheet
* Defect Report
* RTM (Requirement Traceability Matrix)
* Test Summary Report
