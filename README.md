# Jelwo E-Commerce

A full-stack e-commerce web application featuring a customer-facing storefront, an admin dashboard, and a robust backend server.

## 🚀 Features

- **Storefront (Frontend)**: Browse products, filter by categories, view product details, manage cart and wishlist.
- **Admin Dashboard (Admin)**: Manage products, track orders, monitor users, and create discount coupons.
- **Authentication**: Secure user authentication and management (via Clerk).
- **Payment Gateway**: Seamless checkout and payment processing (via Razorpay).
- **Email Notifications**: Automated OTP and transaction emails.

## 🛠️ Tech Stack

- **Frontend**: React.js, Vite, Tailwind CSS (or standard CSS), Context API
- **Admin Panel**: React.js, Vite
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose)

## 📁 Project Structure

The repository is divided into three main folders:

- `/frontend` - The customer-facing React application.
- `/Admin` - The React application for store administrators.
- `/backend` - The Express REST API and database models.

## ⚙️ Installation & Setup

Follow these steps to run the project locally.

### 1. Clone the repository

```bash
git clone <your-github-repo-url>
cd jelwo-project
```

### 2. Install Dependencies

You need to install npm packages for all three parts of the application.

```bash
# Install frontend dependencies
cd frontend
npm install

# Install admin dependencies
cd ../Admin
npm install

# Install backend dependencies
cd ../backend
npm install
```

### 3. Environment Variables (.env)

You need to create a `.env` file in each of the three folders (`frontend`, `Admin`, `backend`). 

*(Note: Never commit your `.env` files to GitHub. They are ignored in this repo via `.gitignore`)*

**Backend (`backend/.env`)**
```env
MONGO_URL=mongodb+srv://<user>:<password>@cluster...
JWT_SECRET=your_jwt_secret
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_key
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_app_password
FRONTEND_URL=http://localhost:5174
```

**Frontend (`frontend/.env`)**
```env
VITE_API_URL=http://localhost:5000/api
VITE_API_IMAGE=http://localhost:5000/uploads
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_RAZORPAY_KEY_ID=your_razorpay_key_id
```

**Admin (`Admin/.env`)**
```env
VITE_API_URL=http://localhost:5000/api
VITE_API_IMAGE=http://localhost:5000/uploads
```

### 4. Running the Application

Open three separate terminal windows and run the following commands:

**Run the Backend Server:**
```bash
cd backend
npm run dev
# Runs on http://localhost:5000
```

**Run the Frontend App:**
```bash
cd frontend
npm run dev
# Runs on http://localhost:5174
```

**Run the Admin Dashboard:**
```bash
cd Admin
npm run dev
# Runs on http://localhost:5173
```

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
