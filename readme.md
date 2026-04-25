# 🛒 GreenCart - Modern Full-Stack E-Commerce Platform

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg) ![React](https://img.shields.io/badge/React-19-61DAFB?logo=react) ![Node](https://img.shields.io/badge/Node.js-20-339933?logo=node.js) ![Tailwind](https://img.shields.io/badge/Tailwind-4.0-06B6D4?logo=tailwind-css) ![MongoDB](https://img.shields.io/badge/MongoDB-latest-47A248?logo=mongodb)

GreenCart is a high-performance, e-commerce platform built with the MERN stack. It features a robust multi-role system (User/Seller), seamless product management, real-time cart updates, and integrated Stripe payments.

---

## 🚀 Key Features

### 👤 User Features

- **Secure Authentication**: JWT-based login/signup with encrypted passwords.
- **Advanced Shopping Cart**: Add, remove, and update product quantities in real-time.
- **Address Management**: Save and manage multiple delivery addresses.
- **Order Tracking**: View order history and real-time status updates.
- **Seamless Payments**: Secure checkout experience powered by Stripe.

### 🏪 Seller Features

- **Multi-Vendor Support**: Dedicated dashboard for sellers to manage their business.
- **Product Management**: Create, edit, and delete products with multi-image support (Cloudinary).
- **Inventory Control**: Real-time stock management and availability toggles.
- **Business Insights**: Track sales and manage customer orders efficiently.

### 🛠 Technical Highlights

- **Modern UI/UX**: Built with React 19 and Tailwind CSS 4 for a fast, responsive, and beautiful experience.
- **Scalable Backend**: Express 5 (latest) with optimized MongoDB queries.
- **Secure API**: Middleware-protected routes (`authUser`, `authSeller`).
- **Cloud Storage**: Integrated Cloudinary for high-quality image hosting.

---

## 🛠️ Tech Stack

### Frontend

- **Framework**: [React 19](https://react.dev/)
- **Styling**: [Tailwind CSS 4.0](https://tailwindcss.com/)
- **Routing**: [React Router 7](https://reactrouter.com/)
- **State Management**: React Context API
- **API Client**: Axios
- **Notifications**: React Hot Toast

### Backend

- **Runtime**: Node.js
- **Framework**: Express 5
- **Database**: MongoDB (Mongoose)
- **File Uploads**: Multer & Cloudinary
- **Payments**: Stripe API
- **Security**: JWT & BcryptJS

---

## 📂 Project Structure

```text
GreenCart/
├── client/              # Frontend (React 19 + Vite)
│   ├── src/
│   │   ├── components/  # Reusable UI components
│   │   ├── context/     # Global state management
│   │   ├── pages/       # Route-level components
│   │   └── assets/      # Static assets
├── server/              # Backend (Node.js + Express)
│   ├── configs/         # Database & Cloudinary config
│   ├── controllers/     # API logic handlers
│   ├── models/          # Mongoose schemas (User, Product, Order)
│   ├── routes/          # API endpoints
│   └── middlewares/     # Auth & validation logic
```

---

## ⚙️ Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB account (Atlas or local)
- Cloudinary account
- Stripe account (for payments)

### 1. Clone the repository

```bash
git clone https://github.com/SathtikBose/GreenCart.git
cd GreenCart
```

### 2. Backend Setup

```bash
cd server
npm install
```

Create a `.env` file in the `server` directory and add your credentials:

```env
MONGODB_URI=your_mongodb_connection_string
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
FRONTEND_URL=http://localhost:5173
```

Run the server:

```bash
npm run dev
```

### 3. Frontend Setup

```bash
cd ../client
npm install
```

Create a `.env` file in the `client` directory:

```env
VITE_BACKEND_URL=http://localhost:4000
VITE_CURRENCY=$
```

Run the frontend:

```bash
npm run dev
```

---

## 🔌 API Endpoints

| Endpoint             | Method | Description       | Access |
| :------------------- | :----- | :---------------- | :----- |
| `/api/user/register` | POST   | User Registration | Public |
| `/api/seller/login`  | POST   | Seller Login      | Public |
| `/api/product/add`   | POST   | Add New Product   | Seller |
| `/api/cart/update`   | POST   | Update Cart Item  | User   |
| `/api/order/place`   | POST   | Place an Order    | User   |

---

## 🚢 Deployment

Both client and server are configured for seamless deployment on **Vercel**.

- **Frontend**: Connect your GitHub repository and set the root directory to `client`.
- **Backend**: Connect your GitHub repository, set the root directory to `server`, and add your environment variables in the Vercel dashboard.

---

## 📄 License

This project is licensed under the [ISC License](LICENSE).

---

Developed with ❤️ by [Sathtik Bose](https://github.com/SathtikBose)
