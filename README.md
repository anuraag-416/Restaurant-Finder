# RestaurantFinder Application

## Team Name: ABHR

| **Team Member**                | **SJSU ID**   |
|--------------------------------|---------------|
| **Venkata Sai Sri Harsha Kata**| 017604522     |
| **Anuraag Ramineni**           | 018196100     |
| **Rishita Konda**              | 017583943     |
| **Bhavika Sodagum**            | 017506567     |


# Team Members and Contributions

| **Team Member** | **Contribution** |
|------------------|------------------|
| **Anuraag**     | - Scrum Master and Frontend/Backend implementation.<br>- Designed class diagrams and database structure.<br>- Developed UI wireframes for Login and Home pages.<br>- Implemented backend for restaurant details, reviews, and listing management.<br>- Finalized and updated admin functionalities and deployed whole backend on aws.<br>- Consistently aligned frontend and backend integration with XP core values of **Feedback** and **Communication**. |
| **Rishita**     | - Backend specialist and database architect.<br>- Designed and implemented database schema.<br>- Integrated backend and frontend functionalities.<br>- Focused on validation logic for business information and user authentication.<br>- Regularly collaborated with the team to refine features based on feedback.<br>- Adhered to XP core values of **Communication** and **Simplicity**. |
| **Harsha**      | - Backend implementation and role-based access.<br>- Designed and developed restaurant management and owner roles.<br>- Finalized database relationships and integrated map api.<br>- Focused on validating and polishing backend features.<br>- Maintained simplicity and efficiency in implementation.<br>- Aligned closely with team efforts under XP values of **Feedback** and **Communication**. |
| **Bhavika**     | - Frontend lead with a focus on user-centric design.<br>- Created user stories, acceptance criteria, and UI wireframes.<br>- Developed user and business owner roles.<br>- Designed and polished UI for restaurant listings and user profiles.<br>- Coordinated frontend-backend integration for seamless user experience.<br>- Focused on feedback-driven improvements and simplicity in design. |

## Tech Stack
React.js, Java/Spring Boot, MySQL, AWS, OpenStreetMap API, Overpass service

## Design Choices

### Why MySQL for Database?
- **Structured Data Storage**: MySQL is a relational database, best suited for structured data - restaurants, users, reviews, and business listings.
- **ACID Compliance**: It ensures consistency in data that becomes critical in restaurant review/rating features.
- **Wide Adoption and Community Support**: A large community of developers and comprehensive documentation ensure quick fixes to challenges.
- **Integration with Spring Boot**: MySQL works perfectly well with Spring Boot, thereby allowing easy communication between the backend and database.

### Why AWS for Cloud Hosting?
- **Scalability**: AWS provides auto-scaling EC2 instances, ensuring the application can handle varying traffic loads efficiently.
- **High Availability**: AWS's load balancers ensure that the application remains accessible even if one or more servers fail.
- **Global Reach**: AWS provides infrastructure in multiple regions, ensuring faster response times for users worldwide.
- **Integrated Ecosystem**: AWS provides services such as RDS for MySQL hosting, S3 for static asset storage, and CloudWatch for monitoring, making deployment and maintenance much easier.

### Why OpenStreetMap API for Location Services?
- **Open Source**: OpenStreetMap is free to use, licensed, and has no licensing restrictions, thus making it very cost-effective to integrate location-based services.
- **Customizability**: It allows developers to customize maps and access raw geolocation data for flexibility in advanced features such as filtering by location.
- **Global Coverage**: OpenStreetMap provides comprehensive global coverage, enabling any region to be searched for restaurants.

### Why Overpass Service for Querying Map Data?
- **Efficient Geospatial Queries**: Overpass efficiently queries data from OpenStreetMap, such as restaurants within a radius or category.
- **Flexibility**: Advanced querying of geospatial data is supported, including things like finding nearby restaurants that are not listed by business owners.
- **Compatibility**: Overpass works smoothly with OpenStreetMap, which provides consistent and reliable location-based functionality.


## XP Core Values Maintained by Team 

### Communication
Effective communication was one of the major principles followed in our project. The regular sprint meeting helped to ensure that all the members were on par regarding their tasks and responsibilities. Team members had an open discussion of their status regarding progress, issues faced, and planning for the next step. This keeps everyone updated and resolves blockers together. Consistent communication also smoothed out the integration of the frontend and backend components and ensured our project met its goals efficiently.

### Simplicity
We have tried to keep the solutions simple and effective throughout the project. This approach included writing clean, modular code that was easy to read, maintain, and modify. Database schemas and backend logic were kept straightforward to meet project requirements without adding unnecessary complexity. Similarly, our UI was designed with simplicity in mind, ensuring it was intuitive and user-friendly for all roles: users, business owners, and admins. This value helped us minimize technical debt and kept the project scalable.

