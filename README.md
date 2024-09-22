# FakeBook

FakeBook is a full-stack clone of the popular social media platform, Facebook. It provides all the core features you'd expect from a social media platform, such as user authentication, friend requests, timeline posts, media uploads, and real-time messaging. The project uses **Node.js** and **Express** for the backend API, **MongoDB** for data storage, and **React** for the frontend with hooks and functional components.

![App Screenshot](./Screenshot%202024-09-22%20at%2014.26.11.png)


![App Screenshot](./Screenshot%202024-09-22%20at%2014.26.03.png)


![App Screenshot](./Screenshot%202024-09-22%20at%2014.25.43.png)


## Table of Contents
- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

---

## Features

### User Authentication
- Sign up and Sign in using JWT-based authentication.
- Password encryption using **bcrypt** for secure password storage.

### User Profiles
- Create and update personal profiles including avatar, bio, and contact information.
- View profiles of other users, including posts, friends, and activities.

### Friend Requests
- Send and accept friend requests.
- View a list of current friends.
- Unfriend or block users as needed.

### Timeline & Posts
- Post images, videos, or text content to your personal timeline.
- Like, comment, and share posts from both friends and public users.
- View the timeline feed, sorted by recency and engagement.

### Media Uploads
- Upload images and videos to posts using **Multer** for file handling in **Node.js**.
- Support for file storage in **Cloudinary** (or local storage as a fallback).

### Chat & Messaging
- Real-time messaging between friends using **Socket.io**.
- View and search chat history.
- Notifications for new messages or friend requests.

### Notifications
- Get notified when someone likes, comments, or shares your post.
- Notification alerts for friend requests and message activities.

### Other Features
- **Post Privacy Settings**: Choose between public, friends-only, or private posts.
- **Search**: Search for users, friends, or posts.
- **User Activity Feed**: Track user activity like posting, commenting, and new friendships.
- **Responsive Design**: Fully responsive web application built with **React**.

---

## Technologies

### Backend:
- **Node.js**, **Express**, **MongoDB**, **Mongoose**, **JWT**, **bcrypt**, **Multer**, **Cloudinary**, **Socket.io**

### Frontend:
- **React**, **React Hooks**, **Redux**, **Axios**, **Bootstrap**

### Database:
- **MongoDB (NoSQL)**

### Authentication:
- **JWT (JSON Web Tokens)**

### Real-Time Features:
- **Socket.io** (for chat and notifications)

---

## Installation

To get started with FakeBook, clone the repository and install the dependencies for both the backend and frontend.

### Clone the repository:

```bash
git clone https://github.com/username/fakebook.git
cd facebook
```

### Install server-side dependencies:

```bash
cd backend
npm install
```

### Install client-side dependencies:

```bash
cd ../frontend
npm install
```

### Set up environment variables: Create a .env file in the backend directory with the following values:

```bash
MONGODB_URI=<Your MongoDB Connection String>
JWT_SECRET=<Your JWT Secret>
CLOUDINARY_API_KEY=<Cloudinary API Key>
CLOUDINARY_SECRET=<Cloudinary Secret>
```
### Run the application:

To start the backend server:
```bash
cd backend
npm run dev
```

### To start the frontend server:
```bash
cd frontend
npm start
```

## Usage
- Sign Up: Create a new account with your personal details.
- Create Profile: After signing in, set up your profile by uploading a picture, adding a bio, and providing other information.
- Find Friends: Search for users and send friend requests.
- Post on Your Timeline: Share posts, images, or videos with friends or the public.
- Chat: Send and receive real-time messages with your friends.
- Engage: Like, comment, and share posts from your friends or other users.

## API Endpoints
### Authentication
- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login an existing user
- User Profile
- GET /api/users/:id - Get user profile by ID
- PUT /api/users/:id - Update user profile

### Friends
- POST /api/friends/request - Send a friend request
- POST /api/friends/accept - Accept a friend request
- DELETE /api/friends/remove/:id - Remove a friend

### Posts
- POST /api/posts - Create a new post
- GET /api/posts - Get all posts (timeline)
- PUT /api/posts/:id/like - Like a post
- POST /api/posts/:id/comment - Comment on a post

### Messages
- GET /api/messages/:friendId - Get chat history
- POST /api/messages - Send a message

### Contributing
We welcome contributions from the community! Feel free to fork the repo, create a feature branch, and submit a pull request with your improvements or bug fixes.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
