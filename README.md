## Django Authentication Example

A comprehensive Django REST Framework authentication example implementing JWT (JSON Web Token) authentication with a custom user model. This project demonstrates best practices for building secure authentication systems in Django applications.

### Features

- Custom User model using email as the primary identifier
- JWT (JSON Web Token) based authentication
- REST API endpoints for user management
- Email-based authentication 
- CORS support for frontend integration
- API documentation with Swagger/OpenAPI
- Secure password handling
- PostgreSQL database support

### Technologies Used

- Django 5.2.4
- Django REST Framework 3.16.0
- djangorestframework-simplejwt 5.5.0
- PostgreSQL (via psycopg2-binary)
- django-cors-headers 4.7.0
- drf-yasg (for API documentation)
- python-decouple (for environment variables)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/sahilverse/Django-Authentication-Example.git
cd Django-Authentication-Example
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the root directory with the following variables:
```
DJANGO_SECRET_KEY=your_secret_key_here
DEBUG=True


DB_ENGINE=your.db.engine.here
DB_NAME=your_db_name_here
DB_USER=your_db_user_here
DB_PASSWORD=your_db_password_here
DB_PORT=your_db_port_here
DB_HOST=your_db_host_here
USE_POSTGRES=True


REDIS_HOST=your_redis_host_here
REDIS_PORT=your_redis_port_here

```

5. Run migrations:
```bash
python manage.py migrate
```

6. Create a superuser:
```bash
python manage.py createsuperuser
```

7. Run the development server:
```bash
python manage.py runserver
```

### API Endpoints

- `POST /api/user/register/`: Register a new user
- `POST /api/user/login/`: Login and obtain JWT tokens
- `POST /api/user/token/refresh/`: Refresh JWT token

For complete API documentation, visit `/` or `/redoc/` after running the server.

### Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Acknowledgments

- Django documentation
- Django REST Framework documentation
- JWT authentication best practices