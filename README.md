# Rival in Retro — Premium Fan Jersey E-Commerce Platform

> A fully production-deployed e-commerce platform for a premium fan jersey brand.  
> Built with zero frameworks. Real customers. Live orders. Pure web.

![Rival in Retro](https://img.shields.io/badge/Status-Live-brightgreen)
![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black)

---

## Overview

Rival in Retro is a complete e-commerce web application built for a premium fan jersey brand selling football, cricket, IPL, World Cup, retro, and croptop jerseys across India.

The entire platform is built in two files — `index.html` for the customer-facing store and `admin.html` for the admin panel. No React. No Vue. No build tools. No npm. Just HTML, CSS, JavaScript, and Firebase — deployed and serving real customers from day one.

Orders are placed through WhatsApp. The cart generates a complete formatted order message with product details, sizes, bundle discounts, free delivery confirmation, and the final payable amount — then opens WhatsApp with the message pre-filled.

## Features

### Customer Store (index.html)

**Navigation**
- Fixed top bar with logo, inline real-time search, and cart icon with live badge counter
- Search filters products by name, description, and category with 180ms debounce
- No-results state shows Browse Jerseys and Check on WhatsApp CTAs

**Homepage Sections**
- Animated gold ticker with promotional announcements
- Full-viewport hero with headline and dual CTAs
- Scroll-triggered animated stat counters using IntersectionObserver
- WhatsApp channel join section
- Signature Collection premium curated section
- Category tabs with filtered product grid
- Features and brand promise block
- Full footer with navigation links

**Signature Collection**
- Only renders when products are marked as signature in the admin panel
- Asymmetric layout: large featured card (3:4 portrait ratio) on the left, 2×2 supporting grid on the right
- Rich layered background: diagonal grain texture, central gold fog, asymmetric corner glows, top gold gradient rule
- View All Signature button filters the main grid to show only curated picks

**Product Cards**
- 1:1 ratio images with object-fit contain, no cropping
- Category label, product name (2-line clamp), star rating, pricing with discount badge
- Full-width Add to Cart button
- SVG jersey art fallback when no image is uploaded (uses category color scheme)

**Product Detail Page (PDP)**
- URL-based routing via History API — each product gets its own shareable URL (#product/slug)
- Desktop: 70:30 asymmetric grid — 2-column image collage left, sticky info panel right
- Mobile: stacked layout — images top, info below, no sticky behavior
- Image collage with cursor-tracking zoom on hover (desktop), transforms to 1.8x at correct origin point
- Fullscreen image viewer: scroll to zoom (up to 5x), click and drag to pan, pinch to zoom on mobile, swipe to navigate, tap to close
- Right panel order: breadcrumb, badge, product name, star rating, price + tax subtext, size selector, quantity selector, item total, Add to Cart, Order on WhatsApp, offer highlights, description with show more toggle, trust block
- Recommendations: up to 6 from the same category + up to 10 from other categories, shuffled with Fisher-Yates

**Cart System**
- Slide-in drawer with backdrop
- Offer banner updates based on cart state — nudges from 1 to 2 items
- Delivery banner showing ₹78 crossed out as FREE
- Full pricing breakdown: original total, discount, delivery, you save, final amount
- Per-item quantity controls with plus and minus
- Upsell popup on first item added: fires
