# Module 8: Expertise Category Management

## Overview
This module allows administrators to manage expertise categories used across the system. It ensures that category data is consistent, non-duplicated, and properly controlled for selection in booking and specialist management.

## Primary Stakeholders
- Administrator / Operations Manager

## Operational Context
The Administrator / Operations Manager is responsible for maintaining expertise categories that are used to classify specialists and support booking filtering.  
The system must support creating, viewing, updating, activating, and deactivating categories while preventing duplicate entries and ensuring only valid categories are selectable.

---

## PBI 1: Create a New Expertise Category

**User Story**  
As an Administrator / Operations Manager, I want to create a new expertise category, so that category data can be recorded consistently.

**Acceptance Criteria**
1. GIVEN the administrator is on the category creation page, WHEN a valid category name is submitted, THEN the system creates a new category record.
2. GIVEN a category is created, WHEN saved, THEN the system assigns a default status of "Active".
3. GIVEN the category list is accessed, WHEN displayed, THEN the new category appears with its name and status.
4. GIVEN the category name is empty, WHEN submitted, THEN the system rejects the input and displays an error message.

---

## PBI 2: View the Expertise Category List

**User Story**  
As an Administrator / Operations Manager, I want to view all expertise categories, so that I can manage them efficiently.

**Acceptance Criteria**
1. GIVEN categories exist, WHEN the list page is opened, THEN all categories are displayed.
2. GIVEN categories are displayed, WHEN viewing each record, THEN the system shows at least the category name and status.
3. GIVEN no categories exist, WHEN the page is accessed, THEN the system displays a “No expertise categories available” message.

---

## PBI 3: Update an Existing Expertise Category

**User Story**  
As an Administrator / Operations Manager, I want to update an existing category, so that incorrect or outdated information can be corrected.

**Acceptance Criteria**
1. GIVEN an existing category is selected, WHEN editing is initiated, THEN the system opens the category for modification.
2. GIVEN valid updates are submitted, WHEN saved, THEN the system updates the category successfully.
3. GIVEN the category list is viewed, WHEN displayed, THEN updated information is reflected.
4. GIVEN the updated name is empty, WHEN submitted, THEN the system rejects the update and displays an error.
5. GIVEN an update is made, WHEN saved, THEN only the selected record is changed.

---

## PBI 4: Activate or Deactivate an Expertise Category

**User Story**  
As an Administrator / Operations Manager, I want to activate or deactivate categories, so that obsolete categories can be controlled without deletion.

**Acceptance Criteria**
1. GIVEN a category is selected, WHEN the status is changed, THEN the system updates and saves the new status.
2. GIVEN the category list is displayed, WHEN viewed, THEN the updated status is visible.
3. GIVEN a category is inactive, WHEN listed, THEN it remains visible with status "Inactive".
4. GIVEN a category is inactive, WHEN selecting categories for other processes, THEN it is excluded from selection.
5. GIVEN status changes are saved, WHEN processed, THEN the category record remains stored in the system.

---

## PBI 5: Prevent Duplicate Expertise Category Names

**User Story**  
As an Administrator / Operations Manager, I want the system to prevent duplicate category names, so that category data remains unique and consistent.

**Acceptance Criteria**
1. GIVEN a category name already exists, WHEN creating a new category with the same name, THEN the system rejects the submission.
2. GIVEN a duplicate name is entered during update, WHEN submitted, THEN the system rejects the update.
3. GIVEN a unique name is provided, WHEN submitted, THEN the system accepts and saves the category.
4. GIVEN a submission is rejected due to duplication, WHEN processed, THEN existing records remain unchanged.
5. GIVEN the name is corrected after rejection, WHEN resubmitted, THEN the system accepts and saves successfully.

---

## Summary
Module 8 ensures that expertise categories are well-managed and consistent across the system. By preventing duplication, supporting status control, and maintaining data integrity, this module provides a reliable classification foundation for specialist management and booking processes.
