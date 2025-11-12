# 🎒 StylishPack — Bilingual E-Commerce Platform 🇰🇼

A **production-ready bilingual (Arabic / English) e-commerce platform** built for retail businesses in Kuwait.  
Developed with **React + TypeScript** on the frontend and **Express + TypeScript** on the backend, it provides a secure, scalable solution with a clean user experience and a professional admin interface.

---

## 🧠 Project Overview

StylishPack is a full-stack e-commerce platform designed for Kuwait’s bilingual retail market.  
Customers can browse products, manage their cart, place orders, and complete payments through a secure, session-based checkout flow.  
Each successful order automatically generates a PDF invoice and sends a confirmation email to the customer.  
The admin dashboard provides full control over products, orders, and sales reporting — all within a clean, responsive UI.

---

## 🧩 Tech Stack

**Frontend**
- React 19 (TypeScript)  
- Vite (bundling & build)  
- Tailwind CSS  
- React Router, React Hook Form, Zustand, TanStack Query  

**Backend**
- Node.js + Express (TypeScript)  
- MongoDB + Mongoose  
- Puppeteer (PDF invoice generation)  
- Multer (uploads)  
- Resend (email provider)  

**Authentication & Security**
- JWT (HTTP-only cookies)  
- bcrypt password hashing  
- Helmet (CSP + HSTS)  
- CSRF protection (`csurf`)  
- express-rate-limit for login & register routes  

**Integrations**
- Google Maps picker (`@react-google-maps/api`)  
- KNET payment gateway setup (fully implemented, awaiting merchant activation)

---

## 🚀 Core Features

- 🌐 **Bilingual UI** (Arabic / English with RTL support)  
- 🛍️ **Product categorization, filtering, and search**  
- 📍 **Google Maps-based address selection**  
- 💳 **Secure KNET payment integration** (sandbox-tested)  
- 📄 **Automated PDF invoice generation** via Puppeteer  
- 📧 **Email notifications** with order summary and invoice  
- 🧾 **Admin dashboard** for products, orders, and reports  
- 🔐 **Role-based authentication** and protected routes  

---

## 🧱 Architecture Overview

The application follows a modular **full-stack TypeScript architecture**:
frontend/ → React + Tailwind UI
backend/ → Express + Mongoose API
shared/ → Common types and validation utilities
invoices/ → Generated PDF invoices (served under /uploads/invoices)


### API & Data Flow
- `/api/products` – list, filter, and search products  
- `/api/orders` – create orders via session-based checkout  
- `/api/payment` – finalize order and trigger invoice generation  
- `/api/admin/*` – secured endpoints for admin management  

All inputs are validated with **express-validator**, and responses are sanitized before delivery.  
Admin and customer sessions are managed through signed **JWTs** stored in **HttpOnly cookies**.

---

## 🔐 Security & Deployment Setup

- Environment variables isolated in `.env` (Mongo URI, JWT secret, session secret, etc.)  
- CSRF protection active in production  
- HTTPS enforced behind **Nginx** reverse proxy  
- Helmet configured for CSP and HSTS headers  
- PDF and static assets served with secure caching headers  

---

## 🌍 Live Demo & Developer

**Live Demo:** [www.stylishpkshop.com](https://www.stylishpkshop.com)  
**Developer:** Hassan Jahandideh  
Full-Stack Developer (React / Node.js / TypeScript)  
📧 jahandideh.2083@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/hassanjahandideh)

---

**Note:**  
This repository contains documentation only.  
The full production source code is private for security reasons, as it includes live payment integration and client data.
