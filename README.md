# portfolio_tracker
# Portfolio Tracker Application

## Overview
This application is a **Portfolio Tracker** that allows users to manage and monitor their stock portfolio. Users can add, view, edit, and delete stock holdings while tracking the total portfolio value based on real-time stock prices. The application consists of a **React frontend** and a **Spring Boot backend** integrated with a MySQL database.

---

## Features

### Frontend
- **Dashboard**: Displays total portfolio value, top-performing stock, and portfolio distribution.
- **Form**: Add or edit stock details (name, ticker, quantity, buy price).
- **Table**: View, edit, or delete stock holdings.

### Backend
- Exposes RESTful APIs for CRUD operations on stocks.
- Real-time stock price integration using a free API.
- Uses JPA with Hibernate for database interactions.

### Database
- MySQL database for storing stock details.
- Schema includes fields for stock name, ticker, quantity, buy price, etc.

### Deployment
- **Backend**: Deployable on Heroku, AWS, or Render.
- **Frontend**: Deployable on Vercel or Netlify.

---

## Prerequisites

### Software Requirements
- **Java** (JDK 17 or above)
- **Maven** (version 3.6 or above)
- **MySQL** (version 8.0 or above)
- **Node.js** (version 18 or above)
- **VS Code** with the following extensions:
  - Extension Pack for Java
  - Prettier
  - ESLint

---

## Project Setup

### 1. Clone the Repository
```bash
git clone <repository_url>
cd portfolio-tracker
```

### 2. Backend Setup
1. Navigate to the `backend` folder:
   ```bash
   cd backend
   ```
2. Update `application.properties` with your MySQL credentials:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/portfolio_tracker
   spring.datasource.username=<your_mysql_username>
   spring.datasource.password=<your_mysql_password>
   spring.jpa.hibernate.ddl-auto=update
   ```
3. Build the project:
   ```bash
   mvn clean install
   ```
4. Run the Spring Boot application:
   ```bash
   mvn spring-boot:run
   ```

### 3. Frontend Setup
1. Navigate to the `frontend` folder:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

---

## Usage
1. Open the frontend application at `http://localhost:3000`.
2. Perform CRUD operations on your portfolio.
3. The backend APIs run on `http://localhost:8080`.

---

## Folder Structure
```
portfolio-tracker/
├── backend/
│   ├── src/main/java/com/example/portfolio/
│   ├── src/main/resources/
│   │   ├── application.properties
│   └── pom.xml
├── frontend/
│   ├── public/
│   ├── src/
│   └── package.json
└── README.md
```

---

## Deployment

### Backend
1. Package the Spring Boot application:
   ```bash
   mvn package
   ```
2. Deploy the generated JAR file on a cloud platform (e.g., Heroku).

### Frontend
1. Build the React application:
   ```bash
   npm run build
   ```
2. Deploy the `build` folder to Vercel or Netlify.

---

## API Endpoints

### Base URL
`http://localhost:8080`

### Endpoints
1. **Add Stock** (POST): `/api/stocks`
2. **Get All Stocks** (GET): `/api/stocks`
3. **Update Stock** (PUT): `/api/stocks/{id}`
4. **Delete Stock** (DELETE): `/api/stocks/{id}`

---

## Troubleshooting

### Common Errors
1. **Database Connection Issues**:
   - Verify MySQL is running.
   - Ensure credentials in `application.properties` are correct.

2. **Frontend Not Connecting to Backend**:
   - Update the API URL in `frontend/src/config.js` to match the backend's deployed URL.

3. **Maven Build Fails**:
   - Run `mvn dependency:resolve`.
   - Ensure you have the correct JDK version installed.

---

## Contributors
- Chanchal Kailash Pawar

---

## License
This project is licensed under the MIT License.
