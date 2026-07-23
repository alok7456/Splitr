# 💸 Splitr

Splitr is an AI-powered expense sharing application inspired by Splitwise. It enables users to split bills, track balances, settle debts, and manage shared expenses in real time. The application also leverages AI to scan receipts and automatically extract expense details, reducing manual data entry.

---

## ✨ Features

* 👥 Create and manage expense groups
* 💰 Add and split expenses among group members
* ⚖️ Automatic balance calculation
* 🔄 Debt simplification to minimize settlements
* 📸 AI-powered receipt scanning using Gemini
* 📊 Expense analytics and financial insights
* 📧 Automated payment reminder emails
* ⚡ Real-time synchronization across all connected users
* 🔒 Secure authentication with Clerk

---

## 🛠 Tech Stack

| Layer           | Technology             |
| --------------- | ---------------------- |
| Frontend        | Next.js 15, React 19   |
| Styling         | Tailwind CSS, Shadcn UI |
| Backend         | Convex                 |
| Database        | Convex Database        |
| Authentication  | Clerk                  |
| AI              | Google Gemini          |
| Background Jobs | Inngest                |
| Email           | Resend                 |
| Charts          | Recharts               |
| Validation      | React Hook Form, Zod   |

---

## 🏗️ System Architecture

```text
                        +-------------------+
                        |       User        |
                        +---------+---------+
                                  |
                                  v
                     +------------------------+
                     | Next.js 15 Frontend    |
                     | React 19 + Tailwind    |
                     +-----------+------------+
                                 |
                                 v
                     +------------------------+
                     | Clerk Authentication   |
                     +-----------+------------+
                                 |
                                 v
                  +-----------------------------+
                  | Convex Backend Functions    |
                  +-----------+-----------------+
                              |
              +---------------+----------------+
              |               |                |
              v               v                v
      Convex Database    Gemini AI       Inngest
                              |               |
                              |               |
                              v               v
                     Receipt Parsing    Background Jobs
                                              |
                                              v
                                           Resend
                                        Email Service
```

---

## 🚀 Engineering Challenges

* **Debt Simplification:** Implemented an algorithm that minimizes the number of transactions required to settle group expenses by calculating each member's net balance.
* **Real-Time Synchronization:** Used Convex's real-time database to instantly update expenses, balances, and settlements across all connected users.
* **AI Receipt Parsing:** Integrated Google Gemini to extract structured expense information from receipt images and convert it into application-ready data.
* **Background Processing:** Used Inngest to handle asynchronous workflows such as reminder emails without affecting application responsiveness.
* **Optimistic UI:** Implemented optimistic updates to provide instant user feedback while ensuring consistency between frontend and backend state.

---

## 🤔 Why These Technologies?

| Technology                | Why it was used                                                                                                      |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Next.js 15**            | Server Components, App Router, optimized rendering, and excellent performance.                                       |
| **React 19**              | Modern component-based UI with efficient rendering.                                                                  |
| **Convex**                | Provides a serverless backend, built-in database, and real-time synchronization without manually creating REST APIs. |
| **Clerk**                 | Secure authentication with OAuth, session management, and user management out of the box.                            |
| **Gemini AI**             | Extracts structured expense information from receipt images using AI.                                                |
| **Inngest**               | Handles scheduled jobs, retries, and event-driven background workflows.                                              |
| **Resend**                | Reliable transactional email delivery.                                                                               |
| **Tailwind CSS**          | Utility-first CSS framework for rapid and consistent UI development.                                                 |
| **Recharts**              | Responsive charts for expense analytics and financial visualization.                                                 |
| **React Hook Form + Zod** | Efficient form handling with robust schema validation.                                                               |

---



## 🚀 Installation

```bash
git clone https://github.com/alok7456/splitr.git

cd splitr

npm install

npm run dev
```


---

## 🔮 Future Improvements

* 🌍 Multi-currency expense support
* ✍️ Better OCR support for handwritten receipts
* 📱 Mobile application
* 📶 Offline synchronization
* 💳 UPI payment integration
* 💸 Budgeting and spending limit tracking
