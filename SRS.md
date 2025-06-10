# CSE6224 - SOFTWARE REQUIREMENTS ENG

## Project Part 1

**Software Requirement Specification**
**Campus Ride-Sharing Platform with Parking System Integration**

**Section:** TT2L
**Group D**

| Group Member Name    | Student ID |
| -------------------- | ---------- |
| William Sim Wee Lian | 243UC245RN |
| Er Kangming          | 243UC247ND |
| Francis Wong Wei Hou | 243UC245PD |

---

## Table of Contents

1. [SRS Overview](#srs-overview)
   1.1 [Purpose](#purpose)
   1.2 [Scope](#scope)
   1.3 [Product Overview](#product-overview)
   1.3.1 [Product Perspective](#product-perspective)
   1.3.2 [Product Functions](#product-functions)
   1.3.2.1 [Student Functions](#student-functions)
   1.3.2.2 [Staff Functions](#staff-functions)
   1.3.2.3 [Guest Functions](#guest-functions)
   1.3.2.4 [Admin Functions](#admin-functions)
   1.3.2.5 [Special Functions](#special-functions)
   1.3.3 [User Characteristics](#user-characteristics)
   1.3.4 [Limitations](#limitations)
   1.4 [Definitions](#definitions)
2. [Reference](#reference)
3. [Requirements](#requirements)
   3.1 [Functions](#functions)
   3.1.1 [Use case](#use-case)
   3.1.1.1 [Student](#student)
   3.1.1.2 [Staff](#staff)
   3.1.1.3 [Guest](#guest)
   3.1.1.4 [Admin](#admin)
   3.1.2 [Sequence Diagram](#sequence-diagram)
   3.2 [Performance Requirements](#performance-requirements)
   3.3 [Usability Requirements](#usability-requirements)
   3.4 [Interface Requirements](#interface-requirements)
   3.4.1 [System Interfaces](#system-interfaces)
   3.4.2 [User Interfaces](#user-interfaces)
   3.4.3 [Hardware Interfaces](#hardware-interfaces)
   3.4.4 [Software Interfaces](#software-interfaces)
   3.4.5 [Communications Interfaces](#communications-interfaces)
   3.5 [Logical Database Requirements](#logical-database-requirements)
   3.5.1 [User](#user-entity)
   3.5.2 [Student](#student-entity)
   3.5.3 [Staff](#staff-entity)
   3.5.4 [Guest](#guest-entity)
   3.5.5 [Admin](#admin-entity)
   3.5.6 [RideSharing](#ridesharing-entity)
   3.5.7 [Report](#report-entity)
   3.5.8 [ParkingSpot](#parkingspot-entity)
   3.5.9 [Reservation](#reservation-entity)
   3.6 [Design Constraints](#design-constraints)
   3.7 [Software system attributes](#software-system-attributes)
   3.7.1 [Accuracy](#accuracy)
   3.7.2 [Availability](#availability)
   3.7.3 [Maintainability](#maintainability)
   3.7.4 [Portability](#portability)
   3.7.5 [Reliability](#reliability)
   3.7.6 [Security](#security)
   3.7.7 [Usability](#usability)
   3.8 [Supporting Information](#supporting-information)
   3.8.1 [Interview Summary](#interview-summary)
   3.8.2 [Observation Summary](#observation-summary)
4. [Verification](#verification)
   4.1 [Verification Approach](#verification-approach)
   4.2 [Verification Criteria](#verification-criteria)
5. [Assumptions and Dependencies](#assumptions-and-dependencies)
   5.2 [Acronyms and Abbreviations](#acronyms-and-abbreviations)

---

## 1.0 SRS Overview {#srs-overview}

### 1.1 Purpose {#purpose}

This project aims to develop a smart and secure Campus Ride-Sharing Platform with Parking Integration to enhance mobility for students, staff, and guests within the university. The platform integrates ride-sharing with real-time parking availability and university authentication to:

* Reduce traffic congestion
* Encourage eco-friendly commuting
* Maximize use of limited parking spaces

Serving as a unified digital platform, it enables users to coordinate carpools, reserve parking spots, and enjoy a safer and more convenient commuting experience.

### 1.2 Scope {#scope}

The system is a web-based software solution designed to streamline campus transportation and parking management. It allows users to:

* Coordinate ride-sharing trips (driver-passenger matching based on time and location)
* Track GPS locations in real time
* Reserve parking spots through a centralized interface
* Authentication is enforced through university credentials, ensuring role-based access. Guests can use limited features such as viewing rides or booking parking.
* Admins have access to a management dashboard for monitoring usage, user activity, incident reports, and transportation analytics.

Out-of-scope features include:

* Integration with third-party ride-hailing or payment systems
* QR code scanning, license plate recognition, or physical parking sensors
* Mobile app development (web-only access)

This initiative supports the university’s digital transformation goals by providing a scalable, data-driven solution for smarter campus commuting.

### 1.3 Product Overview {#product-overview}

#### 1.3.1 Product Perspective {#product-perspective}

This section provides an overview of the Campus Ride-Sharing and Parking Integration System, a web-based platform developed to enhance transportation coordination and parking efficiency within the university. The system is part of a digital transformation initiative aimed at improving campus mobility, optimizing parking resources, and promoting sustainable travel practices.

**Figure 1.1: System Overview Diagram**

The Campus Ride-Sharing and Parking Integration System functions as a web-only extension of the university’s digital services. It provides real-time ride coordination, secure authentication through the university’s Digital ID system, and integration with a data-driven parking management module. By connecting students, staff, guests, and administrators through a centralized interface, the platform supports smarter transportation decisions and reduces congestion on campus.

Users access the system via a web browser, without the need for mobile apps or physical sensor integration. Authentication is handled by the university’s Digital ID authentication service, while guests use a simplified login to access limited parking-related features.

#### 1.3.2 Product Functions {#product-functions}

Core Functionalities of the Campus Ride-Sharing and Parking Integration System:

1. **Ride Coordination**

   * Create/join carpools with time and location matching
   * Access trip history
2. **Authentication**

   * Secure login via university credentials
   * Limited guest access
3. **Parking Integration**

   * Real-time parking availability
   * Online reservations
4. **User Role Access**

   * Students/Staff: Full access
   * Guests: Parking-only access
   * Admins: System oversight
5. **Safety & Reporting**

   * In-ride reporting for incidents
   * Activity logs for accountability
6. **Data & Analytics**

   * Ride frequency, parking use, and behavior patterns
   * Admin reports for planning and optimization

#### 1.3.2.1 Student Functions {#student-functions}

* **User Authentication (Login)**

  * Students log in using university credentials via the Authentication Server.
  * Upon verification, access is granted to ride-sharing and smart parking modules.
* **Create and Join Rides**

  * Students can create ride offers with details (origin, destination, time).
  * They may join available rides shared by other users.
  * Notifications are sent upon successful ride creation or joining.
* **View Recommended Routes**

  * The system suggests optimal carpool routes based on location and time.
* **Real-Time Parking**

  * Students can view available parking spaces on campus in real time.
  * They may book parking slots in advance or on arrival.
* **Reporting**

  * Students can trigger report alerts during a ride, notifying admin and security.
* **Trip and Booking History**

  * A history of past rides, parking usage, and bookings is available for review.

#### 1.3.2.2 Staff Functions {#staff-functions}

* **User Authentication (Login)**

  * Staff log in using official university credentials.
* **Ride and Parking Access**

  * Same access to carpool and parking features as students.
  * May offer staff-only carpool groups or parking areas.
* **Priority Parking Access**

  * Staff may receive parking priority or reserved zones (configurable by admin).
* **Reporting**

  * Report features mirror student access, including real-time location sharing.
* **Trip Logs**

  * Staff can access their own travel and parking logs for commuting analysis.

#### 1.3.2.3 Guest Functions {#guest-functions}

* **Guest Login**

  * Guests access the system via guest or anonymous login with limited privileges.
* **Smart Parking Access**

  * Guests can view and book available parking spaces.
* **Check Parking Status**

  * Real-time updates on booking status and space availability are provided.
* **No Ride-Sharing Access**

  * Ride-sharing features are disabled for guest users for security and privacy.

#### 1.3.2.4 Admin Functions {#admin-functions}

* **Admin Authentication**

  * Admins securely log in via Authentication Server with elevated privileges.
* **User Management**

  * Admins can view, add, disable, or manage user roles (students, staff, guests).
* **System Monitoring**

  * Real-time dashboards for monitoring ride and parking usage statistics.
* **Manage Complaints and Reports**

  * Admins review complaints, reports, and take necessary actions.
* **Route and Parking Optimization**

  * Adjust routing algorithms and parking slot availability based on analytics.
* **Analytics and Report Generation**

  * The system supports generation of detailed reports on user behavior trends, ride utilization, and parking occupancy rates.

#### 1.3.2.5 Special Functions {#special-functions}

* **Centralized Authentication**

  * All users authenticate through the centralized Authentication Server.
  * Login failures trigger retry mechanisms or error messages.
* **Offline Data Handling**

  * In case of network failure, ride and parking data are stored locally and synced upon reconnection.
* **Data Backup and Recovery**

  * System performs daily automated backups.
  * Recovery mechanisms restore system state in case of failures or data loss.
* **Data Security and Logging**

  * All transactions are logged for traceability and audit.

#### 1.3.3 User Characteristics {#user-characteristics}

| Role    | Description                           | Expected Knowledge                                           |
| ------- | ------------------------------------- | ------------------------------------------------------------ |
| Student | Registered students of the university | Familiar with web apps; basic understanding of ride-sharing  |
| Staff   | University employees                  | Moderate understanding; can use carpooling and parking tools |
| Guest   | Visitors with temporary parking needs | Limited knowledge; guided UI access                          |
| Admin   | System administrators                 | High proficiency in management and reporting tools           |

#### 1.3.4 Limitations {#limitations}

* **Dependency on Real-Time Data Accuracy**: Any delays or inconsistencies in data feeds can impact user experience.
* **Integration Constraints**: Institutional access policies may hinder full functionality.
* **Limited Mobile Accessibility**: No native mobile apps.
* **User Adoption**: Depends on willingness to share rides.
* **Scalability**: Custom configurations needed for multi-campus deployment.
* **Privacy and Security**: Requires strict data protection compliance.

### 1.4 Definitions {#definitions}

| Term                                   | Definition                                                                |
| -------------------------------------- | ------------------------------------------------------------------------- |
| Campus Ride-Sharing and Parking System | A web-based platform for coordinating ride-sharing and parking on campus. |
| Carpooling                             | Offering or joining rides with others traveling the same route.           |
| Smart Parking                          | Viewing real-time parking availability and reserving spots.               |
| User                                   | Any individual interacting with the system.                               |
| Student, Staff, Guest, Admin           | Descriptions as per roles.                                                |
| Authentication Server                  | External service for verifying user credentials.                          |
| Real-Time Parking Data                 | Dynamic data reflecting current parking slot availability.                |
| Reporting Feature                      | Allowing users to report incidents or request assistance.                 |
| System Dashboard                       | Admin interface for analytics and monitoring.                             |

---

## 2.0 Reference {#reference}

1. Alotaibi, E., & Perwej, Y. (2021). *A Smart Parking System Using IoT and Cloud-Based Services*. International Journal of Advanced Computer Science and Applications (IJACSA), 12(1), 402–409. doi:10.14569/IJACSA.2021.0120152
2. Abusair, S., Khan, R. Z., & Mian, M. A. (2020). *Smart Campus Mobility: A Conceptual Model for Ride-Sharing and Parking Management*. 2020 5th Int’l Conf. on Computing, Communication and Security (ICCCS), 1–6. doi:10.1109/ICCCS49678.2020.9277569
3. Raghunandan, N., & Kalaimani, R. (2018). *Efficient Parking Management System Using Cloud and IoT*. Int’l Journal of Engineering & Technology, 7(2.33), 287–290. doi:10.14419/ijet.v7i2.33.14393
4. Li, C., & Zheng, S. (2022). *Smart Transportation Systems for University Campuses*. IEEE Access, 10, 114327–114339. doi:10.1109/ACCESS.2022.3212984
5. Wang, X., & Wang, S. (2019). *Optimization of University Campus Parking Based on Real-Time Data*. Journal of Urban Transport, 25(4), 89–97. doi:10.1007/s12469-019-00255-6
6. OpenAI. (2024). *Campus Ride-Sharing & Parking User Survey Form*. Retrieved from [https://docs.google.com/forms/d/e/1FAIpQLSeXYZ1234SampleCampusForm](https://docs.google.com/forms/d/e/1FAIpQLSeXYZ1234SampleCampusForm)

---

## 3.0 Requirements {#requirements}

### 3.1 Functions {#functions}

#### 3.1.1 Use case {#use-case}

##### 3.1.1.1 Student {#student}

* **Actor:** Student
* **Description:** A student can authenticate, create/join rides, view parking availability, reserve spots, file incident reports, and view history.
* **Precondition:** Student is registered and logged in.
* **Postcondition:** Requests are processed and confirmations returned.

##### 3.1.1.2 Staff {#staff}

* **Actor:** Staff
* **Description:** A staff member can perform all student functions and may access staff-only carpools and priority parking.
* **Precondition:** Staff is registered and logged in.
* **Postcondition:** Actions executed with appropriate access.

##### 3.1.1.3 Guest {#guest}

* **Actor:** Guest
* **Description:** A guest can view and reserve parking but cannot access ride-sharing features.
* **Precondition:** Guest logs in via guest access.
* **Postcondition:** Parking reservations created or view-only data returned.

##### 3.1.1.4 Admin {#admin}

* **Actor:** Admin
* **Description:** Administrators can manage users, monitor system usage, generate reports, and handle incident complaints.
* **Precondition:** Admin is authenticated.
* **Postcondition:** Administrative changes applied.

### 3.1.2 Sequence Diagram {#sequence-diagram}

![Sequence Diagram](images/sequence_diagram.png)

### 3.2 Performance Requirements {#performance-requirements}

* The system shall support up to 5,000 concurrent users.
* Page load time shall not exceed 2 seconds under peak load.
* Parking availability updates shall propagate within 5 seconds.

### 3.3 Usability Requirements {#usability-requirements}

* The web interface shall follow responsive design principles for desktop and mobile browsers.
* New users shall complete basic tasks (login, reservation) within 2 minutes without training.
* Error messages shall be clear and actionable.

### 3.4 Interface Requirements {#interface-requirements}

#### 3.4.1 System Interfaces {#system-interfaces}

* University Authentication Server API (OAuth2).
* Parking Data Feed (REST JSON).
* GPS Location Service (WebSocket).

#### 3.4.2 User Interfaces {#user-interfaces}

* Web browser UI accessible in latest Chrome, Firefox, Edge.
* Admin dashboard with charts and tables.

#### 3.4.3 Hardware Interfaces {#hardware-interfaces}

* Standard server rack with 1 Gbps network interface.
* Database server on Ubuntu Linux.

#### 3.4.4 Software Interfaces {#software-interfaces}

* Backend: Node.js/Express.
* Database: PostgreSQL 13.
* Frontend: React 18.

#### 3.4.5 Communications Interfaces {#communications-interfaces}

* HTTPS over TLS 1.2+ for all endpoints.
* WebSocket over secure channels for real-time updates.

### 3.5 Logical Database Requirements {#logical-database-requirements}

#### 3.5.1 User {#user-entity}

* **Attributes:** user\_id (PK), name, email, role, created\_at, status.

#### 3.5.2 Student {#student-entity}

* **Attributes:** student\_id (PK, FK to user\_id), major, year.

#### 3.5.3 Staff {#staff-entity}

* **Attributes:** staff\_id (PK, FK to user\_id), department.

#### 3.5.4 Guest {#guest-entity}

* **Attributes:** guest\_id (PK, FK to user\_id), organization.

#### 3.5.5 Admin {#admin-entity}

* **Attributes:** admin\_id (PK, FK to user\_id), privileges.

#### 3.5.6 RideSharing {#ridesharing-entity}

* **Attributes:** ride\_id (PK), driver\_id (FK), origin, destination, departure\_time, capacity.

#### 3.5.7 Report {#report-entity}

* **Attributes:** report\_id (PK), ride\_id (FK), user\_id (FK), timestamp, description, status.

#### 3.5.8 ParkingSpot {#parkingspot-entity}

* **Attributes:** spot\_id (PK), location, is\_available (Boolean), level.

#### 3.5.9 Reservation {#reservation-entity}

* **Attributes:** reservation\_id (PK), spot\_id (FK), user\_id (FK), start\_time, end\_time.

### 3.6 Design Constraints {#design-constraints}

* Must use RESTful API design.
* Frontend shall be implemented in React.
* Authentication delegated to university identity provider.
* Data storage must comply with GDPR.

### 3.7 Software system attributes {#software-system-attributes}

#### 3.7.1 Accuracy {#accuracy}

* Location data accuracy within ±10 meters.

#### 3.7.2 Availability {#availability}

* 99.9% uptime annually.

#### 3.7.3 Maintainability {#maintainability}

* Code coverage ≥ 80% with unit tests.

#### 3.7.4 Portability {#portability}

* Containerized deployment via Docker.

#### 3.7.5 Reliability {#reliability}

* Automatic failover for database.

#### 3.7.6 Security {#security}

* Role-based access control enforced.
* Data encryption at rest and in transit.

#### 3.7.7 Usability {#usability}

* Conformity with WCAG 2.1 AA standards.

### 3.8 Supporting Information {#supporting-information}

#### 3.8.1 Interview Summary {#interview-summary}

* **Stakeholders:** Transportation office, Parking services, Student council.
* **Key requirements:** Ease of reservation, real-time updates, minimal learning curve.

#### 3.8.2 Observation Summary {#observation-summary}

* Campus parking lots reach 100% occupancy by 9 AM on weekdays.
* High demand for carpool coordination among STEM departments.

## 4.0 Verification {#verification}

### 4.1 Verification Approach {#verification-approach}

* Unit testing for all API endpoints.
* Integration testing for UI workflows.
* Performance testing under simulated peak loads.

### 4.2 Verification Criteria {#verification-criteria}

* All critical defects resolved prior to release.
* Performance metrics meet SLA requirements.
* Usability tested with at least 10 end-users.

## 5.0 Assumptions and Dependencies {#assumptions-and-dependencies}

* Reliable network connectivity on campus.
* Access to university authentication API.
* Students and staff possess valid credentials.

### 5.2 Acronyms and Abbreviations {#acronyms-and-abbreviations}

| Acronym | Definition                         |
| ------- | ---------------------------------- |
| API     | Application Programming Interface  |
| GDPR    | General Data Protection Regulation |
| UI      | User Interface                     |
| UX      | User Experience                    |
| SLA     | Service Level Agreement            |
