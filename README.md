# 🎀 Musubi (結び)

> **"Connecting moments, guests, and memories."**

![Project Status](https://img.shields.io/badge/Status-Active_Development-brightgreen)

## 📖 About

**Musubi** is a next-generation Wedding Management System designed to modernize the traditional wedding workflow. From the first e-invitation to the final toast, Musubi ensures a seamless experience for both the couple and their guests.

**Musubi** (Japanese: 結び) means "knot" or "connection", symbolizing the bond between people.

Built as a Monorepo, the system leverages the bleeding edge of web and mobile technologies to deliver high performance, offline capabilities, and an elegant user interface.

## 🏗️ Tech Stack Highlights

We use a cutting-edge stack to ensure performance, scalability, and developer experience.

* **Guest Portal**: **Nuxt 4** (SSR) + **Nuxt UI 3** + **Tailwind 4** for a lightning-fast, immersive RWD experience.
* **Management App**: **Flutter** (Material 3) for robust, offline-first tablet/mobile operations during the reception.
* **Backend Core**: **.NET 10** Web API implementing **DDD** (Domain-Driven Design) and **CQRS** architecture.

### Detailed Component View

| Component | Technology | Version | Key Features |
| :--- | :--- | :--- | :--- |
| **Guest Portal** | [Nuxt](https://nuxt.com/) | **v4** | SSR, Nitro Engine |
| **UI Framework** | [Nuxt UI](https://ui.nuxt.com/) | **v3** | Modern Components |
| **Styling** | [Tailwind CSS](https://tailwindcss.com/) | **v4** | Oxide Engine, Zero-runtime |
| **Management App** | [Flutter](https://flutter.dev/) | **Stable** | Material 3 Design, Offline-first |
| **Backend API** | [.NET](https://dotnet.microsoft.com/) | **10 (Preview)** | Minimal APIs, Native AOT |
| **Database** | PostgreSQL | 16+ | JSONB support, Reliable |
| **Architecture** | DDD + CQRS | - | Clean Architecture |

## 📂 Project Structure

This repository is organized as a monorepo:

* **`apps/guest-portal`**: The public-facing RWD website for e-invitations and RSVPs.
* **`apps/management-app`**: The tablet/mobile app for the couple and staff (Reception/Seating).
* **`backend`**: The centralized API service handling core logic and data consistency.

## 🚀 Getting Started

### Prerequisites

* **Node.js**: v22+ (for Nuxt 4)
* **Flutter SDK**: Latest Stable
* **.NET SDK**: 10.0 Preview
* **Docker**: For local database orchestration

### Local Development

1. **Clone the repo**

   ```bash
   git clone https://github.com/zoozxc456/musubi.git
   cd musubi
