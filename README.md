# Clothing Exchange Platform

A modern web-based platform that enables users to exchange unused clothing through direct swaps or a point-based redemption system. Built with Node.js, Express, MongoDB, and React.

## 🌟 Features

### User Features
- **User Authentication**: Secure registration and login system
- **Item Management**: Add, edit, and delete clothing items
- **Exchange System**: 
  - Direct item-to-item swaps
  - Points-based redemption system
- **Search & Filter**: Advanced search with category, size, condition, and exchange type filters
- **User Dashboard**: Track items, exchanges, and points
- **Profile Management**: Edit profile information and view activity history

### Admin Features
- **Item Approval**: Review and approve/reject new item listings
- **User Management**: Manage user roles and ban/unban users
- **Platform Statistics**: View comprehensive platform analytics
- **Exchange Monitoring**: Track all exchange activities

### Technical Features
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Real-time Updates**: Live notifications and status updates
- **Image Upload**: Multiple image support with preview
- **Security**: JWT authentication, password hashing, and input validation
- **API Documentation**: RESTful API with comprehensive endpoints

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd clothing-exchange-platform
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Environment Setup**
   ```bash
   # Backend
   cd ../backend
   cp env.example .env
   # Edit .env with your configuration
   ```

5. **Database Setup**
   - Ensure MongoDB is running
   - Update the `MONGODB_URI` in your `.env` file

6. **Start the application**
   ```bash
   # Terminal 1 - Backend
   cd backend
   npm run dev

   # Terminal 2 - Frontend
   cd frontend
   npm start
   ```

7. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000

## 📁 Project Structure

```
clothing-exchange-platform/
├── backend/
│   ├── models/          # MongoDB schemas
│   ├── routes/          # API endpoints
│   ├── middleware/      # Authentication & validation
│   ├── uploads/         # Image storage
│   ├── server.js        # Main server file
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/  # Reusable UI components
│   │   ├── pages/       # Page components
│   │   ├── contexts/    # React contexts
│   │   └── App.js       # Main app component
│   ├── public/          # Static assets
│   └── package.json
└── README.md
```

## 🔧 Configuration

### Backend Environment Variables
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/clothing-exchange
JWT_SECRET=your-super-secret-jwt-key
NODE_ENV=development
```

### Frontend Configuration
The frontend automatically proxies API requests to the backend. Update the proxy in `package.json` if needed.

## 📚 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile

### Items
- `GET /api/items` - Get all approved items
- `GET /api/items/:id` - Get item by ID
- `POST /api/items` - Create new item
- `PUT /api/items/:id` - Update item
- `DELETE /api/items/:id` - Delete item
- `POST /api/items/:id/exchange` - Initiate exchange

### Users
- `GET /api/users/:id` - Get user profile
- `GET /api/users/:id/items` - Get user's items
- `GET /api/users/exchanges` - Get user's exchanges
- `PUT /api/users/exchanges/:id/respond` - Respond to exchange

### Admin
- `GET /api/admin/stats` - Platform statistics
- `GET /api/admin/pending-items` - Pending items
- `PUT /api/admin/items/:id/approve` - Approve/reject item
- `GET /api/admin/users` - Get all users
- `PUT /api/admin/users/:id/role` - Update user role
- `PUT /api/admin/users/:id/ban` - Ban/unban user

## 🎨 UI Components

The application uses a custom component library built with Tailwind CSS:

- **Cards**: Consistent card layouts
- **Buttons**: Primary, secondary, and danger variants
- **Forms**: Styled form inputs with validation
- **Modals**: Reusable modal components
- **Loading States**: Spinner and skeleton components

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt for password security
- **Input Validation**: Express-validator for data validation
- **CORS Protection**: Cross-origin resource sharing configuration
- **File Upload Security**: Image type and size validation

## 🚀 Deployment

### Backend Deployment
1. Set up environment variables
2. Install dependencies: `npm install`
3. Build: `npm run build`
4. Start: `npm start`

### Frontend Deployment
1. Install dependencies: `npm install`
2. Build: `npm run build`
3. Deploy the `build` folder to your hosting service

### Database
- Use MongoDB Atlas for cloud hosting
- Set up proper indexes for performance
- Configure backup and monitoring

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the documentation
- Review the API endpoints

## 🔮 Future Enhancements

- Real-time chat system
- Push notifications
- Advanced analytics
- Mobile app
- Payment integration
- Social features
- AI-powered recommendations 