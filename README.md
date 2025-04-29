#   📓 eNotebook

**eNotebook** is a full-stack MERN (MongoDB, Express.js, React.js, Node.js) web application that allows users to securely manage their personal notes. It supports creating, updating, deleting, and categorizing notes. Authentication is handled via JWT tokens, ensuring user privacy and secure access to data.

This app features a clean Bootstrap-based UI, robust backend API, and contextual alerts for improved user experience. It’s an ideal project to demonstrate full-stack development skills and how frontend and backend interact in a secure, real-time environment.

---

##   🚀 Features

-   Secure user authentication using JWT.
-   CRUD operations for notes: Add, Edit, Delete, View.
-   Note categorization with tags.
-   Protected routes that redirect unauthenticated users to login.
-   Real-time UI updates.
-   Alert messages for success and error handling.

---

##   🛠️ Technologies Used

**Frontend**: React.js, Bootstrap, Context API, React Router
**Backend**: Node.js, Express.js, MongoDB, Mongoose, JWT
**Dev Tools**: Postman, Concurrently, dotenv

---

##   📁 Folder Structure

    eNotebook/
    ├── backend/
    │   ├── db.js          # MongoDB connection setup
    │   ├── index.js       # Main Express server file
    │   ├── .env           # Environment variables (PORT, DB_URI, JWT_SECRET)
    │   ├── package.json   # Backend dependencies
    │   └── routes/
    │       ├── auth.js    # User authentication routes
    │       └── notes.js   # Notes CRUD routes
    │
    ├── frontend/
    │   ├── public/        # Public assets
    │   │   └── index.html # HTML root file
    │   ├── src/
    │   │   ├── App.js     # Root React component
    │   │   ├── index.js   # Entry point for React app
    │   │   ├── context/
    │   │   │   └── notes/
    │   │   │       ├── NoteContext.js # React context for notes
    │   │   │       └── NoteState.js   # Context state provider
    │   │   ├── components/
    │   │   │   ├── AddNote.js     # Add note form component
    │   │   │   ├── Noteitem.js    # Single note display component
    │   │   │   ├── Notes.js       # Notes list and modal for editing
    │   │   │   ├── Navbar.js      # Navigation bar
    │   │   └── pages/
    │   │       ├── Home.js        # Home page
    │   │       ├── About.js       # About page
    │   │       ├── Login.js       # Login page
    │   │       └── Signup.js      # Signup page
    │   ├── .env           # Frontend environment variables (if any)
    │   └── package.json   # Frontend dependencies
    │
    └── README.md          # Project documentation

---

##   ⚙️ Configuration

To run both frontend and backend concurrently, the root-level `package.json` uses the `concurrently` package:

```json
"scripts": {
    "both": "concurrently \"npm run start --prefix backend\" \"npm run start --prefix frontend\""
}
🚀 InstallationClone the repository:git clone <repository_url>
cd eNotebook
Set up the backend:Navigate to the backend folder:cd backend
Install dependencies:npm install
Create a .env file in the backend directory and add your MongoDB URI and JWT secret:PORT=5000
DB_URI="your_mongodb_connection_string"
JWT_SECRET="your_jwt_secret_key"
Set up the frontend:Navigate to the frontend folder:cd ../frontend
Install dependencies:npm install
Create a .env file in the frontend directory if you have any frontend specific environment variables.🏃‍♂️ How to Run the ApplicationRun the application:From the root directory, run:npm run both
This will start both the frontend and backend servers concurrently.Open your browser:Visit http://localhost:3000 to view the application.🤝 Contribution GuidelinesContributions are welcome! Here's how you can contribute:**Fork