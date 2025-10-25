# Student Dropout Analysis System

## 📊 Project Overview

The Student Dropout Analysis System is a comprehensive data-driven platform designed to help educational authorities identify and address the reasons behind student dropouts at the school level. This system analyzes dropout trends based on multiple socio-economic and demographic parameters to assist in policy-making and targeted interventions.

### 🎯 Objective
To analyze and predict student dropout patterns using demographic and socio-economic data, enabling governments and educational institutions to take proactive measures to reduce dropout rates.

### 🚀 Key Features
- **Student Profile Management**: Upload, validate, and manage student data
- **Interactive Dashboard**: Visualize dropout statistics across multiple dimensions
- **Risk Scoring & Prediction**: AI-powered dropout risk assessment with explainable insights
- **Role-based Access Control**: Secure authentication for different user types
- **Custom Report Builder**: Generate tailored reports with chart visualizations
- **Data Validation Pipeline**: Automated data cleaning and error handling

## 🏗️ System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   React.js      │    │   Spring Boot   │    │     MySQL       │
│   Frontend      │◄──►│    Backend      │◄──►│    Database     │
│                 │    │                 │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🛠️ Technology Stack

### Frontend
- **Framework**: React.js
- **HTTP Client**: Axios
- **Routing**: React Router
- **Charts**: Chart.js / Recharts
- **UI Components**: Material-UI / Bootstrap

### Backend
- **Framework**: Spring Boot
- **ORM**: Hibernate / JPA
- **Security**: Spring Security + JWT
- **API Documentation**: Swagger
- **Build Tool**: Maven

### Database
- **Database**: MySQL
- **Connection Pool**: HikariCP

### Development Tools
- **API Testing**: Postman
- **Version Control**: Git/GitHub
- **IDE**: VS Code / IntelliJ IDEA

## 📁 Project Structure

```
student-dropout-analysis-ai/
│
├── backend/
│   ├── src/
│   │   ├── main/java/com/dropoutanalysis/
│   │   │   ├── controller/          # REST Controllers
│   │   │   ├── model/              # Entity Models
│   │   │   ├── repository/         # Data Access Layer
│   │   │   ├── service/            # Business Logic
│   │   │   └── config/             # Configuration Classes
│   │   ├── main/resources/
│   │   │   ├── application.properties
│   │   │   └── data.sql
│   ├── pom.xml
│   └── README.md
│
├── frontend/
│   ├── src/
│   │   ├── components/             # Reusable Components
│   │   ├── pages/                 # Page Components
│   │   ├── services/              # API Services
│   │   ├── utils/                 # Utility Functions
│   │   └── App.js                 # Main App Component
│   ├── package.json
│   ├── .env
│   └── README.md
│
├── docs/
│   ├── SRS_StudentDropoutAnalysis.docx     # Requirements Document
│   ├── UML_Diagrams/                       # System Diagrams
│   │   ├── DFD.png                         # Data Flow Diagram
│   │   ├── ER_Diagram.png                  # Entity Relationship
│   │   ├── Class_Diagram.png               # Class Diagram
│   │   ├── UseCase_Diagram.png             # Use Case Diagram
│   │   └── Sequence_Diagram.png            # Sequence Diagram
│   ├── Project_Poster.pdf                  # Project Poster
│   └── API_Documentation.md                # API Documentation
│
└── README.md                               # This File
```

## 🚀 Getting Started

### Prerequisites
- **Java**: JDK 11 or higher
- **Node.js**: v14 or higher
- **MySQL**: v8.0 or higher
- **Maven**: v3.6 or higher
- **Git**: Latest version

### 📥 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yashjangid249-hue/expert-octo-broccoli.git
   cd expert-octo-broccoli
   ```

2. **Database Setup**
   ```sql
   CREATE DATABASE student_dropout_db;
   CREATE USER 'dropout_user'@'localhost' IDENTIFIED BY 'password123';
   GRANT ALL PRIVILEGES ON student_dropout_db.* TO 'dropout_user'@'localhost';
   FLUSH PRIVILEGES;
   ```

### 🔧 Backend Setup

1. **Navigate to Backend Directory**
   ```bash
   cd backend
   ```

2. **Configure Database Connection**
   Update `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/student_dropout_db
   spring.datasource.username=dropout_user
   spring.datasource.password=password123
   ```

3. **Build and Run Backend**
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

   Backend will be available at: `http://localhost:8080`

### 🎨 Frontend Setup

1. **Navigate to Frontend Directory**
   ```bash
   cd frontend
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Configure Environment Variables**
   Create `.env` file:
   ```env
   REACT_APP_API_BASE_URL=http://localhost:8080/api
   ```

4. **Start Development Server**
   ```bash
   npm start
   ```

   Frontend will be available at: `http://localhost:3000`

## 📚 Documentation

The `docs/` directory contains comprehensive project documentation:

- **📋 SRS Document**: Complete Software Requirements Specification
- **🎨 Project Poster**: Visual project overview and architecture
- **📊 UML Diagrams**: System design diagrams including:
  - Data Flow Diagram (DFD)
  - Entity-Relationship Diagram
  - Class Diagram
  - Use Case Diagram
  - Sequence Diagram
- **📖 API Documentation**: Complete REST API reference

## 🔐 User Roles

| Role | Permissions |
|------|-------------|
| **Admin** | Full system access, user management, data administration |
| **Data Analyst** | Data upload, analysis, report generation |
| **Viewer** | Read-only access to dashboards and reports |

## 📊 Key Modules

### 1. Student Profile Management
- CSV/Excel data upload functionality
- Data validation and error reporting
- Student record management interface
- Bulk data processing capabilities

### 2. Dashboard & Analytics
- Interactive visualization dashboards
- Multi-dimensional filtering (school, area, gender, caste, age)
- Custom report generation
- Export functionality (PDF, Excel)

### 3. Risk Scoring & Prediction
- AI-powered dropout risk assessment
- Explainable AI for prediction transparency
- Actionable recommendations
- Risk trend analysis

### 4. Access Control & Security
- JWT-based authentication
- Role-based authorization
- Secure API endpoints
- User session management

## 🧪 Testing

### Backend Testing
```bash
cd backend
mvn test
```

### Frontend Testing
```bash
cd frontend
npm test
```

### API Testing
Use the provided Postman collection in `docs/` for comprehensive API testing.

## 🚀 Deployment

### Production Build

**Backend:**
```bash
cd backend
mvn clean package
java -jar target/student-dropout-analysis-0.0.1-SNAPSHOT.jar
```

**Frontend:**
```bash
cd frontend
npm run build
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Team

- **Project Lead**: yashjangid249-hue
- **Backend Developer**: Spring Boot Team
- **Frontend Developer**: React Team
- **Database Administrator**: MySQL Team

## 📞 Support

For support and queries:
- 📧 Email: yashjangid249@example.com
- 🐛 Issues: [GitHub Issues](https://github.com/yashjangid249-hue/expert-octo-broccoli/issues)
- 📖 Documentation: `/docs` directory

## 🎯 Future Enhancements

- Mobile application development
- Advanced ML model integration
- Real-time data streaming
- Multi-language support
- Cloud deployment automation

---

**Made with ❤️ for Educational Advancement**
