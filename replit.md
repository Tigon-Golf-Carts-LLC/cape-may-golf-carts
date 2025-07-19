# NJ Golf Carts - Application Architecture

## Overview

This is a full-stack web application for a golf cart dealership serving New Jersey. The application features a React frontend built with Vite, a Node.js Express backend, and uses PostgreSQL with Drizzle ORM for data management. The project uses modern web technologies including TypeScript, Tailwind CSS, and shadcn/ui components.

The application includes comprehensive town-specific landing pages for 12 locations in Cape May County, each with unique SEO-optimized content and location-specific branding while maintaining consistent structure and design elements.

## User Preferences

Preferred communication style: Simple, everyday language.

## Recent Changes (January 2025)

**Town Pages Completion:**
- ✅ All 12 town-specific landing pages completed with unique content
- ✅ Cape May, Cape May Point, Wildwood, Wildwood Crest, North Wildwood, Stone Harbor, Avalon, Sea Isle City, Ocean City, Rio Grande, Middle Township, Lower Township
- ✅ Each page has unique, location-specific content reflecting local attractions and characteristics
- ✅ SEO-optimized titles and descriptions for each location
- ✅ Interactive maps for each service area
- ✅ Consistent branding and design elements across all pages
- ✅ All routes properly configured in App.tsx
- ✅ Application successfully running with complete town page structure
- ✅ Content highlights each town's unique features (Victorian history, boardwalks, lighthouse, bird sanctuary, etc.)
- ✅ Comprehensive SEO implementation with sitemap.xml, robots.txt, and business schema
- ✅ Scroll-to-top functionality implemented on all pages for optimal user experience

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: TanStack Query (React Query) for server state
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Management**: PostgreSQL sessions with connect-pg-simple
- **API Structure**: RESTful endpoints with typed request/response handling

### Development Environment
- **Deployment**: Replit-optimized with custom build scripts
- **Bundling**: ESBuild for server-side bundling
- **Development**: Hot module replacement via Vite
- **Type Safety**: Full TypeScript coverage across frontend, backend, and shared types

## Key Components

### Database Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Schema**: Centralized schema definition in `/shared/schema.ts`
- **Migrations**: Automated migrations in `/migrations` directory
- **Connection**: Neon Database serverless connection with connection pooling

### UI Components
- **Component Library**: shadcn/ui built on Radix UI primitives
- **Design System**: Consistent theming with CSS variables
- **Responsive Design**: Mobile-first approach with Tailwind breakpoints
- **Accessibility**: ARIA-compliant components from Radix UI

### Business Logic
- **Contact System**: Contact form handling with email notifications
- **Vehicle Catalog**: Product showcase with detailed specifications
- **SEO Optimization**: Dynamic meta tags and structured data
- **Brand Integration**: Multi-brand inventory management (Club Car, EZ-GO, Denago, Evolution, etc.)

## Data Flow

### Frontend to Backend
1. User interactions trigger form submissions or API calls
2. TanStack Query manages request state and caching
3. API requests use typed interfaces from shared schema
4. Backend validates requests using Zod schemas
5. Database operations performed through Drizzle ORM
6. Responses sent back with proper error handling

### Static Assets
- Product images and marketing materials stored in `/attached_assets`
- Legacy HTML pages for specific vehicle models maintained for SEO
- Build process optimizes and serves static content

## External Dependencies

### Database
- **Neon Database**: Serverless PostgreSQL provider
- **Connection**: Environment variable `DATABASE_URL` required
- **Pooling**: Built-in connection pooling for performance

### UI Framework
- **Radix UI**: Comprehensive component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide Icons**: SVG icon library
- **Date-fns**: Date manipulation utilities

### Development Tools
- **TypeScript**: Type safety across the stack
- **ESLint**: Code linting and formatting
- **Drizzle Kit**: Database migration and introspection tools

## Deployment Strategy

### Build Process
1. **Frontend**: Vite builds optimized client bundle to `/dist/public`
2. **Backend**: ESBuild bundles server code to `/dist/index.js`
3. **Database**: Migrations applied via `drizzle-kit push`
4. **Assets**: Static files served from build directory

### Environment Configuration
- **Development**: `npm run dev` - Hot reloading with tsx
- **Production**: `npm run build && npm start` - Optimized build
- **Database**: Automatic schema synchronization in development

### Performance Optimizations
- **Code Splitting**: Vite automatically splits bundles
- **Static Generation**: Pre-built HTML for vehicle pages
- **Caching**: TanStack Query provides client-side caching
- **Compression**: Gzip compression for static assets

### Monitoring and Maintenance
- **Error Handling**: Comprehensive error boundaries and API error handling
- **Logging**: Structured logging for debugging
- **Health Checks**: Database connectivity monitoring
- **SEO**: Meta tags and structured data for search optimization

The application is designed to be easily maintainable and scalable, with clear separation of concerns between frontend presentation, backend business logic, and data persistence layers.