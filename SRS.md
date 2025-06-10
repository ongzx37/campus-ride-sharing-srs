# Software Requirement Specification (SRS)

## Campus Ride-Sharing Platform with Parking System Integration

---

**Section:** TT2L
**Group:** D
**Group Members:**

| Group Member Name    | Student ID |
| -------------------- | ---------- |
| William Sim Wee Lian | 243UC245RN |
| Er Kangming          | 243UC247ND |
| Francis Wong Wei Hou | 243UC245PD |

---

# Table of Contents

1. [SRS Overview](#srs-overview)

   * [Purpose](#purpose)
   * [Scope](#scope)
   * [Product Overview](#product-overview)
   * [Product Functions](#product-functions)
   * [User Characteristics](#user-characteristics)
   * [Limitations](#limitations)
   * [Definitions](#definitions)
2. [Reference](#reference)
3. [Requirements](#requirements)

   * [Functions](#functions)
   * [Performance Requirements](#performance-requirements)
   * [Usability Requirements](#usability-requirements)
   * [Interface Requirements](#interface-requirements)
   * [Logical Database Requirements](#logical-database-requirements)
   * [Design Constraints](#design-constraints)
   * [Software System Attributes](#software-system-attributes)
   * [Supporting Information](#supporting-information)
4. [Verification](#verification)

   * [Verification Approach](#verification-approach)
   * [Verification Criteria](#verification-criteria)
5. [Assumptions and Dependencies](#assumptions-and-dependencies)
6. [Acronyms and Abbreviations](#acronyms-and-abbreviations)

---

# 1. SRS Overview

## 1.1 Purpose

Develop a smart, secure, and scalable Campus Ride-Sharing Platform with Parking Integration to:

* Reduce traffic congestion.
* Encourage eco-friendly commuting.
* Maximize use of limited parking spaces.

## 1.2 Scope

A web-based system enabling:

* Ride-sharing coordination.
* GPS-based real-time tracking.
* Parking spot reservation and availability display.
* Role-based access via university credentials.
* Admin monitoring and reporting dashboard.

Out-of-scope:

* Third-party ride-hailing or payment integrations.
* QR code or physical sensor integration.
* Mobile app (web-only).

## 1.3 Product Overview

### 1.3.1 Product Perspective

Web-only system enhancing campus mobility and promoting sustainable travel.

**Core Functionalities:**

1. Ride Coordination
2. Authentication
3. Parking Integration
4. User Role Access
5. Safety & Reporting
6. Data & Analytics

### 1.3.2 Product Functions

#### 1.3.2.1 Student Functions

* Login via university credentials.
* Create/join rides.
* View recommended routes.
* View/reserve parking spots.
* Report incidents.
* View trip/parking history.

#### 1.3.2.2 Staff Functions

* Same as student functions with priority parking.

#### 1.3.2.3 Guest Functions

* Guest login.
* View/reserve parking.
* No ride-sharing access.

#### 1.3.2.4 Admin Functions

* Admin login.
* User management.
* System monitoring.
* Manage reports.
* Route/parking optimization.
* Generate analytics reports.

#### 1.3.2.5 Special Functions

* Centralized authentication.
* Offline data handling.
* Data backup and recovery.
* Data security and logging.

### 1.3.3 User Characteristics

| Role    | Expected Knowledge                          |
| ------- | ------------------------------------------- |
| Student | Basic ride-sharing & parking apps knowledge |
| Staff   | Moderate platform understanding             |
| Guest   | Guided, limited access                      |
| Admin   | High proficiency in backend management      |

### 1.3.4 Limitations

* Real-time data accuracy dependency.
* Integration constraints.
* Limited mobile support.
* User adoption challenges.
* Scalability concerns.
* Privacy & security requirements.

## 1.4 Definitions

| Term                   | Definition                                         |
| ---------------------- | -------------------------------------------------- |
| CRPIS                  | Campus Ride-Sharing and Parking Integration System |
| Carpooling             | Users share rides with others.                     |
| Smart Parking          | Real-time parking status and reservation system.   |
| User                   | System user (student, staff, guest, admin).        |
| Authentication Server  | Verifies user credentials.                         |
| Real-Time Parking Data | Live parking availability data.                    |

# 2. Reference

* Alotaibi, E., & Perwej, Y. (2021). *A Smart Parking System Using IoT and Cloud-Based Services.*
* Abusair, S., Khan, R. Z., & Mian, M. A. (2020). *Smart Campus Mobility.*
* Others as per document.

# 3. Requirements

## 3.1 Functions

Use cases for:

* Student
* Staff
* Guest
* Admin

## 3.2 Performance Requirements

| Req ID    | Description                     | Priority |
| --------- | ------------------------------- | -------- |
| REQ\_P001 | Respond within 0-3 seconds.     | High     |
| REQ\_P002 | Support 5,000 concurrent users. | High     |
| ...       | ...                             | ...      |

## 3.3 Usability Requirements

| Req ID     | Description        | Priority |
| ---------- | ------------------ | -------- |
| REQ\_UR001 | Seamless login.    | High     |
| REQ\_UR002 | Real-time updates. | Medium   |
| ...        | ...                | ...      |

## 3.4 Interface Requirements

### 3.4.1 System Interfaces

* Authentication Server.
* Carpooling Server.
* Parking Management Server.

### 3.4.2 User Interfaces

* Responsive, intuitive UI design.
* Consistent styling across devices.

### 3.4.3 Hardware Interfaces

* Minimum: 64-bit processor, 4GB RAM, internet connectivity.

### 3.4.4 Software Interfaces

* OS: Windows, macOS, Linux, iOS, Android.
* Browser: Chrome, Edge, Safari.
* Backend: Node.js, MySQL.

### 3.4.5 Communications Interfaces

* HTTP/HTTPS.
* SAML, OAuth.
* WebSocket.

## 3.5 Logical Database Requirements

ERD covering:

* User (Students, Staff, Guests, Admins)
* RideSharing
* Report
* ParkingSpot
* Reservation

## 3.6 Design Constraints

* WCAG compliance.
* GDPR compliance.
* 1-year development timeline.
* Role-based access.
* Encryption.

## 3.7 Software System Attributes

* Accuracy: Error < 0.0001%.
* Availability: Max 12 hours downtime/year.
* Maintainability: Modular, documented.
* Portability: Multi-platform.
* Reliability: High volume handling.
* Security: HTTPS, AES-256 encryption.
* Usability: Core features within 5 clicks.

## 3.8 Supporting Information

### 3.8.1 Interview Summary

* Stakeholder interviews conducted.
* Key expectations gathered.

### 3.8.2 Observation Summary

* Competitor analysis (SpotHero).
* Improvement recommendations documented.

# 4. Verification

## 4.1 Verification Approach

* Unit Testing.
* System Integration Testing.
* Load Testing.
* Stress Testing.
* Security Testing.
* Usability Testing.

## 4.2 Verification Criteria

* Ride offer creation.
* Route matching.
* Parking reservation.
* Access control.
* Data integrity.

# 5. Assumptions and Dependencies

* Stable internet connection.
* University authentication server.
* Real-time parking data source.
* Campus security integration.

# 6. Acronyms and Abbreviations

| Acronym | Definition                                         |
| ------- | -------------------------------------------------- |
| CRPIS   | Campus Ride-Sharing and Parking Integration System |
| UI      | User Interface                                     |
| UX      | User Experience                                    |
| GPS     | Global Positioning System                          |
| API     | Application Programming Interface                  |
| SSO     | Single Sign-On                                     |
| HTTPS   | Hypertext Transfer Protocol Secure                 |

---

*End of Document*
