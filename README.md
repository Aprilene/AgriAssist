# AgriAssist
AgriAssist is an agricultural monitoring and farm management system designed to help farmers manage farming activities more efficiently. It provides real-time weather forecasting, pest risk prediction, market price monitoring, emergency alerts, crop tracking, expense management, and farm scheduling through an integrated Progressive Web App (PWA) and an administrative web dashboard.

# Group Members:
- Espinile, Ralph Ryan
- Melodillar, Lawrence Angelo B.
- Torres, Aprilene E.

# Course: ITST 303 – Web and Database Integration
# Section: 3WMAD-2

# Project Description 
AgriAssist addresses the lack of accessible digital tools for local farmers by providing:
1.Real-time weather forecasts via Weather API integration
2.Pest risk prediction using a trained machine learning model (Scikit-learn)
3.Market price monitoring with price trend tracking
4.Emergency and pest outbreak alerts with push notifications via Firebase Cloud Messaging (FCM)
5.Crop monitoring and tracking with growth stage management
6.Expense and income tracking per crop cycle
7.Farm calendar and scheduling for farming activities
8.Farming guides with category based agricultural content
9.Secure authentication with JWT, bcrypt password hashing, OTP verification, and AES-256 encryption
10. Admin dashboard for centralized monitoring and management of all farmer data

# Technologies Used
# Backend
Technology
- Python 3 - Primary programming language
- FastAPI - Backend web framework and REST API
- SQLAlchemy - ORM and database management
- Uvicorn - ASGI server
- Pydantic - Data validation
- PassLib / bcrypt - Password hashing
- python-jose - JWT authentication
- cryptography - AES-256 encryption for sensitive data
- Scikit-learn - Pest risk prediction ML model
- Pandas - Dataset processing
- NumPy - Numerical computations
- SlowAPI - Rate limiting
- python-dotenv - Environment variable management

# Frontend
- HTML5 / CSS3 - Page structure and styling
- JavaScript (Vanilla) - Dynamic UI interactions
- Progressive Web App (PWA) - Mobile-first farmer interfaceFont AwesomeIcons

# Database
- MySQL - Primary relational database
- phpMyAdmin - Database administration (local)

# APIs & External Services
Weather API - Real-time weather forecasts, temperature, humidity, rainfall
Firebase Cloud Messaging (FCM) - Push notifications for alerts and announcements

# DevOps & Deployment
- AWS EC2 (Ubuntu 24.04, t3.micro) - Cloud server hosting
- GitHub - Version control and source code management
- systemd - Service management and auto-restart
- Cloudflared - Tunnel service for external access

# Installation Instructions
Prerequisites
- Python 3.10+
- MySQL Server
- Git
- pip

# Deployment Link
The system is deployed and accessible at:
- Farmer PWA: https://elimination-room-serum-mill.trycloudflare.com/frontend/pwa/index.html?fbclid=IwY2xjawSCgoJleHRuA2FlbQIxMABicmlkETBYNWRad0ZzQ01FRjBleEVMc3J0YwZhcHBfaWQQMjIyMDM5MTc4ODIwMDg5MgABHh3kjffHaIKodc7xTtUVk_jDu7nAOwDXYNd8zazq_vwjK4OeNLrKoEUziRHb_aem_mvZELG4UYz71JmycBBrhRw

- Admin Dashboard: https://elimination-room-serum-mill.trycloudflare.com/frontend/admin/index.html?fbclid=IwY2xjawSCgqdleHRuA2FlbQIxMABicmlkETBYNWRad0ZzQ01FRjBleEVMc3J0YwZhcHBfaWQQMjIyMDM5MTc4ODIwMDg5MgABHk88knVjRPyd0llC4r9yZj8Y3IKadS58oksQlE3QcWRe6l1OQ8siF2xEvsRX_aem_L-BGrj859raQ23PxeclXDQ

# Database Structure
The system uses MySQL with the following tables:
- users - Farmer and admin accounts
- login_attempts - Brute force protection tracking
- token_blacklist - Invalidated JWT access tokens
- refresh_token_blacklist - Invalidated refresh tokens
- password_reset_tokens - Secure password recovery tokens
- otp_verification - OTP codes for 2FA
- audit_logs - System-wide action audit trail
- notification_inbox - Per-user notification records
- announcements - Admin-created announcements
- emergency_alerts - Emergency and disaster alerts
- pest_alerts - Pest outbreak notifications
- market_prices - Current crop market prices
- market_price_history - Historical price trend records
- farming_guides - Agricultural educational content
- crop_tracker - Farmer crop monitoring
- recordscrop_losses - Crop loss incident records
- expense_tracker - Farm income and expense records
- farm_calendar - Scheduled farming activities

# Machine Learning
The pest risk prediction model uses the following Kaggle datasets:
- https://www.kaggle.com/datasets/madhuraatmarambhagat/jassids-prediction-dataset
- https://www.kaggle.com/datasets/zsinghrahulk/rice-pest-and-diseases
- https://www.kaggle.com/datasets/zsinghrahulk/cotton-pest-and-disease

# Security Features
- JWT access tokens (15-minute expiry) + refresh tokens (7-day expiry)
- Token blacklisting for server side logout
- bcrypt password hashing
- AES-256-CBC encryption for sensitive personal data (contact, location, FCM tokens)
- OTP email verification for new accounts
- Brute-force protection via login attempt tracking
- Rate limiting on authentication endpoints
- Audit logging for all admin actions
- Environment variable based secret management (no hardcoded credentials)

# License
This project was developed as an final academic requirement for ITST 303 – Web and Database Integration at the Polytechnic University San Pablo City Campus.

# Canva Link Presentation
- https://canva.link/hwi8rogsswli4k9

# Youtube Presentation Link
- https://www.youtube.com/watch?v=ALK6uJkWEP0
