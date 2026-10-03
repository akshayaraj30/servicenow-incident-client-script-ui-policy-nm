# ServiceNow Incident Management – Client Script & UI Policy

## 📌 Project Title

**Implement Client Script & UI Policy (Incident)**

---

## 📖 Project Overview

This project demonstrates the implementation of **Client Scripts** and **UI Policies** in ServiceNow Incident Management.

The project focuses on controlling Incident form behavior dynamically based on field values. It implements conditional mandatory fields, read-only controls, automatic field updates, save-time validation, and restrictions on list editing.

The implementation is designed to improve **data integrity, validation, and user experience** while creating and updating Incident records.

---

## 🎯 Objective

The main objective of this project is to demonstrate how ServiceNow client-side configurations can be used to:

- Enforce data integrity
- Dynamically make fields mandatory
- Automatically populate field values
- Control field behavior based on conditions
- Validate data before saving an Incident
- Restrict unwanted list-based modifications
- Improve Incident form usability

---

## 🛠️ Platform & Technologies

- **Platform:** ServiceNow
- **Application:** Incident Management
- **Table:** Incident
- **Configuration Types:**
  - UI Policy
  - UI Policy Action
  - Client Script
- **Client Script Types:**
  - onChange
  - onSubmit
  - onCellEdit

---

# ⚙️ Project Features

The project implements the following features:

1. High Impact Control using UI Policy
2. Urgency field read-only control
3. Automatic Urgency update using onChange Client Script
4. Assigned To validation using onSubmit Client Script
5. State list-edit blocking using onCellEdit Client Script
6. Complete functional testing of all configurations

---

# 🔹 Task 1 – High Impact Control UI Policy

## Purpose

A UI Policy named **High Impact Control** was created for the Incident table.

The policy is triggered when the Incident **Impact** field is set to **1 – High**.

When the condition is satisfied, the **Assignment Group** field becomes mandatory.

### Configuration

| Property | Value |
|---|---|
| Name | High Impact Control |
| Table | Incident |
| Active | True |
| Condition | Impact is 1 – High |
| Reverse if false | True |

### UI Policy Action

The UI Policy Action makes:

**Assignment Group → Mandatory**

This ensures that an Incident with high impact contains an appropriate Assignment Group.

---

# 🔹 Task 2 – UI Policy Action – Urgency

An additional UI Policy Action was created under the **High Impact Control** UI Policy.

When Impact is High, the **Urgency** field becomes read-only.

### Configuration

| Property | Value |
|---|---|
| UI Policy | High Impact Control |
| Field | Urgency |
| Read-only | True |
| Visible | Unchanged |

### Expected Behavior

When:

```text
Impact = High
