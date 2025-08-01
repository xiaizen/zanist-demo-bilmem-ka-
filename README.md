Zanist - AI-Powered STEM News Platform
A comprehensive scientific research platform featuring the latest breakthroughs from leading universities worldwide.

Features
🔬 Research Articles - Latest scientific discoveries and breakthroughs
🏛️ University Profiles - Top 50 universities with detailed information
👨‍🔬 Professor Profiles - Leading researchers and their work
🏆 Nobel Prize Winners - Comprehensive database of laureates
📊 Analytics Dashboard - Admin panel with detailed insights
🔍 Advanced Search - Full-text search across all content
📧 Newsletter System - Automated email campaigns
🔐 Role-based Access - Secure authentication and authorization
Tech Stack
Frontend
React 18 with TypeScript
Tailwind CSS for styling
Framer Motion for animations
React Router for navigation
React Hook Form for form handling
Lucide React for icons
Backend
Supabase for database and authentication
Express.js API server
PostgreSQL with Row Level Security
Node.js runtime
Getting Started
Prerequisites
Node.js 18+
npm or yarn
Supabase account
Installation
Clone the repository

git clone <repository-url>
cd zanist
Install dependencies

npm install
Set up environment variables

cp .env.example .env
Fill in your Supabase credentials and other configuration.

Set up Supabase

Create a new Supabase project
Run the migrations in supabase/migrations/
Update your .env file with Supabase credentials
Seed the database (optional)

npm run seed
Start the development servers

# Start both frontend and backend
npm run start:full

# Or start individually
npm run dev        # Frontend only
npm run server:dev # Backend only
Project Structure
zanist/
├── src/                    # Frontend React application
│   ├── components/         # Reusable UI components
│   ├── pages/             # Page components
│   ├── services/          # API service layers
│   ├── hooks/             # Custom React hooks
│   ├── contexts/          # React contexts
│   ├── types/             # TypeScript type definitions
│   └── lib/               # Utility libraries
├── server/                # Backend API server
│   ├── routes/            # Express route handlers
│   ├── middleware/        # Express middleware
│   ├── config/            # Configuration files
│   ├── utils/             # Utility functions
│   ├── scripts/           # Database seeding scripts
│   └── docs/              # API documentation
├── supabase/              # Database migrations
│   └── migrations/        # SQL migration files
└── public/                # Static assets
API Documentation
Detailed API documentation is available in server/docs/API.md.

Key Endpoints
GET /api/articles - Get published articles
GET /api/categories - Get research categories
GET /api/universities - Get university data
GET /api/professors - Get professor profiles
GET /api/search - Global search functionality
POST /api/newsletter/subscribe - Newsletter subscription
Database Schema
The application uses PostgreSQL with the following main tables:

profiles - User accounts and roles
articles - Research articles and essays
categories - Research field categories
universities - University information
professors - Professor profiles and research
comments - Article comments
newsletter_subscriptions - Email subscribers
access_logs - User activity tracking
Authentication & Authorization
The platform supports role-based access control:

Visitor - Basic read access
Member - Can comment and bookmark
Moderator - Can manage content
Admin - Full system access
Development
Running Tests
npm test
Building for Production
npm run build
Environment Variables
Required environment variables:

VITE_SUPABASE_URL - Supabase project URL
VITE_SUPABASE_ANON_KEY - Supabase anonymous key
VITE_SUPABASE_SERVICE_ROLE_KEY - Supabase service role key
Optional for full functionality:

SMTP_HOST, SMTP_USER, SMTP_PASS - Email configuration
JWT_SECRET - JWT signing secret
Contributing
Fork the repository
Create a feature branch
Make your changes
Add tests if applicable
Submit a pull request
License
This project is licensed under the MIT License.

Support
For support, email contact@zanist.com or create an issue in the repository.
