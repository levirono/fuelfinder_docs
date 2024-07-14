# FUELFINDER

## 1. Introduction

FUELFINDER is an innovative mobile application meticulously designed to address the pressing issue of fuel shortages, with a particular emphasis on rural areas and stations located far from urban centers. In today's fast-paced world, access to fuel is crucial for both personal and commercial transportation. However, fuel shortages can cause significant disruptions, leading to wasted time, increased costs, and frustration for drivers.

The primary objective of FUELFINDER is to empower drivers by enabling them to locate available fuel stations and track fuel availability in real-time. This capability significantly improves efficiency and reduces inconvenience for users, transforming the often stressful experience of finding fuel into a streamlined, informed process.

The application is built using the Flutter framework and written in Dart language, ensuring cross-platform compatibility and a smooth user experience. By leveraging modern mobile development technologies and real-time data management, FUELFINDER aims to revolutionize the way drivers interact with fuel stations and manage their fueling needs.

### 1.1 Technological Foundation

FUELFINDER is built using cutting-edge mobile development technologies:

- **Frontend**: The application utilizes the Flutter framework, a popular open-source UI software development kit created by Google. Flutter allows for the development of cross-platform applications from a single codebase, ensuring consistency across different devices and operating systems.
- **Programming Language**: The entire application is written in Dart, a client-optimized programming language for fast apps on multiple platforms. Dart's sound type system and null safety features contribute to more robust and maintainable code.

By leveraging these modern technologies, FUELFINDER ensures cross-platform compatibility and delivers a smooth, responsive user experience across various devices and screen sizes.

### 1.2 Key Benefits

FUELFINDER aims to revolutionize the way drivers interact with fuel stations and manage their fueling needs by offering:

1. Real-time fuel availability information
2. Accurate and up-to-date fuel station locations
3. Current fuel pricing data
4. Comprehensive station service information
5. User-friendly interfaces for all stakeholders
6. Efficient fuel station discovery and information dissemination

## 2. System Architecture

The FUELFINDER application is structured around three main dashboards, each catering to a specific user role:

1. Driver Dashboard
2. Admin Dashboard
3. Station Dashboard

This role-based architecture ensures that each user type has access to functionalities relevant to their needs and responsibilities, creating a tailored experience for all stakeholders involved in the fuel management ecosystem.

## 3. Authentication System

### 3.1 Login Page

When users open the application for the first time, they are presented with a login page that includes:

- A carousel displaying basic information about the application, providing users with an overview of its features and benefits
- Login fields for email and password, allowing returning users to access their accounts quickly

### 3.2 Signup Page

For new users, the signup page offers a straightforward process to create an account by providing:

- Email address
- Password
- Role selection (driver or station)

After successful signup, the user's role is saved in the system, ensuring proper access rights and dashboard routing in future sessions.

### 3.3 Role-based Navigation

Upon successful login, the system performs a check of the user's role (driver, station, or admin) and automatically navigates them to the appropriate dashboard. It's worth noting that the admin role is assigned directly from the database to a single user, ensuring centralized control over the application's management features.

### 3.4 Profile Completion

To ensure comprehensive user data and enhance the application's functionality, the system checks if the user's profile is complete before fully loading the dashboard. If the profile is incomplete, a dialog prompts the user to provide the necessary information. Once the profile is completed, the user is automatically navigated to their respective dashboard.

### 3.5 State Persistence

To enhance user experience and reduce friction, the system maintains the state of the user's dashboard. This feature eliminates the need for repeated logins, allowing users to quickly access their personalized information upon reopening the application.

## 4. Driver Dashboard

The Driver Dashboard is designed to provide a comprehensive suite of tools and information for drivers seeking fuel stations. Its main components include:

### 4.1 Fuel Efficiency Dialog

This feature displays one random fuel efficiency tip each time a driver logs in or opens the application. The tip has a delay of about 20 seconds before it displays. These tips can cover a range of topics, from driving habits to vehicle maintenance, providing valuable information to users.

### 4.2 Search Function

The search functionality allows drivers to look for specific routes or fuel station names within their region. This feature enhances the user's ability to plan their trips effectively and locate preferred stations quickly.

### 4.3 Map View

The map view provides a visual representation of the user's surroundings and available fuel stations. Key features of the map view include:

- Real-time centering on the driver's current location and is marked with the marker of their location.
- Display of all registered stations as markers using fuel station icon and station Name below it.
- Zoom capabilities for detailed area exploration
- Information container that appears upon tapping a station marker this container will contain the status of the station which include fuel availability, operation hours and whether it is open or not.
- Search functionality for exploring different regions

### 4.4 List of Fuel Stations

This component provides a comprehensive list of nearby fuel stations, offering the following information:

- Displays fuel stations within a 30 km radius
- Sorted by nearest distance for easy decision-making
- Shows station name, distance, fuel availability, and operational status
- Color-coded fuel availability (red for unavailable, green for available)
- Displays operation hours and 24-hour availability status
- To see all the fuel stations there is a button below the list that will enable you to open a page with all stations.

