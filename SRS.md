# CSE6224-SOFTWARE REQUIREMENTS ENG

Project Part 1

Software Requirement Specification

Campus Ride-Sharing Platform with
Parking System Integration

Section: TT2L
Group D

| Group Member Name    | Student ID |
| -------------------- | ---------- |
| William Sim Wee Lian | 243UC245RN |
| Er Kangming          | 243UC247ND |
| Francis Wong Wei Hou | 243UC245PD |

---

## Table Content

| Section                                                                | Page |
| ---------------------------------------------------------------------- | ---- |
| 1.0 SRS Overview                                                       | 6    |
| 1.3 Product Overview                                                   | 9    |
| 1.3.2 Product Functions                                                | 12   |
| 1.3.2.1 Student Functions                                              | 13   |
| 1.3.2.2 Staff Functions                                                | 13   |
| 1.3.2.3 Guest Functions                                                | 14   |
| 1.3.2.4 Admin Functions                                                | 14   |
| 1.3.2.5 Special Functions                                              | 15   |
| 1.3.3 User Characteristics                                             | 16   |
| Table 1.2: User Characteristics                                        | 17   |
| 1.3.4 Limitations                                                      | 17   |
| 1.4 Definitions                                                        | 19   |
| 2.0 Reference                                                          | 20   |
| 3.0 Requirements                                                       | 21   |
| 3.1 Functions                                                          | 21   |
| 3.1.1.1 Student                                                        | 22   |
| 3.1.1.2 Staff                                                          | 23   |
| 3.1.1.3 Guest                                                          | 25   |
| 3.1.1.4 Admin                                                          | 26   |
| 3.1.2 Sequence Diagram                                                 | 28   |
| 3.1.2.4 Join Ride(Student and Staff)                                   | 33   |
| Figure 3.9: Join Ride                                                  | 34   |
| 3.1.2.7 Report Feature(Student and Staff)                              | 38   |
| Figure 3.12: Report Feature                                            | 38   |
| 3.2 Performance Requirements                                           | 47   |
| Table 3.1: Performance Requirements                                    | 49   |
| 3.3 Usability Requirements                                             | 50   |
| Table 3.2: Usability Requirements                                      | 50   |
| 3.4 Interface Requirements                                             | 52   |
| 3.4.1 System Interfaces                                                | 52   |
| 3.4.2 User Interfaces                                                  | 54   |
| Table 3.4: User Interfaces                                             | 54   |
| 3.4.3 Hardware Interfaces                                              | 54   |
| 3.4.4 Software Interfaces                                              | 54   |
| 3.4.5 Communications Interfaces                                        | 57   |
| 3.5 Logical Database Requirements                                      | 58   |
| 3.5.1 User                                                             | 60   |
| 3.5.2 Student                                                          | 60   |
| 3.5.3 Staff                                                            | 60   |
| 3.5.4 Guest                                                            | 61   |
| 3.5.5 Admin                                                            | 61   |
| 3.5.6 RideSharing                                                      | 61   |
| 3.5.7 Report                                                           | 62   |
| 3.5.8 ParkingSpot                                                      | 62   |
| 3.5.9 Reservation                                                      | 63   |
| 3.6 Design Constraints                                                 | 64   |
| 3.7 Software system attributes                                         | 66   |
| 3.7.1 Accuracy                                                         | 66   |
| 3.7.2 Availability                                                     | 66   |
| 3.7.3 Maintainability                                                  | 67   |
| 3.7.4 Portability                                                      | 67   |
| 3.7.5 Reliability                                                      | 68   |
| 3.7.7 Usability                                                        | 69   |
| 3.8 Supporting Information                                             | 70   |
| 3.8.1 Interview Summary                                                | 72   |
| Figure 3.8.1 Screenshot of Francis Wong Wei Hou interviewing           | 73   |
| 3.8.2 Observation Summary                                              | 74   |
| Figure 3.8.2 Screenshot of SpotHero Website                            | 74   |
| i. Overview                                                            | 74   |
| ii. User Interface Design                                              | 75   |
| iii. Functionality                                                     | 76   |
| iv. Performance Indicators                                             | 77   |
| v. Recommendations                                                     | 77   |
| b. Prototyping                                                         | 78   |
| Figure 3.8.3 Screenshot of Prototype Log In Page                       | 78   |
| Figure 3.8.4 Screenshot of Prototype Student Dashboard                 | 79   |
| Figure 3.8.5 Screenshot of Prototype Staff Dashboard                   | 79   |
| Figure 3.8.6 Screenshot of Prototype Guest Dashboard                   | 80   |
| Figure 3.8.7 Screenshot of Prototype Student Carpooling services       | 80   |
| Figure 3.8.8 Screenshot of Prototype Staff Carpooling services         | 81   |
| Figure 3.8.9 Screenshot of Prototype Student Carpooling Manage History | 82   |
| Figure 3.8.10 Screenshot of Prototype Staff Carpooling Manage History  | 82   |
| Figure 3.8.11 Screenshot of Prototype Student Smart Parking Services   | 82   |
| Figure 3.8.12 Screenshot of Prototype Staff Smart Parking Services     | 83   |
| Figure 3.8.13 Screenshot of Prototype Guest Smart Parking Services     | 83   |
| Figure 3.8.14 Screenshot of Prototype Admin Manage User Accounts       | 84   |
| Figure 3.8.15 Screenshot of Prototype Admin Manage User Accounts       | 85   |
| Figure 3.8.16 Screenshot of Prototype Admin Manage User Accounts       | 85   |
| 4. Verification                                                        | 87   |
| 4.1 Verification Approach                                              | 87   |
| 4.1.1 Functional Requirements Verification                             | 87   |
| 4.1.2 Performance Requirements Verification                            | 87   |
| 4.1.3 Security Requirements Verification                               | 88   |
| 4.1.4 Usability Requirements Verification                              | 88   |
| 4.1.5 Maintainability Requirements Verification                        | 89   |
| 4.1.6 Portability Requirements Verification                            | 89   |
| 4.2 Verification Criteria                                              | 90   |
| 5.1 Assumptions and Dependencies                                       | 91   |
| 5.2 Acronyms and Abbreviations                                         | 91   |



---

## 1.0 SRS Overview

### 1.1 Purpose

This project aims to develop a smart and secure Campus Ride-Sharing Platform with Parking Integration to enhance mobility for students, staff, and guests within the university. The platform integrates ride-sharing with real-time parking availability and university authentication to:

* Reduce traffic congestion
* Encourage eco-friendly commuting
* Maximize use of limited parking spaces

Serving as a unified digital platform, it enables users to coordinate carpools, reserve parking spots, and enjoy a safer and more convenient commuting experience.&#x20;

### 1.2 Scope

The system is a web-based software solution designed to streamline campus transportation and parking management. It allows users to:

* Coordinate ride-sharing trips (driver-passenger matching based on time and location)
* Track GPS locations in real time
* Reserve parking spots through a centralized interface

Authentication is enforced through university credentials, ensuring role-based access. Guests can use limited features such as viewing rides or booking parking.

Admins have access to a management dashboard for monitoring usage, user activity, incident reports, and transportation analytics.

This project follows software requirements engineering principles and incorporates user interviews and observations to accurately capture stakeholder needs.

Out-of-scope features include:

* Integration with third-party ride-hailing or payment systems
* QR code scanning, license plate recognition, or physical parking sensors
* Mobile app development (web-only access)

This initiative supports the university’s digital transformation goals by providing a scalable, data-driven solution for smarter campus commuting.&#x20;

---

## 1.3 Product Overview

### 1.3.1 Product Perspective

This section provides an overview of the Campus Ride-Sharing and Parking Integration System, a web-based platform developed to enhance transportation coordination and parking efficiency within the university. The system is part of a digital transformation initiative aimed at improving campus mobility, optimizing parking resources, and promoting sustainable travel practices.

The Campus Ride-Sharing and Parking Integration System functions as a web-only extension of the university's digital services. It provides real-time ride coordination, secure authentication through the university’s Digital ID system, and integration with a data-driven parking management module. By connecting students, staff, guests, and administrators through a centralized interface, the platform supports smarter transportation decisions and reduces congestion on campus.

Users access the system via a web browser, without the need for mobile apps or physical sensor integration. Authentication is handled by the university’s Digital ID authentication service, while guests use a simplified login to access limited parking-related features.&#x20;

#### Core Functionalities of the Campus Ride-Sharing and Parking Integration System

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

#### Table 1.1: Goals of the System

