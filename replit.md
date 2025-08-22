# Replit Configuration

## Overview

This is a full-stack web application for user management built with React, Express.js, and PostgreSQL. The system provides role-based authentication with admin and user dashboards, user profile management, and comprehensive CRUD operations for user accounts. It features a modern UI built with Tailwind CSS and shadcn/ui components, type-safe database operations using Drizzle ORM, and secure authentication with JWT tokens and bcrypt password hashing.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **React 18** with TypeScript for type safety and modern development
- **Vite** as the build tool and development server for fast hot module replacement
- **Wouter** for lightweight client-side routing instead of React Router
- **TanStack Query** for server state management, caching, and data fetching
- **React Hook Form** with Zod validation for form handling and validation
- **Tailwind CSS** with shadcn/ui component library for consistent, accessible UI components
- **Component structure**: Organized into pages, components/ui (reusable components), components/layout (layout components), and components/modals

### Backend Architecture
- **Express.js** server with TypeScript for API endpoints and middleware
- **RESTful API design** with clear separation of concerns
- **Middleware-based architecture** for authentication, error handling, and logging
- **Modular routing** with dedicated route handlers for auth and admin operations
- **Service layer** for email functionality and business logic separation
- **Storage abstraction layer** with interface-based design for database operations

### Authentication & Authorization
- **JWT-based authentication** with 7-day token expiration
- **Role-based access control** (admin/user roles)
- **Bcrypt password hashing** with salt rounds for security
- **Token verification middleware** for protected routes
- **Admin-only endpoints** with additional authorization checks
- **Session management** with local storage for token persistence

### Database Design
- **PostgreSQL** with Neon serverless database for scalability
- **Drizzle ORM** for type-safe database operations and migrations
- **User schema** with comprehensive fields including roles, status, and verification
- **Enum types** for roles (admin/user) and status (active/inactive/pending)
- **UUID primary keys** with auto-generation
- **Timestamp tracking** for created/updated dates and last login

### Data Validation
- **Zod schemas** shared between client and server for consistent validation
- **Type inference** from Zod schemas to ensure type safety
- **Runtime validation** on both frontend forms and backend API endpoints
- **Custom validation rules** for password complexity and email formats

### UI/UX Design
- **Responsive design** with mobile-first approach using Tailwind breakpoints
- **Accessible components** using Radix UI primitives
- **Dark mode support** built into the design system
- **Toast notifications** for user feedback on actions
- **Loading states** and error handling throughout the application
- **Data tables** with pagination, search, and filtering capabilities

## External Dependencies

### Core Framework Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL database driver for Neon
- **drizzle-orm**: Type-safe ORM for database operations
- **drizzle-kit**: Database migration and introspection tools

### Authentication & Security
- **jsonwebtoken**: JWT token generation and verification
- **bcrypt**: Password hashing and comparison
- **@types/bcrypt** and **@types/jsonwebtoken**: TypeScript definitions

### Frontend Libraries
- **@tanstack/react-query**: Server state management and caching
- **@hookform/resolvers**: Form validation resolvers for React Hook Form
- **wouter**: Lightweight routing library
- **@radix-ui/react-***: Accessible component primitives (30+ components)
- **class-variance-authority**: Component variant management
- **clsx**: Conditional CSS class utility
- **tailwind-merge**: Tailwind class merging utility

### UI & Styling
- **tailwindcss**: Utility-first CSS framework
- **postcss**: CSS processing tool
- **autoprefixer**: CSS vendor prefix automation
- **lucide-react**: Icon library for consistent iconography

### Development Tools
- **vite**: Build tool and development server
- **@vitejs/plugin-react**: React support for Vite
- **typescript**: Type checking and compilation
- **tsx**: TypeScript execution for development
- **esbuild**: Fast JavaScript bundler for production builds

### Email Services
- **nodemailer**: Email sending functionality for user verification
- **connect-pg-simple**: PostgreSQL session store (configured but not actively used)

### Utility Libraries
- **date-fns**: Date manipulation and formatting
- **cmdk**: Command palette component
- **nanoid**: Unique ID generation
- **ws**: WebSocket support for database connections