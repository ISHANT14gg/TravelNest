# 🏠 Travel Nest

> A full-stack web application for listing and discovering travel accommodations

Built with **Node.js** • **Express** • **MongoDB** • **EJS**

---

## ✨ Features

- 🔐 **User Authentication** - Secure signup/login with Passport.js
- 🏠 **Manage Listings** - Create, edit, delete travel accommodations
- 📸 **Image Upload** - Upload property images with Multer
- ⭐ **Review System** - Add and manage reviews
- 🔍 **Search & Filter** - Find listings by location and price
- 💬 **Flash Messages** - Real-time success/error notifications

---

## 🛠️ Tech Stack

**Backend:** Node.js • Express.js • MongoDB • Mongoose

**Authentication:** Passport.js • Passport-Local-Mongoose

**Template Engine:** EJS • EJS-Mate

**File Upload:** Multer • Cloudinary

**Other:** Express-Session • Connect-Flash • Method-Override

---

## 🚀 Quick Start

### Prerequisites
- Node.js (v18+)
- MongoDB (v6+)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/ISHANT14gg/travel-nest.git
cd travel-nest
```

2. **Install dependencies**
```bash
npm install
```

3. **Start MongoDB**
```bash
mongod
```

4. **Seed sample data** (Optional)
```bash
node init.js
```
> Note: Update `ownerId` in `init.js` after creating your first user

5. **Run the application**
```bash
node App.js
```

6. **Open your browser**
```
http://localhost:8080
```

---

## 📂 Project Structure

```
travel-nest/
├── models/              # Database schemas
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── middleware/          # Auth middleware
├── utils/               # Helper functions
├── views/               # EJS templates
│   ├── listings/
│   └── users/
├── public/              # Static files
├── uploads/             # Uploaded images
├── App.js               # Main app file
└── init.js              # Database seeder
```

---

## 🛣️ Main Routes

### Authentication
- `GET /signup` - Sign up page
- `POST /signup` - Create account
- `GET /login` - Login page
- `POST /login` - Authenticate
- `GET /logout` - Logout

### Listings
- `GET /listings` - View all listings
- `GET /listings/new` - Create listing (auth required)
- `POST /listings` - Save listing (auth required)
- `GET /listings/:id` - View single listing
- `PUT /listings/:id` - Update listing (owner only)
- `DELETE /listings/:id` - Delete listing (owner only)

### Reviews
- `POST /listings/:id/reviews` - Add review (auth required)
- `DELETE /listings/:id/reviews/:reviewId` - Delete review (author only)

---

## 🔐 Security Features

- 🔒 Password hashing with bcrypt
- 🎟️ Session-based authentication
- 👤 Owner-based authorization
- 🍪 Secure HTTP-only cookies
- ⏰ 7-day session expiry

---

## 🎨 Sample Data

The app includes **30 sample listings** with:
- 🏖️ Beach properties
- 🏔️ Mountain cabins
- 🏙️ City apartments
- 🏰 Historic villas

---

## ⚙️ Environment Variables

Create a `.env` file:

```env
PORT=8080
MONGODB_URI=mongodb://127.0.0.1:27017/wanderlust
SESSION_SECRET=your_secret_key
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

---

## 👨‍💻 Author

**Ishant Sharma**
- 📧 Email: ishant6589@gmail.com
- 💼 GitHub: [@ISHANT14gg](https://github.com/ISHANT14gg)

---

## 📄 License

ISC License

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the project
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

---

<div align="center">

**Made with ❤️ by Ishant Sharma**

⭐ Star this repo if you find it helpful!

📧 Questions? Reach out at ishant6589@gmail.com

</div>
