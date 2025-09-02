# YouTube Growth Calculator

## Overview

This is a full-stack web application that helps YouTube content creators calculate how many videos they need to upload to reach their subscriber goals within a specific timeframe. The application uses the YouTube Data API v3 to fetch real channel statistics and provides growth projections based on historical performance data.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **UI Components**: Shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation via @hookform/resolvers

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Build System**: esbuild for production bundling, tsx for development
- **Development Server**: Custom Vite integration for SSR and HMR
- **Storage**: In-memory storage implementation with interface for future database integration

### Data Layer
- **ORM**: Drizzle ORM configured for PostgreSQL
- **Database**: PostgreSQL (via Neon serverless driver)
- **Schema**: Shared schema definitions between client and server
- **Migrations**: Drizzle Kit for database migrations and schema management

### Authentication & Sessions
- **Session Store**: PostgreSQL-backed sessions using connect-pg-simple
- **User Management**: Basic user schema with username/password authentication

### Development & Deployment
- **Hot Reload**: Vite HMR integration with Express middleware
- **Error Handling**: Runtime error overlays in development
- **Environment**: Replit-optimized with cartographer plugin for development
- **Static Assets**: Vite handles client bundling, Express serves in production

### API Integration
- **YouTube API**: Direct integration with YouTube Data API v3 for fetching channel statistics
- **Growth Calculations**: Client-side algorithms for calculating video upload requirements
- **Error Handling**: Comprehensive error states for API failures and invalid data

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL serverless driver for Neon database
- **drizzle-orm**: Type-safe ORM for database operations
- **@tanstack/react-query**: Server state management and caching
- **wouter**: Lightweight React router
- **react-hook-form**: Form state management and validation

### UI & Styling
- **@radix-ui/***: Headless UI primitives for accessibility
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Type-safe variant styling
- **lucide-react**: Icon library
- **react-icons**: Additional icon sets (Font Awesome)

### Development Tools
- **vite**: Build tool and development server
- **tsx**: TypeScript execution for development
- **esbuild**: Production bundling
- **@replit/vite-plugin-***: Replit-specific development enhancements

### External APIs
- **YouTube Data API v3**: Fetches channel statistics, video counts, and subscriber data
- **API Key Required**: VITE_YT_API_KEY environment variable for YouTube API access

### Session & Storage
- **connect-pg-simple**: PostgreSQL session store for Express sessions
- **Database URL**: PostgreSQL connection string via DATABASE_URL environment variable