# 🏥 Service Booking System – Process Documentation

## 1. Patient Onboarding

- **New Patient**:
  
  - Registers with **basic details** (Name, Age, Gender, Contact, Address, ID proof if needed).
  - Creates a **Patient ID** in the system.
- **Returning Patient**:
  
  - Uses Patient ID / Phone number to access records.
  - Previous history auto-linked.

---

## 2. Appointment / Booking Scenarios

### **A. Regular Appointment (First Visit)**

- Patient books a **general appointment** (doctor consultation or health check-up).
- Tests may be prescribed after consultation.

### **B. Walk-in with Prescription**

- Patient arrives with a **doctor’s prescription** mentioning test names.
- Staff uploads/scans the document or selects equivalent tests from system catalog.
- Booking created for those tests.

### **C. Self-requested / Preventive Tests (No Prescription Needed)**

- Some tests (like blood sugar, cholesterol, vitamin levels, routine blood panel, pregnancy test, eye checkup, etc.) do **not require prescription**.
- Patient can directly choose these tests from the catalog.

---

## 3. Test Categorization

Tests are grouped into:

- **Prescription-only Tests** → e.g., MRI, CT Scan, certain hormone/genetic tests.
- **Self-requested / Walk-in Tests** → e.g., Blood sugar, Lipid profile, Eye vision check, X-ray (sometimes).
- **Packages** (Health check bundles) → e.g., Full Body Checkup, Diabetes Package.

The software must enforce these rules during booking.

---

## 4. Booking Workflow

**Step 1: Service Selection**

- Patient (or staff) selects test(s) or package.
- Prescription uploaded if required.

**Step 2: Slot & Location**

- Choose test center/branch.
- Select date & available time slot.

**Step 3: Payment**

- Cash / Card / UPI / Insurance (if applicable).

**Step 4: Confirmation**

- Patient receives booking ID + reminders (SMS/Email/WhatsApp).

**Step 5: Test Execution**

- Patient visits center OR technician visits home (if home collection).
- Sample/test performed.

**Step 6: Processing & Reporting**

- Test processed in lab.
- Report uploaded to patient portal.
- Patient notified when results are ready.

---

## 5. System Features (Minimum Necessary)

- **Patient Registration & History Tracking**
- **Test Catalog** with categories: Prescription-only, Non-prescription, Packages
- **Prescription Upload Module**
- **Appointment Scheduling** (slot booking, calendar)
- **Payment Gateway Integration**
- **Notification System** (reminders, results ready alerts)
- **Report Management** (digital reports in PDF)
- **Admin Dashboard** (for test center to track workload & revenue)

---

## 6. Example Flow Diagram (Simplified)

```
[Patient Registration] 
        ↓
[Choose Test/Service]
        ↓
   ┌───────────────┬───────────────┐
   │ Self-request  │ Doctor Presc. │
   │ (Allowed)     │ (Required)    │
   └───────────────┴───────────────┘
        ↓
[Slot & Location Selection]
        ↓
[Payment & Confirmation]
        ↓
[Test Performed]
        ↓
[Processing in Lab]
        ↓
[Report Uploaded & Notified]
```



