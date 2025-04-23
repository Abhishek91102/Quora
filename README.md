# Quora Clone - Backend

![Java](https://img.shields.io/badge/Java-17-blue.svg)
![Spring Boot](https://img.shields.io/badge/SpringBoot-3.0-green)
![MySQL](https://img.shields.io/badge/Database-MySQL-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen)

This is a **backend-only clone of Quora**, built using **Spring Boot**. It includes APIs for user management, posting questions, answering, liking, and commenting—offering the core backend logic of a real-world Q&A platform.

---

## 🚀 Features

✅ User registration & login (JWT-based)  
✅ Secure authentication and authorization  
✅ CRUD for questions, answers, and comments  
✅ Like/dislike feature for questions and answers  
✅ Search and category filter support  
✅ Clean REST API structure with Swagger docs  

---

## 🧰 Tech Stack

- **Backend:** Java 17, Spring Boot 3.x  
- **Security:** Spring Security + JWT  
- **Database:** MySQL  
- **ORM:** JPA & Hibernate  
- **Testing:** Postman / Swagger  
- **Dev Tools:** Maven, IntelliJ IDEA  

---

## 📁 Project Structure

<pre> ```bash src/ ├── config/ # JWT, security configs ├── controller/ # REST API endpoints ├── dto/ # Request/Response payloads ├── entity/ # JPA Entities ├── exception/ # Global exception handling ├── repository/ # Spring Data Repositories ├── service/ # Business logic └── QuoraApplication.java # Main class ``` </pre>



---

## 📄 Sample APIs

| Method | Endpoint               | Description                         |
|--------|------------------------|-------------------------------------|
| POST   | `/api/auth/register`   | Register a new user                 |
| POST   | `/api/auth/login`      | Authenticate user, returns JWT      |
| GET    | `/api/questions`       | Get all questions                   |
| POST   | `/api/questions`       | Post a new question                 |
| POST   | `/api/answers/{id}`    | Post answer to question             |
| PUT    | `/api/like/{id}`       | Like a question or answer           |
| GET    | `/api/categories`      | Get all question categories         |

---

## 🧪 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Abhishek91102/Quora.git
cd Quora

2. Configure MySQL in application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/quora_db
spring.datasource.username=root
spring.datasource.password=yourpassword
jwt.secret=your_jwt_secret_key
spring.jpa.hibernate.ddl-auto=update

3. Run the App
./mvnw spring-boot:run
📊 Database Schema (ER Diagram)
Here’s a basic outline of the database entities:

User — id, username, email, password, role

Question — id, title, content, user_id, category, timestamp

Answer — id, content, question_id, user_id, timestamp

Like — id, user_id, entity_id, entity_type

Comment — id, content, answer_id, user_id, timestamp

Full ER diagram and SQL schema available in the /docs folder (can be added upon request).

📖 Swagger Documentation
You can test all APIs using Swagger UI once the application is running.

🔗 URL: http://localhost:8080/swagger-ui/index.html

This interactive documentation allows:

Testing of all endpoints

Viewing request/response formats

Exploring secured routes (with JWT token input)

🧑‍💻 Author
Abhishek Gunjal
Java Backend Developer | Final Year CSE @ MIT ADT
📫 GitHub | LinkedIn

📄 License
This project is licensed under the MIT License.

yaml
Copy
Edit

---

You're good to go! You can copy and paste the above directly into your `README.md` file. Let me know if 
