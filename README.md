# AkshaMart - Enterprise Ecommerce Platform

🌍 **Rooted in India, Loved Worldwide**

A production-ready, enterprise-grade ecommerce platform built with modern technologies, scalable architecture (Amazon/Flipkart standards), and comprehensive security measures.

## 🏗️ Architecture Overview

```
aksha-mart/
├── packages/
│   ├── backend/          # NestJS + PostgreSQL + GraphQL
│   ├── frontend/         # Next.js + TypeScript + TailwindCSS
│   ├── shared/           # Shared types and utilities
│   └── admin/            # Admin panel (Next.js)
├── infrastructure/       # Docker, K8s, Nginx configs
├── deployment/           # CI/CD, deployment scripts
├── docs/                 # API docs, deployment guide
└── docker-compose.yml    # Local development setup
```

## 🚀 Tech Stack

### Frontend
- **Framework**: Next.js 14+ with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS + ShadCN UI
- **State Management**: Redux Toolkit
- **Features**: SSR, PWA, Mobile-first

### Backend
- **Runtime**: Node.js 20+
- **Framework**: NestJS with dependency injection
- **APIs**: REST + GraphQL
- **ORM**: Prisma
- **Database**: PostgreSQL
- **Cache**: Redis
- **Security**: Helmet, JWT, RBAC

### DevOps
- **Containerization**: Docker
- **Orchestration**: Kubernetes-ready
- **CI/CD**: GitHub Actions
- **Monitoring**: Prometheus + Grafana
- **Logging**: ELK Stack

## ✨ Key Features

### User Features
✅ Multi-factor authentication (Email, OTP, Google)
✅ Advanced product search with ElasticSearch
✅ Smart recommendations and personalization
✅ Wishlist and cart management
✅ Secure checkout with multiple payment options
✅ Order tracking and invoice generation
✅ Product reviews and ratings
✅ Multi-address support
✅ Real-time notifications

### Seller Features
✅ Seller dashboard with analytics
✅ Inventory management
✅ Order management system
✅ Revenue tracking and reporting
✅ Seller approval workflow

### Admin Features
✅ Advanced analytics dashboard
✅ Product and user management
✅ Seller approval and control
✅ Refund management
✅ CMS and banner management
✅ Coupon engine
✅ Tax configuration
✅ Audit logs and monitoring

### Payment Integration
✅ Razorpay integration
✅ Stripe integration
✅ Cash on Delivery (COD)
✅ Webhook verification
✅ Payment failure recovery

### Logistics
✅ Shipping API integration
✅ Real-time delivery tracking
✅ Pincode availability check
✅ Dynamic shipping charges

### AI/ML Features
✅ AI-powered recommendations
✅ Personalized product feed
✅ Similar product engine
✅ AI chatbot support

## 🔐 Security Standards

- ✅ OWASP Top 10 compliance
- ✅ JWT-based authentication
- ✅ Role-based access control (RBAC)
- ✅ Secure password hashing (bcrypt)
- ✅ CSRF/XSS protection
- ✅ SQL Injection prevention
- ✅ Rate limiting and throttling
- ✅ Encryption for sensitive data
- ✅ Audit logging
- ✅ 2FA support
- ✅ Secure headers
- ✅ Environment variable management

## 📊 Database Schema

Comprehensive PostgreSQL schema with:
- Optimized indexes
- Referential integrity
- Audit trails
- Soft deletes support
- Caching strategies

## 🧪 Testing

- ✅ Unit tests (Jest)
- ✅ Integration tests
- ✅ E2E tests (Cypress)
- ✅ API testing
- ✅ Security testing
- ✅ Performance testing

## 📈 Performance Optimization

- ✅ Server-side rendering (SSR)
- ✅ Static generation (SSG)
- ✅ Code splitting
- ✅ Image optimization
- ✅ Lazy loading
- ✅ Redis caching
- ✅ CDN optimization
- ✅ Database query optimization
- ✅ SEO optimization

## 🚀 Quick Start

### Prerequisites
- Node.js 20+
- PostgreSQL 15+
- Redis 7+
- Docker & Docker Compose

### Development Setup

```bash
# Clone the repository
git clone https://github.com/vrahmdevtiwari/aksha-mart.git
cd aksha-mart

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env.local

# Start development services (PostgreSQL, Redis)
docker-compose up -d

# Run database migrations
npm run db:migrate

# Seed initial data
npm run db:seed

# Start development servers
npm run dev
```

### Access Points
- **Frontend**: http://localhost:3000
- **API**: http://localhost:3001
- **Admin**: http://localhost:3002
- **GraphQL**: http://localhost:3001/graphql
- **Kibana**: http://localhost:5601
- **Mailhog**: http://localhost:8025

### Production Deployment

See [DEPLOYMENT.md](./docs/DEPLOYMENT.md) for:
- Docker build and push
- Kubernetes deployment
- CI/CD pipeline configuration
- Environment setup
- Monitoring and logging

