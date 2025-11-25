# OpenCart Bug Report

> **Note:** This bug report is a practice sample created to demonstrate my understanding of QA documentation, bug reporting standards, and defect tracking workflow. These entries are not based on real defects in the OpenCart application.

---

## **Bug Summary**

| Bug ID    | Title                      | Module       | Severity | Status |
| --------- | -------------------------- | ------------ | -------- | ------ |
| OC_BUG_01 | Login button not working   | Login        | High     | Open   |
| OC_BUG_02 | Weak passwords accepted    | Registration | High     | Open   |
| OC_BUG_03 | Irrelevant items in search | Search       | Medium   | Open   |
| OC_BUG_04 | Product image not loading  | Product Page | Critical | Open   |
| OC_BUG_05 | Cart quantity not updating | Cart         | High     | Open   |

---

## **Detailed Bugs**

### **OC_BUG_01 – Login Button Not Working**

**Module:** Login
**Severity:** High
**Environment:** Chrome / Windows 10

**Steps:**

1. Open My Account → Login.
2. Enter valid email and password.
3. Click Login.

**Expected:** User should be logged in.
**Actual:** Button does nothing.
**Status:** Open

---

### **OC_BUG_02 – Weak Passwords Accepted**

**Module:** Registration
**Severity:** High

**Steps:**

1. Open Registration page.
2. Enter password like `12345`.
3. Submit form.

**Expected:** Password should be rejected with validation.
**Actual:** Account is created.
**Status:** Open

---

### **OC_BUG_03 – Irrelevant Search Results**

**Module:** Search
**Severity:** Medium

**Steps:**

1. Search for "Laptop".
2. Observe displayed products.

**Expected:** Only laptop-related items.
**Actual:** Random unrelated items.

**Status:** Open

---

### **OC_BUG_04 – Product Image Fails to Load**

**Module:** Product Page
**Severity:** Critical

**Steps:**

1. Open any product page.

**Expected:** Product image should load.
**Actual:** Broken image icon.
**Status:** Open

---

### **OC_BUG_05 – Cart Quantity Not Updating**

**Module:** Cart
**Severity:** High

**Steps:**

1. Add product to cart.
2. Change quantity.

**Expected:** Updated total price.
**Actual:** Quantity changes but total stays same.
**Status:** Open

