# 🔬 Research Project: Automated Student Attendance System via QR Codes

An academic study exploring the application of **Computer Vision (CV)** and **Relational Database Management** to mitigate "buddy signing" and administrative overhead in higher education.

This project demonstrates the integration of **QR Code decoding, image processing, and secure database storage** to create a verifiable and automated attendance tracking system.

---

## 📖 Research Abstract

Manual attendance tracking is inherently inefficient and error-prone.  
This system leverages **QR Code Steganography** and **Image Processing** to automate the process. By using `PyZbar` for decoding and `SQLite` for immutable record-keeping, the system provides:

- Accurate verification of student presence  
- Reduced administrative workload  
- An auditable digital attendance trail  

---

## 🏗️ Technical Architecture & Methodology

The system is built using a **Three-Tier Architecture** for modularity and maintainability.

### 1️⃣ Logic Layer (Computer Vision)

The **Decoding Engine** performs:

- **Grayscale Transformation:** Normalizes images for consistent QR bit detection.  
- **Localization:** Detects "Position Detection Patterns" in QR corners.  
- **Bitstream Extraction:** Converts pixel patterns into a unique student identifier.

### 2️⃣ Data Layer (Relational Modeling)

- **SQLite3 Backend** ensures referential integrity.  
- Attendance logs are strictly mapped to validated `username` entries in the `users` table.  
- Prevents orphaned or inconsistent records.

---

## 📊 System Design (UML)

The system follows **Software Engineering (SDLC)** principles:

- **Process Sequence Diagram:** Shows interaction between Student, Python decoding logic, and Database.  
- **Use Case Diagram:** Defines strict permissions—only authorized Teachers can generate valid QR codes.

---

## 🛠️ Technical Stack

| Category | Technology | Purpose |
|----------|------------|---------|
| **CV Engine** | OpenCV / PyZbar | QR localization & data extraction |
| **Backend** | Python 3.10 | Business logic & session validation |
| **Database** | SQLite3 | Persistent storage of timestamped attendance logs |
| **Interface** | Gradio | Modern, web-based tabbed dashboard |

---

## 📂 Research Repository Structure

```text
.
├── student_attendance_tracker_notebook.py  # Primary Source Code
├── Group 18 report.pdf                     # Full Research Paper (PDF)
├── group_18_uml_diagram/                   # Architectural Blueprints
│   ├── class_uml_diagram.jpg               # Data Relationships
│   ├── sequence_uml_diagram.jpg            # Process Timeline
│   └── use_case_diagram.jpg                # Actor Roles
├── .gitignore                              # Environment Config
└── README.md                               # Research Documentation
