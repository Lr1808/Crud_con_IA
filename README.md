# Django CRUD Application

A robust Django-based web application that implements full CRUD (Create, Read, Update, Delete) functionality for managing posts, integrated with a secure user authentication system.

## 🚀 Features

### 🔐 User Authentication
- **User Registration**: New users can sign up for an account.
- **Login/Logout**: Secure authentication using Django's built-in auth system.
- **Authorization**: Access control ensures that only authenticated users can perform write operations.

### 📝 Post Management (CRUD)
- **Create**: Authenticated users can publish new posts with a title and content.
- **Read**: 
  - **List View**: Browse all posts ordered by the most recent.
  - **Detail View**: View the full content of a specific post.
- **Update**: Authors can edit their own posts.
- **Delete**: Authors can permanently remove their own posts.

### 🛡️ Permissions & Security
- **Author-Only Access**: Editing and deleting are strictly restricted to the author of the post.
- **Protected Routes**: Unauthenticated users are redirected to the login page when attempting to access restricted views.

## 🛠️ Technology Stack

- **Backend Framework**: [Django 5.2.8](https://www.djangoproject.com/) (Python)
- **Database**: SQLite3 (Default Django database, easy to set up)
- **Frontend**: Django Templates (HTML/CSS)
- **Styling**: Custom CSS (located in `static/`)

## 📂 Project Structure

```
django_project/
├── django_project/      # Project configuration (settings, main urls)
├── posts/               # Main application handling posts and signup
│   ├── models.py        # Post model definition
│   ├── views.py         # Class-based views for CRUD and Auth
│   ├── urls.py          # URL routing for the posts app
│   └── templates/       # HTML templates for views
├── signup/              # (Auxiliary app structure)
├── static/              # Static files (CSS, JS, Images)
├── templates/           # Global templates (base.html, etc.)
├── db.sqlite3           # SQLite database file
├── manage.py            # Django command-line utility
└── requirements.txt     # Project dependencies
```

## ⚡ Installation & Setup

Follow these steps to get the project running locally:

### 1. Clone the Repository
```bash
git clone <repository-url>
cd crud_2
```

### 2. Create a Virtual Environment
It's recommended to use a virtual environment to manage dependencies.
```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS/Linux
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Apply Database Migrations
Initialize the database schema.
```bash
python manage.py migrate
```

### 5. Create a Superuser (Optional)
To access the Django Admin interface:
```bash
python manage.py createsuperuser
```

### 6. Run the Development Server
```bash
python manage.py runserver
```
Access the application at: `http://127.0.0.1:8000/`

## 📖 Usage Guide

1.  **Home Page**: Visit `http://127.0.0.1:8000/` to see the list of posts.
2.  **Sign Up**: Click on the "Sign Up" link to create a new account.
3.  **Login**: Log in with your credentials to access full features.
4.  **Create Post**: Click "New Post" to share your thoughts.
5.  **Edit/Delete**: Navigate to a post you created. You will see "Edit" and "Delete" options (these are hidden for posts you didn't author).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open-source and available for educational purposes.
