---
layout: page
title: Full-Stack E-Commerce Platform
description: A comprehensive online electronics store featuring role-based management, dynamic inventory tracking, and automated invoicing.
img: /assets/img/Teknosu.png
importance: 3
category: Course Project
---

**TL;DR:** Developed an end-to-end e-commerce platform utilizing a Spring Boot backend and TypeScript frontend. The system handles concurrent sessions and features distinct operational dashboards for Customers, Sales Managers, and Product Managers.

<div class="row justify-content-center">
    <div class="col-sm-auto mt-3">
        <a href="https://github.com/Akseldindisyan/CS308_Online_Shopping_Website" target="_blank" class="btn btn-outline-primary btn-sm"><i class="fab fa-github"></i> View Repository</a>
    </div>
</div>

### Technologies & Methodology
- **Tech Stack:** Spring Boot (Backend), TypeScript (Frontend), Web API Architecture.
- **Software Engineering Practices:** Agile methodology utilizing 2-week SCRUM sprints. 
- **Quality Assurance:** Extensive unit testing, continuous bug reporting, and active product/sprint backlog management.

### Core Architecture & User Roles

**Customer Experience**
- Users can browse, search products by name or description, and sort inventory by price or popularity without requiring an account.
- Secure checkout process that automatically decreases stock upon payment and generates an automated PDF invoice emailed directly to the user.
- Integrated interaction features including wishlists, 1-5 star product ratings, and a 30-day automated refund/return request system.

**Sales Management**
- Sales Managers can execute dynamic discount campaigns that automatically calculate new prices and trigger notifications to customers who have the item in their wishlist.
- Features financial reporting dashboards to calculate revenue, track profit/loss over specific date ranges, and visualize data via charts.
- Responsible for evaluating and authorizing customer refund requests.

**Product & Delivery Management**
- Product Managers maintain the inventory database, manage product categories, and moderate customer comments for approval.

**Security & Concurrency**
- The application architecture was designed to securely handle multiple users operating concurrently without data race conditions[cite: 65].
- Defensive programming principles were implemented to encrypt all sensitive data, including user accounts, passwords, mock credit card information, and invoices[cite: 64, 65].
