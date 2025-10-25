# 📝 Flask Blog Website – Full Stack Blog Application

A full-featured **Flask Blog Application** with user authentication, rich-text editor, RESTful CRUD operations, comment system, admin-only access, and live deployment using **Render & PostgreSQL**.

🚀 [**Live Demo:**](https://personal-blog-l8cb.onrender.com)

---

## ✅ Features

| Feature | Description |
|---------|-------------|
| 📝 Blog Posts | Create, Read, Update, Delete (CRUD) blog posts using RESTful routes |
| 🔐 Authentication | Register, Login, Logout using **Flask-Login** |
| 🔑 Password Security | Password hashing & salting with **Werkzeug** |
| 👑 Admin Access | Only admin can create/edit/delete posts |
| 💬 Comments | Users can comment on blog posts |
| 👤 Gravatar Integration | Profile pictures based on email |
| 📧 Contact Form | Users can send messages via email (SMTP) |
| 🖋️ Rich Text Editor | Integrated **Flask-CKEditor** for formatting posts |
| 💾 Database | SQLite (development) → PostgreSQL (production) |
| ☁️ Deployment | Hosted using **Render + Gunicorn + Environment Variables** |

---

## 🛠️ Tech Stack

**Backend:** Flask, Flask-SQLAlchemy, Flask-Login, Flask-WTF  
**Frontend:** HTML, CSS, Bootstrap 5, Jinja2 Templating  
**Database:** SQLite (local), PostgreSQL (production)  
**Deployment:** Render.com, Gunicorn, Environment Variables  
**Others:** CKEditor, Gravatar API, smtplib (email)

---

## 📂 Project Structure

```
Flask-Blog/
│
├── templates/
│   ├── header.html
│   ├── footer.html
│   ├── index.html
│   ├── post.html
│   ├── login.html
│   ├── register.html
│   ├── contact.html
│   ├── make-post.html
│   └── ...
│
├── static/
│   ├── css/styles.css
│   └── assets/img/
│
├── main.py or app.py         # Main Flask application
├── forms.py                   # WTForms for login, register, post
├── models.py                  # SQLAlchemy models (User, Post, Comment)
├── requirements.txt           # Python dependencies
├── Procfile                   # For deployment (Gunicorn)
├── .gitignore                 # Ignore unnecessary files
└── README.md
```

---

## ⚙️ Installation & Setup (Local Development)

### 1. **Clone the repository**

```bash
git clone https://github.com/dilshadparambil/Python_Personal.blog.git
cd Python_Personal.blog
```

### 2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

### 3. **Install dependencies**

```bash
pip install -r requirements.txt
```

### 4. **Set environment variables**

```bash
export FLASK_KEY="your_secret_key"
export EMAIL="your_email"
export EMAIL_APP_PASS="your_email_app_password"
export DB_URI="sqlite:///posts.db"
```

### 5. **Run the application**

```bash
python main.py
```

### 6. **Open the browser** → `http://127.0.0.1:5000/`

---

## 🚀 Deployment on Render

1. Push your project to GitHub
2. Create a new Web Service on https://render.com
3. Connect your repository
4. Set Start Command:
   ```
   gunicorn main:app
   ```
5. Add environment variables in Render Dashboard → Environment
6. Deploy!

---

## 🗃️ PostgreSQL Migration (Production)

1. Create a PostgreSQL database on Render
2. Copy the Internal Database URL → modify it to:
   ```bash
   postgresql://username:password@host/database_name
   ```
3. Add to environment variables as `DB_URI`
4. Re-deploy the service

---

## 💡 Future Improvements

- ✅ User profile pages (posts commented, profile info)
- ✅ Like/Bookmark system for blog posts
- ✅ Image upload instead of URL-based images
- ✅ Dark mode toggle
- ✅ Pagination & search functionality
- ✅ Admin dashboard for managing users/posts

---

## 📜 License

This project is open-source and available under the MIT License.

---

## ⭐ Show Your Support

If you like this project, don't forget to ⭐ the repository!  
Feel free to fork and contribute to make it better.

---

## 👨‍💻 Developed by Dilshad P