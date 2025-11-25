# **Test Execution Report**

**Project:** OpenCart E-Commerce Web Application
**Prepared By:** QA Engineer
**Test Cycle:** Cycle 01
**Date:** DD/MM/YYYY
**Test Environment:** Chrome v119, Windows 10 / 11, [https://demo.opencart.com](https://demo.opencart.com)

---

## **1. Objective**

The purpose of this report is to summarize the test execution status for the OpenCart application, including pass/fail statistics, blocked cases, and defect references.

---

## **2. Test Summary**

| Total Test Cases | Executed | Passed | Failed | Blocked | Execution Coverage | Pass % |
| ---------------- | -------- | ------ | ------ | ------- | ------------------ | ------ |
| 45               | 45       | 38     | 5      | 2       | 100%               | 84%    |

---

## **3. Test Execution Status by Module**

| Module             | Total | Executed | Passed | Failed | Blocked |
| ------------------ | ----- | -------- | ------ | ------ | ------- |
| Login              | 5     | 5        | 4      | 1      | 0       |
| Registration       | 7     | 7        | 6      | 1      | 0       |
| Search             | 4     | 4        | 3      | 1      | 0       |
| Product Page (PDP) | 6     | 6        | 5      | 1      | 0       |
| Cart               | 5     | 5        | 3      | 1      | 1       |
| Checkout           | 6     | 6        | 5      | 0      | 1       |
| Wishlist           | 3     | 3        | 3      | 0      | 0       |
| Orders             | 4     | 4        | 4      | 0      | 0       |
| Admin Modules      | 5     | 5        | 4      | 1      | 0       |

---

## **4. Defects Linked to Failed Test Cases**

| Test Case ID  | Module       | Description                                   | Defect ID  | Severity |
| ------------- | ------------ | --------------------------------------------- | ---------- | -------- |
| TC_LOGIN_003  | Login        | Error message not displayed for invalid login | BUG_OC_001 | High     |
| TC_REG_006    | Registration | Weak password accepted                        | BUG_OC_002 | High     |
| TC_SEARCH_002 | Search       | Irrelevant search results                     | BUG_OC_003 | Medium   |
| TC_PDP_002    | Product Page | Product images not loading                    | BUG_OC_004 | Critical |
| TC_CART_002   | Cart         | Cart totals not updating                      | BUG_OC_005 | High     |

---

## **5. Blocked Test Cases**

| Test Case ID | Module   | Reason                                    |
| ------------ | -------- | ----------------------------------------- |
| TC_CART_004  | Cart     | Dependent on BUG_OC_005                   |
| TC_CO_002    | Checkout | Address validation impacted by BUG_OC_002 |

---

## **6. Observations & Remarks**

* Core flows (Login, Registration, Cart, Checkout, PDP) executed successfully except for defects noted.
* Critical issues in product images and cart calculations need immediate attention.
* Overall application is stable for further testing cycles after bug fixes.