| Requirement ID | Goals                                                                                                                |
| -------------- | -------------------------------------------------------------------------------------------------------------------- |
| REQ\_CRPS\_001 | The system shall enable users to coordinate ride-sharing trips based on schedules, locations, and preferences.       |
| REQ\_CRPS\_002 | The system shall provide a real-time display of available parking spots to assist users in making parking decisions. |
| REQ\_CRPS\_003 | The system shall allow users to reserve parking spots in advance to reduce search time and avoid congestion.         |
| REQ\_CRPS\_004 | The system shall authenticate users through secure university credentials to ensure authorized access.               |
| REQ\_CRPS\_005 | The system shall include GPS-based location tracking to improve matching accuracy and parking navigation.            |
| REQ\_CRPS\_006 | The system shall provide a centralized web-based interface for ride-sharing and parking services.                    |
| REQ\_CRPS\_007 | The system shall support trip history tracking and real-time notifications for upcoming rides and changes.           |
| REQ\_CRPS\_008 | The system shall provide reporting and contact features to enhance user safety during trips.                         |
| REQ\_CRPS\_009 | The system shall promote ride-sharing as a sustainable commuting alternative to reduce emissions and traffic.        |
| REQ\_CRPS\_010 | The system shall include analytics dashboards for administrators to monitor usage and generate actionable insights.  |



---

## 1.3.2 Product Functions

This section outlines the normal and special operations performed by different user roles (Students, Staff, Guests, and Admins) in the Campus Ride-Sharing and Parking Integration System.&#x20;

### 1.3.2.1 Student Functions

* **User Authentication (Login)**
  Students log in using university credentials via the Authentication Server.
  Upon verification, access is granted to ride-sharing and smart parking modules.

* **Create and Join Rides**
  Students can create ride offers with details (origin, destination, time).
  They may join available rides shared by other users.
  Notifications are sent upon successful ride creation or joining.

* **View Recommended Routes**
  The system suggests optimal carpool routes based on location and time.

* **Real-Time Parking**
  Students can view available parking spaces on campus in real time.
  They may book parking slots in advance or on arrival.

* **Reporting**
  Students can trigger report alerts during a ride, notifying admin and security.

* **Trip and Booking History**
  A history of past rides, parking usage, and bookings is available for review.&#x20;

### 1.3.2.2 Staff Functions

* **User Authentication (Login)**
  Staff log in using official university credentials.

* **Ride and Parking Access**
  Same access to carpool and parking features as students.
  May offer staff-only carpool groups or parking areas.

* **Priority Parking Access**
  Staff may receive parking priority or reserved zones (configurable by admin).

* **Reporting**
  Report features mirror student access, including real-time location sharing.

* **Trip Logs**
  Staff can access their own travel and parking logs for commuting analysis.&#x20;

### 1.3.2.3 Guest Functions

* **Guest Login**
  Guests access the system via guest or anonymous login with limited privileges.

* **Smart Parking Access**
  Guests can view and book available parking spaces.

* **Check Parking Status**
  Real-time updates on booking status and space availability are provided.

* **No Ride-Sharing Access**
  Ride-sharing features are disabled for guest users for security and privacy.&#x20;

### 1.3.2.4 Admin Functions

* **Admin Authentication**
  Admins securely log in via Authentication Server with elevated privileges.

* **User Management**
  Admins can view, add, disable, or manage user roles (students, staff, guests).

* **System Monitoring**
  Real-time dashboards for monitoring ride and parking usage statistics.

* **Manage Complaints and Reports**
  Admins review complaints, reports, and take necessary actions.

* **Route and Parking Optimization**
  Adjust routing algorithms and parking slot availability based on analytics.

* **Analytics and Report Generation**
  Detailed reports on user behavior trends, ride utilization, and parking occupancy.&#x20;

### 1.3.2.5 Special Functions

* **Centralized Authentication**
  All users authenticate through the centralized Authentication Server.
  Login failures trigger retry mechanisms or error messages.

* **Offline Data Handling**
  In case of network failure, ride and parking data are stored locally and synced upon reconnection.

* **Data Backup and Recovery**
  System performs daily automated backups.
  Recovery mechanisms restore system state in case of failures or data loss.

* **Data Security and Logging**
  All transactions (rides, parking, report alerts) are logged for traceability and audit.&#x20;

---

## 1.3.3 User Characteristics

This section describes the end users of the system, their expected familiarity with its features, and how their level of knowledge may impact usage.&#x20;

| Role    | Description                                                                           | Expected Knowledge                                                                       |
| ------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Student | Registered students of the university who use the platform for commuting and parking. | Familiar with mobile/web apps; basic understanding of ride-sharing and parking systems.  |
| Staff   | Faculty and administrative staff of the university who commute to campus.             | Moderate understanding of the platform features; can use carpooling and parking tools.   |
| Guest   | Visitors or external individuals accessing campus with temporary parking needs.       | Limited system knowledge; guided access to parking functions through a simplified UI.    |
| Admin   | System administrators who oversee operations, analytics, and user management.         | High proficiency in backend management, user account handling, and data reporting tools. |

Table 1.2: User Characteristics&#x20;

---

## 1.3.4 Limitations

The Campus Ride-Sharing and Parking Integration System faces several limitations that may affect its performance, usability, and scalability. These limitations stem from technical dependencies, real-time data reliability, access restrictions, and adoption challenges. The key limitations are as follows:&#x20;

* **Dependency on Real-Time Data Accuracy**
  The effectiveness of the ride-sharing and smart parking features heavily relies on the accuracy and timeliness of real-time data (e.g., GPS, parking availability). Any delays or inconsistencies in data feeds can negatively impact user experience and trust.

* **Integration Constraints with University Infrastructure**
  Integration with university authentication systems, campus maps, and databases may be subject to institutional access policies and technical limitations. Incompatibility or restricted access could hinder full functionality.

* **Limited Mobile Accessibility**
  The system is primarily web-based and does not currently support native mobile applications. This may reduce convenience for users who prefer mobile apps for on-the-go commuting and parking interactions.

* **User Adoption and Behavioral Change**
  The success of ride-sharing features depends on user willingness to share rides and coordinate with others. Cultural or personal preferences may limit adoption, requiring awareness campaigns and incentives.

* **Scalability for Multi-Campus Deployment**
  While designed for campus-wide use, scaling the system to additional campuses or institutions may require custom configurations, added infrastructure, and policy alignment, potentially increasing complexity and maintenance effort.

* **Privacy and Security Considerations**
  Handling sensitive user data such as location, vehicle, and trip history demands strict data protection measures. Ensuring privacy and security compliance with university policies and legal standards is critical but challenging.

---

## 1.4 Definitions

Below are terms, phrases and words used in the document and their related definitions:&#x20;

| Terms                                              | Definition                                                                                                                                  |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Campus Ride-Sharing and Parking Integration System | A web-based platform that enables university students, staff, and guests to coordinate ride-sharing and smart parking activities on campus. |
| Carpooling                                         | A transportation service where users can offer or join rides with others traveling along the same route.                                    |
| Smart Parking                                      | A system that allows users to view real-time parking availability, reserve parking spots, and check parking status on campus.               |
| User                                               | Any individual who interacts with the system, including students, staff, guests, and administrators.                                        |
| Student                                            | An end user enrolled at the university who uses the system to access ride-sharing and parking services.                                     |
| Staff                                              | University employees who can also access ride-sharing and parking services, similar to students.                                            |
| Guest                                              | External users who can access limited parking features through guest login.                                                                 |
| Admin                                              | A user with administrative rights to manage system users, review reports, and monitor usage analytics.                                      |
| Authentication Server                              | An external service used to verify user credentials and manage secure access to the platform.                                               |
| Real-Time Parking Data                             | Dynamic data that reflects the current availability of parking spots across campus.                                                         |
| Reporting Feature                                  | A feature that allows users to report incidents or request assistance during carpooling activities.                                         |
| System Dashboard                                   | The interface used by administrators to view analytics, manage content, and respond to user issues.                                         |

Table 1.3: Definition&#x20;

---

## 2.0 Reference

