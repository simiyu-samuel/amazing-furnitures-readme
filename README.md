# Amazing Furnitures E-commerce Platform

A modern, full-stack furniture e-commerce platform built with React, TypeScript, and Supabase. Features include customer shopping, admin management, M-Pesa payment integration, and comprehensive order management.

![Platform Preview](https://images.pexels.com/photos/1350789/pexels-photo-1350789.jpeg)

## 🚀 Features

### Customer Features
- **Product Catalog**: Browse furniture with advanced filtering and search
- **Shopping Cart**: Persistent cart with real-time updates
- **User Authentication**: Secure login/register with profile management
- **Order Management**: Track orders with real-time status updates
- **Payment Options**: M-Pesa integration and Pay Later option
- **Product Reviews**: Rate and review purchased products
- **Responsive Design**: Optimized for mobile, tablet, and desktop

### Admin Features
- **Dashboard**: Sales analytics and business insights
- **Product Management**: CRUD operations with inventory tracking
- **Order Management**: Process and track customer orders
- **Customer Management**: View customer profiles and order history
- **Analytics**: Revenue reports and product performance metrics

### Technical Features
- **M-Pesa Integration**: Real STK Push payments via Daraja API
- **Real-time Updates**: Live inventory and order status updates
- **Security**: Row Level Security (RLS) with Supabase
- **Performance**: Optimized queries and lazy loading
- **Scalability**: Modular architecture for easy expansion

## 🛠️ Technology Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Backend**: Supabase (PostgreSQL, Auth, Real-time)
- **State Management**: Zustand
- **Form Handling**: React Hook Form + Zod validation
- **UI Components**: Headless UI, Lucide React icons
- **Payment**: M-Pesa Daraja API
- **Deployment**: Netlify (Frontend), Supabase (Backend)

## 📋 Prerequisites

- Node.js 18+ and npm
- Supabase account
- M-Pesa Developer account (for payments)

## 🚀 Quick Start

### 1. Extract the downloaded zip and Install
```bash
cd amazing-furnitures
npm install
```

### 2. Environment Setup
Create `.env` file in the root directory:
```env
# Supabase Configuration
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key

# M-Pesa Configuration
VITE_MPESA_CONSUMER_KEY=your_mpesa_consumer_key
VITE_MPESA_CONSUMER_SECRET=your_mpesa_consumer_secret
VITE_MPESA_ENVIRONMENT=sandbox
VITE_MPESA_BUSINESS_SHORT_CODE=174379
VITE_MPESA_PASSKEY=your_mpesa_passkey
VITE_MPESA_CALLBACK_URL=https://your-domain.com/api/mpesa/callback
```

### 3. Database Setup
1. Create a new Supabase project
2. Run the migration files in `supabase/migrations/` in order
3. Enable Row Level Security (RLS) on all tables
4. Configure authentication settings

### 4. Run Development Server
```bash
npm run dev
```

Visit `http://localhost:5173` to see the application.

## 📁 Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── Layout/         # Header, Footer, Layout
│   ├── Product/        # Product-related components
│   └── UI/             # Base UI components
├── hooks/              # Custom React hooks
├── lib/                # Utilities and configurations
├── pages/              # Page components
│   ├── Admin/          # Admin panel pages
│   └── ...             # Customer pages
├── services/           # External service integrations
├── store/              # State management
└── types/              # TypeScript type definitions
```

## 🗄️ Database Schema

### Core Tables
- **profiles**: User profiles extending Supabase auth
- **categories**: Product categories
- **products**: Furniture products with specifications
- **orders**: Customer orders with status tracking
- **order_items**: Individual items in orders
- **cart**: Shopping cart items
- **reviews**: Product reviews and ratings
- **mpesa_transactions**: M-Pesa payment tracking

## 🔐 Authentication & Security

- **Supabase Auth**: Email/password authentication
- **Row Level Security**: Database-level access control
- **Role-based Access**: Customer and Admin roles
- **Input Validation**: Zod schemas for all forms
- **CORS Protection**: Configured for production

## 💳 Payment Integration

### M-Pesa STK Push
1. Customer selects M-Pesa payment
2. System initiates STK Push request
3. Customer receives prompt on phone
4. Payment confirmation updates order status
5. Receipt generated automatically

### Pay Later Option
- Orders created without immediate payment
- Admin can track unpaid orders
- Customers can pay later from dashboard

## 🎨 UI/UX Features

- **Responsive Design**: Mobile-first approach
- **Dark/Light Mode**: System preference detection
- **Loading States**: Skeleton loaders and spinners
- **Error Handling**: User-friendly error messages
- **Accessibility**: ARIA labels and keyboard navigation
- **Animations**: Smooth transitions and micro-interactions

## 📱 Mobile Optimization

- Touch-friendly interface
- Optimized images for mobile
- Progressive Web App features
- Offline functionality (coming soon)

## 🔧 Development

### Available Scripts
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
```

### Code Quality
- TypeScript strict mode
- ESLint configuration
- Prettier formatting
- Husky pre-commit hooks

## 🚀 Deployment

### Frontend (Netlify)
1. Connect repository to Netlify
2. Set environment variables
3. Deploy automatically on push

### Backend (Supabase)
- Automatic scaling
- Global CDN
- Real-time subscriptions
- Built-in monitoring

## 📊 Analytics & Monitoring

- Order tracking and analytics
- Product performance metrics
- Customer behavior insights
- Revenue reporting
- Error monitoring

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support, email support@amazingfurnitures.com or join our Slack channel.

## 🙏 Acknowledgments

- [Supabase](https://supabase.com) for the backend infrastructure
- [Tailwind CSS](https://tailwindcss.com) for the styling system
- [Lucide](https://lucide.dev) for the beautiful icons
- [Pexels](https://pexels.com) for the stock images

---

**Built with love by Samuel Simiyu**