### 4.5 Station Details Page

Users can access detailed information about a specific station by tapping on it. The Station Details Page includes:

- Comprehensive location information
- Current fuel status
- Up-to-date fuel prices
- List of available services at the station

### 4.6 Profile Page

The Profile Page allows drivers to input and edit their personal information, including:

- Contact details for account management
- Vehicle name and model, driving licence etc.

## 5. Station Dashboard

The Station Dashboard is designed to empower station managers with tools to manage their fuel station's information and services effectively. Its main components include:

### 5.1 Information Carousel

Similar to the Driver Dashboard, this feature provides relevant information and updates for station managers.

### 5.2 Verification Status Panel

This panel displays the current verification status of the station, ensuring transparency in the registration process.

### 5.3 Station Status Toggle

A simple yet crucial feature that allows station managers to quickly toggle their station's status between open and closed, ensuring drivers have accurate information about the station's availability.

### 5.4 Fuel Availability Panels

Separate panels for petrol and diesel allow station managers to update fuel availability in real-time. This feature is critical for providing accurate information to drivers. It utilizes tap functionality where stations can tap to change the availability.

### 5.5 Fuel Price Settings

This component enables station managers to update fuel prices as they change, ensuring that drivers always have access to the most current pricing information.

### 5.6 Available Services Checklist

A comprehensive checklist of services that the station offers, allowing managers to easily update their service offerings as they evolve.

### 5.7 Station Profile

The Station Profile section allows managers to edit key information about their station, including:

- Station name
- Location details
- GPS link
- Operation hours
- Available services
- Etc.

### 5.8 GPS Coordinates

To ensure accurate location data, the Station Dashboard includes:

- A GPS link field for inputting station coordinates
- An integrated map for easy coordinate selection
- Automatic coordinate filling and clipboard copying for convenience

## 6. Admin Dashboard

The Admin Dashboard serves as the central control point for the entire FUELFINDER ecosystem. Its main features include:

### 6.1 Overview Statistics

The dashboard displays the total number of registered fuel stations and drivers, providing a quick snapshot of the application's user base.

### 6.2 Fuel Efficiency Tips Management

Admins can manage the fuel efficiency tips displayed to drivers, including:

- Adding new tips
- Editing existing tips
- Removing outdated or irrelevant tips

### 6.3 User Management

This feature allows admins to oversee both stations and drivers, with capabilities including:

- Viewing all registered users
- Deleting users when necessary
- Verifying stations to ensure the legitimacy of listed fuel stations

### 6.4 Station Verification Process

The admin dashboard includes a robust station verification system:

- Automatic 24-hour system check for new station registrations
- Admin notifications for pending verifications
- Verification button for each station to streamline the process
- Option to delete fake or invalid stations to maintain data integrity

## 7. Database and Backend Architecture

FUELFINDER utilizes Firebase, a Google service, as its backend solution. Firebase was chosen for its speed, efficiency, and comprehensive feature set, providing all necessary features for the application's functionality.

### 7.1 Cloud Firestore Database

The application uses Cloud Firestore, a NoSQL database, to organize its data into "collections" rather than traditional tables. The main collections include:

1. Users Collection: Stores information about all users, including usernames, email addresses, and user roles.
2. Fuel Stations Collection: Contains detailed information about different fuel stations, including names, locations, and contact details.
3. Station Services Collection: Keeps track of services offered by each fuel station, updating in real-time.
4. Drivers Collection: Stores details about drivers using the app, including vehicle types and preferred fuel stations.
5. Fuel Efficiency Tips Collection: A repository of helpful tips for users to save fuel.

### 7.2 Database Interaction

To interact with the database efficiently, a Firestore Service class was created with methods to:

- Create new collections
- Add new data to collections
- Retrieve data from collections
- Filter data based on specific criteria
- Stream data for real-time updates

### 7.3 Data Models

To ensure data consistency and organization, model classes were created for each type of data stored, including user models, Fuel Station models, and others.

### 7.4 Authentication Service

Firebase Authentication is used to handle user logins. A dedicated class manages all authentication-related tasks, including:

- Creating new user accounts
- Logging users in and out
- Checking the current login status of users

### 7.5 Maps Service

For mapping functionality, FUELFINDER integrates Mapbox, a service based on OpenStreetMap. Mapbox allows for customization of map appearance through their Map Studio tool, enabling the app to maintain a consistent visual style.

### 7.6 Real-time Operations

A key feature of FUELFINDER is its real-time update capability:

- Streams are set up in the Firestore Service class to listen for database changes.
- When changes occur (e.g., fuel price updates), the streams detect them immediately.
- The app automatically updates to reflect new information without user intervention.
- This ensures users always have access to the most current data on fuel availability, prices, and station status.