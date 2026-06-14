# Paychex GraphQL Schema

This document describes a conceptual GraphQL schema for the Paychex Developer APIs covering payroll, human resources, benefits, time and attendance, and related HR data services.

## Overview

Paychex provides REST-based APIs through its Developer Program for partners and clients to automate integrations with payroll and HR services. This GraphQL schema is a conceptual representation of the domain model exposed by those APIs, organized around companies, employees, payroll, time, benefits, and onboarding.

Source: https://developer.paychex.com/

## Schema Source

Conceptual — derived from Paychex Developer Program documentation and domain knowledge of payroll/HR platforms.

## Top-Level Types

- **Company** — employer entity with associated workers and payroll configuration
- **Employee** — worker record including personal info, employment, and pay data
- **PayStatement** — per-period payroll record with earnings, deductions, and taxes
- **BenefitEnrollment** — employee enrollment in a benefit plan
- **TimeEntry** — clock-in/clock-out or hour-entry record for time and attendance

## Domain Coverage

### Company and Organization
Company, CompanyDetails, Department, CostCenter, PayGroup, PayFrequency

### Employee Core
Employee, EmployeeDetails, EmployeeStatus, EmployeeProfile, PersonalInfo, FullName, BirthDate, Gender

### Employee Contact
HomeAddress, EmployeeAddress, ContactInfo, Phone, Email, EmergencyContact

### Sensitive / Compliance
SSN

### Employment
Employment, HireDate, TerminationDate, Position, JobTitle, Manager, ReportsTo

### Payroll
PayPeriod, PayStatement, Earning, EarningCode, Deduction, DeductionCode, NetPay

### Tax
Tax, FederalTax, StateTax, LocalTax

### Banking
DirectDeposit, BankAccount

### Benefits
Benefits, BenefitPlan, BenefitEnrollment

### Time and Attendance
TimeOff, LeaveType, LeaveBalance, TimeEntry, WorkHours, OvertimeHours, HolidayHours, SickHours, VacationHours

### Compliance / Garnishments
Garnishment, ChildSupport

### Onboarding
OnboardingTask, NewHireDocument, I9, W4, DirectDepositForm

### API Access
APIKey, OAuthToken, Webhook
