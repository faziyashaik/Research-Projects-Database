# Research Projects Database

A lightweight relational schema for tracking **research projects**, their funding agencies, and the employees who work on (and manage) them.  
The design is intended for instructional / demo use—feel free to extend it for production scenarios.

---

## 📐  Entity–Relationship Overview
| Entity           | Key(s)              | Important Attributes                 | Relationships |
|------------------|---------------------|--------------------------------------|---------------|
| **Employee**     | `SSN`               | `Emp_Name`, `Salary`                 | • Works on ⇄ **Project** (M : N)<br>• May **manage** a project |
| **FundingAgency**| `Agency_ID`         | `Name`, `Address`                    | • Funds 1 : N **Project** |
| **Project**      | `Project_ID`        | `Agency_ID` (FK), `Name`, `Duration`, `Budget` | • Funded by 1 **FundingAgency**<br>• Managed by 1 **Employee**<br>• Has many **Employee** collaborators |

<details>
<summary>ER D​iagram (text)</summary>

![image](https://github.com/user-attachments/assets/73527630-c368-41d4-b34d-97936b88860c)
![pj1](https://github.com/user-attachments/assets/cc7801fc-eeaf-4977-b202-bd9d67521d5d)
