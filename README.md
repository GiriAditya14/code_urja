# ✨ Multi-Tenant Website Builder Platform

Finalist in **Code Urja 1.0 – 36 Hour National Hackathon** among top-performing teams.

This project is a **scalable multi-tenant website builder backend** that enables dynamic website section creation, customization, and rendering capabilities for different tenants (users or clients). It is ideal for content-heavy platforms like startups, businesses, or agencies needing tailored landing pages or portfolios without building from scratch.

## 🚀 Tech Stack

- **Backend Framework:** Node.js + Express.js
- **Database:** MongoDB (with dynamic tenant-specific schema handling)
- **Authentication:** JWT-based secured access
- **Styling Support:** Tailwind-compatible layout generation
- **Language:** JavaScript (ESM)
- **Cloud Deployment:** Vercel for backend APIs
- **AI API Integration:** Gemini AI for generating frontend layout code from submitted content

---

## 🎯 Problem Statement

Many businesses require customizable websites but lack the technical expertise or budget to build and maintain one. This platform solves that by enabling multi-tenant content management through a robust backend where clients can dynamically create and manage website sections like Hero, FAQ, Footer, etc., and automatically generate the frontend layout using AI.

---

## ✅ Key Features

### 🔑 Authentication
- JWT-based login system
- Secure route access per tenant

### 🧠 Multi-Tenant Architecture
- Every route respects `tenantId` to isolate user data
- Routes are designed to work per-tenant for security and scalability

### 📦 Modular Content Management
- `POST` and `DELETE` routes to create or remove:
  - Hero Section
  - Why Choose Us
  - FAQ Section
  - Footer Section
  - About Us Section
  - Home Sections
  - Products
  - Contact Form Entries

### 🧠 AI-Powered Frontend Layout Generator
- Sends section data to Gemini API
- Returns styled, reusable React + Tailwind JSX layout code
- Works for Hero, FAQ, and other homepage sections

### 📤 API Endpoints (Examples)
- `POST /api/website/create/home/hero`
- `POST /api/website/create/home/faq`
- `POST /api/website/create/about`
- `POST /api/product/add`
- `POST /api/contact/submit`
- `DELETE /api/website/delete/home/:id`
- `DELETE /api/website/delete/about/:id`

### 📬 Contact Form
- Saves submissions with timestamps
- Includes name, email, and message

---

## 📌 Sample API Test Data (for Postman)

### Hero Section
```json
{
  "title": "Build Websites Fast",
  "subtitle": "A modular CMS for custom sections",
  "cta": "Get Started Now",
  "style": {
    "theme": "modern",
    "color": "blue"
  },
  "tenantId": "tenant_123"
}
```

### FAQ Section
```json
{
  "faqs": [
    { "question": "How to use the platform?", "answer": "Just sign up and add sections." },
    { "question": "Is it secure?", "answer": "Yes, each tenant has isolated data." }
  ],
  "style": {
    "theme": "minimal",
    "color": "indigo"
  },
  "tenantId": "tenant_123"
}
```

### Contact Form
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "message": "I'd like a demo of this CMS"
}
```

---

## 📂 Project Structure
```arduino
├── config/
│   └── db.js
├── controllers/
│   ├── websiteController.js
│   ├── productController.js
│   └── contactController.js
├── models/
│   ├── Hero.js
│   ├── FAQ.js
│   ├── Footer.js
│   ├── About.js
│   ├── Product.js
│   └── Contact.js
├── routes/
│   ├── websiteRoutes.js
│   ├── productRoutes.js
│   └── contactRoutes.js
├── utils/
│   └── api.js  // Gemini layout generation logic
├── .env
├── index.js
```

---

## 🌐 Deployment Instructions (Vercel)
1. Create a new MongoDB cluster on MongoDB Atlas

2. Add the connection string to .env as:
    ```env
    MONGO_URI=your_connection_string
    ```
3. Push code to GitHub and link your repository to Vercel

4. Set NODE_ENV, MONGO_URI, and PORT in Vercel project environment variables

5. Deploy 🎉

---

## 📈 Future Enhancements
- Admin dashboard for managing sections
- Drag-and-drop UI builder frontend
- Subscription/paywall-based access control
- Prebuilt themes library

---

## 🏁 Conclusion
This project delivers a solid foundation for building scalable, customizable, and tenant-specific websites powered by dynamic backend logic and AI-generated frontend layout components. It demonstrates full-stack capabilities with a focus on modularity, clean architecture, and practical use cases in business environments.

---

## 🙌 Acknowledgements
- Built in 36 hours during Code Urja 1.0 National Hackathon
- Thanks to the organizers and judges for the opportunity