## 📚 Documentation

- [API Documentation](./docs/API.md) - REST and GraphQL endpoints
- [Deployment Guide](./docs/DEPLOYMENT.md) - Production deployment
- [Architecture Guide](./docs/ARCHITECTURE.md) - System design
- [Database Schema](./docs/DATABASE.md) - Schema design and migrations
- [Security Best Practices](./docs/SECURITY.md) - Security guidelines
- [Contributing Guide](./CONTRIBUTING.md) - Development standards

## 🔗 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/google` - Google OAuth login
- `POST /api/auth/verify-otp` - OTP verification
- `POST /api/auth/refresh` - Token refresh
- `POST /api/auth/logout` - Logout

### Products
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product details
- `GET /api/products/search` - Search products
- `POST /api/products` - Create product (admin/seller)

### Cart & Checkout
- `GET /api/cart` - Get cart
- `POST /api/cart/items` - Add to cart
- `PUT /api/cart/items/:id` - Update cart item
- `DELETE /api/cart/items/:id` - Remove from cart
- `POST /api/checkout` - Initiate checkout

### Orders
- `GET /api/orders` - Get user orders
- `GET /api/orders/:id` - Get order details
- `POST /api/orders/:id/cancel` - Cancel order
- `POST /api/orders/:id/return` - Request return

### Payments
- `POST /api/payments/razorpay/create-order` - Create Razorpay order
- `POST /api/payments/razorpay/verify` - Verify Razorpay payment
- `POST /api/payments/stripe/create-session` - Create Stripe session
- `POST /api/payments/webhook` - Payment webhook handler

### Admin
- `GET /api/admin/analytics` - Dashboard analytics
- `GET /api/admin/users` - Manage users
- `GET /api/admin/sellers` - Manage sellers
- `GET /api/admin/orders` - Manage orders
- `POST /api/admin/refunds` - Process refunds

### GraphQL
- `POST /graphql` - GraphQL endpoint
- Interactive schema available at `/graphql/playground`

## 📊 Monitoring & Logging

- **Prometheus**: Metrics collection at `/metrics`
- **Grafana**: Dashboard visualization
- **ELK Stack**: Centralized logging
- **Sentry**: Error tracking and monitoring

## 🛠️ Development Commands

```bash
# Development
npm run dev              # Start all services
npm run dev:frontend    # Frontend only
npm run dev:backend     # Backend only
npm run dev:admin       # Admin only

# Database
npm run db:migrate      # Run migrations
npm run db:seed         # Seed data
npm run db:reset        # Reset database

# Testing
npm run test            # Run all tests
npm run test:unit       # Unit tests
npm run test:e2e        # E2E tests
npm run test:coverage   # Coverage report

# Building
npm run build           # Build all packages
npm run build:frontend  # Build frontend
npm run build:backend   # Build backend
npm run build:admin     # Build admin

# Production
npm run start           # Start production servers
npm run docker:build    # Build Docker images
npm run docker:up       # Start Docker services
npm run docker:down     # Stop Docker services
npm run docker:push     # Push to registry

# Code Quality
npm run lint            # Run linter
npm run format          # Format code
npm run type-check      # Type checking
```

## 📁 Project Structure

```
packages/backend/
├── src/
│   ├── common/           # Shared utilities, guards, pipes
│   ├── config/           # Configuration modules
│   ├── database/         # Prisma schema, migrations
│   ├── features/         # Feature modules
│   │   ├── auth/
│   │   ├── users/
│   │   ├── products/
│   │   ├── orders/
│   │   ├── payments/
│   │   └── admin/
│   ├── infrastructure/   # External services
│   ├── graphql/          # GraphQL schema and resolvers
│   └── main.ts           # Application entry
├── test/                 # Test files
└── prisma/               # Database migrations

packages/frontend/
├── app/                  # Next.js app directory
│   ├── (auth)/          # Auth routes
│   ├── (store)/         # Store routes
│   ├── admin/           # Admin dashboard
│   └── layout.tsx       # Root layout
├── components/           # Reusable components
├── hooks/                # Custom React hooks
├── lib/                  # Utilities
├── redux/                # Redux store
├── services/             # API services
└── styles/               # Global styles

packages/admin/
├── app/                  # Admin dashboard app
├── components/           # Admin components
├── hooks/                # Admin hooks
└── lib/                  # Admin utilities
```

## 🤝 Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for development guidelines, code standards, and PR process.

## 📄 License

MIT License - See [LICENSE](./LICENSE) file for details.

## 📞 Support

For issues, feature requests, and questions:
- GitHub Issues: [Report Issues](https://github.com/vrahmdevtiwari/aksha-mart/issues)
- Documentation: [Full Docs](./docs)
- Email: support@aksha-mart.com

## 🌟 Acknowledgments

Built with enterprise-grade standards inspired by Amazon, Flipkart, and industry best practices.

---

**AkshaMart** - Rooted in India, Loved Worldwide 🌍
