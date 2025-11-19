# 📝 FastAPI Blog

## 📘 Overview

**FastAPI Blog** is a fully featured backend-only blogging system built using **FastAPI**, **SQLAlchemy ORM**, and **Pydantic**. The project follows a clean and scalable architecture using the **Repository Pattern**, **eager loading for optimized queries**, and a well-structured module layout suitable for real-world production applications.

This backend handles user authentication, posts, comments, likes, tags, profiles, and a follow system between users. It demonstrates how to implement complete business logic in a clean and maintainable way.

---

## 🌟 Key Features

### 👤 **User Management**

* Create, update, delete users
* User profiles
* Follow/unfollow system
* Secure password hashing

### 📝 **Posts & Comments**

* Full CRUD for posts
* Comment system with CRUD
* Like/unlike both posts and comments
* Relation-based querying

### 🏷️ **Tags System**

* Add tags to posts
* List posts by tag
* Many-to-many relationships

### ❤️ **Likes System**

* Users can like/unlike posts and comments
* Prevent multiple likes from same user

### 🔐 **Authentication**

* JWT-based authentication
* OAuth2 password flow
* Access token creation & validation

### ⚡ **Performance Techniques**

* **Eager loading** for efficient queries (selectinload/joinedload)
* Clean repository abstraction for data access

### 🏗️ **Architecture Highlights**

* Repository pattern
* Models and schemas separation
* Modular API routes
* Centralized database session handling

---

## 📂 Project Structure

```
fastapi-blog/
│
├── app/
│   ├── api/                # All API route files
│   │   ├── auth.py
│   │   ├── users.py
│   │   ├── posts.py
│   │   ├── comments.py
│   │   └── tags.py
│   │
│   ├── core/               # Core system utilities & configs
│   │   ├── config.py
│   │   ├── database.py
│   │   ├── enums.py
│   │   ├── events.py
│   │   ├── hashing.py
│   │   ├── helpers.py
│   │   ├── oauth2.py
│   │   └── token.py
│   │
│   ├── models/             # SQLAlchemy ORM models
│   │   ├── users.py
│   │   ├── profile.py
│   │   ├── posts.py
│   │   ├── comments.py
│   │   ├── tags.py
│   │   ├── users_followers.py
│   │   ├── post_tags.py
│   │   ├── post_likes.py
│   │   └── comment_likes.py
│   │
│   ├── repositories/       # Repository pattern implementation
│   │   ├── auth_repository.py
│   │   ├── user_repository.py
│   │   ├── post_repository.py
│   │   ├── comment_repository.py
│   │   └── tag_repository.py
│   │
│   ├── schemas/            # Pydantic schemas for validation/response
│       ├── auth_schema.py
│       ├── user_schema.py
│       ├── post_schema.py
│       ├── comment_schema.py
│       └── tag_schema.py
│
├── alembic/                # Database migrations
├── scripts/
│   └── seed.py             # Database seeding script
│
├── .env                    # Environment configuration
├── .env.example
├── alembic.ini
├── main.py                 # FastAPI entry point
└── requirements.txt        # Dependencies
```

---

## 🚀 Getting Started

### 1️⃣ **Clone the repository**

```
git clone https://github.com/IslamAhmd95/fastapi-blog
cd fastapi-blog/
```

### 2️⃣ **Create and activate a virtual environment**

```
python3 -m venv venv
source venv/bin/activate
```

### 3️⃣ **Install dependencies**

```
pip install -r requirements.txt
```

### 4️⃣ **Apply migrations**

```
alembic upgrade head
```

### 5️⃣ **Seed the database**

```
python -m scripts.seed
```

### 6️⃣ **Run the development server**

```
uvicorn main:app --reload
```

---
