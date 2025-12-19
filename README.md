# Blog Platform - Node.js Workshop Project

A full-featured blog platform built with Node.js, Express, and MySQL. This project demonstrates core web development concepts including authentication, CRUD operations, file uploads, and database integration.

## Features

- 📝 **Blog Management**: Create, read, update, and delete blog posts
- 🔐 **User Authentication**: Secure registration and login system with bcrypt password hashing
- 📤 **File Uploads**: Upload and manage images for blog posts using Multer
- 🎨 **Responsive UI**: EJS templating with custom styling
- 🗄️ **Database Integration**: MySQL database with Sequelize ORM
- 🛣️ **RESTful Routes**: Clean and organized routing structure

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MySQL with Sequelize ORM
- **Templating**: EJS (Embedded JavaScript)
- **Authentication**: bcrypt for password hashing
- **File Upload**: Multer
- **Environment Variables**: dotenv

## Project Structure

```
NodeJsWorkshop/
├── app.js                  # Main application entry point
├── package.json            # Project dependencies and scripts
├── config/
│   └── dbConfig.js        # Database configuration
├── controllers/
│   ├── authController.js  # Authentication logic
│   └── blogController.js  # Blog CRUD operations
├── middleware/
│   └── multerConfig.js    # File upload configuration
├── models/
│   ├── index.js           # Sequelize initialization
│   ├── userModel.js       # User model
│   └── blogModel.js       # Blog post model
├── routes/
│   ├── authRoutes.js      # Authentication routes
│   └── blogRoutes.js      # Blog routes
├── views/
│   ├── layout.ejs         # Main layout template
│   ├── index.ejs          # Homepage
│   ├── blogs.ejs          # Blog listing page
│   ├── create.ejs         # Create blog form
│   ├── edit.ejs           # Edit blog form
│   ├── login.ejs          # Login page
│   ├── register.ejs       # Registration page
│   ├── about.ejs          # About page
│   ├── contact.ejs        # Contact page
│   └── partials/
│       ├── header.ejs     # Header component
│       └── footer.ejs     # Footer component
├── public/
│   ├── css/
│   │   └── styles.css     # Custom styles
│   └── assets/
│       └── images/        # Static images
└── uploads/               # User-uploaded files
```

## Prerequisites

Before running this project, make sure you have the following installed:

- Node.js (v14 or higher)
- npm (Node Package Manager)
- MySQL Server

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd NodeJsWorkshop
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory and add the following:
   ```env
   HOST=localhost
   USERNAME2=your_mysql_username
   PASSWORD=your_mysql_password
   PORT=3306
   DATABASE=blog_platform
   ```

4. **Set up the database**
   
   Create a MySQL database:
   ```sql
   CREATE DATABASE blog_platform;
   ```
   
   The application will automatically create tables using Sequelize models when you start the server.

5. **Start the server**
   ```bash
   node app.js
   ```
   
   The application will be available at `http://localhost:3000`

## Usage

### Authentication

- **Register**: Navigate to `/register` to create a new account
- **Login**: Navigate to `/login` to sign in

### Blog Management

- **View Blogs**: Visit the homepage to see all blog posts
- **Create Blog**: After logging in, navigate to `/create` to create a new blog post
- **Edit Blog**: Click on a blog post and select the edit option
- **Delete Blog**: Remove blog posts from the edit page

### Static Pages

- **About**: `/about` - Information about the platform
- **Contact**: `/contact` - Contact form

## API Routes

### Authentication Routes
- `GET /register` - Registration page
- `POST /register` - Create new user
- `GET /login` - Login page
- `POST /login` - Authenticate user

### Blog Routes
- `GET /` - Homepage with blog listing
- `GET /blogs` - View all blogs
- `GET /create` - Create blog form
- `POST /create` - Submit new blog
- `GET /edit/:id` - Edit blog form
- `POST /edit/:id` - Update blog
- `POST /delete/:id` - Delete blog

## Development

### Adding New Features

1. **Models**: Add new database models in the `models/` directory
2. **Controllers**: Create controller logic in `controllers/`
3. **Routes**: Define routes in the `routes/` directory
4. **Views**: Add EJS templates in the `views/` directory

### Database Migrations

This project uses Sequelize ORM. Models are automatically synced when the application starts. For production environments, consider using proper migrations.

## Security Features

- Password hashing using bcrypt
- Environment variables for sensitive data
- Input validation and sanitization
- Secure file upload handling

## Future Enhancements

- [ ] Add user session management with express-session
- [ ] Implement user profile pages
- [ ] Add comment functionality
- [ ] Implement pagination for blog listings
- [ ] Add search functionality
- [ ] Implement role-based access control
- [ ] Add image optimization
- [ ] Create API endpoints for mobile apps

## Troubleshooting

### Database Connection Issues
- Ensure MySQL server is running
- Verify credentials in `.env` file
- Check if the database exists

### File Upload Issues
- Ensure the `uploads/` directory has write permissions
- Check Multer configuration in `middleware/multerConfig.js`

### Port Already in Use
- Change the port in `app.js` if port 3000 is occupied
- Or kill the process using port 3000

## Contributing

This is a workshop project for learning purposes. Feel free to fork and experiment with new features!

## License

ISC

## Contact

For questions or feedback, please use the contact form at `/contact` or reach out through the repository.

---

**Happy Coding! 🚀**
