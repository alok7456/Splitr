# Splitr

Splitr is a modern, full-stack web application designed to make expense sharing and bill splitting among friends, family, or colleagues as effortless as possible. Think of it as a clone of Splitwise, but with a more modern tech stack and AI-powered features.

## 🚀 What Problem It Solves

Managing shared expenses manually can be a nightmare. Who paid for dinner? How much does Alice owe Bob for the trip? Did Charlie pay his share of the rent? Splitr solves these common problems by providing a centralized platform to:

- **Track Shared Expenses:** Easily add bills and specify who participated.
- **Calculate Balances:** Automatically compute complex debt networks to minimize the number of transactions needed to settle up.
- **Settle Debts:** Keep a clear, historical record of who has paid what, so there is never any ambiguity.
- **Automate Reminders:** Send notifications and reminders for unsettled balances.

## 💻 Tech Stack

This project is built using a bleeding-edge modern web development stack:

- **Frontend Framework:** [Next.js 15](https://nextjs.org/) (App Router, React 19)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) with Radix UI components for a beautiful, accessible UI
- **Authentication:** [Clerk](https://clerk.com/) for secure and seamless user login/registration
- **Backend & Database:** [Convex](https://www.convex.dev/) for real-time data syncing and serverless backend functions
- **AI Integration:** [Google Generative AI (Gemini)](https://ai.google.dev/) for intelligent features like receipt scanning and parsing
- **Background Jobs:** [Inngest](https://www.inngest.com/) for reliable background tasks and event-driven workflows
- **Email Notifications:** [Resend](https://resend.com/) for transactional emails
- **Data Visualization:** [Recharts](https://recharts.org/) for beautiful financial charts
- **Form Handling:** React Hook Form & Zod for robust data validation

## 🧠 Most Difficult Parts of Building This

Building a robust expense-sharing application involves several complex challenges:

1. **Complex Debt Simplification Algorithm:** Designing the math and logic that minimizes the total number of transactions between a group of people (e.g., if A owes B $10, and B owes C $10, the algorithm simplifies it to A owing C $10). 
2. **Real-time Data Synchronization:** Ensuring that when one user adds an expense, all other involved users see the update instantly across their devices, which was handled gracefully using Convex.
3. **AI Receipt Parsing:** Integrating Google Generative AI to accurately extract line items, prices, and taxes from varied and messy receipt formats, and reliably mapping them to the app's strict database structures.
4. **Reliable Background Processes:** Handling scheduled tasks (like periodic email reminders) and asynchronous webhook operations reliably without blocking the main application flow, requiring careful orchestration with Inngest.
5. **State Management & UI Optimism:** Keeping the UI snappy and responsive with optimistic updates while managing the complex relational data of users, groups, and expenses.
