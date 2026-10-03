# 🚀 Naan Mudhalvan

# PROJECT: IMPLEMENT CLIENT SCRIPT & UI POLICY

# 🚀 ServiceNow Incident Management

### *Powered by ServiceNow Incident Management*

![ServiceNow](https://img.shields.io/badge/Platform-ServiceNow-107C41?style=for-the-badge&logo=servicenow&logoColor=white)
![Client Script](https://img.shields.io/badge/Configuration-Client%20Script-FF6F00?style=for-the-badge)
![UI Policy](https://img.shields.io/badge/Configuration-UI%20Policy-0078D4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

# 🚀 ServiceNow Incident Management


## 👥 Team Members

- **Akshaya B** — Team Lead
- **Madhusri S T** — Team Member

![ServiceNow](https://img.shields.io/badge/Platform-ServiceNow-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Project Overview

This project demonstrates the implementation of **Client Scripts** and **UI Policies** in ServiceNow Incident Management.

The project focuses on dynamically controlling Incident form behavior, validating data, and improving data integrity and user experience.

---

## 🎯 Objective

The main objective of this project is to demonstrate how ServiceNow client-side configurations can be used to:

- Enforce data integrity
- Dynamically make fields mandatory
- Automatically populate field values
- Control field behavior based on conditions
- Validate data before saving an Incident
- Restrict unwanted list-based modifications

---

## 🛠️ Technologies

- ServiceNow
- Incident Management
- UI Policy
- UI Policy Action
- Client Script
  - onChange
  - onSubmit
  - onCellEdit

---

## ⚙️ Key Features

1. High Impact Control using UI Policy
2. Urgency field read-only control
3. Automatic Urgency update using onChange Client Script
4. Assigned To validation using onSubmit Client Script
5. State list-edit blocking using onCellEdit Client Script
6. Functional testing of all configurations

---

## 🔹 Task 1 – High Impact Control

A UI Policy named **High Impact Control** was created for the Incident table.

When **Impact = 1 – High**, the **Assignment Group** field becomes mandatory.

### Configuration

| Property | Value |
|---|---|
| Name | High Impact Control |
| Table | Incident |
| Active | True |
| Condition | Impact is 1 – High |
| Reverse if false | True |

---

## 🔹 Task 2 – Urgency Read-Only Control

An additional UI Policy Action was created under the **High Impact Control** UI Policy.

When Impact is High, the **Urgency** field becomes read-only.

| Property | Value |
|---|---|
| UI Policy | High Impact Control |
| Field | Urgency |
| Read-only | True |
| Visible | Unchanged |

---

## 🔹 Task 3 – Automatic Urgency Update

An **onChange Client Script** was implemented to automatically update the Urgency field based on the selected Incident field values.

This helps maintain consistent Incident data and reduces manual entry.

---

## 🔹 Task 4 – Assigned To Validation

An **onSubmit Client Script** was implemented to validate the **Assigned To** field before submitting an Incident.

This prevents the Incident from being saved when the required validation condition is not satisfied.

---

## 🔹 Task 5 – State List-Edit Blocking

An **onCellEdit Client Script** was implemented to control changes made to the **State** field directly from the Incident list.

This helps prevent unwanted or invalid list-based modifications.

---

## 📸 Screenshots

Screenshots of the implemented UI Policies, UI Policy Actions, and Client Scripts are included in this repository.

---

## ✅ Project Status

**Completed**
