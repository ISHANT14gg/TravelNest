Travel Nest 🏡✈️
A full-stack web application for listing and discovering travel accommodations, built with Node.js, Express, MongoDB, and EJS templating.
📋 Features

User Authentication

Sign up and login functionality
Passport.js integration with local strategy
Session management with secure cookies
Password hashing with passport-local-mongoose


Listing Management

Create, read, update, and delete (CRUD) travel listings
Image upload support with Multer
Filter listings by price and location
Owner-based listing permissions


Review System

Add reviews to listings
Author attribution for reviews
Delete reviews (authorized users only)


Flash Messages

Success and error notifications
User-friendly feedback system


Search & Filter

Search listings by location (case-insensitive)
Filter by maximum price



🛠️ Technologies Used

Backend:

Node.js
Express.js v5.1.0
MongoDB with Mongoose v8.19.1


Authentication:

Passport.js
Passport-Local
Passport-Local-Mongoose


Template Engine:

EJS (Embedded JavaScript)
EJS-Mate for layouts


File Upload:

Multer v2.0.2
Cloudinary integration support


Middleware:

express-session
connect-flash
method-override
cookie-parser



📦 Installation

Clone the repository:

bash   git clone <your-repository-url>
   cd travel-nest

Install dependencies:

bash   npm install

Set up MongoDB:

Make sure MongoDB is running locally on mongodb://127.0.0.1:27017
Or update the connection string in App.js


Initialize sample data (optional):

bash   node init.js
Note: Update the ownerId in init.js with a valid user ID from your database

Start the server:

bash   node App.js
```

6. **Access the application:**
   Open your browser and navigate to `http://localhost:8080`

## 🗂️ Project Structure
```
travel-nest/
├── models/
│   ├── listing.js      # Listing schema
│   ├── review.js       # Review schema
│   └── user.js         # User schema
├── middleware/
│   └── middleware.js   # Authentication middleware
├── utils/
│   ├── wrapasync.js    # Async error handler
│   └── ExpressErrors.js # Custom error class
├── views/
│   ├── listings/       # Listing views
│   ├── users/          # User authentication views
│   └── error.ejs       # Error page
├── public/             # Static assets (CSS, JS, images)
├── uploads/            # Uploaded images storage
├── App.js              # Main application file
├── init.js             # Database seeding script
└── package.json        # Project dependencies
```

## 🔑 Key Routes

### Authentication
- `GET /signup` - Sign up page
- `POST /signup` - Register new user
- `GET /login` - Login page
- `POST /login` - Authenticate user
- `GET /logout` - Logout user

### Listings
- `GET /listings` - View all listings (with optional filters)
- `GET /listings/new` - Create new listing form (auth required)
- `POST /listings` - Create new listing (auth required)
- `GET /listings/:id` - View single listing
- `GET /listings/:id/edit` - Edit listing form (auth required)
- `PUT /listings/:id` - Update listing (auth required)
- `DELETE /listings/:id` - Delete listing (auth required)

### Reviews
- `POST /listings/:id/reviews` - Add review (auth required)
- `DELETE /listings/:id/reviews/:reviewId` - Delete review (auth required)

## 🔒 Authentication & Authorization

- Users must be logged in to create, edit, or delete listings
- Only listing owners can edit or delete their listings
- Flash messages provide feedback for authentication actions
- Sessions persist for 7 days

## 🎨 Sample Data

The `init.js` script includes 30 sample listings featuring:
- Beachfront cottages
- Mountain retreats
- Urban lofts
- Historic villas
- Luxury penthouses
- And more!

Each listing includes:
- Title and description
- Image URL
- Price per night
- Location and country
- Owner reference

## 🚀 Environment Setup

For production deployment, consider:

1. **Environment Variables:**
```
   PORT=8080
   MONGODB_URI=your_mongodb_connection_string
   SESSION_SECRET=your_secret_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret

Update session configuration in App.js for production
Set up Cloudinary for image storage instead of local uploads

🐛 Error Handling

Custom error handling middleware
Async error wrapper for database operations
404 handler for unknown routes
User-friendly error pages

👤 Author
Suraj Rawat
📝 License
ISC
🤝 Contributing
Contributions, issues, and feature requests are welcome!

Happy Traveling! ✈️🌍Claude is AI and can make mistakes. Please double-check responses.
