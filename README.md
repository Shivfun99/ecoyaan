# Ecoyaan Checkout Flow – Frontend Engineering Assignment

## Overview

This project implements a simplified **checkout flow inspired by Ecoyaan** using **Next.js, React, and Tailwind CSS**.
The application demonstrates **Server-Side Rendering (SSR), state management, responsive UI components, and form validation**.

The flow allows users to:

1. View cart items and order summary
2. Enter shipping address details
3. Review order and simulate payment
4. See an order success confirmation

---

# Tech Stack

**Framework**

* Next.js (App Router)

**Frontend**

* React
* Tailwind CSS

**State Management**

* Zustand

**Form Handling**

* React Hook Form

**Backend Mock**

* Next.js API Routes

**Deployment**

* Vercel (recommended)

---

# Application Architecture

The project follows a **component-based architecture** with clear separation of concerns.

### Folder Structure

```
app/
 ├ page.tsx                → Cart / Order Summary (SSR)
 ├ checkout/
 │   └ page.tsx            → Shipping Address Page
 ├ payment/
 │   └ page.tsx            → Payment Confirmation
 ├ success/
 │   └ page.tsx            → Order Success Page
 ├ layout.tsx
 └ globals.css

components/
 ├ CartItem.tsx            → Product display component
 ├ OrderSummary.tsx        → Pricing calculation + checkout button
 └ AddressForm.tsx         → Shipping form with validation

pages/api/
 └ cart.ts                 → Mock backend API for cart data

store/
 └ checkoutStore.ts        → Zustand global state (address data)

types/
 └ types.ts                → TypeScript types
```

---

# Key Architectural Decisions

### 1. Server-Side Rendering (SSR)

The cart data is fetched using **Next.js Server Components** to ensure the order summary is rendered on the server before the page loads.

Benefits:

* Faster initial load
* SEO-friendly
* Simulates real production e-commerce systems

---

### 2. Global State with Zustand

Zustand is used to store the **shipping address state across pages**.

This allows:

* Checkout → Payment page state persistence
* Minimal boilerplate compared to Redux
* Clean and scalable architecture

---

### 3. Component-Based UI

Reusable UI components were created:

* **CartItem** → Displays individual product
* **OrderSummary** → Handles pricing calculations
* **AddressForm** → Handles form validation and submission

This improves **maintainability and scalability**.

---

### 4. Form Validation

Shipping form validation is implemented using **React Hook Form**, ensuring:

* Required fields validation
* Proper form handling
* Better performance than controlled forms

---

### 5. Mock Backend API

A **Next.js API route** (`/api/cart`) is used to simulate backend data fetching.

This mimics a real-world API request and allows testing SSR behavior.

---

# Checkout Flow

```
Cart Page (SSR)
        ↓
Shipping Address Form
        ↓
Payment Confirmation
        ↓
Order Success Page
```

---

# Features

* Server-side rendered cart data
* Responsive checkout UI
* Form validation
* State persistence across pages
* Simulated payment confirmation
* Clean modular architecture

---

# Running the Project Locally

### 1. Clone the Repository

```
git clone <your-repository-link>
cd ecoyaan-checkout
```

---

### 2. Install Dependencies

```
npm install
```

---

### 3. Run Development Server

```
npm run dev
```

---

### 4. Open in Browser

```
http://localhost:3000
```

---

# Mock API Endpoint

Cart data is served from:

```
http://localhost:3000/api/cart
```

---

# Deployment

The project can be deployed easily using **Vercel**.

Steps:

1. Push repository to GitHub
2. Import repository in Vercel
3. Deploy

---
# Deployment Link
vercel:
https://ecoyaan-checkout-wine.vercel.app/
github:https://github.com/Shivfun99/ecoyaan


# Future Improvements

If extended further, the following improvements could be added:

* Real payment gateway integration
* Persistent cart storage
* Authentication
* Backend database integration
* Order history tracking

---
## Assets & References

* Product images used in the cart UI are placeholder images.
* The bamboo toothbrush illustration used for demonstration was generated using AI for visual representation purposes only.
* Cart data is mock data provided in the assignment and served through a Next.js API route.


# Author

**Shiv Kumar Mishra**
VIT-AP University
Competitive Programmer – Codeforces Specialist
