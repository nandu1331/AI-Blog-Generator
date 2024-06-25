# AI Blog Article Generator

AI Blog Article Generator is a Django-based application that leverages AI to generate blog articles. This tool is designed to assist bloggers and content creators in generating high-quality content efficiently.

![AI Blog Article Generator]

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **AI-Powered Content Generation**: Generate blog articles using AI.
- **User Authentication**: Secure user registration and login.
- **CRUD Operations**: Create, Read, Update, and Delete blog posts.
- **Rich Text Editor**: Write and format blog posts with a built-in rich text editor.
- **Category Management**: Organize blog posts into categories.
- **Search Functionality**: Search for blog posts by title or content.

## Requirements

- Python 3.8+
- Django 3.2+
- MySQL 5.7+ or MariaDB 10.2+
- [OpenAI API Key](https://openai.com/api/)

## Installation

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/ai-blog-article-generator.git
cd ai-blog-article-generator
```

### 2. Set Up Virtual Environment

```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. Install Dependencies

```sh
pip install -r requirements.txt
```

### 4. Configure Database

Create a MySQL database named `blog`. Update the `DATABASES` setting in `settings.py` with your database credentials.

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'your_database_name',
        'USER': 'your_mysql_user',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

### 5. Apply Migrations

```sh
python manage.py migrate
```

### 6. Create a Superuser

```sh
python manage.py createsuperuser
```

### 7. Run the Server

```sh
python manage.py runserver
```

### 8. Set Up OpenAI API Key

Set your OpenAI API key as an environment variable:

```sh
export OPENAI_API_KEY='your_openai_api_key'
```

On Windows:

```sh
set OPENAI_API_KEY=your_openai_api_key
```

## Usage

1. Navigate to `http://127.0.0.1:8000/` in your web browser.
2. Register a new account or log in with your superuser credentials.
3. Use the dashboard to create and manage blog posts.
4. Generate new blog content using the AI-powered content generation feature.

### Screenshots

#### Home Page
![Home Page]!(https://github.com/nandu1331/AI-Blog-Generator/assets/116256681/ee1ec094-a9e6-46b6-a39f-3f1b9fdc07eb)

#### Dashboard
![Dashboard](images/dashboard.png)

#### New Blog Post
![New Blog Post](images/new_blog_post.png)

## How It Works

1. **User Authentication**: Users register and log in to access the application.
2. **Creating a Blog Post**:
    - Navigate to the 'New Blog Post' section.
    - Fill in the title and content of the blog post.
    - Use the AI generation feature to create content based on a prompt.
3. **AI Content Generation**:
    - Users provide a prompt or topic for the blog post.
    - The application sends the prompt to the OpenAI API.
    - The API returns generated content, which is then inserted into the blog post editor.
4. **Managing Posts**:
    - Users can edit or delete their posts from the dashboard.
    - Posts can be categorized for better organization.
5. **Publishing**:
    - Once satisfied, users can publish their posts to be viewed by others.

## Configuration

Configuration settings are primarily managed in `settings.py`. Key settings include:

- **Database**: Configure your database connection.
- **Email**: Set up email backend for sending notifications.
- **Static Files**: Configure static file handling for production.

## Contributing

We welcome contributions to the AI Blog Article Generator! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

Be sure to replace placeholder text (like `yourusername`, `your_mysql_user`, etc.) with your actual information.
