# 🚀 FAQ Management System

A **Django-based FAQ Management System** with multilingual support, caching for performance, and a rich text editor for managing answers effectively.

## 🌟 Features
- 📝 **WYSIWYG Editor** for formatting answers (`django-ckeditor`).
- 🌍 **Multi-language translation support** using Google Translate API (`googletrans`).
- ⚡ **Fast & optimized API** with **Redis caching**.
- 🔍 **REST API** with language selection (`?lang=hi`, `?lang=bn`).
- 🏗 **Admin panel** for managing FAQs.
- ✅ **Unit tests & code quality checks** with `pytest` & `flake8`.
- 🐳 **Docker support** for easy deployment.
- 🚀 **Optional deployment** on Heroku/AWS.

---

## 📌 Table of Contents
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Running the Project](#-running-the-project)
- [API Usage](#-api-usage)
- [Testing](#-testing)
- [Linting](#-linting)
- [Deployment with Docker](#-deployment-with-docker)
- [Contributing](#-contributing)

---

## 🛠 Tech Stack
- **Backend:** Django, Django REST Framework
- **Database:** SQLite (default), PostgreSQL (optional)
- **Caching:** Redis
- **Translation:** Google Translate API (`googletrans`)
- **Admin Panel:** Django Admin
- **Testing & Linting:** `pytest`, `flake8`

---

## 🔧 Installation

1️⃣ **Clone the Repository**
```bash
git clone <https://github.com/AK261102/faq_project.git>
cd faq_project
```

2️⃣ **Create and Activate a Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3️⃣ **Install Dependencies**
```bash
pip install -r requirements.txt
```

4️⃣ **Apply Migrations**
```bash
python manage.py migrate
```

5️⃣ **Create a Superuser** (for admin panel access)
```bash
python manage.py createsuperuser
```

6️⃣ **Run the Server**
```bash
python manage.py runserver
```
🔗 Open in browser: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

---

## 📡 API Usage

### 🔍 Fetch FAQs in Default Language (English)
```bash
GET http://127.0.0.1:8000/api/faqs/
```

### 🌍 Fetch FAQs in Hindi
```bash
GET http://127.0.0.1:8000/api/faqs/?lang=hi
```

### 🌍 Fetch FAQs in Bengali
```bash
GET http://127.0.0.1:8000/api/faqs/?lang=bn
```

Example Response:
```json
[
  {
    "id": 1,
    "question": "What is Django?",
    "answer": "Django is a guitarist...",
    "question_hi": "डjango क्या है?",
    "question_bn": "ডjango কি?"
  }
]
```

---

## 🧪 Testing
Run unit tests using `pytest`:
```bash
pytest
```

---

## 📏 Linting
Ensure code quality using `flake8`:
```bash
flake8 .
```

---

## 🐳 Deployment with Docker

1️⃣ **Build Docker Image**
```bash
docker build -t faq-api .
```

2️⃣ **Run Container**
```bash
docker run -p 8000:8000 faq-api
```

---

## 🤝 Contributing

We welcome contributions! To contribute:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch`.
3. Commit your changes: `git commit -m "feat: Add new feature"`.
4. Push to the branch: `git push origin feature-branch`.
5. Create a Pull Request.

---

## 📜 License
This project is licensed under the **MIT License**.

---

Made with ❤️ by **Team BharatFD** 🚀

