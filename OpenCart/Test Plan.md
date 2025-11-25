# OpenCart Test Plan

## 1. Introduction

This document outlines the approach and activities for testing the OpenCart demo application. The goal is to ensure that all essential user flows and core e‑commerce features work reliably. The plan is written in a practical, concise manner so it can be used directly in a real testing workflow.

## 2. Objectives

* Verify that major user-facing features behave as expected.
* Ensure key business flows—such as browsing, adding to cart, and checkout—operate without issues.
* Detect defects early and track them clearly for development.
* Maintain consistency through regression cycles whenever new fixes or updates are deployed.

## 3. Scope

### In Scope

* User account creation and login
* Navigation, product browsing, and filtering
* Product details validation
* Cart and wishlist behavior
* Checkout with test data
* Order history and profile actions
* Basic admin operations: product, category, and order checks
* Browser compatibility and responsive behaviour

### Out of Scope

* Live payment gateway integrations
* External plugins or marketplace extensions
* High‑volume load or performance benchmarking

## 4. Test Strategy

### 4.1 Test Types

* Functional validation of UI and workflows
* Basic usability checks
* Smoke tests for build verification
* Regression testing after major fixes
* Cross‑browser checks on commonly used browsers
* Responsive tests on mobile viewports

### 4.2 Test Design

Test cases will focus on realistic actions a user would perform. Data sets will include both valid and invalid combinations to uncover errors under normal usage.

## 5. Test Environment

* **URL:** [https://demo.opencart.com/](https://demo.opencart.com/)
* **Browsers:** Chrome, Firefox, Edge (latest versions)
* **Devices:** Laptop + mobile emulator
* **Data:** Test accounts, dummy addresses, and sample product sets

## 6. Roles & Responsibilities

* **Tester:** Write and execute tests, report issues, track retests.
* **QA Lead:** Review coverage, monitor progress, finalize reports.
* **Developer:** Investigate and resolve defects promptly.

## 7. Test Deliverables

* Test plan
* Test scenarios and cases
* Bug reports with evidence
* Daily/weekly execution status
* Final summary report

## 8. Entry & Exit Criteria

### Entry Criteria

* Application build deployed and stable
* Test data available
* Tools and environment ready

### Exit Criteria

* No open critical or major defects
* All planned test cases executed
* Summary report approved

## 9. Risk & Mitigation

| Risk                | Impact | Mitigation                     |
| ------------------- | ------ | ------------------------------ |
| Unstable builds     | High   | Coordinate early with dev team |
| Slow bug turnaround | Medium | Prioritize based on severity   |
| Environment issues  | High   | Keep alternate testing windows |

## 10. Schedule

| Activity     | Timeline |
| ------------ | -------- |
| Planning     | 1 day    |
| Test Design  | 2 days   |
| Execution    | 3–4 days |
| Regression   | 1 day    |
| Final Report | 1 day    |

## 11. Approval

* QA Lead: __________________
* Project Manager: __________________
* Date: __________________
