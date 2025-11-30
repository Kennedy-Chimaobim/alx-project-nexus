A modern, interactive supply chain traceability dashboard built with React, TailwindCSS, MetaMask Wallet Authentication, and Mock Service Worker (MSW) for realistic API simulation.

This project provides real-time visibility into product movement across the supply chain—from origin → processing → warehouses → retail—using a clean, responsive UI.



📖 1. Project Overview

The Xinetee Supply Chain Dashboard is a frontend application that allows users to:

Track product movement in real-time

Add new products with metadata and batch details

Add checkpoints across the supply chain

Login using email/password or MetaMask Ethereum wallet

Visualize product status using intuitive progress bars & cards

Manage user profiles for both individual and organization types


The entire system uses MSW to simulate backend APIs—mocking authentication, product creation, and checkpoint updates.




⭐ 2. Key Features

🔐 Authentication

Email + password login

Wallet connection using MetaMask

Signature-based Web3 login (personal_sign)


📦 Product Management

Add products with:

Category

Batch number

Quantity

Dates (production/expiry)

Attached documentation (file upload)


Fully responsive product list

Dynamic progress bars

Real-time supply chain visualization


🧭 Checkpoint Tracking

Add checkpoints with:

Status

Location

Notes

Timestamp

Optional environmental conditions



👤 Profile Management

View user details

Update password

Connect wallet

Organization vs Individual views


🎨 UI/UX

Clean TailwindCSS design

Dark mode ready

Smooth transitions

Dashboard-style layout

Visual hierarchy for analytics





🛠️ 3. Tech Stack

Frontend

React (Vite)

TailwindCSS

React Router

React Context API


Web3

MetaMask

Ethers.js


Mock API

Mock Service Worker (MSW)

LocalStorage persistence


📂 4. Folder Structure

src/
│── components/
│   ├── Login.jsx
│   ├── MainDashboard.jsx
│   ├── Profile.jsx
│   ├── AddProductForm.jsx
│   ├── AddCheckpointForm.jsx
│   ├── Navbar.jsx
│── contexts/
│   ├── ThemeContext.jsx
│── mocks/
│   ├── handlers.js      # MSW API handlers
│── App.jsx
│── main.jsx




⚙️ 5. Installation & Setup

1. Clone the repo

git clone https://github.com/yourusername/xinetee-dashboard.git
cd xinetee-dashboard

2. Install dependencies

npm install

3. Start dev server

npm run dev

4. MSW Setup (Auto)

MSW automatically starts because it’s imported in main.jsx.




🧪 6. Usage Guide

Login Options

Email & password

Wallet connect → sign message → proceed


Adding a Product

1. Go to Add Product


2. Fill product metadata


3. Submit


4. Product appears instantly via mock API



Adding a Checkpoint

1. Select product


2. Fill checkpoint info


3. Submit


4. Dashboard shows updated progress



Profile

View user info

Change password

Connect wallet





🔧 7. API Mocking (MSW)

The entire backend is simulated using Mock Service Worker, found in:

/src/mocks/handlers.js

Endpoints include:

POST /auth/login

POST /auth/login/wallet

GET /auth/profile

POST /products

GET /products

POST /checkpoints

GET /products/:id/checkpoints


All data persists in localStorage.




🪙 8. Web3 Wallet Login

The app supports wallet login using:

MetaMask injection

eth_requestAccounts

personal_sign

Wallet address stored in context + localStorage


Used in:

Login.jsx
Profile.jsx
App.jsx




🧱 9. Best Practices Implemented

Reusable React components

Context-based auth management

Form validation & error states

Accessibility labels

Responsive grid layout

Clean separation of UI / data / state

Smooth animations & transitions

LocalStorage persistence

JWT-based mock tokens





🚀 11. Future Improvements

Real backend integration (FastAPI or Node.js)

Role-based access control

Multi-product filtering & search

QR code generation for batches

Real GPS tracking + live map

Push notifications for updates



📄 12. License

MIT License. Free to modify and reuse.