### Feedback
The team insisted on continuous feedback for the improvement of individual contributions and overall project quality. Continuous code reviews were carried out where every pull request was carefully reviewed before being merged to the main branch. Feedback loops during sprints allowed us to refine functionalities, enhance UI/UX designs, and address integration issues between modules. This feedback-driven approach would ensure that the project keeps evolving toward meeting user needs and requirements effectively.

### Respect
Respect was maintained within the team by valuing each member's ideas and contributions. During discussions and sprint retrospectives, everyone was encouraged to share their opinions, which fostered a positive and inclusive environment. Each member's expertise was acknowledged, and tasks were assigned based on individual strengths, ensuring that everyone felt valued and motivated to perform their best.

### Courage
Courage for this team was taken by owning different challenging tasks and resolving the blockers head-on, like handling complex integrations and performance tuning issues under tight deadlines. That means every team member did a jump out of their comfort zones as needed to learn new tools and technologies to make this project meet its technical and functional needs. Courage also played into ensuring timely completion of the sprints and overall project outcomes.

## Architecture Diagram
![Architecture Diagram](images/architecturediag.png)

## Use Case Diagram
![Use Case Diagram](images/UseCaseDiag.jpeg)

## Database Design
![Database Design](images/DBDesign.jpeg)

## Deployment Diagram
![Deployment Diagram](images/Deploymentdiag.jpeg)






## Feature Set

### For All Users:
- **Search Restaurants**:  
  Search for restaurants by various parameters, including:
  - Name
  - Category (e.g., type of cuisine, food preferences like Vegetarian/Vegan)
  - Price Range (Low/Medium/High)
  - Ratings (1 to 5 stars)

- **View Restaurant Details**:  
  View detailed information about restaurants, including:
  - Reviews and Ratings
  - Address and Contact Details

- **Submit Reviews and Ratings**:  
  Post reviews and rate restaurants based on user experience.

- **Location-Based Search**:  
  Search for restaurants by location using a Maps API, even if the restaurant is not listed by the business owner.

- **User Registration and Login**:  
  Create an account and log in to access user-specific features.

---

### For Business Owners:
- **Add New Listings**:  
  Add new restaurants to the platform, including:
  - Name, Address, and Contact Information
  - Hours of Operation
  - Description and Photos

- **Update Listings**:  
  Modify existing restaurant details, including:
  - Contact Info
  - Descriptions and Photos
  - Operating Hours

- **Manage Owned Listings**:  
  View and manage all restaurant listings owned by the business (e.g., restaurant chains).

- **Manual Registration**:  
  Register manually to gain access to the Business Owner role.

---

### For Admins:
- **Detect Duplicate Listings**:  
  Identify and manage duplicate restaurant entries in the system.

- **Remove Listings**:  
  Remove restaurants from the platform if the business is closed or inactive.

- **Role-Based Access**:  
  Admins have privileged access to manage all restaurant data on the platform.

---

### Deployment and Integration:
- **API Integration**:  
  - Use OpenStreetMap API and Overpass Service for geospatial queries.
  - Provide location-based restaurant search functionality.

- **Cloud Hosting**:  
  - APIs and database are deployed on an auto-scaled AWS EC2 cluster with a load balancer for high availability.

- **Responsive UI**:  
  A user-friendly web application developed with React.js, providing seamless interaction for all roles (Users, Business Owners, Admins).


## UI Wireframes

### Adding New Restaurant
![Adding New Restaurant](UI%20Wireframes/Adding%20New%20Restaurant.jpeg)

### Adding Reviews
![Adding Reviews](UI%20Wireframes/Adding-Reviews.jpeg)

### Admin Account
![Admin Account](UI%20Wireframes/Admin-Account.jpeg)

### Admin Dashboard
![Admin Dashboard](UI%20Wireframes/Admin-Dashboard.jpeg)

### Registration and SignIn
![Registration and SignIn](UI%20Wireframes/Registration%20and%20SignIn.jpeg)

### Restaurant Owner Dashboard
![Restaurant Owner Dashboard](UI%20Wireframes/RestaurantOwner-Dashboard.jpeg)

### Review
![Reviews](UI%20Wireframes/Reviews.jpeg)

### Searching Restaurant
![Searching Restaurant](UI%20Wireframes/Searching%20Restaurant.jpeg)

### Searching by Location
![Searching by Location](UI%20Wireframes/Searching%20by%20Location.jpeg)

## Sprint Burndown Chart

[Click here to view the Sprint Burndown Chart](SprintTaskSheet-teamABHR.xlsx)

## Daily Scrum Sheet
[Click here to view the Daily Scrum Sheet](DAILYSCRUMSHEET_TeamABHR.xlsx)

## Sprint Journal
[Click here to view the Sprint Journal](Journal-ABHR.pdf)
