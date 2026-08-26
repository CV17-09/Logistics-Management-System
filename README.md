<div align="center">

# 🚚 FleetOps

### Logistics Management System

**A modern full-stack platform for managing shipments, drivers, vehicles, routes, customers, and delivery operations.**

Built with **Angular • TypeScript • REST APIs • PostgreSQL**

<br>

![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge\&logo=angular\&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge\&logo=typescript\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge\&logo=postgresql\&logoColor=white)
![REST API](https://img.shields.io/badge/REST-API-009688?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge\&logo=docker\&logoColor=white)

</div>

---

## 📖 About

**FleetOps** is a full-stack Logistics Management System designed to simulate the daily operations of a transportation and logistics company.

The platform provides a centralized interface for managing the complete delivery lifecycle — from creating a shipment and assigning a driver to tracking its progress and confirming delivery.

FleetOps was created to demonstrate modern **Angular development, REST API integration, relational database design, authentication, authorization, and real-world business workflows.**

---

## ✨ Features

### 📦 Shipment Management

september 

* Create, update, view, and manage shipments
* Assign drivers and vehicles
* Track shipment progress
* Store pickup and delivery information
* Search and filter shipments
* View complete shipment history

### 🚛 Fleet Management

* Register and manage company vehicles
* Track vehicle availability
* Store vehicle capacity and specifications
* Monitor maintenance status
* View current vehicle assignments

### 👨‍✈️ Driver Management

* Manage driver profiles
* Track driver availability
* Store license and contact information
* View current assignments
* View delivery history

### 🗺️ Route Management

* Define shipment origins and destinations
* Assign routes to shipments
* Store estimated distances
* Track estimated delivery times
* Connect routes with drivers and vehicles

### 👥 Customer Management

* Create and manage customer accounts
* Store contact information
* Manage pickup and delivery addresses
* View customer shipment history

### 🏢 Warehouse Management

* Manage warehouse locations
* Monitor incoming shipments
* Monitor outgoing shipments
* Track warehouse capacity

### 📊 Operations Dashboard

* Active shipments
* Completed deliveries
* Delayed shipments
* Available drivers
* Vehicles currently in use
* Shipment status distribution
* Recent logistics activity

### 🔐 Security

* User authentication
* JWT authorization
* Protected routes
* Role-based permissions
* Admin, Dispatcher, and Driver access

---

## 🖥️ Dashboard Preview

```text
┌─────────────────────────────────────────────────────────────────┐
│ 🚚 FleetOps                                      🔔    👤 Admin │
├─────────────────┬───────────────────────────────────────────────┤
│                 │                                               │
│  📊 Dashboard   │     LOGISTICS OVERVIEW                       │
│                 │                                               │
│  📦 Shipments   │   ┌──────────┐ ┌──────────┐ ┌──────────┐    │
│  🚛 Vehicles    │   │    24    │ │    18    │ │     3    │    │
│  👨‍✈️ Drivers     │   │  ACTIVE  │ │DELIVERED │ │ DELAYED  │    │
│  🗺️ Routes      │   └──────────┘ └──────────┘ └──────────┘    │
│  👥 Customers   │                                               │
│  🏢 Warehouses  │   RECENT SHIPMENTS                           │
│  📈 Reports     │                                               │
│                 │   SH-1024  Dallas       In Transit           │
│  ⚙️ Settings    │   SH-1025  Austin       Delivered            │
│                 │   SH-1026  Houston      Delayed              │
│                 │   SH-1027  San Antonio  Scheduled            │
│                 │                                               │
└─────────────────┴───────────────────────────────────────────────┘
```

---

## 🔄 Shipment Lifecycle

```text
                      ┌───────────┐
                      │  Pending  │
                      └─────┬─────┘
                            │
                            ▼
                      ┌───────────┐
                      │ Scheduled │
                      └─────┬─────┘
                            │
                            ▼
                      ┌───────────┐
                      │ Assigned  │
                      └─────┬─────┘
                            │
                            ▼
                     ┌────────────┐
                     │ In Transit │
                     └──────┬─────┘
                            │
                            ▼
                  ┌──────────────────┐
                  │ Out for Delivery │
                  └────────┬─────────┘
                           │
                           ▼
                     ┌───────────┐
                     │ Delivered │
                     └───────────┘
```

Shipments can also transition to:

`Delayed` • `Cancelled` • `Failed Delivery` • `Returned`

---

## 👤 User Roles

| Role              | Permissions                                                        |
| ----------------- | ------------------------------------------------------------------ |
| 👑 **Admin**      | Full system access, users, fleet, shipments, customers and reports |
| 🎧 **Dispatcher** | Create shipments, assign drivers/vehicles and manage routes        |
| 🚚 **Driver**     | View assigned deliveries and update shipment status                |

---

## 🛠️ Tech Stack

### Frontend

| Technology         | Purpose                         |
| ------------------ | ------------------------------- |
| **Angular**        | Frontend framework              |
| **TypeScript**     | Application development         |
| **RxJS**           | Reactive data handling          |
| **Angular Router** | Navigation and protected routes |
| **Reactive Forms** | Forms and validation            |
| **HTML / SCSS**    | Interface and styling           |

### Backend

| Technology                 | Purpose             |
| -------------------------- | ------------------- |
| **ASP.NET Core / FastAPI** | REST API            |
| **PostgreSQL**             | Relational database |
| **JWT**                    | Authentication      |
| **Docker**                 | Containerization    |

---

## 🧠 Angular Concepts

FleetOps demonstrates practical use of:

```text
✓ Component-based architecture
✓ Standalone components
✓ Angular Router
✓ Route Guards
✓ Services
✓ Dependency Injection
✓ Reactive Forms
✓ Form Validation
✓ HttpClient
✓ REST API Integration
✓ RxJS Observables
✓ HTTP Interceptors
✓ Reusable Components
✓ Pagination
✓ Search & Filtering
✓ Role-Based Interfaces
✓ Error Handling
```

---

## 🏗️ Architecture

```text
┌───────────────────────────────┐
│          Angular UI           │
│                               │
│ Components • Forms • Routing  │
└───────────────┬───────────────┘
                │
                │ HTTPS / JSON
                ▼
┌───────────────────────────────┐
│           REST API            │
│                               │
│ Auth • Business Logic • CRUD  │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│          PostgreSQL           │
│                               │
│ Shipments • Drivers • Routes  │
│ Vehicles • Customers • Users  │
└───────────────────────────────┘
```

---

## 🗃️ Data Model

```text
                         ┌──────────────┐
                         │   Customer   │
                         └──────┬───────┘
                                │
                                │ creates
                                ▼
                         ┌──────────────┐
                         │   Shipment   │
                         └──────┬───────┘
                                │
                  ┌─────────────┼─────────────┐
                  │             │             │
                  ▼             ▼             ▼
              ┌────────┐   ┌─────────┐   ┌────────┐
              │ Driver │   │ Vehicle │   │ Route  │
              └────────┘   └─────────┘   └────────┘
```

### Core Entities

`User` • `Customer` • `Driver` • `Vehicle` • `Shipment` • `Route` • `Warehouse` • `Delivery` • `Address`

---

## 🌐 API

### Shipments

```http
GET    /api/shipments
GET    /api/shipments/{id}
POST   /api/shipments
PUT    /api/shipments/{id}
DELETE /api/shipments/{id}
```

### Drivers

```http
GET    /api/drivers
GET    /api/drivers/{id}
POST   /api/drivers
PUT    /api/drivers/{id}
```

### Vehicles

```http
GET    /api/vehicles
GET    /api/vehicles/{id}
POST   /api/vehicles
PUT    /api/vehicles/{id}
```

### Customers

```http
GET    /api/customers
POST   /api/customers
PUT    /api/customers/{id}
```

### Routes

```http
GET    /api/routes
POST   /api/routes
PUT    /api/routes/{id}
```

---

## 📂 Project Structure

```text
src/
│
├── app/
│   │
│   ├── core/
│   │   ├── guards/
│   │   ├── interceptors/
│   │   ├── models/
│   │   └── services/
│   │
│   ├── shared/
│   │   ├── components/
│   │   ├── directives/
│   │   └── pipes/
│   │
│   ├── features/
│   │   ├── dashboard/
│   │   ├── shipments/
│   │   ├── drivers/
│   │   ├── vehicles/
│   │   ├── customers/
│   │   ├── routes/
│   │   ├── warehouses/
│   │   └── reports/
│   │
│   ├── auth/
│   │
│   ├── app.component.ts
│   ├── app.config.ts
│   └── app.routes.ts
│
├── assets/
│
└── environments/
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

* Node.js
* npm
* Angular CLI
* PostgreSQL
* Git

Check your Angular installation:

```bash
ng version
```

---

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/logistics-management-system.git
```

### 2. Enter the Project

```bash
cd logistics-management-system
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Start the Development Server

```bash
ng serve
```

### 5. Open the Application

```text
http://localhost:4200
```

The application automatically reloads when source files are modified.

---

## 🗺️ Roadmap

* [x] Project architecture
* [ ] Authentication
* [ ] Dashboard
* [ ] Shipment management
* [ ] Driver management
* [ ] Vehicle management
* [ ] Customer management
* [ ] Route management
* [ ] Warehouse management
* [ ] Role-based authorization
* [ ] Reporting dashboard
* [ ] Live GPS tracking
* [ ] Interactive maps
* [ ] Delivery notifications
* [ ] Proof of delivery
* [ ] Vehicle maintenance tracking
* [ ] Fuel consumption tracking
* [ ] Invoice generation
* [ ] Production deployment

---

## 🔮 Future Improvements

Future versions of FleetOps could support:

**📍 Live Tracking**
Real-time GPS tracking for active vehicles and shipments.

**🗺️ Interactive Maps**
Visual route planning and delivery location management.

**🔔 Notifications**
Email or SMS notifications for shipment status changes.

**📸 Proof of Delivery**
Allow drivers to upload signatures, photos, or delivery documents.

**🔧 Fleet Maintenance**
Schedule vehicle maintenance and track service history.

**⛽ Fuel Analytics**
Monitor fuel consumption and vehicle efficiency.

**📈 Advanced Reporting**
Generate operational reports for shipments, drivers, vehicles, and customers.

---

## 🎯 Project Purpose

FleetOps was developed as a portfolio project to demonstrate the development of a realistic enterprise-style application using **Angular and modern backend technologies**.

The project focuses on:

* Scalable frontend architecture
* Real-world business workflows
* RESTful API design
* Relational data modeling
* Authentication and authorization
* Responsive UI development
* Clean and maintainable code

---

## 🤝 Contributing

Contributions, suggestions, and feedback are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push your branch
5. Open a Pull Request

---

## 📄 License

This project is available for **educational and portfolio purposes**.

---

<div align="center">

### 🚚 FleetOps

**Moving logistics forward, one shipment at a time.**

⭐ If you find this project useful, consider starring the repository.

</div>
