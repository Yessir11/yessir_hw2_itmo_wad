# User Profile Management with Flask and MongoDB

## Project Description
This Flask-based web application allows users to register, log in, update their profile information (city, profession, and profile picture), change passwords, and log out. The application uses MongoDB as the database and supports secure password hashing with bcrypt.

## Features
- User authentication (registration, login, logout)
- Profile update (city, profession, and profile picture)
- Secure password storage using bcrypt
- Session-based authentication
- Flash messages for user feedback

## Installation and Setup

### Prerequisites
Ensure you have the following installed on your system:
- Python 3
- MongoDB
- pip (Python package manager)

### Clone the Repository
```bash
git clone https://github.com/Yessir11/yessir_hw2_itmo_wad.git
cd yessir_hw2_itmo_wad
```

### Create a Virtual Environment (Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate    # On Windows
```
### Required Python Libraries
This project requires the following Python libraries:
```bash
Flask
pymongo
bcrypt
Werkzeug
```
To install manually, run:
```bash
pip install Flask pymongo bcrypt Werkzeug
```

### Setting Up MongoDB
1. Connect to MongoDB shell:
   ```bash
   mongo
   ```
2. Create the database and collection:
   ```js
   use itmo_wad_hw2
   db.createCollection("users")
   ```

### Running the Application
```bash
python3 app.py
```
The application will run on `http://localhost:5000/`

## Folder Structure
```
flask-profile-management/
│── static/
│   ├── styles.css
│   ├── uploads/  # Folder for user profile pictures
│── templates/
│   ├── login.html
│   ├── registration.html
│   ├── profile.html
│   ├── updateInfo.html
│── app.py
│── requirements.txt
│── README.md
```

## Routes and Endpoints
| Route           | Method | Description |
|----------------|--------|-------------|
| `/`            | GET/POST | Login page |
| `/registration` | GET/POST | User registration |
| `/profile`      | GET | User profile page |
| `/update`       | GET/POST | Update profile information |
| `/changepasswd` | POST | Change user password |
| `/logout`       | GET | Logout user |

## Additional Notes
- User passwords are securely hashed using bcrypt.
- Default profile pictures are used if users do not upload one.
- Users can update either one or both profile fields (city and profession) independently.
- The `UPLOAD_FOLDER` is set to `static/uploads` to store profile pictures.

---
For any issues or improvements, feel free to contribute!

