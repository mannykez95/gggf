# BudPal.world - Cannabis Trading Card Game Platform

## Overview

BudPal is a cannabis-themed trading card collection game featuring strain-based collectible cards with rarity mechanics. The platform presents a landing page for "Seed Drop 001," a limited edition collection of 500 exclusive founder packs containing cannabis strain cards. The application combines gaming mechanics (collect, roll, flex, unlock) with community building around cannabis culture.

The project is built as a modern web application with a React frontend and Express backend, designed for rapid deployment and waitlist collection to validate market demand before full product launch.

## Recent Changes

### September 22, 2025 - Major Asset Cleanup
- **Comprehensive File Optimization**: Removed 94 unused files (75 images + 19 text files) from attached_assets directory
- **Preserved Core Assets**: Kept only 33 files that are actually referenced in the codebase via @assets imports
- **Verified Functionality**: All pages tested and confirmed working with no broken images or 404 errors
- **Project Optimization**: Significantly reduced project bloat while maintaining full website functionality

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Styling**: Tailwind CSS with shadcn/ui component library for consistent, modern UI components
- **State Management**: TanStack Query (React Query) for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework for RESTful API endpoints
- **Database ORM**: Drizzle ORM for type-safe database operations and schema management
- **API Design**: RESTful endpoints for waitlist management (/api/waitlist, /api/waitlist/count)
- **Validation**: Zod for runtime type validation and data sanitization
- **Development**: Hot module replacement with Vite dev server integration

### Database Architecture
- **Database**: PostgreSQL configured for cloud deployment
- **Connection**: Neon serverless PostgreSQL with connection pooling
- **Schema**: 
  - Users table for authentication (prepared for future expansion)
  - Waitlist table for email collection with metadata (IP, user agent, source tracking)
- **Migrations**: Drizzle Kit for schema versioning and database migrations

### Design System
- **Color Palette**: Cannabis-themed green gradients (Deep Forest Green, Warm Cannabis Green) with accent colors (Sunset Orange, Soft Sage)
- **Typography**: Inter for body text, Space Grotesk for headings
- **Component Library**: Custom components built on Radix UI primitives
- **Responsive Design**: Mobile-first approach with Tailwind breakpoints

### Development Workflow
- **TypeScript Configuration**: Strict type checking across client and server
- **Path Aliases**: Clean imports with @ for client, @shared for common types
- **Asset Management**: Static assets in attached_assets directory
- **Environment**: Separate development and production configurations

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL database connection
- **drizzle-orm**: Type-safe ORM with PostgreSQL dialect
- **@tanstack/react-query**: Server state management and caching
- **express**: Web framework for API endpoints
- **zod**: Schema validation for API requests and database operations

### UI Dependencies
- **@radix-ui/***: Headless UI components (accordion, dialog, dropdown-menu, etc.)
- **tailwindcss**: Utility-first CSS framework
- **lucide-react**: Icon library for consistent iconography
- **class-variance-authority**: Component variant management
- **clsx**: Conditional className utilities

### Development Dependencies
- **vite**: Build tool and dev server
- **typescript**: Static type checking
- **wouter**: Lightweight React router
- **date-fns**: Date manipulation utilities
- **connect-pg-simple**: PostgreSQL session store (prepared for future authentication)

### Planned Integrations
- Payment processing (mentioned in design docs but not yet implemented)
- Discord/Telegram community integration
- Email marketing platform (Mailchimp mentioned in attached notes)
- Asset management for card images and game content