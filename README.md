# CRM Pro - Professional Customer Relationship Management System

A modern, secure CRM application built with React and Express, featuring comprehensive customer management, deal pipeline tracking, and analytics dashboard.

## Features

### 🔐 Secure Authentication
- Integrated authentication system with session management
- User-specific data access controls
- Secure login/logout functionality

### 👥 Customer Management
- Add, view, edit, and search customer companies
- Comprehensive customer profiles with industry classification
- Advanced search and filtering capabilities

### 💼 Deal Pipeline
- Track sales opportunities through customizable stages
- Visual pipeline representation with stage-based organization
- Deal value tracking and conversion analytics

### 📞 Contact Management
- Manage business contacts with detailed information
- Link contacts to customer companies
- Role-based contact organization

### 📊 Advanced Analytics Dashboard
- Real-time metrics and KPI tracking
- Interactive sales pipeline visualization
- Recent activity feed with filtering
- Enhanced task management with time tracking
- Revenue and growth analytics with charts

### 📧 Email Integration
- Email template management for consistent communication
- Send personalized emails to customers and contacts
- Email tracking and delivery status monitoring
- Template-based communication workflows

### 🎯 Enhanced Task Management
- Create and track tasks with estimated/actual hours
- Priority-based task organization with tags
- Completion tracking and time analysis
- Upcoming task notifications and reminders

### 🔍 Advanced Search & Filtering
- Complex multi-field search capabilities
- Date range filtering with calendar interface
- Saved searches for frequently used filters
- Real-time sorting and pagination

### 📈 Comprehensive Reporting
- Sales analytics with conversion tracking
- Customer analytics and lifetime value
- Pipeline performance analysis
- Activity reports and engagement metrics
- Interactive charts and data visualization

### 📤 Data Export
- Export to multiple formats (CSV, PDF, Excel)
- Apply current filters to exported data
- Background export job processing
- Download management and file tracking

### ⚙️ Customization Features
- Custom fields for customers, contacts, and deals
- Pipeline stage customization with colors and probabilities
- Activity type management with icons
- Flexible field ordering and requirements

## Technology Stack

### Frontend
- **React** - Modern UI framework
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **shadcn/ui** - Professional component library
- **TanStack Query** - Data fetching and caching
- **React Hook Form** - Form management
- **Wouter** - Lightweight routing
- **Recharts** - Data visualization

### Backend
- **Express.js** - Web application framework
- **TypeScript** - Server-side type safety
- **PostgreSQL** - Relational database
- **Drizzle ORM** - Type-safe database toolkit
- **Passport.js** - Authentication middleware
- **Zod** - Schema validation

## Security Features

- Input sanitization and validation using Zod schemas
- SQL injection prevention through parameterized queries
- Session-based authentication with secure cookies
- User-specific data access controls
- CSRF protection and secure headers

## Getting Started

### Prerequisites
- Node.js 18+ 
- PostgreSQL database
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/crm-pro.git
cd crm-pro
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```env
DATABASE_URL=your_postgresql_connection_string
SESSION_SECRET=your_secure_session_secret
REPL_ID=your_replit_app_id
ISSUER_URL=https://replit.com/oidc
REPLIT_DOMAINS=your-domain.replit.dev
```

4. Initialize the database:
```bash
npm run db:push
```

5. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Application pages
│   │   ├── hooks/          # Custom React hooks
│   │   └── lib/            # Utility functions
├── server/                 # Express backend
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API route definitions
│   ├── storage.ts         # Data access layer
│   ├── db.ts              # Database configuration
│   └── replitAuth.ts      # Authentication setup
├── shared/                 # Shared types and schemas
│   └── schema.ts          # Database schema and types
└── package.json           # Project dependencies
```

## Database Schema

The application uses PostgreSQL with the following main tables:
- `users` - User authentication and profiles
- `customers` - Customer company information
- `contacts` - Individual contact records
- `deals` - Sales opportunity tracking
- `activities` - User activity logging
- `tasks` - Task management
- `sessions` - Secure session storage

## API Endpoints

### Authentication
- `GET /api/auth/user` - Get current user
- `GET /api/login` - Initiate login flow
- `GET /api/logout` - User logout

### Customers
- `GET /api/customers` - List all customers
- `POST /api/customers` - Create new customer
- `GET /api/customers/:id` - Get customer details
- `PATCH /api/customers/:id` - Update customer
- `DELETE /api/customers/:id` - Delete customer

### Deals
- `GET /api/deals` - List all deals
- `POST /api/deals` - Create new deal
- `GET /api/deals/:id` - Get deal details
- `PATCH /api/deals/:id` - Update deal
- `DELETE /api/deals/:id` - Delete deal

### Contacts
- `GET /api/contacts` - List all contacts
- `POST /api/contacts` - Create new contact
- `PATCH /api/contacts/:id` - Update contact
- `DELETE /api/contacts/:id` - Delete contact

### Dashboard
- `GET /api/dashboard/metrics` - Get dashboard metrics
- `GET /api/dashboard/pipeline` - Get pipeline data

## Deployment

### Replit Deployment (Recommended)
1. Import this repository to Replit
2. Configure environment variables
3. Run `npm run db:push` to initialize database
4. Deploy using Replit's deployment feature

### Manual Deployment
1. Build the application: `npm run build`
2. Configure production environment variables
3. Deploy to your preferred hosting platform
4. Ensure PostgreSQL database is accessible

## Development

### Available Scripts
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run db:push` - Push schema changes to database
- `npm run db:studio` - Open Drizzle Studio

### Code Style
- TypeScript for type safety
- ESLint and Prettier for code formatting
- Consistent component architecture
- Separation of concerns between frontend and backend

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and add tests
4. Commit your changes: `git commit -am 'Add new feature'`
5. Push to the branch: `git push origin feature-name`
6. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For questions or issues, please open an issue on GitHub or contact the development team.

---

Built with ❤️ using modern web technologies for professional customer relationship management.