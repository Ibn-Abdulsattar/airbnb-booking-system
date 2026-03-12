<div align="center">

<img src="https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-Mongoose-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/Deployed-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />
<img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" />

<br/><br/>

```
 █████╗ ██╗██████╗ ██████╗ ███╗   ██╗██████╗
██╔══██╗██║██╔══██╗██╔══██╗████╗  ██║██╔══██╗
███████║██║██████╔╝██████╔╝██╔██╗ ██║██████╔╝
██╔══██║██║██╔══██╗██╔══██╗██║╚██╗██║██╔══██╗
██║  ██║██║██║  ██║██████╔╝██║ ╚████║██████╔╝
╚═╝  ╚═╝╚═╝╚═╝  ╚═╝╚═════╝ ╚═╝  ╚═══╝╚═════╝
```

### **Full-Stack Accommodation Booking System**
*An Airbnb-inspired property listing & booking web application — built, deployed & production-ready*

<br/>

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-airbnb--project--pink.vercel.app-FF5A5F?style=flat-square)](https://airbnb-project-pink.vercel.app)
[![JavaScript](https://img.shields.io/badge/JavaScript-42.3%25-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![EJS](https://img.shields.io/badge/EJS-34.9%25-8A2BE2?style=flat-square)](https://ejs.co/)
[![CSS](https://img.shields.io/badge/CSS-22.8%25-1572B6?style=flat-square&logo=css3)](https://developer.mozilla.org/en-US/docs/Web/CSS)

</div>

---

## 📌 Overview

**Airbnb Booking System** is a production-deployed, full-stack web application inspired by Airbnb. It allows users to browse, create, and manage property listings with full authentication, image uploads via Cloudinary, server-side validation, and a clean MVC architecture.

This project was built as a first deployment milestone, demonstrating real-world backend skills including RESTful routing, database modeling, cloud storage integration, middleware design, and live deployment on Vercel.

🔗 **Live at:** [airbnb-project-pink.vercel.app](https://airbnb-project-pink.vercel.app)

---

## ✨ Features

- 🏠 **Property Listings** — Browse, create, edit, and delete accommodation listings
- 🔐 **User Authentication** — Secure signup, login, and session management
- 🖼️ **Image Uploads** — Cloud-based image storage via Cloudinary
- ✅ **Form Validation** — Server-side schema validation using Joi
- 🗺️ **MVC Architecture** — Clean separation of models, views, and controllers
- 🛡️ **Middleware Layer** — Auth guards, error handlers, and request processing
- 📦 **Database Seeding** — `init/` scripts to seed the database with sample data
- 🌐 **Deployed to Vercel** — Fully live and accessible on the web

---

## 🗂️ Project Structure

```
airbnb-booking-system/
│
├── 📁 controllers/          # Route handler logic (listings, users, reviews)
├── 📁 models/               # Mongoose data models (Listing, User, Review)
├── 📁 routes/               # Express route definitions
├── 📁 views/                # EJS templates (listings, auth, errors, partials)
├── 📁 public/               # Static assets (CSS, client-side JS, images)
├── 📁 uploads/              # Temporary local upload handling
├── 📁 utilis/               # Utility helpers (async error wrapper, etc.)
├── 📁 init/                 # Database seed scripts
│
├── app.js                   # Express app entry point
├── cloudConfig.js           # Cloudinary cloud storage configuration
├── middleware.js            # Custom middleware (auth, validation, errors)
├── schema.js                # Joi validation schemas
├── .gitignore
└── package.json
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Runtime** | Node.js |
| **Framework** | Express.js |
| **Templating** | EJS (Embedded JavaScript) |
| **Database** | MongoDB + Mongoose ODM |
| **Authentication** | Passport.js / express-session |
| **Image Storage** | Cloudinary + Multer |
| **Validation** | Joi |
| **Styling** | Custom CSS + Bootstrap |
| **Deployment** | Vercel |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v16+
- [MongoDB](https://www.mongodb.com/) (local instance or MongoDB Atlas)
- [Cloudinary](https://cloudinary.com/) account (for image uploads)

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Ibn-Abdulsattar/airbnb-booking-system.git
cd airbnb-booking-system
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

### 3️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

```env
# MongoDB
ATLASDB_URL=mongodb+srv://<username>:<password>@cluster.mongodb.net/airbnb

# Session
SECRET=your_super_secret_session_key

# Cloudinary
CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret
```

---

### 4️⃣ Seed the Database (Optional)

```bash
node init/index.js
```

> This populates the database with sample property listings to get started quickly.

---

### 5️⃣ Start the Application

```bash
node app.js
```

> App will be running at `http://localhost:8080`

For development with auto-reload:

```bash
npx nodemon app.js
```

---

## 🔌 Route Overview

| Method | Route | Description |
|---|---|---|
| `GET` | `/listings` | View all property listings |
| `GET` | `/listings/new` | Form to create a new listing |
| `POST` | `/listings` | Submit a new listing |
| `GET` | `/listings/:id` | View a single listing |
| `GET` | `/listings/:id/edit` | Edit form for a listing |
| `PUT` | `/listings/:id` | Update a listing |
| `DELETE` | `/listings/:id` | Delete a listing |
| `POST` | `/listings/:id/reviews` | Add a review to a listing |
| `DELETE` | `/listings/:id/reviews/:reviewId` | Delete a review |
| `GET` | `/signup` | User registration page |
| `POST` | `/signup` | Register a new user |
| `GET` | `/login` | User login page |
| `POST` | `/login` | Authenticate user |
| `GET` | `/logout` | Log out the current user |

---

## 📸 Screenshots

| Page | Description |
|---|---|
| 🏠 Home / Listings | Grid of all property listings with images |
| 📄 Listing Detail | Full property page with reviews |
| ➕ Create Listing | Form with image upload support |
| 🔐 Auth Pages | Login & signup with validation feedback |

> *(Drag and drop your screenshots here directly in the GitHub editor)*

---

## 🧠 What I Learned

- Structuring a **full MVC web app** with Express.js from scratch
- Implementing **user authentication** with sessions and Passport.js
- Integrating **Cloudinary** for scalable cloud image uploads via Multer
- Writing **server-side validation** with Joi schemas
- Designing **MongoDB models** with relationships (Listing → Reviews → Users)
- Building and applying **custom middleware** for auth guards and error handling
- **Deploying a Node.js app** to Vercel for the first time with environment configs

---

## 🤝 Contributing

Contributions, suggestions, and improvements are always welcome!

```bash
# 1. Fork the repository
# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit your changes
git commit -m "feat: describe your change"

# 4. Push to the branch
git push origin feature/your-feature-name

# 5. Open a Pull Request
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## ⚠️ Disclaimer

This project is developed **purely for educational and portfolio purposes**. It is not affiliated with, endorsed by, or connected to [Airbnb, Inc.](https://airbnb.com) in any capacity. All brand names and trademarks belong to their respective owners.

---

<div align="center">

Made with ❤️ by **[Ibn-Abdulsattar](https://github.com/Ibn-Abdulsattar)**

🌐 **[View Live Demo](https://airbnb-project-pink.vercel.app)** &nbsp;|&nbsp; ⭐ *Star this repo if you found it helpful!*

</div>
