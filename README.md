# Webapp-UI-Testcases
Manual, UI, and exploratory testing of the Urban Routes web application, focusing on the carsharing feature and the unreleased Aero Taxi feature (QA Bootcamp Projecy)
# Urban Routes Web App QA Testing
This project includes manual and exploratory QA testing for the Urban Routes app, completed as part of the Tripleten QA Engineering bootcamp

## Project Summary
- Tested Features:
  - Carsharing: a previously existing feature that was recoded and tested as if it was new
  - Aero Taxi: a confidential feature not yet released and was accessed for early testing
- Testing focus: Functional, regression, and exploratory testing
- Platform: Web (Chrome)
- Tools: Excel (test cases), Jira (bug tracking), Chrome browser developer tools

## Requirements analysis
Before testing, I reviewed the feature requirements documents to understand the app's intended functionality and guide test case development.

### Carsharing Payments Feature

- FR-CS32: Add Card for Payment
  - User must enter card number and CVV/CVC to activate the “Add” button
  - User can add multiple cards; no restriction on number of cards added
  - Clicking “Add” submits the card details for processing

- FR-CS33: Input Validation Rules
  Card Number:
  - Must be numeric only
  - Exactly 12 digits required (auto-format as `nnnn nnnn nnnn`)
  - Boundary values: 0000 to 9999 for each block
  - Add button remains inactive if length is < 12 digits
    
- CVV/CVC:
  - Must be numeric only
  - Exactly 2 digits required (format: `nn`)
  - Boundary values: 01 to 99
  - Add button remains inactive if length is < 2 digits
- Automatic formatting is applied when the input field loses focus

- FR-CS35 (Optional): Encryption
  -Card payment details must be encrypted during transmission from client to server

### Aero Taxi Booking Feature

- FR-AT4: Travel Time & Cost Calculation
  - The system must accurately calculate total travel time and total cost based on input parameters

- FR-AT6: Display of Results
- The system must display the calculated total travel time and total cost to the user after booking inputs are completed

These atomic blocks were used to design targeted manual and UI test cases to validate both front-end behavior and business logic alignment with requirements.
 
## Files Included
1.`Deedee Ozoh — Sprint 3 Sheets.xlsx`: Manual test cases for carsharing and Aero taxi features
2.`Deedee Ozoh, Sprint 3 Project.pdf`: Decomposition of key functional requirements into atomic, testable blocks

## Highlights
- Designed tests based on decomposed requirements using boundary value analysis and equivalence partitioning
- Performed regression testing on the carsharing feature to ensure existing functionality remained intact after code changes
- Discovered multiple bugs in the unreleased Aero Taxi feature; all 4 test cases failed due to the feature showing a blank white page instead of calculating and presenting the travel time and cost
- 
