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



![image](https://github.com/user-attachments/assets/3a44b5d3-2b9c-4242-ae11-b0d98b84a23c)

![image](https://github.com/user-attachments/assets/97be70d4-9317-4ec4-a738-d9c88bd16502)

