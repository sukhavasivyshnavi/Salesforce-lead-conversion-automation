# 🚀 Salesforce Automation: Lead Conversion Project

This project automates the **Lead Conversion process** in Salesforce using **Process Builder and Flow**. When a lead is marked as **Qualified**, the system automatically creates:

- An **Account**
- A **Contact**
- An **Opportunity**

---

## 🎯 Objective

Automate the manual process of lead conversion to improve sales efficiency and reduce human errors.

---

## 🧰 Tools & Features Used

- Salesforce Lightning Experience
- Process Builder
- Flow Builder (Record-Triggered Flow)
- Custom Fields (optional)
- Standard Lead Object

---

## 🔄 How the Automation Works

1. A user creates a new **Lead**.
2. When the **Lead Status** is updated to `Qualified`, a **Record-Triggered Flow** is executed.
3. The Flow:
   - Creates a **Contact** using Lead info
   - Creates an **Account** if not already existing
   - Creates an **Opportunity** linked to the new Account and Contact
4. The Lead gets marked as **Converted**

---

## 🖼️ Screenshots

| Lead Record Before Conversion | Flow Diagram in Flow Builder | Converted Account, Contact & Opportunity |
|-------------------------------|-------------------------------|------------------------------------------|
| ![lead-object](./screenshots/lead-object.png) | ![flow-diagram](./screenshots/process-builder-flow.png) | ![converted-records](./screenshots/converted-records.png) |

---

## 🧠 Logic Behind the Flow

- **Entry Condition**: Lead Status equals `Qualified`
- **Decision Element**: Checks if required fields like Company, Email are filled
- **Create Records Elements**:
  - Create Account (only if it doesn’t already exist)
  - Create Contact from Lead
  - Create Opportunity using Account and Contact
- **Update Lead**: Set converted fields (system-managed)

---

## 🛠️ Setup Instructions

1. Login to your Salesforce Developer Org
2. Navigate to **Flows** under Setup
3. Create a new **Record-Triggered Flow**
   - Object: `Lead`
   - Trigger: On `Update`
4. Build the flow logic:
   - Decision node
   - Create records
   - Update records
5. Activate the flow and test

---

## 📚 Learning Outcome

- Hands-on experience with Salesforce Flow
- Understanding of lead lifecycle and CRM best practices
- No Apex code needed (fully declarative)

---

## 📌 Use-Cases

- Automates lead follow-up and sales workflow
- Reduces manual conversion errors
- Great for B2B & B2C CRM systems

---

## ✨ Author

Vyshnavi Sukhavasi  
B.Tech CSE | Data & CRM Enthusiast

---

## 📃 License

This project is intended for educational and portfolio purposes.  
Salesforce, Lightning, and related marks are trademarks of Salesforce.com, Inc.
