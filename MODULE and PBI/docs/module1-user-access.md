# Module 1: User Access and Personal Information Management

## Overview
This module provides the account and identity foundation for all system users, including customers, specialists, and administrators. It supports account registration, login verification, password recovery, active logout, and personal profile editing with system validation.

## Primary Stakeholders
- Customer
- Specialist
- Administrator / Operations Manager

## Operational Context
This module supports basic account operations and personal profile management for customers, specialists, and administrators. It covers email-password registration confirmation, login, password retrieval, active logout, and individual profile editing and authentication. It provides a secure account basis for customers to book specialist services later, for administrators to handle system operations, and for specialists to access consultation services.

---

## PBI 1: New User Email-Password Registration Verification

**User Story**  
As a new customer/specialist/administrator, I want to complete account registration by filling in my email and password with system verification, so that I can obtain a unique legal account for the system.

**Acceptance Criteria**
1. Given the input email does not conform to the general format of `xxx@xxx.xxx`, when the registration information is submitted, then the system prompts “Please enter a valid email address” and rejects the registration.
2. Given the email already exists in the system, when the registration information is submitted, then the system prompts “This email has been registered” and rejects the registration.
3. Given the input password does not meet the rule (at least 8 characters, including numbers, letters, and special characters), when the registration information is submitted, then the system prompts “Password is invalid” and rejects the registration.
4. Given the email is valid and unique, and the password meets the rule, when the registration information is submitted, then the system prompts “Registration successful” and redirects to the login page within 2 seconds.

---

## PBI 2: Registered User Account Login Verification

**User Story**  
As a registered customer/specialist/administrator, I want to log in to the system with my email and password, so that I can verify my identity and access the role-specific operation interface.

**Acceptance Criteria**
1. Given the email is unregistered or the password does not match the email, when the login information is submitted, then the system prompts “This email is not registered” or “Incorrect password” respectively and rejects the login.
2. Given the incorrect password is entered 3 times in a row, when attempting to log in again, then the system prompts “Account locked for 10 minutes” and blocks login requests for the account.
3. Given the “Forgot Password” button on the login page is clicked, when the click operation is confirmed, then within 2 seconds a separate forgot password screen opens up for password retrieval.
4. Given the email and password are correct, when the login information is submitted, then the system redirects to the role-specific homepage and creates an encrypted login session within 3 seconds.

---

## PBI 3: Registered User Password Recovery

**User Story**  
As a customer/specialist/administrator who has forgotten my password, I want to recover my password via my registered email, so that I can reset my password and log in to the system normally.

**Acceptance Criteria**
1. Given an unregistered email is entered on the recovery page, when “Get Verification Code” is clicked, then the system prompts “This email is not registered, password recovery is unavailable”.
2. Given a registered email is entered, when “Get Verification Code” is clicked, then the system sends a 6-digit numeric verification code to the email within 1 minute, and the page displays a verification code input box with a countdown.
3. Given an incorrect or expired verification code is entered, when “Verify” is clicked, then the system prompts “Verification code is incorrect/expired, please re-obtain”.
4. Given the verification code is verified successfully, when the verification result is confirmed by the system, then the system redirects to the new password setting page, requiring a new password that meets the registration password rules.
5. Given the new password is set successfully, when the new password submission is completed, then the system prompts “Password reset successful” and redirects to the login page within 2 seconds; the new password can be used for normal login.

---

## PBI 4: Active Logout for Logged-in Users

**User Story**  
As a logged-in customer/specialist/administrator, I want to log out of the system with one click, so that I can manually terminate the login session and ensure account security.

**Acceptance Criteria**
1. Given the user is in the logged-in state, when the “Logout” button at the top right of the page is clicked, then the system immediately pops up a secondary confirmation prompt “Confirm logout?”.
2. Given the user is in the logged-in state and the logout confirmation is triggered, when “Confirm” in the prompt box is clicked, then the system clears the encrypted login session and redirects to the login page within 2 seconds.
3. Given the manual logout is completed, when attempting to access role-specific functions, then the system directly blocks the access and prompts “Please log in first”.

---

## PBI 5: Personal Profile Self-Editing and Verification

**User Story**  
As a logged-in customer/specialist/administrator, I want to edit my name, mobile phone number, and email with system verification, so that I can ensure the accuracy and validity of my personal information.

**Acceptance Criteria**
1. Given the name is edited (no format restrictions), when the modification is submitted, then the system saves it immediately, prompts “Profile updated successfully”, and synchronizes the name across all pages in real time.
2. Given the input mobile phone number is not an 11-digit pure number, when the modification is submitted, then the system prompts “Please enter an 11-digit pure number mobile phone number” and rejects the save.
3. Given the input email does not conform to the general format of `xxx@xxx.xxx`, when the modification is submitted, then the system prompts “Please enter a valid email address” and rejects the save.
4. Given the edited mobile phone number or email meets the format rules, when “Get Verification” is clicked, then the system sends a 6-digit numeric verification code to the new mobile phone number and a verification link to the new email within 1 minute.
5. Given the verification code or link is verified successfully, when the modification is submitted, then the system prompts “Profile updated successfully” and synchronizes the personal information across all pages within 5 seconds; the new information takes effect officially.

---

## Summary
Module 1 establishes the identity and account management foundation of the Specialist Consultation Booking System. It ensures that users can securely register, log in, recover access, log out safely, and maintain valid personal information before using later business functions such as booking and consultation services.
