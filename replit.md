# Hapo - Family Payments App

## Overview

Hapo is a modern family financial management application that enables secure and controlled spending for children while providing comprehensive monitoring and control tools for parents. The app features QR-code based payments, real-time transaction monitoring, spending limits, balance management, and a reward system. Built as a mobile-first progressive web application, it uses a dual-role system where users can switch between parent and child views to manage family finances effectively.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development patterns
- **Routing**: Wouter for lightweight client-side routing with role-based view switching
- **State Management**: TanStack React Query for server state management and caching
- **UI Framework**: Radix UI primitives with shadcn/ui components for accessible, consistent design
- **Styling**: Tailwind CSS with CSS variables for theming and responsive design
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js for the REST API server
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Authentication**: Replit Auth with OpenID Connect for secure user authentication
- **Session Management**: Express sessions with PostgreSQL session store for persistent login state
- **API Design**: RESTful endpoints with role-based access control and comprehensive error handling

### Database Design
- **User Management**: Hierarchical user model supporting parent-child relationships with role-based permissions
- **Financial Tracking**: Comprehensive transaction logging with categorization, merchant tracking, and spending analytics
- **Spending Controls**: Configurable daily and weekly limits with real-time enforcement
- **Notifications**: Event-driven notification system for transaction alerts and limit warnings
- **Session Storage**: Secure session persistence using PostgreSQL for scalability

### Mobile-First Design Pattern
- **Responsive Layout**: Mobile-optimized with desktop compatibility using Tailwind's responsive utilities
- **Touch Interface**: Bottom navigation with gesture-friendly controls optimized for mobile usage
- **Progressive Enhancement**: Core functionality works across all device sizes with enhanced features on larger screens

### Authentication Flow
- **OpenID Connect Integration**: Secure authentication through Replit's identity provider
- **Role-Based Access**: Dynamic role switching between parent and child modes with appropriate permission enforcement
- **Session Persistence**: Secure session management with automatic cleanup and configurable expiration

## External Dependencies

### Core Infrastructure
- **Database**: Neon PostgreSQL for managed database hosting with connection pooling
- **Authentication Provider**: Replit Auth for OpenID Connect identity management
- **Session Store**: PostgreSQL-backed session storage for scalable session management

### Frontend Libraries
- **UI Components**: Radix UI for accessible component primitives
- **Form Handling**: React Hook Form with Zod validation for type-safe form management
- **Date Management**: date-fns for consistent date formatting and manipulation
- **Icons**: Lucide React for consistent iconography throughout the application

### Development Tools
- **Code Quality**: TypeScript for static type checking and enhanced developer experience
- **Build Optimization**: ESBuild for fast server-side compilation and Vite for client bundling
- **Development Experience**: Replit-specific plugins for enhanced development workflow and error handling

### Payment Processing Architecture
- **QR Code Simulation**: Mock payment system for demonstration purposes (ready for real payment gateway integration)
- **Transaction Processing**: Atomic transaction handling with balance validation and limit enforcement
- **Real-time Updates**: Immediate UI updates with optimistic updates and error rollback capabilities