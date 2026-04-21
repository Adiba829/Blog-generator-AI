# AI Blog Generator

## Overview

AI Blog Generator is a Django-based web application that leverages artificial intelligence to transform YouTube video content into well-structured blog posts. By simply pasting a YouTube URL, the application transcribes the video's audio and generates a comprehensive, readable article automatically. This tool is perfect for content creators, marketers, educators, and bloggers looking to repurpose video content into written form efficiently.

## Features

- **YouTube Video Transcription**: Automatically transcribes audio from YouTube videos.
- **AI-Powered Blog Generation**: Uses advanced AI to create coherent and engaging blog posts from transcriptions.
- **User Authentication**: Secure login and signup functionality for user management.
- **Blog Management**: View all generated blogs and detailed blog pages.
- **Responsive UI**: Built with Tailwind CSS for a modern, mobile-friendly interface.
- **Admin Panel**: Django admin interface for content management.

## Technology Stack

- **Backend**: Django 5.2.5
- **Database**: SQLite (default Django database)
- **Frontend**: HTML, Tailwind CSS
- **AI Integration**: (To be implemented - e.g., OpenAI API for transcription and generation)

## Prerequisites

Before running this application, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package installer)
- Git (for cloning the repository)

## Installation

1. **Clone the Repository**

   ```bash
   git clone <repository-url>
   cd Blog-generator-AI-main/Backend
   ```

2. **Create a Virtual Environment** (Recommended)

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run Database Migrations**

   ```bash
   python manage.py migrate
   ```

5. **Create a Superuser** (For admin access)

   ```bash
   python manage.py createsuperuser
   ```

   Follow the prompts to create an admin user.

## Configuration

### Environment Variables

For production deployment, set the following environment variables:

- `DJANGO_SETTINGS_MODULE`: Set to `ai_blog_app.settings`
- `SECRET_KEY`: Generate a secure secret key for Django
- `DEBUG`: Set to `False` for production

### AI Integration Setup

To enable AI features, you'll need to integrate with an AI service (e.g., OpenAI). Add your API keys to the settings or environment variables.

## Usage

1. **Start the Development Server**

   ```bash
   python manage.py runserver
   ```

2. **Access the Application**

   Open your browser and navigate to `http://127.0.0.1:8000/`

3. **Generate a Blog**

   - On the homepage, paste a YouTube video URL into the input field.
   - Click the "Generate" button.
   - The application will process the video and display the generated blog post.

4. **User Management**

   - Register a new account or log in with existing credentials.
   - Access the admin panel at `http://127.0.0.1:8000/admin/` using superuser credentials.

## Project Structure

```
Backend/
├── ai_blog_app/
│   ├── ai_blog_app/
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── main.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   ├── blog_generator/
│   │   ├── __init__.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── models.py
│   │   ├── tests.py
│   │   ├── urls.py
│   │   ├── views.py
│   │   └── migrations/
│   ├── db.sqlite3
│   ├── manage.py
│   └── templates/
│       ├── all-blogs.html
│       ├── blog-detail.html
│       ├── index.html
│       ├── login.html
│       └── signup.html
├── requirements.txt
└── README.md
```

## API Endpoints

- `/`: Homepage with blog generation form
- `/admin/`: Django admin panel
- `/generate_blog`: POST endpoint for blog generation (to be implemented)

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Testing

Run the Django test suite:

```bash
python manage.py test
```

## Deployment

For production deployment:

1. Set `DEBUG = False` in `settings.py`
2. Configure a production database (e.g., PostgreSQL)
3. Use a WSGI server like Gunicorn
4. Set up a reverse proxy with Nginx
5. Configure environment variables securely

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Powered by Django
- UI styled with Tailwind CSS
- Inspired by the need for efficient content repurposing

## Contact

For questions or support, please open an issue on GitHub or contact the maintainers.

---

**Note**: This is a development version. AI integration and full functionality are still under development.