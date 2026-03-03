# 🎵 Song REST API

A RESTful API for managing songs built using **Spring Boot** and **MySQL**.

---

## 🚀 Features

- Create, read, update, and delete songs (CRUD)
- Search songs by artist and genre
- Find songs by name, artist, or genre
- Layered architecture (Controller → Service → Repository)

---

## 🛠 Technologies

- Java  
- Spring Boot  
- Spring Data JPA  
- MySQL  
- Maven (Wrapper included)

---

## 📁 Project Structure


src/main/java/org/hartford/songrestapi/
│
├── controller # REST controllers
├── service # Service layer
├── repository # Repository layer
├── entity # JPA entities
│
src/main/resources/
├── application.properties # App & database configuration


---

## ⚙️ Database Configuration

Update `src/main/resources/application.properties` with your MySQL credentials:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/song_db
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
Make sure:

MySQL is running

Database song_db is created

📌 API Endpoints
➕ Create Song

POST /songs

{
  "name": "Song Name",
  "artist": "Artist Name",
  "genre": "Pop",
  "duration": 180,
  "releaseDate": "2024-01-01"
}
📄 Get All Songs

GET /songs

🔍 Get Song by ID

GET /songs/{id}

Example:

GET /songs/1
✏️ Update Song

PUT /songs/{id}

❌ Delete Song

DELETE /songs/{id}

🔎 Search by Artist and Genre

GET

/songs/search?artist=ArtistName&genre=GenreName

Example:

/songs/search?artist=Arijit&genre=Romantic
🎵 Find by Name

GET

/songs/name/{name}
🎤 Find by Artist

GET

/songs/artist/{artist}
🎼 Find by Genre

GET

/songs/genre/{genre}
▶️ Running the Application
1️⃣ Clone the Repository
git clone <your-repository-url>
cd songrestapi
2️⃣ Configure Database

Update application.properties.

3️⃣ Run the Application

Using Maven wrapper:

./mvnw spring-boot:run

Or using installed Maven:

mvn spring-boot:run

Application runs at:

http://localhost:8080
