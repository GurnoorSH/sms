# Student Management System (SMS)

A secure, full‑stack MERN‑based Student Management System enabling role‑based access, robust data import/export, and automated reporting.

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [Getting Started](#getting-started)

   * [Prerequisites](#prerequisites)
   * [Installation](#installation)
   * [Configuration](#configuration)
5. [Usage](#usage)

   * [Running the Server](#running-the-server)
   * [Accessing the Frontend](#accessing-the-frontend)
6. [API Endpoints](#api-endpoints)
7. [Data Import & Export](#data-import--export)
8. [Authentication & Security](#authentication--security)
9. [Testing](#testing)
10. [Contributing](#contributing)
11. [License](#license)

---

## 🌟 Overview

The SMS project provides a scalable solution to manage student records, featuring:

* **Role‑Based Access Control:** Admin, Instructor, and Student roles.
* **Secure Authentication:** JWT tokens and OTP‑based password resets.
* **Data Management:** CRUD operations, CSV/JSON import‑export, and automated PDF reports.
* **Responsive UI:** Built with React, ShadCN UI, and Tailwind CSS.

## ✅ Features

* **Authentication:** JWT login, refresh tokens, and OTP password reset.
* **Student CRUD:** Add, update, delete, and view student profiles.
* **Bulk Data:** CSV/JSON upload and download for large‑scale record handling.
* **PDF Reports:** Generate and download student summaries via PDFKit.
* **Performance:** Mongoose pagination and optimized aggregations for fast queries.

## 🛠 Tech Stack

* **Frontend:** React, ShadCN UI, Tailwind CSS, Axios
* **Backend:** Node.js, Express.js, MongoDB, Mongoose
* **Auth & Security:** JWT, OTP, CORS, Input Validation
* **Utilities:** csvtojson, json2csv, pdfkit, mongoose‑aggregate‑paginate‑v2

## 🚀 Getting Started

### Prerequisites

* Node.js v14+ and npm
* MongoDB instance (local or cloud)

### Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/GurnoorSH/sms.git
   cd sms
   ```
2. **Install dependencies**

   ```bash
   npm install
   ```

### Configuration

1. **Environment Variables**
   Create a `.env` file in the root directory with:

   ```env
   PORT=5000
   MONGODB_URI=<your_mongo_uri>
   JWT_SECRET=<your_jwt_secret>
   OTP_SECRET=<your_otp_secret>
   ```

## 🎬 Usage

### Running the Server

```bash
npm run dev
```

### Accessing the Frontend

Open your browser and navigate to `http://localhost:3000` after starting the React app:

```bash
cd client
npm start
```

## 📡 API Endpoints

| Method | Endpoint                   | Description                         |
| ------ | -------------------------- | ----------------------------------- |
| POST   | `/api/auth/register`       | Register new user                   |
| POST   | `/api/auth/login`          | Authenticate and receive JWT        |
| POST   | `/api/auth/otp`            | Request OTP for password reset      |
| POST   | `/api/auth/reset-password` | Reset password using OTP            |
| GET    | `/api/students`            | Fetch paginated student list        |
| POST   | `/api/students`            | Create a new student record         |
| PUT    | `/api/students/:id`        | Update student details              |
| DELETE | `/api/students/:id`        | Delete a student record             |
| GET    | `/api/reports/pdf`         | Generate PDF report of student data |

## 📂 Data Import & Export

* **Import:** Upload CSV or JSON via `/api/students/import`.
* **Export:** Download CSV/JSON at `/api/students/export`.

## 🔒 Authentication & Security

* **JWT:** Secures API routes with access and refresh tokens.
* **OTP:** One‑time passwords for secure reset flows.
* **Validation:** Input schema checks to prevent injection.

## 🧪 Testing

* **Unit Tests:** Run backend tests with Jest & Supertest:

  ```bash
  npm test
  ```

## 🤝 Contributing

Contributions are welcome! Please open issues or pull requests for enhancements, bug fixes, or ideas.

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
