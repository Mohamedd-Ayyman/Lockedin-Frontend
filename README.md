<div align="center">

# 🔒 LockedIn: Professional Networking Platform

**A full-featured LinkedIn clone built by a ~20-person engineering team (web, backend, cross-platform, testing and DevOps) as the Software Engineering capstone at Cairo University.**

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Redux](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=for-the-badge&logo=redux&logoColor=white)
![React Query](https://img.shields.io/badge/React_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
<br/>
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

[**Organization**](https://github.com/ClinkedIn) · [Frontend](https://github.com/ClinkedIn/Frontend) · [Backend](https://github.com/ClinkedIn/Backend) · [Cross-Platform](https://github.com/ClinkedIn/Cross-Platform) · [Testing](https://github.com/ClinkedIn/Testing)

</div>

---

## 📖 Overview

**LockedIn** recreates LinkedIn's core experience: professional profiles, a networking graph, a news feed, real-time messaging, a jobs marketplace, company pages, notifications, an admin panel and a Stripe-powered premium plan. The team worked like a real software organisation, in incremental **sprints**, with an **API-first contract** between subteams, a code style for each subteam, auto-generated documentation and unit-test coverage targets.

This repository is my fork of the **web frontend**.

## 👨‍💻 My Contributions (Frontend Engineer)

**28 commits** to the main frontend repository (March to May 2025). I owned the identity, profile and networking areas:

- **My Profile and Other-User Profiles:** profile header, experience, education, skills with **endorsements**, résumé upload, activity feed, and "People you may know". All of it is **integrated with the backend REST API**.
- **Profile privacy:** *Public / Connections-only / Private* profiles, including a dedicated private-profile view.
- **Account settings:** update **email**, **username** and **password**, **delete account**, plus a reusable **confirmation dialog** component.
- **Networking:** **connect / follow / block** buttons, **remove connection**, invitations, connections list, a blocked-users page, and message/block actions on profiles.
- **Auth flows:** fixed the **forgot-password** experience and its UI consistency.
- **Testing:** **unit tests with API mocking** (Vitest, Testing Library, axios-mock-adapter / MSW) for Forgot Password, Update Username and Update Password.
- **Documentation:** **JSDoc** functional documentation for the profile modules, published as HTML docs.

## ✨ Platform Features (team)

| Module | Highlights |
|---|---|
| 🔐 Authentication | Register with reCAPTCHA, email verification, password reset, Google sign-in, account deletion |
| 👤 Profiles | Experience, education, skills and endorsements, résumé, profile and cover photos, privacy levels |
| 🔗 Networking | Search, connection requests, follow, block/unblock, connections & invitations |
| 📰 Feed | Posts with media, reactions, comments, reposts, hashtags, saved posts, reporting |
| 💬 Messaging | 1:1 conversations, media messages, read receipts, unread counts, blocking |
| 🔔 Notifications | Real-time notifications for reactions, comments, connections and messages (Firebase Cloud Messaging) |
| 💼 Jobs | Job search & filters, applications with screening questions, application tracking, employer hiring dashboard |
| 🏢 Company Pages | Create and manage company pages, posts, followers and analytics |
| 🛡️ Admin Panel | Reported content moderation, job listing management, platform analytics |
| 💳 Premium | Subscription plans and payment flow with **Stripe** (test mode) |

## 🏗️ Architecture

```
┌───────────────────────────┐        REST (Swagger-documented)        ┌──────────────────────────────┐
│  Web Frontend (this repo) │ ──────────────────────────────────────▶ │  Backend: Node.js / Express  │
│  React · TS · Redux ·     │                                         │  MongoDB · JWT · Cloudinary  │
│  React Query · Tailwind   │ ◀──── Firebase Cloud Messaging ──────── │  Firebase · Stripe · Mailer  │
└───────────────────────────┘                                         └──────────────────────────────┘
┌───────────────────────────┐                                         ┌──────────────────────────────┐
│  Cross-Platform (Flutter) │ ─────────────── same API ─────────────▶ │  Testing team: E2E suites    │
└───────────────────────────┘                                         └──────────────────────────────┘
                        DevOps: Docker images · CI/CD · cloud deployment
```

## 🧰 Frontend Tech Stack

| Area | Tools |
|---|---|
| UI | React, TypeScript & JavaScript, Tailwind CSS, Headless UI, Framer Motion, Font Awesome, Lucide |
| State & data | Redux Toolkit, TanStack React Query, Axios, React Router |
| Charts | Chart.js, Recharts |
| Integrations | Firebase (auth & push), Google reCAPTCHA, Stripe |
| Quality | Vitest, Jest, React Testing Library, MSW, axios-mock-adapter, ESLint, JSDoc |
| Build & deploy | Vite (SWC), Docker |

## 🚀 Running Locally

```bash
git clone https://github.com/Mohamedd-Ayyman/Lockedin-Frontend.git
cd Lockedin-Frontend
npm install
cp .env.example .env   # set the API base URL and Firebase keys
npm run dev
```

## 🤝 Team

LockedIn was built by around 20 engineers organised into **Frontend**, **Backend**, **Cross-Platform**, **Testing** and **DevOps** subteams under a team leader. Thanks to every teammate in the [ClinkedIn](https://github.com/ClinkedIn) organisation.

## 👤 Author

**Mohamed Ayman**, Frontend Engineer · [GitHub](https://github.com/Mohamedd-Ayyman) · [LinkedIn](https://linkedin.com/in/mohamed-ayman-8787b0269)
