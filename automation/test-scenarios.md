# RedBus — Playwright Automation Test Scenarios

## 1. Purpose

This document defines the automated test scenarios planned for the RedBus web application using Playwright.

The scenarios focus on critical user journeys, functional validation, negative testing, and regression coverage.

---

## 2. Automation Scenario Matrix

| Scenario ID | Scenario                                      | Test Type  | Priority | Automation |
| ----------- | --------------------------------------------- | ---------- | -------- | ---------- |
| RB-AUTO-001 | Verify RedBus homepage loads successfully     | Smoke      | High     | Playwright |
| RB-AUTO-002 | Verify source location can be entered         | Functional | High     | Playwright |
| RB-AUTO-003 | Verify destination location can be entered    | Functional | High     | Playwright |
| RB-AUTO-004 | Verify valid source and destination selection | Functional | High     | Playwright |
| RB-AUTO-005 | Verify travel date selection                  | Functional | High     | Playwright |
| RB-AUTO-006 | Search buses using valid travel details       | End-to-End | High     | Playwright |
| RB-AUTO-007 | Validate search results                       | Functional | High     | Playwright |
| RB-AUTO-008 | Validate bus information displayed in results | Functional | Medium   | Playwright |
| RB-AUTO-009 | Apply bus filter                              | Functional | Medium   | Playwright |
| RB-AUTO-010 | Apply bus sorting                             | Functional | Medium   | Playwright |
| RB-AUTO-011 | Select an available bus                       | Functional | High     | Playwright |
| RB-AUTO-012 | Validate selected bus details                 | Functional | High     | Playwright |
| RB-AUTO-013 | Validate seat selection workflow              | Functional | High     | Playwright |
| RB-AUTO-014 | Select an available seat                      | Functional | High     | Playwright |
| RB-AUTO-015 | Validate passenger information form           | Functional | High     | Playwright |
| RB-AUTO-016 | Submit valid passenger information            | End-to-End | High     | Playwright |
| RB-AUTO-017 | Validate mandatory passenger fields           | Negative   | High     | Playwright |
| RB-AUTO-018 | Validate invalid passenger information        | Negative   | Medium   | Playwright |
| RB-AUTO-019 | Validate navigation between booking steps     | Functional | Medium   | Playwright |
| RB-AUTO-020 | Validate critical booking workflow            | End-to-End | Critical | Playwright |

---

## 3. Homepage Scenarios

### RB-AUTO-001 — Homepage Load

**Objective:** Verify that the RedBus homepage loads successfully.

**Expected Result:** The homepage loads without critical errors and the primary search interface is visible.

---

## 4. Search Scenarios

### RB-AUTO-002 — Source Location

**Objective:** Verify that a source location can be entered and selected.

**Expected Result:** The selected source location is displayed correctly.

### RB-AUTO-003 — Destination Location

**Objective:** Verify that a destination location can be entered and selected.

**Expected Result:** The selected destination location is displayed correctly.

### RB-AUTO-004 — Valid Route

**Objective:** Verify that valid source and destination locations can be selected.

**Expected Result:** Both locations are accepted and displayed correctly.

### RB-AUTO-005 — Travel Date

**Objective:** Verify that a valid travel date can be selected.

**Expected Result:** The selected date is displayed correctly.

### RB-AUTO-006 — Bus Search

**Objective:** Verify that buses can be searched using valid travel information.

**Expected Result:** Search results are displayed for the selected route and date.

---

## 5. Search Results Scenarios

### RB-AUTO-007 — Search Results

**Objective:** Verify that search results are displayed after a valid search.

**Expected Result:** Available results are displayed according to the selected search criteria.

### RB-AUTO-008 — Bus Information

**Objective:** Verify that important bus information is displayed.

**Expected Result:** Relevant information such as operator, timing, availability, and pricing is displayed where provided by the application.

### RB-AUTO-009 — Filtering

**Objective:** Verify that available search filters work correctly.

**Expected Result:** Results are filtered according to the selected criteria.

### RB-AUTO-010 — Sorting

**Objective:** Verify that available sorting options work correctly.

**Expected Result:** Search results are reordered according to the selected sorting option.

---

## 6. Bus Selection Scenarios

### RB-AUTO-011 — Select Bus

**Objective:** Verify that an available bus can be selected.

**Expected Result:** The selected bus is opened or expanded for further booking actions.

### RB-AUTO-012 — Verify Bus Details

**Objective:** Verify that the selected bus details are displayed correctly.

**Expected Result:** The relevant bus information is displayed without critical inconsistencies.

---

## 7. Seat Selection Scenarios

### RB-AUTO-013 — Seat Selection Workflow

**Objective:** Verify that the seat-selection workflow is accessible.

**Expected Result:** The seat-selection interface is displayed successfully.

### RB-AUTO-014 — Select Available Seat

**Objective:** Verify that an available seat can be selected.

**Expected Result:** The selected seat is visually identified and reflected in the booking workflow.

---

## 8. Passenger Information Scenarios

### RB-AUTO-015 — Passenger Form

**Objective:** Verify that the passenger information form is displayed correctly.

**Expected Result:** Required passenger fields and available controls are displayed.

### RB-AUTO-016 — Valid Passenger Information

**Objective:** Verify that valid passenger information can be entered.

**Expected Result:** Valid information is accepted and the workflow proceeds to the next stage.

### RB-AUTO-017 — Mandatory Field Validation

**Objective:** Verify validation of missing mandatory passenger information.

**Expected Result:** Appropriate validation messages are displayed and the workflow does not proceed until required information is provided.

### RB-AUTO-018 — Invalid Passenger Information

**Objective:** Verify that invalid passenger information is handled correctly.

**Expected Result:** Invalid information is rejected or appropriate validation is displayed.

---

## 9. Navigation Scenarios

### RB-AUTO-019 — Booking Navigation

**Objective:** Verify navigation between relevant booking steps.

**Expected Result:** Users can move through the workflow according to the application's expected behavior.

---

## 10. End-to-End Scenario

### RB-AUTO-020 — Critical Booking Workflow

**Objective:** Validate the critical RedBus user journey.

**Flow:**

1. Open RedBus.
2. Enter source.
3. Enter destination.
4. Select travel date.
5. Search for buses.
6. Validate search results.
7. Select an available bus.
8. Select an available seat where supported.
9. Enter passenger information.
10. Validate the next booking step.

**Expected Result:** Each stage behaves according to the application's expected workflow.

---

## 11. Negative Automation Scenarios

The automation suite should also consider:

* Empty source
* Empty destination
* Missing travel date
* Invalid search combinations
* Invalid passenger information
* Missing mandatory passenger information
* Attempting to continue without required selections
* Unavailable seat selection
* Unexpected navigation states

---

## 12. Regression Automation

The following scenarios are candidates for automated regression execution:

* Homepage availability
* Valid search
* Search result validation
* Filtering
* Sorting
* Bus selection
* Seat selection
* Passenger information validation
* Critical booking workflow

---

## 13. Automation Notes

The scenarios are designed for Playwright automation and should use:

* Stable locators
* Explicit assertions
* Reusable page components
* Independent test cases
* Appropriate synchronization
* Test data separation
* Failure diagnostics

AI-assisted development may be used to support test creation and maintenance, but every generated suggestion should be reviewed and validated before execution.

---

## 14. Project Status

These scenarios represent the planned automation coverage for the personal RedBus Playwright QA portfolio project.

Executable automation scripts will be added separately when the implementation is available.
