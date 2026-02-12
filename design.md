# System Design Document

## 1. Architecture Overview

The system follows a client-server architecture with AI integration.

User Mobile App 
        ↓
        
Google Maps / GPS API

        ↓
        
Backend Server (Node.js / Express)

        ↓
Database (MongoDB / MySQL)

        ↓
Notification Service

        ↑
        
Pharmacy Dashboard

## 2. Component Description

### 2.1 User App
- Search & order interface
- Displays pharmacy list on map
- Shows real-time status

### 2.2 Backend API
- Handles authentication
- Manages pharmacy & order data
- Connects AI engine
- Sends notifications

### 2.3 AI Engine
- Analyzes distance, demand, and order history
- Ranks pharmacies
- Suggests alternatives
- Detects emergency priority cases

### 2.4 Database
Stores:
- User data
- Pharmacy details
- Order history
- Availability data

### 2.5 Pharmacy Dashboard
- Updates medicine stock
- Updates open/closed status
- Manages incoming orders

## 3. Data Flow

1. User enables GPS.
2. Nearby pharmacies fetched using Google Maps API.
3. Backend retrieves real-time status from database.
4. AI ranks pharmacies.
5. User places order.
6. Pharmacy updates order status.
7. Notifications sent to user.

## 4. Security Design
- JWT Authentication
- HTTPS API calls
- Encrypted database storage
- Role-based access control

## 5. Future Enhancements
- Online payments
- Prescription upload & validation
- Drone/express delivery integration
- Advanced AI analytics

