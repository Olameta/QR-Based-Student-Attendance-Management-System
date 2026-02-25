🔬 Research Project: Automated Student Attendance System via QR Codes

An academic study exploring the application of **Computer Vision (CV)** and **Relational Database Management** to mitigate "buddy signing" and administrative overhead in higher education.

This project demonstrates the integration of **QR Code decoding, image processing, and secure database storage** to create a verifiable and automated attendance tracking system.

---

## 📖 Research Abstract

Manual attendance tracking is inefficient and error-prone.  
This system leverages **QR Code Steganography** and **Image Processing** to automate attendance logging. By using `PyZbar` for decoding and `SQLite` for immutable record-keeping, the system provides:

- Accurate verification of student presence  
- Reduced administrative workload  
- An auditable digital attendance trail  

---

## 🏗️ Technical Architecture & Methodology

The system follows a **Three-Tier Architecture** for modularity and maintainability.

### 1️⃣ Logic Layer (Computer Vision)

The **Decoding Engine** performs:

- **Grayscale Transformation:** Normalizes images for consistent QR bit detection  
- **Localization:** Detects "Position Detection Patterns" in QR corners  
- **Bitstream Extraction:** Converts pixel patterns into a unique student identifier  

### 2️⃣ Data Layer (Relational Modeling)

- **SQLite3 Backend** ensures referential integrity  
- Attendance logs are strictly mapped to validated `username` entries in the `users` table  
- Prevents orphaned or inconsistent records  

---

## 📊 System Design (UML)

The project follows **Software Engineering (SDLC)** principles:

- **Process Sequence Diagram:** Shows interaction between Student, Python decoding logic, and Database  
- **Use Case Diagram:** Defines strict permissions—only authorized Teachers can generate valid QR codes  

---

## 🛠️ Technical Stack

| Category     | Technology                     | Purpose                                  |
|-------------|--------------------------------|------------------------------------------|
| CV Engine    | OpenCV / PyZbar                | QR localization & data extraction       |
| Backend      | Python 3.10                    | Business logic & session validation     |
| Database     | SQLite3                        | Persistent storage of timestamped logs  |
| Interface    | Gradio                         | Modern, web-based tabbed dashboard      |

---

## 📂 Repository Structure


.
├── student_attendance_tracker_notebook.py # Primary Source Code
├── Group 18 report.pdf # Full Research Paper (PDF)
├── group_18_uml_diagram/ # Architectural Blueprints
│ ├── class_uml_diagram.jpg # Data Relationships
│ ├── sequence_uml_diagram.jpg # Process Timeline
│ └── use_case_diagram.jpg # Actor Roles
├── .gitignore # Environment Config
└── README.md # Research Documentation

## ⚙️ Installation, Deployment, Research Findings & License

To run this project, first install the required system dependency (for Linux/Ubuntu/Colab):

sudo apt-get install libzbar0

Then install the required Python libraries:

pip install gradio qrcode pillow pyzbar opencv-python-headless

After installation, run the application with:

python student_attendance_tracker_notebook.py

The system will launch a web-based interface for uploading and decoding student QR codes.

---

### 📉 Research Findings & Conclusion

QR-based automation reduces attendance-taking from approximately 15 minutes per class (manual method) to under 10 seconds per student.

The system provides:
- A secure and verifiable digital attendance record
- Reduced administrative workload
- Structured and timestamped database logging

Future work may explore biometric integration to further enhance verification and prevent impersonation.

Academic Contribution: Group 18 | Software Engineering (CSC 403)

---

### 📄 License

This project is licensed under the MIT License.