Alotaibi, E., & Perwej, Y. (2021). A Smart Parking System Using IoT and Cloud-Based Services. International Journal of Advanced Computer Science and Applications (IJACSA), 12(1), 402–409. doi:10.14569/IJACSA.2021.0120152
Abusair, S., Khan, R. Z., & Mian, M. A. (2020). Smart Campus Mobility: A Conceptual Model for Ride-Sharing and Parking Management. 2020 5th International Conference on Computing, Communication and Security (ICCCS), 1–6. doi:10.1109/ICCCS49678.2020.9277569
Raghunandan, N., & Kalaimani, R. (2018). Efficient Parking Management System Using Cloud and IoT. International Journal of Engineering & Technology, 7(2.33), 287–290. doi:10.14419/ijet.v7i2.33.14393
Li, C., & Zheng, S. (2022). Smart Transportation Systems for University Campuses: Integrating Ride-Sharing and Parking Solutions. IEEE Access, 10, 114327–114339. doi:10.1109/ACCESS.2022.3212984
Wang, X., & Wang, S. (2019). Optimization of University Campus Parking Based on Real-Time Data. Journal of Urban Transport, 25(4), 89–97. doi:10.1007/s12469-019-00255-6
OpenAI. (2024). Campus Ride-Sharing & Parking User Survey Form. Retrieved from [https://docs.google.com/forms/d/e/1FAIpQLSeXYZ1234SampleCampusForm](https://docs.google.com/forms/d/e/1FAIpQLSeXYZ1234SampleCampusForm)

---

## 3.0 Requirements

The following sections specify the functional, performance, usability, interface, database, design, and support requirements for the Campus Ride-Sharing and Parking Integration System. Each requirement is identified, described, and—where applicable—assigned a priority or other attribute to guide implementation and verification.

---

## 3.1 Functions

This section describes the primary functions of the system, organized by use case, sequence diagrams, and the detailed scenarios for each user role.

### 3.1.1 Use case

This is the overall use case diagram that shows all use cases for all actors.

Figure 3.1: Use Case Diagram of Campus Ride-Sharing and Parking Integration System

#### 3.1.1.1 Student

Figure 3.2: Use Case Diagram of Actor (Student)

| Use Case ID | Use Case Name                    | Description                                                            |
| ----------- | -------------------------------- | ---------------------------------------------------------------------- |
| REQ\_UCS001 | Login and Logout                 | Allows student to securely log in and out using university credentials |
| REQ\_UCS002 | Create Ride Offer                | Allows student to create a carpooling trip offer                       |
| REQ\_UCS003 | Join Ride                        | Allows student to join available ride offers                           |
| REQ\_UCS004 | View Recommended Routes          | Shows best-matched carpooling routes based on preferences              |
| REQ\_UCS005 | Manage Trip Schedule and History | Enables student to view, edit, or cancel rides and view history        |
| REQ\_UCS006 | Report Feature                   | Allows student to send alerts or reports for security and complaints   |
| REQ\_UCS007 | View Real-time Parking           | Displays available parking spots in real time                          |
| REQ\_UCS008 | Reserve Parking Spot             | Enables student to book parking space before arrival                   |
| REQ\_UCS009 | Check Parking Status             | Allows student to view parking reservation details                     |

#### 3.1.1.2 Staff

Figure 3.3: Use Case Diagram of Actor (Staff)

| Use Case ID | Use Case Name                    | Description                                                          |
| ----------- | -------------------------------- | -------------------------------------------------------------------- |
| REQ\_UCT001 | Login and Logout                 | Allows staff to securely log in and out using university credentials |
| REQ\_UCT002 | Create Ride Offer                | Allows staff to create a carpooling trip offer                       |
| REQ\_UCT003 | Join Ride                        | Allows staff to join available ride offers                           |
| REQ\_UCT004 | View Recommended Routes          | Shows best-matched carpooling routes based on preferences            |
| REQ\_UCT005 | Manage Trip Schedule and History | Enables staff to view, edit, or cancel rides and view history        |
| REQ\_UCT006 | Report Feature                   | Allows staff to send alerts or reports for security and complaints   |
| REQ\_UCT007 | View Real-time Parking           | Displays available parking spots in real time                        |
| REQ\_UCT008 | Reserve Parking Spot             | Enables staff to book parking space before arrival                   |
| REQ\_UCT009 | Check Parking Status             | Allows staff to view parking reservation details                     |

#### 3.1.1.3 Guest

| Use Case ID | Use Case Name          | Description                                                                 |
| ----------- | ---------------------- | --------------------------------------------------------------------------- |
| REQ\_UCG001 | Guest Login/Log Out    | Allows guest to log in or log out anonymously or with temporary credentials |
| REQ\_UCG002 | View Real-time Parking | Allows guest to see current available parking spaces                        |
| REQ\_UCG003 | Reserve Parking Spot   | Enables guest to reserve parking space                                      |
| REQ\_UCG004 | Check Parking Status   | Allows guest to check status of reserved parking                            |

#### 3.1.1.4 Admin

| Use Case ID | Use Case Name               | Description                                              |
| ----------- | --------------------------- | -------------------------------------------------------- |
| REQ\_UCA001 | Admin Login/Log out         | Allows admin to securely log in or log out to the system |
| REQ\_UCA002 | Manage User Accounts        | Enables admin to create, edit, or delete user accounts   |
| REQ\_UCA003 | Review Reports & Complaints | Admin reviews submitted complaints                       |
| REQ\_UCA004 | Access Carpooling Data      | Admin views and manages carpooling-related records       |
| REQ\_UCA005 | Access Parking Data         | Admin views and manages parking-related records          |

---

### 3.1.2 Sequence Diagram

#### 3.1.2.1 Login and Logout with University Credentials (Student and Staff）

**Figure 3.6: Login and Logout with University Credentials**

| Field             | Description                                                        |
| ----------------- | ------------------------------------------------------------------ |
| **ID**            | REQSQ001                                                           |
| **Feature**       | Login and Logout with University Credentials                       |
| **Version**       | 1.0                                                                |
| **Purpose**       | To allow students, staff, and admins to securely access the system |
| **Actor**         | Student / Staff                                                    |
| **Precondition**  | User must have valid university credentials                        |
| **Postcondition** | User is authenticated and redirected to the system dashboard       |
| **Main Flow**     | 1. User navigates to login page                                    |

2. System displays login form
3. User submits credentials
4. System authenticates credentials
5. On success, user is redirected to dashboard                                          |
   \| **Alternate Scenario** | 1. If credentials are invalid, system displays an error
6. If fields are empty, system prompts for required input                                              |

*Table 3.5: Login and Logout with University Credentials*&#x20;

#### 3.1.2.2 Guest Login/Logout (Guest）

**Figure 3.7: Guest Login and Logout**

| Field             | Description                                                             |
| ----------------- | ----------------------------------------------------------------------- |
| **ID**            | REQSQ002                                                                |
| **Feature**       | Guest Login and Logout                                                  |
| **Version**       | 1.0                                                                     |
| **Purpose**       | To allow guests to access parking services without credentials          |
| **Actor**         | Guest                                                                   |
| **Precondition**  | Guest navigates to guest login page                                     |
| **Postcondition** | Guest is granted temporary access and redirected to the guest dashboard |
| **Main Flow**     | 1. Guest clicks “Guest Login”                                           |

2. System creates guest session
3. System redirects to dashboard                                              |
   \| **Alternate Scenario** | 1. If session creation fails, system displays an error                                              |

*Table 3.6: Guest Login and Logout*&#x20;

#### 3.1.2.3 Create Ride Offer (Student and Staff）

**Figure 3.8: Create Ride Offer**

| Field             | Description                                                      |
| ----------------- | ---------------------------------------------------------------- |
| **ID**            | REQSQ003                                                         |
| **Feature**       | Create Ride Offer                                                |
| **Version**       | 1.0                                                              |
| **Purpose**       | To allow users to create and publish a new carpooling ride offer |
| **Actor**         | Student / Staff                                                  |
| **Precondition**  | User must be logged in                                           |
| **Postcondition** | New ride offer is saved and listed in user's trip history        |
| **Main Flow**     | 1. User clicks "Carpooling Service"                              |

2. System opens Carpool Dashboard
3. User clicks "Create Ride"
4. System shows ride creation form
5. User fills and submits
6. System validates and saves
7. System confirms and redirects                  |
   \| **Alternate Scenario** | 1. If required fields are missing, system prompts user
8. If DB save fails, system shows error                                                |

*Table 3.7: Create Ride Offer*&#x20;

#### 3.1.2.4 Join Ride (Student and Staff）

**Figure 3.9: Join Ride**

| Field             | Description                                                             |
| ----------------- | ----------------------------------------------------------------------- |
| **ID**            | REQSQ005                                                                |
| **Feature**       | View Recommended Matches and Routes (as part of Join Ride)              |
| **Version**       | 1.0                                                                     |
| **Purpose**       | To provide users with personalized carpool matches and suggested routes |
| **Actor**         | Student / Staff                                                         |
| **Precondition**  | User is logged in and clicks "Join Ride"                                |
| **Postcondition** | User sees best-matched rides with optimized routes                      |
| **Main Flow**     | 1. User clicks "Carpooling Service"                                     |

2. System opens Carpool Dashboard
3. User clicks "Join Ride"
4. System fetches ride data and preferences
5. Mapping API is called
6. Results are matched and displayed                          |
   \| **Alternate Scenario** | 1. If no matches, system shows “No recommended rides”
7. If API fails, system shows default results                                               |

*Table 3.8: Join Ride*&#x20;

##### 3.1.2.5 View Recommended Matches and Routes (Student and Staff）

*Figure 3.10: View Recommended Matches and Routes*

| Field                  | Description                                                                                                                                                                               |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ005                                                                                                                                                                                  |
| **Feature**            | View Recommended Matches and Routes                                                                                                                                                       |
| **Version**            | 1.0                                                                                                                                                                                       |
| **Purpose**            | To provide users with personalized carpool matches and suggested routes                                                                                                                   |
| **Actor**              | Student / Staff                                                                                                                                                                           |
| **Precondition**       | User must be logged in with stored preferences or past ride data                                                                                                                          |
| **Postcondition**      | User views best-matched rides with optimized routes                                                                                                                                       |
| **Main Flow**          | 1. User opens “Recommended Matches and Routes”<br>2. System fetches ride data and preferences<br>3. System calls mapping API<br>4. System matches results<br>5. Recommendations displayed |
| **Alternate Scenario** | 1. If no matches, system shows “No recommended rides”<br>2. If route API fails, system shows limited results                                                                              |

Table 3.9: View Recommended Matches and Routes

##### 3.1.2.6 Manage Trip Schedule and History (Student and Staff）

*Figure 3.11: Manage Trip Schedule and History*

| Field                  | Description                                                                                                                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ID**                 | REQSQ006                                                                                                                                                                                         |
| **Feature**            | Manage Trip Schedule and History                                                                                                                                                                 |
| **Version**            | 1.0                                                                                                                                                                                              |
| **Purpose**            | To allow users to view, edit, or cancel their trips and access trip history                                                                                                                      |
| **Actor**              | Student / Staff                                                                                                                                                                                  |
| **Precondition**       | User must be logged in and have trip data (created via ride offer) in the system                                                                                                                 |
| **Postcondition**      | User views trip history or updated future trip details                                                                                                                                           |
| **Main Flow**          | 1. User logs in<br>2. Clicks “Carpooling Service”<br>3. Enters “Manage / History” page<br>4. System loads trips<br>5. Trips displayed<br>6. User edits/cancels<br>7. System updates and confirms |
| **Alternate Scenario** | 1. If DB fails, system shows error<br>2. If no trips, system shows empty state                                                                                                                   |

Table 3.10: Manage Trip Schedule and History

##### 3.1.2.7 Report Feature (Student and Staff）

*Figure 3.12: Report Feature*

| Field                  | Description                                                                                                                                                                                                                                                                                                                                                                                                         |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ007                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Feature**            | Report Feature                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Version**            | 1.0                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Purpose**            | To allow users to submit reports regarding issues or complaints                                                                                                                                                                                                                                                                                                                                                     |
| **Actor**              | Student / Staff                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Precondition**       | User is logged in and accesses the Report/Feedback page from Carpooling Dashboard                                                                                                                                                                                                                                                                                                                                   |
| **Postcondition**      | Report is submitted and stored in the database; user receives confirmation                                                                                                                                                                                                                                                                                                                                          |
| **Main Flow**          | 1. User logs in<br>2. User clicks “Carpooling Service”<br>3. User clicks “Manage History”<br>4. System displays Report / Feedback page<br>5. User clicks “Report” button<br>6. System displays the Report form<br>7. User fills in the report details and clicks Submit<br>8. System validates the input fields<br>9. System stores the report in the database<br>10. System shows confirmation message to the user |
| **Alternate Scenario** | • If required fields are empty, the system prompts the user to complete all mandatory fields<br>• If submission fails due to a system error, an error message is displayed                                                                                                                                                                                                                                          |

Table 3.7: Report Feature&#x20;

##### 3.1.2.8 View Real-time Parking Availability (Except Admin)

*Figure 3.13: View Real-time Parking Availability*

| Field                  | Description                                                                                                                                            |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ID**                 | REQSQ008                                                                                                                                               |
| **Feature**            | View Real-time Parking Availability                                                                                                                    |
| **Version**            | 1.0                                                                                                                                                    |
| **Purpose**            | To allow users to view current availability of parking slots                                                                                           |
| **Actor**              | Student / Staff / Guest                                                                                                                                |
| **Precondition**       | User is logged in (or guest accessed) and navigates to the Smart Parking page                                                                          |
| **Postcondition**      | System displays updated parking availability                                                                                                           |
| **Main Flow**          | 1. User clicks “Smart Parking” on dashboard<br>2. System requests real-time data<br>3. Parking DB returns status<br>4. System displays available slots |
| **Alternate Scenario** | 1. If parking DB is unavailable, system shows error<br>2. If no slots available, system shows “Full” message                                           |

Table 3.8: View Real-time Parking Availability&#x20;

##### 3.1.2.9 Reserve Parking Spot (Except Admin)

*Figure 3.14: Reserve Parking Spot*

| Field                  | Description                                                                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ009                                                                                                                                          |
| **Feature**            | Reserve Parking Spot                                                                                                                              |
| **Version**            | 1.0                                                                                                                                               |
| **Purpose**            | To allow users to check and confirm their reserved parking spot                                                                                   |
| **Actor**              | Student / Staff / Guest                                                                                                                           |
| **Precondition**       | User is logged in (or guest accessed) and has made a reservation                                                                                  |
| **Postcondition**      | User sees reservation details or system notifies of no reservation                                                                                |
| **Main Flow**          | 1. User clicks “Smart Parking”<br>2. System checks for reservation<br>3. Reservation status returned<br>4. System displays confirmation or prompt |
| **Alternate Scenario** | 1. If no reservation, system shows “No reservation made”<br>2. If DB fails, system shows error                                                    |

Table 3.9: Reserve Parking Spot&#x20;

##### 3.1.2.10 Check Parking Status (Except Admin)

*Figure 3.15: Check Parking Status*

| Field                  | Description                                                                                                                                  |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ010                                                                                                                                     |
| **Feature**            | Check Parking Status                                                                                                                         |
| **Version**            | 1.0                                                                                                                                          |
| **Purpose**            | To allow users to check their current parking usage status                                                                                   |
| **Actor**              | Student / Staff / Guest                                                                                                                      |
| **Precondition**       | User is logged in (or guest accessed) and has previously reserved a parking slot                                                             |
| **Postcondition**      | System displays real-time status of the user’s parking slot                                                                                  |
| **Main Flow**          | 1. User clicks “Smart Parking”<br>2. System checks current status of parking slot<br>3. Status is returned<br>4. User views real-time status |
| **Alternate Scenario** | 1. If no reservation found, system shows “No active parking”<br>2. If DB fails, system shows error                                           |

Table 3.10: Check Parking Status&#x20;

##### 3.1.2.11 Admin Login

*Figure 3.16: Admin Login*

| Field                  | Description                                                                                                     |
| ---------------------- | --------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ011                                                                                                        |
| **Feature**            | Admin Login                                                                                                     |
| **Version**            | 1.0                                                                                                             |
| **Purpose**            | To allow administrators to securely access the system via login credentials                                     |
| **Actor**              | Admin                                                                                                           |
| **Precondition**       | Admin has a valid account and accesses the login page                                                           |
| **Postcondition**      | Admin is redirected to the admin dashboard upon successful login                                                |
| **Main Flow**          | 1. Admin enters credentials<br>2. System validates credentials<br>3. If valid, admin is redirected to dashboard |
| **Alternate Scenario** | 1. If credentials are invalid, system shows error message                                                       |

Table 3.11: Admin Login&#x20;

##### 3.1.2.12 Access Carpooling Data & Review Reports and Complaints (Admin)

*Figure 3.17: Access Carpooling Data & Review Reports and Complaints*

| Field                  | Description                                                                                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ012                                                                                                                                                       |
| **Feature**            | Access Carpooling Data & Review Reports and Complaints                                                                                                         |
| **Version**            | 1.0                                                                                                                                                            |
| **Purpose**            | To allow admins to view carpooling data and access detailed reports and complaints                                                                             |
| **Actor**              | Admin                                                                                                                                                          |
| **Precondition**       | Admin must be logged in and access the admin dashboard                                                                                                         |
| **Postcondition**      | Carpooling data is displayed; reports and complaints are accessible after clicking feedback button                                                             |
| **Main Flow**          | 1. Admin clicks “Carpooling Data & Feedback”<br>2. System loads carpooling data<br>3. Admin clicks “Feedback” button<br>4. System loads reports and complaints |
| **Alternate Scenario** | 1. If data retrieval fails, system shows error message                                                                                                         |

Table 3.12: Access Carpooling Data & Review Reports and Complaints&#x20;

##### 3.1.2.12B Review Reports and Complaints (Admin)

*Figure 3.18: Review Reports and Complaints*

| Field                  | Description                                                                                                                              |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ012B                                                                                                                                |
| **Feature**            | Review Reports and Complaints                                                                                                            |
| **Version**            | 1.0                                                                                                                                      |
| **Purpose**            | To allow admins to review user-submitted reports and complaints                                                                          |
| **Actor**              | Admin                                                                                                                                    |
| **Precondition**       | Admin must be logged in and access the admin dashboard                                                                                   |
| **Postcondition**      | Reports and complaints list is displayed after clicking the feedback button                                                              |
| **Main Flow**          | 1. Admin clicks “Carpooling Data & Feedback”<br>2. Admin clicks “Feedback” button<br>3. System loads and displays reports and complaints |
| **Alternate Scenario** | 1. If data retrieval fails, system shows error message                                                                                   |

Table 3.13: Review Reports and Complaints&#x20;

##### 3.1.2.14 Manage User Accounts (Admin)

*Figure 3.19: Manage User Accounts*

| Field                  | Description                                                                                                                                           |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ013                                                                                                                                              |
| **Feature**            | Manage User Accounts                                                                                                                                  |
| **Version**            | 1.0                                                                                                                                                   |
| **Purpose**            | To allow admin to view, add, edit, or delete user accounts                                                                                            |
| **Actor**              | Admin                                                                                                                                                 |
| **Precondition**       | Admin must be logged in and have accessed the admin dashboard                                                                                         |
| **Postcondition**      | User accounts data is displayed and admin can manage accounts                                                                                         |
| **Main Flow**          | 1. Admin logs in and enters admin dashboard<br>2. System loads user accounts<br>3. Admin edits/adds/deletes user<br>4. System updates DB and confirms |
| **Alternate Scenario** | 1. If database fails, system shows error message                                                                                                      |

Table 3.14: Manage User Accounts&#x20;

##### 3.1.2.15 Access Parking Data (Admin)

*Figure 3.20: Access Parking Data*

| Field                  | Description                                                                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | REQSQ014                                                                                                                                          |
| **Feature**            | Access Parking Data                                                                                                                               |
| **Version**            | 1.0                                                                                                                                               |
| **Purpose**            | To allow admin to view parking usage data and statistics                                                                                          |
| **Actor**              | Admin                                                                                                                                             |
| **Precondition**       | Admin must be logged in and access the admin dashboard                                                                                            |
| **Postcondition**      | Parking data is displayed to the admin                                                                                                            |
| **Main Flow**          | 1. Admin logs in and accesses admin dashboard<br>2. Admin clicks “Parking Data”<br>3. System retrieves parking data<br>4. Data displayed to admin |
| **Alternate Scenario** | 1. If database fails, system shows error message                                                                                                  |

Table 3.15: Access Parking Data&#x20;

---

#### 3.2 Performance Requirements

This section defines the performance and quality expectations for the Campus Ride-Sharing and Parking Integration System. These requirements ensure the system delivers a responsive, stable, and scalable user experience under different load conditions.

| Requirement ID | Description                                                                                                  | Priority |
| -------------- | ------------------------------------------------------------------------------------------------------------ | -------- |
| REQ\_P001      | The system shall respond to user interactions (e.g., booking, joining a ride) within 0 to 3 seconds.         | High     |
| REQ\_P002      | The platform shall support up to 5,000 concurrent users without performance degradation.                     | High     |
| REQ\_P003      | The system shall ensure 99.9% uptime availability excluding scheduled maintenance periods.                   | High     |
| REQ\_P004      | Real-time parking data shall be retrieved and displayed within 2 seconds.                                    | Medium   |
| REQ\_P005      | The system shall process up to 100,000 ride-sharing and parking transactions daily without performance loss. | High     |
| REQ\_P006      | User dashboards and trip/parking history shall load within 1 second.                                         | Medium   |
| REQ\_P007      | Ride creation, join requests, and parking reservations shall be processed in under 1 second.                 | High     |
| REQ\_P008      | The system shall maintain database transaction latency below 100 ms.                                         | Medium   |
| REQ\_P009      | The system shall support horizontal scaling to handle growth in users and data.                              | High     |
| REQ\_P010      | The system shall maintain a crash rate of less than 1 crash per 10,000 sessions.                             | Medium   |
| REQ\_P011      | Administrative reports and analytics shall be generated within 5 seconds of request.                         | Medium   |
| REQ\_P012      | The system shall perform automatic backups with a maximum data loss window of 1 hour.                        | High     |
| REQ\_P013      | Real-time ride and parking notifications shall be delivered to users within 1 second.                        | High     |
| REQ\_P014      | The system shall use load balancing techniques to efficiently distribute user requests across servers.       | High     |
| REQ\_P015      | Secure communications shall use encryption with a processing delay of less than 50 ms.                       | Medium   |

Table 3.1: Performance Requirements

---

#### 3.3 Usability Requirements

These requirements aim to enhance user satisfaction by providing a smooth, intuitive, and accessible experience for all users.

| Requirement ID | Description                                                                                                                     | Priority |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------- | -------- |
| REQ\_UR001     | The system shall provide a seamless login experience using university credentials or guest access.                              | High     |
| REQ\_UR002     | The interface shall display relevant real-time updates such as parking availability and ride offers.                            | Medium   |
| REQ\_UR003     | Users shall be able to share their ride details or parking bookings with others through a unique shareable link.                | High     |
| REQ\_UR004     | The platform shall include a notification system to alert users of trip changes, new ride matches, or parking status updates.   | Medium   |
| REQ\_UR005     | The interface shall offer a clean, responsive, and intuitive design to minimize user confusion and cognitive load.              | High     |
| REQ\_UR006     | The admin dashboard shall provide usage analytics and feedback summaries from users regarding ride and parking experiences.     | Medium   |
| REQ\_UR007     | The platform shall integrate with campus services (e.g., maps, timetable systems) for enhanced navigation and scheduling.       | High     |
| REQ\_UR008     | Users shall be able to customize their dashboard to show preferred features such as parking status or trip history.             | Low      |
| REQ\_UR009     | The platform shall provide onboarding tutorials and tooltips to guide first-time users through core features.                   | Medium   |
| REQ\_UR010     | The platform shall protect user data during all interactions, especially during login and trip/parking sharing.                 | High     |
| REQ\_UR011     | The platform shall be fully mobile-friendly and responsive, ensuring smooth use on smartphones and tablets.                     | High     |
| REQ\_UR012     | The system shall offer a feedback form where users can report issues or suggest improvements for usability.                     | Medium   |
| REQ\_UR013     | Users shall be able to tag co-riders or carpool buddies in ride details for better coordination.                                | Low      |
| REQ\_UR014     | The platform shall include accessibility features such as screen reader compatibility, color contrast, and keyboard navigation. | High     |
| REQ\_UR015     | The system shall be regularly updated to maintain compatibility with browsers and device operating systems.                     | Medium   |

Table 3.2: Usability Requirements

---

#### 3.4 Interface Requirements

**3.4.1 System Interfaces**
The system interfaces with several subsystems and external services to enable authentication, ride-sharing, parking management, notifications, and mapping APIs.

| Interface ID | System Name               | Description                                                               | Details                                                                   |
| ------------ | ------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| REQ\_SI001   | Authentication Server     | Handles login and access control for students, staff, guests, and admins  | Supports university SSO and guest login via OAuth 2.0, JWT                |
| REQ\_SI002   | Carpooling Server         | Manages ride creation, joining, scheduling, reporting & admin data access | APIs for ride offer, match recommendations, trip history, and report data |
| REQ\_SI003   | Parking Management Server | Manages smart parking, admin usage logs, and parking analytics            | Provides real-time data, reservations, and logs accessible by admin       |
| REQ\_SI004   | Notification Service      | Sends alerts to users across all roles including report and admin use     | API integration with email/SMS (e.g., SendGrid, Twilio)                   |
| REQ\_SI005   | Map & Route API           | Recommends optimal carpool routes                                         | Connects to map services (e.g., Google Maps) for location and routing     |

Table 3.3: System Interfaces

**3.4.2 User Interfaces**
Design principles adhere to MMU branding and dashboard style for clarity, accessibility, and consistency.

| Module ID  | Description                                                                                                                                | Priority |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
| REQ\_UI001 | The overall GUI uses a primary white content background, with light gray panels (#D3D3D3) for sidebars and subtle shadowed containers.     | High     |
| REQ\_UI002 | The left sidebar layout is persistent across all pages, using black icons with dark gray labels (#333333) in Roboto, size 14pt.            | High     |
| REQ\_UI003 | The system font family is Roboto for all interface text and Roboto Slab for headers or section titles.                                     | Medium   |
| REQ\_UI004 | Text colors follow a consistent theme: Dark Gray (#333333) for body text, and White (#FFFFFF) when displayed over colored buttons or bars. | High     |
| REQ\_UI005 | Font sizes are structured for readability: 14pt minimum, 16pt standard text, 20pt subtitles, and 32pt section headers.                     | High     |
| REQ\_UI006 | Font weight is medium (500) for general content and bold for headers and actionable elements (e.g., button text, section titles).          | High     |
| REQ\_UI007 | Buttons are color-coded by function: Bright Blue (#007BFF) for primary actions (e.g., Edit, Logout), Red (#FF4136) for Delete/warnings.    | Medium   |
| REQ\_UI008 | Buttons use white text, have slightly rounded corners, and consistent padding with hover feedback (slight shade or pointer change).        | Medium   |
| REQ\_UI009 | Tables are styled with no outer borders, clear column headers, and use padding and spacing to separate content for clean visibility.       | High     |
| REQ\_UI010 | Icons and labels in navigation menus are vertically aligned, maintain equal spacing, and ensure usability even on mid-sized screens.       | Medium   |
| REQ\_UI011 | The top navigation bar includes user role display, a Logout button styled in blue (#007BFF), and an icon for intuitive access.             | High     |
| REQ\_UI012 | All interfaces are designed for desktop resolution first, with flexible layout containers that prevent horizontal scrolling.               | Medium   |

Table 3.4: User Interfaces&#x20;

**3.4.3 Hardware Interfaces**
Minimum device specifications to ensure smooth operation across desktops, laptops, tablets, and smartphones.

| Interface ID | Description                                                                                                                              |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| REQ\_HI001   | The processor of the device shall be at least a 64-bit processor (e.g., Intel Core i3 or equivalent) for optimal performance             |
| REQ\_HI002   | The device shall have a minimum of 4GB RAM to support multitasking and real-time data processing                                         |
| REQ\_HI003   | The device shall have at least 2GB of free storage space to accommodate application data and cache                                       |
| REQ\_HI004   | The device must support internet connectivity via Ethernet, Wi-Fi, or mobile data networks to enable real-time updates and communication |

Table 3.5: Hardware Interfaces Requirements

**3.4.4 Software Interfaces**
Dependencies on operating systems, browsers, database, server runtime, and API frameworks.

| ID         | Category         | Name              | Version Number                        | Purpose                                                                                | Reference                    |
| ---------- | ---------------- | ----------------- | ------------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------- |
| REQ\_SI001 | Operating System | Microsoft Windows | Windows 10 or later                   | Software platform managing device hardware and resources to support system execution   | Microsoft Official Page      |
|            |                  | macOS             | macOS Mojave 10.14 or later           |                                                                                        | Apple Official Page          |
|            |                  | Linux             | Ubuntu 20.04+, Debian 11+, Fedora 40+ |                                                                                        | Linux Distribution Pages     |
|            |                  | iOS               | iOS 15.0 or later                     |                                                                                        | Apple Official Page          |
|            |                  | Android           | Android 10.0 or later                 |                                                                                        | Android Official Page        |
| REQ\_SI002 | Browser          | Google Chrome     | 124.0.6367.159                        | Used by end users to access the web application and communicate with the server        | Chrome Official Page         |
|            |                  | Microsoft Edge    | 124.0.2478.80                         |                                                                                        | Microsoft Edge Official Page |
|            |                  | Safari            | 16.6.1                                |                                                                                        | Safari Official Page         |
| REQ\_SI003 | Database         | MySQL             | 8.0 or later                          | Database system used to store and manage data for users, trips, parking, and analytics | MySQL Official Page          |
| REQ\_SI004 | Backend Server   | Node.js           | 18.x or later                         | Server runtime environment for handling API requests and business logic                | Node.js Official Page        |
| REQ\_SI005 | API Framework    | Express.js        | 4.x                                   | Framework for building RESTful APIs to support client-server communication             | Express Official Page        |

Table 3.6: Software Interfaces

**3.4.5 Communications Interfaces**
Protocols and methods used for secure and real-time communication with external systems.

| Interface ID | Description                                                                                                      | Protocols / Methods     | Priority |
| ------------ | ---------------------------------------------------------------------------------------------------------------- | ----------------------- | -------- |
| REQ\_CI001   | The system shall support HTTP/HTTPS protocols for secure web communication                                       | HTTP/HTTPS              | High     |
| REQ\_CI002   | The system shall integrate with university authentication services for user login (e.g., SAML, OAuth 2.0)        | SAML, OAuth 2.0         | High     |
| REQ\_CI003   | The system shall use WebSocket protocol for real-time updates, notifications, and ride matching                  | WebSocket               | Medium   |
| REQ\_CI004   | The system shall support SMTP for sending emails to users for notifications, booking confirmations, and alerts   | SMTP                    | Medium   |
| REQ\_CI005   | The system shall support integration with campus LDAP or Active Directory for user authentication and management | LDAP / Active Directory | High     |
| REQ\_CI006   | The system shall support secure file transfer protocol (SFTP) for exchanging files with external systems         | SFTP                    | Medium   |
| REQ\_CI007   | The system shall ensure response time for ride offer posting and updates to be under 1 second                    | MQTT                    | Low      |
| REQ\_CI008   | The system shall enable data exchange with external databases through JDBC/ODBC connections                      | JDBC / ODBC             | Medium   |
| REQ\_CI009   | The system shall support JSON and XML data formats for data interchange between clients and servers              | JSON, XML               | High     |

Table 1.6: Communications Interfaces&#x20;

---

#### 3.5 Logical Database Requirements

The Entity-Relationship Diagram represents the structure and relationship between the system entities: User (with subtypes Student, Staff, Guest, Admin), RideSharing, Reservation, Report, and ParkingSpot.

*Figure 3.1: Class Diagram*
*Figure 3.2: Entity Relationship Diagram*&#x20;

**3.5.1 User**

| Field Name | Description                                      | Data Type    | Constraints      | Extra Notes                          |
| ---------- | ------------------------------------------------ | ------------ | ---------------- | ------------------------------------ |
| userID     | Unique identifier for each user.                 | Integer (PK) | PK, Not Null     | Used as university login credentials |
| name       | Full name of the user.                           | Varchar (50) | Not Null         | Used as guest login credentials      |
| email      | Email address of the user.                       | Varchar (50) | Unique, Not Null | –                                    |
| password   | Encrypted user password.                         | Varchar (30) | Not Null         | Used as login credentials            |
| role       | Role of the user (student, staff, admin, guest). | Varchar (10) | Not Null         | –                                    |

Table 3.4: User Data Dictionary&#x20;

**3.5.2 Student**

| Field Name | Description                 | Data Type | Constraints                      | Extra Notes |
| ---------- | --------------------------- | --------- | -------------------------------- | ----------- |
| studentID  | Unique ID for student user. | Integer   | PK, FK to User(userID), Not Null | –           |

Table 3.5: Student Data Dictionary&#x20;

**3.5.3 Staff**

| Field Name | Description               | Data Type | Constraints                      | Extra Notes |
| ---------- | ------------------------- | --------- | -------------------------------- | ----------- |
| staffID    | Unique ID for staff user. | Integer   | PK, FK to User(userID), Not Null | –           |

Table 3.6: Staff Data Dictionary&#x20;

**3.5.4 Guest**

| Field Name | Description               | Data Type | Constraints                      | Extra Notes |
| ---------- | ------------------------- | --------- | -------------------------------- | ----------- |
| guestID    | Unique ID for guest user. | Integer   | PK, FK to User(userID), Not Null | –           |

Table 3.7: Guest Data Dictionary&#x20;

**3.5.5 Admin**

| Field Name | Description               | Data Type | Constraints                      | Extra Notes |
| ---------- | ------------------------- | --------- | -------------------------------- | ----------- |
| adminID    | Unique ID for admin user. | Integer   | PK, FK to User(userID), Not Null | –           |

Table 3.8: Admin Data Dictionary&#x20;

**3.5.6 RideSharing**

| Field Name       | Description                            | Data Type | Constraints                  | Extra Notes                         |
| ---------------- | -------------------------------------- | --------- | ---------------------------- | ----------------------------------- |
| rideID           | Unique identifier for each ride.       | Integer   | PK, Not Null                 | –                                   |
| driverID         | ID of the user offering the ride.      | Integer   | Not Null                     | –                                   |
| origin           | Starting location.                     | Varchar   | Not Null                     | –                                   |
| destination      | Destination location.                  | Varchar   | Not Null                     | –                                   |
| time             | Departure time.                        | Datetime  | Not Null                     | –                                   |
| availabilitySeat | Available seats.                       | Integer   | Not Null                     | –                                   |
| userID           | References the user offering the ride. | Integer   | FK to User(userID), Not Null | Used to record who joined this trip |

Table 3.9: RideSharing Data Dictionary&#x20;

**3.5.7 Report**

| Field Name  | Description       | Data Type    | Constraints                         | Extra Notes |
| ----------- | ----------------- | ------------ | ----------------------------------- | ----------- |
| reportID    | Unique report ID. | Integer      | PK, Not Null                        | –           |
| rideID      | Associated ride.  | Integer      | FK to RideSharing(rideID), Not Null | –           |
| submittedBy | Reporting user.   | Varchar (50) | Not Null                            | –           |
| reportType  | Type of report.   | Varchar (20) | Not Null                            | –           |
| content     | Report details.   | Text         | Not Null                            | –           |

Table 3.10: Report Data Dictionary&#x20;

**3.5.8 ParkingSpot**

| Field Name | Description             | Data Type     | Constraints  | Extra Notes |
| ---------- | ----------------------- | ------------- | ------------ | ----------- |
| parkingID  | Unique parking spot ID. | Integer       | PK, Not Null | –           |
| location   | Spot location.          | Varchar (100) | Not Null     | –           |
| status     | Availability status.    | Varchar (10)  | Not Null     | –           |

Table 3.11: ParkingSpot Data Dictionary&#x20;

**3.5.9 Reservation**

| Field Name    | Description            | Data Type    | Constraints                            | Extra Notes |
| ------------- | ---------------------- | ------------ | -------------------------------------- | ----------- |
| reservationID | Unique reservation ID. | Integer      | PK, Not Null                           | –           |
| status        | Reservation status.    | Varchar (10) | Not Null                               | –           |
| userID        | Reserving user.        | Integer      | FK to User(userID), Not Null           | –           |
| parkingID     | Reserved parking spot. | Integer      | FK to ParkingSpot(parkingID), Not Null | –           |

Table 3.12: Reservation Data Dictionary&#x20;

---

#### 3.6 Design Constraints

Design constraints and limitations to be considered during development.

| Requirement ID | Description                                                                                                                                                        | Priority | Author               |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- | -------------------- |
| REQ\_DC001     | The system must comply with Web Content Accessibility Guidelines (WCAG) to ensure usability for all users, including those with disabilities.                      | Medium   | Francis Wong Wei Hou |
| REQ\_DC002     | The system must comply with applicable data protection regulations (GDPR) to protect user data like names, emails, and ride/parking details.                       | High     | Francis Wong Wei Hou |
| REQ\_DC003     | The system must be developed within a 1-year period to meet organizational or campus deployment deadlines.                                                         | High     | Francis Wong Wei Hou |
| REQ\_DC004     | The system must not display or allow any offensive content in ride descriptions, reports, or user profiles.                                                        | Medium   | Francis Wong Wei Hou |
| REQ\_DC005     | The system must use open-source libraries and frameworks approved by the organization.                                                                             | Medium   | Francis Wong Wei Hou |
| REQ\_DC006     | The system must be compatible with major web browsers (Google Chrome, Firefox, Safari, Microsoft Edge) and support mobile devices (iOS and Android).               | High     | Francis Wong Wei Hou |
| REQ\_DC007     | The system must enforce strict role-based access control (Guests can only view parking, Admins can manage accounts) to prevent unauthorized access.                | High     | Francis Wong Wei Hou |
| REQ\_DC008     | The system must integrate with existing campus IT systems (user authentication via SSO, parking databases) without major infrastructure changes.                   | High     | Francis Wong Wei Hou |
| REQ\_DC009     | The system must support real-time updates for parking spot availability and ride-sharing status to ensure accurate information for users.                          | High     | Francis Wong Wei Hou |
| REQ\_DC010     | The system must be designed with a modular architecture to handle an increasing number of users and future feature additions.                                      | High     | Francis Wong Wei Hou |
| REQ\_DC011     | The system must incorporate data encryption for sensitive user data (userID, email, ride details) in transit and at rest, per organizational IT security policies. | High     | Francis Wong Wei Hou |
| REQ\_DC012     | The system must ensure reports submitted by users are reliably logged and immediately accessible to Admins for quick response.                                     | High     | Francis Wong Wei Hou |

Table 3.13: Design Constraints

---

#### 3.7 Software System Attributes

Quality attributes that the system must exhibit.

**3.7.1 Accuracy**

| Requirement ID | Description                                                                             | Priority | Author               |
| -------------- | --------------------------------------------------------------------------------------- | -------- | -------------------- |
| REQ\_SRA001    | The system shall have an error rate of less than 0.0001% in all computational processes | High     | Francis Wong Wei Hou |

Table 3.14: Accuracy&#x20;

**3.7.2 Availability**

| Requirement ID | Description                                                                                           | Priority | Author               |
| -------------- | ----------------------------------------------------------------------------------------------------- | -------- | -------------------- |
| REQ\_SRA002    | The system’s server shall maintain consistent uptime with a maximum of 12 hours of downtime per year. | High     | Francis Wong Wei Hou |

Table 3.15: Availability&#x20;

**3.7.3 Maintainability**

| Requirement ID | Description                                                                                                                                 | Priority | Author               |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------- |
| REQ\_SRA003    | The system shall be designed with modular components to allow updates or bug fixes within 24 hours without affecting other functionalities. | High     | Francis Wong Wei Hou |
| REQ\_SRA004    | The system shall include detailed documentation for all code and processes to facilitate future maintenance by developers.                  | Medium   | Francis Wong Wei Hou |

Table 3.16: Maintainability&#x20;

**3.7.4 Portability**

| Requirement ID | Description                                                                                                                                        | Priority | Author               |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------- |
| REQ\_SRA005    | The system shall operate on multiple platforms (Windows, macOS, Linux for servers; iOS, Android for mobile) without requiring significant changes. | High     | Francis Wong Wei Hou |
| REQ\_SRA006    | The system shall use platform-independent technologies (web-based frontend, REST APIs) to ensure compatibility across environments.                | High     | Francis Wong Wei Hou |

Table 3.17: Portability&#x20;

**3.7.5 Reliability**

| Requirement ID | Description                                                                                            | Priority | Author               |
| -------------- | ------------------------------------------------------------------------------------------------------ | -------- | -------------------- |
| REQ\_SRA007    | The system shall handle a high volume of transactions and concurrent users without crashing.           | High     | Francis Wong Wei Hou |
| REQ\_SRA008    | All transactions shall be recorded accurately, ensuring no data loss or corruption.                    | High     | Francis Wong Wei Hou |
| REQ\_SRA009    | The system shall receive notifications for the success or failure of user actions within the platform. | High     | Francis Wong Wei Hou |

Table 3.18: Reliability&#x20;

**3.7.6 Security**

| Requirement ID | Description                                                                                                                           | Priority | Author               |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------- |
| REQ\_SRA010    | The system shall use encryption (HTTPS, AES-256) for all data transmission to protect user information (userID, email, ride details). | High     | Francis Wong Wei Hou |
| REQ\_SRA011    | The system shall implement secure user authentication to prevent unauthorized access.                                                 | High     | Francis Wong Wei Hou |

Table 3.19: Security&#x20;

**3.7.7 Usability**

| Requirement ID | Description                                                                                                                                          | Priority | Author               |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------- |
| REQ\_SRA012    | The system shall provide an intuitive interface, allowing users to complete tasks (reserving a parking spot, joining a ride) in fewer than 5 clicks. | High     | Francis Wong Wei Hou |
| REQ\_SRA013    | The system shall include a help section or tooltips to assist users in understanding functionalities.                                                | Medium   | Francis Wong Wei Hou |

Table 3.20: Usability&#x20;

---

#### 3.8 Supporting Information

Additional information gathered during requirements elicitation.

**3.8.1 Interview Summary**

> **Participant Profile:**
>
> * Gender: Male
> * Occupation: Student at a private local university
>
> **Project Vision and Scope Understanding**
> **Question:** After reading the vision and scope of this application, please rate 1 to 5 of how much you understand the project objective.
> **Response:** Rating 4
>
> **Expected Functionalities for ride-sharing system (Satisfier)**
> **Question:** What specific functionalities do you expect the ride-sharing system to provide?
> **Response:** User can view the current location of the driver of the trips in order to meet.
>
> **Necessity of ride-sharing history feature (Delighter)**
> **Question:** Do you think ride-sharing history is needed for this application?
> **Response:** Yes. For example, the user can find the specific driver again if he/she wants from ride-sharing history.
>
> **Expected Functionalities for parking system (Satisfier)**
> **Question:** What specific functionalities do you expect the parking system to provide?
> **Response:** System will navigate the driver to available parking slots of the set faculty parking.

**3.8.2 Observation Summary**

* *Overview, User Interface Design, Functionality, Performance Indicators* (detailed in document)
* Key findings include the need for guided tours, campus-specific filters, integrated calendar, and trend analytics.&#x20;

**3.8.3 Prototyping**
Screenshots of prototype pages were presented to stakeholders, including Login, Student/Staff/Guest Dashboards, Carpooling Services, Manage History, Smart Parking Services, and Admin Management pages.&#x20;

---

## 4.0 Verification

This section provides the verification approaches and methods planned to qualify the software of the Campus Ride-Sharing Platform with Parking System Integration. The verification actions are organized in parallel with the functional requirements, performance requirements, security requirements, usability requirements, maintainability requirements, and portability requirements. Each action includes details on how, who, when, and where.&#x20;

### 4.1 Verification Approach

#### 4.1.1 Functional Requirements Verification

| Requirement ID | Method                     | Responsibility | Event-based Timing               | Venue/ Environment          |
| -------------- | -------------------------- | -------------- | -------------------------------- | --------------------------- |
| REQ\_V001      | Unit Testing               | Developers     | During implementation phase      | Developer Environment / IDE |
| REQ\_V002      | System Integration Testing | QA Team        | After integrating system modules | Testing Lab                 |

*Table 4.1: Functional Requirements Verification*&#x20;

#### 4.1.2 Performance Requirements Verification

| Requirement ID | Method         | Responsibility | Event-based Timing                          | Venue/ Environment        |
| -------------- | -------------- | -------------- | ------------------------------------------- | ------------------------- |
| REQ\_V003      | Load Testing   | QA Team        | After system completion                     | Performance Testing Tools |
| REQ\_V004      | Stress Testing | QA Engineers   | Before deployment under peak load scenarios | Performance Lab           |

*Table 4.2: Performance Requirements Verification*&#x20;

#### 4.1.3 Security Requirements Verification

| Requirement ID | Method                 | Responsibility       | Event-based Timing                              | Venue/ Environment                 |
| -------------- | ---------------------- | -------------------- | ----------------------------------------------- | ---------------------------------- |
| REQ\_V005      | Authentication Testing | Security Analyst, QA | After login & role-based access are implemented | Secure Testing Environment         |
| REQ\_V006      | Vulnerability Scanning | Security Team        | Before production release                       | Security Testing Tools / Cloud Lab |

*Table 4.3: Security Requirements Verification*&#x20;

#### 4.1.4 Usability Requirements Verification

| Requirement ID | Method                    | Responsibility          | Event-based Timing                          | Venue/ Environment                 |
| -------------- | ------------------------- | ----------------------- | ------------------------------------------- | ---------------------------------- |
| REQ\_V007      | User Interface Evaluation | UX Designers, End Users | After prototype or beta version development | Usability Lab                      |
| REQ\_V008      | User Feedback Session     | UX Team                 | During user testing or pilot launch         | Online Surveys / Interview Session |

*Table 4.4: Usability Requirements Verification*&#x20;

#### 4.1.5 Maintainability Requirements Verification

| Requirement ID | Method                      | Responsibility        | Event-based Timing                | Venue/ Environment                  |
| -------------- | --------------------------- | --------------------- | --------------------------------- | ----------------------------------- |
| REQ\_V009      | Code Review                 | Development Team Lead | After each development sprint     | Code Repository / Review Tools      |
| REQ\_V010      | Design Documentation Review | Developers, Analysts  | During design validation meetings | Meeting Room / Online Documentation |

*Table 4.5: Maintainability Requirements Verification*&#x20;

#### 4.1.6 Portability Requirements Verification

| Requirement ID | Method                        | Responsibility | Event-based Timing                      | Venue/ Environment          |
| -------------- | ----------------------------- | -------------- | --------------------------------------- | --------------------------- |
| REQ\_V011      | Cross-Platform Testing        | QA Engineers   | Before deploying to multiple OS/devices | Device Lab / Emulator Tools |
| REQ\_V012      | Browser Compatibility Testing | QA Team        | During front-end testing phase          | BrowserStack / Cloud Tools  |

*Table 4.6: Portability Requirements Verification*&#x20;

### 4.2 Verification Criteria

This section shows that the system will be verified based on the following criteria to ensure it meets the defined functional and quality requirements:

| Requirement ID | Requirement/Feature       | Verification Criteria                                                                                                                                                           |
| -------------- | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| REQ\_VC001     | Ride offer creation       | The system shall allow a user to create a ride offer with details like origin, destination, time, and available seats. A successful message is displayed upon valid submission. |
| REQ\_VC002     | Route matching            | When a user searches for a trip, the system must display matched ride offers within a 5 km radius of the user’s specified route.                                                |
| REQ\_VC003     | Parking reservation       | A user must be able to reserve a parking spot only if it is marked as available in the system.                                                                                  |
| REQ\_VC004     | View parking availability | The system must update and display current parking spot status in real-time.                                                                                                    |
| REQ\_VC005     | Report submission         | Users must be able to submit an report while in an active ride, and the system shall record the report linked to the ride ID.                                                   |
| REQ\_VC006     | User authentication       | Login attempts with correct credentials must be authenticated, and users should be redirected based on their roles.                                                             |
| REQ\_VC007     | Access control            | Guests can access only parking-related features; they must not be allowed to view or create ride-sharing offers.                                                                |
| REQ\_VC008     | Performance               | The system shall return search results for ride offers or parking availability within 3 seconds under normal load.                                                              |
| REQ\_VC009     | Usability                 | All primary actions (view parking availability, reserve parking, search ride, join ride, report) must be accessible within 3 clicks from the dashboard.                         |
| REQ\_VC010     | Data Integrity            | A ride offer must not be created without mandatory fields such as origin, destination, time, and seat count.                                                                    |

*Table 4.7: Verification Criteria*&#x20;

---

## 5.0 Assumptions, Dependencies, Acronyms & Abbreviations

### 5.1 Assumptions and Dependencies

**Assumptions:**

* Users (students and staff) have access to a stable internet connection when using the system.
* Users are familiar with basic web applications and can navigate the system without extensive training.
* The system will be accessed primarily via modern desktop or mobile web browsers.
* All registered university users have valid credentials stored in the university authentication system.
* Campus facilities such as parking lots have IoT sensors or manual updates to provide real-time parking data.&#x20;

**Dependencies:**

* The system depends on the university’s authentication server for verifying student and staff logins.
* Real-time parking data depends on integration with campus parking management infrastructure or sensors.
* Accurate GPS functionality depends on the device’s built-in location services and browser support.
* Reporting functionality may rely on integration with campus security systems or alert services.
* Continuous server uptime and hosting infrastructure are required to ensure uninterrupted system access.
* System updates and maintenance depend on cooperation from university IT departments.&#x20;

---

### 5.2 Acronyms and Abbreviations

| Acronym / Abbreviation | Definition                                         |
| ---------------------- | -------------------------------------------------- |
| CRPIS                  | Campus Ride-Sharing and Parking Integration System |
| UI                     | User Interface                                     |
| UX                     | User Experience                                    |
| GPS                    | Global Positioning System                          |
| DB                     | Database                                           |
| API                    | Application Programming Interface                  |
| OTP                    | One-Time Password                                  |
| SSO                    | Single Sign-On                                     |
| HTTPS                  | Hypertext Transfer Protocol Secure                 |
| RTD                    | Real-Time Parking Data                             |
| ERF                    | Reporting Feature                                  |
| ASD                    | Authentication Server                              |
| SD                     | System Dashboard                                   |

Table 5.1&#x20;

---
