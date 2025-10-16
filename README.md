# 💸 Finance Management

## FinBuild

A modern, responsive **finance management system** tailored for students — now rebuilt with **Flutter** for a seamless cross-platform experience (Web, Mobile, and Desktop).
This project demonstrates full-stack integration using **Flutter**, **Flask**, and **PostgreSQL**, with AI-driven insights to empower smart financial decisions.

---

## 📚 Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Contributors](#contributors)
6. [Contact](#contact)

---

## ✨ Features

* **Budget Tracking**: Track expenses and budgets effectively through an intuitive dashboard.
* **AI-Based Budget Recommendations**: Get personalized recommendations using trained ML models.
* **Budget Goals & Planning**: Set spending limits and track progress toward savings goals.
* **Statement Analyzer**: Analyze uploaded financial statements and receive AI-generated insights.
* **Articles Section**: Read financial literacy articles fetched dynamically using APIs.
* **Chatbot Integration**: Chat with an AI finance assistant for instant help and insights.
* **Stock Prediction**: Predict future stock prices using machine learning models.
* **Reminders & Alerts**: Get notified for bill payments, low balances, and goal deadlines.
* **Mutual Funds Tracker**: Track performance and returns of your selected mutual funds.

---

## 🧩 Technologies Used

| Layer                | Technologies                             |
| -------------------- | ---------------------------------------- |
| **Frontend**         | Flutter (Web, Mobile, Desktop)           |
| **Backend**          | Flask (Python)                           |
| **Database**         | PostgreSQL                               |
| **Machine Learning** | K-Means, Random Forest                   |
| **APIs**             | News API, Gemini API                     |
| **Security**         | TLS Certificates (`cert.pem`, `key.pem`) |
| **Version Control**  | Git & GitHub                             |

---

## ⚙️ Installation

### 🔧 Prerequisites

* Python 3.x
* Flutter SDK
* PostgreSQL installed and running
* Create `.env` file with your API keys:

  ```bash
  NEWS_API_KEY=your_news_api_key
  GEMINI_API_KEY=your_gemini_api_key
  ```

---

### 🐠 Backend Setup (Flask)

1. Clone the repository:

   ```bash
   git clone https://github.com/Archana-K-M/Finance_management.git
   ```
2. Navigate to the backend folder:

   ```bash
   cd Finance_management/backend
   ```
3. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   venv\Scripts\activate   # For Windows
   ```
4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
5. Set up the PostgreSQL database:

   * Create a database named `Archons` with user and password as `Archana`
   * Run the following SQL commands:

     ```sql
     CREATE TABLE customer (
       serial_id SERIAL PRIMARY KEY,
       username VARCHAR(20) UNIQUE NOT NULL,
       password VARCHAR(60) NOT NULL
     );

     CREATE TABLE records (
       record_id SERIAL PRIMARY KEY,
       serial_id INTEGER NOT NULL,
       transaction_date DATE NOT NULL,
       transaction_type VARCHAR(10) NOT NULL,
       category VARCHAR(50) NOT NULL,
       amount NUMERIC(15, 2) NOT NULL,
       total NUMERIC(15, 2),
       FOREIGN KEY (serial_id) REFERENCES customer(serial_id) ON DELETE CASCADE
     );

     CREATE TABLE budgets (
       budget_id SERIAL PRIMARY KEY,
       serial_id INTEGER NOT NULL,
       category VARCHAR(50) NOT NULL,
       limit NUMERIC(15, 2) NOT NULL,
       spent NUMERIC(15, 2) DEFAULT 0,
       remaining NUMERIC(15, 2),
       FOREIGN KEY (serial_id) REFERENCES customer(serial_id) ON DELETE CASCADE
     );
     ```
6. Run the Flask app:

   ```bash
   flask run
   ```
7. The backend will start at: `https://127.0.0.1:5000`

---

### 🧠 Frontend Setup (Flutter)

1. Navigate to the frontend directory:

   ```bash
   cd Finance_management/frontend
   ```
2. Get the dependencies:

   ```bash
   flutter pub get
   ```
3. Run the app (choose your platform):

   ```bash
   flutter run -d chrome       # Web
   flutter run -d windows      # Desktop
   flutter run -d emulator-5554  # Android Emulator
   ```

---

## 🦯 Usage

* Sign up or log in to your account.
* Access your **personal finance dashboard** to:

  * Manage income and expense records.
  * Set and monitor **budget goals**.
  * Get **AI-based financial recommendations**.
  * Explore **stock predictions** and **mutual fund performance**.
  * Receive **reminders and alerts**.
  * Interact with the **chatbot** for queries and advice.

---

## 👥 Contributors

We thank the following people for their valuable contributions:

* **Archana K M** — [GitHub](https://github.com/Archana-K-M)
* **Anirudhh S** — [GitHub](https://github.com/rudhhstoic)
* **Devanidharsan K** — [GitHub](https://github.com/Deva399212)
* **Varsha G** — [GitHub](https://github.com/Varshavishnu)

---

## 📬 Contact

For inquiries or collaborations:

* **Name**: Archana K M
* **Email**: [archanakm297@gmail.com](mailto:archanakm297@gmail.com)
* **GitHub**: [Archana-K-M](https://github.com/Archana-K-M)

---

## 🛡️ License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) f
