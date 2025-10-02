# DecoBlu USA - Architectural Vinyl Wrap Showcase

## Overview

DecoBlu USA is a professional architectural vinyl wrap company specializing in premium surface transformations. The application is a modern, responsive website showcasing their INFeel product line with advanced slideshow features, smooth animations, and mobile-optimized design. The tagline "Transforming Surfaces" emphasizes their core service of surface transformation across automotive and interior applications.

## Recent Changes (October 2025)

**Fresh Replit Import Setup (October 2, 2025):**
- Successfully imported GitHub repository clone to Replit environment
- Verified workflow "Start application" properly configured with webview output and port 5000
- Confirmed Vite configuration has `allowedHosts: true` for Replit proxy compatibility
- Verified deployment configuration for autoscale with build and start scripts
- Confirmed Express server binding to 0.0.0.0:5000 for frontend access
- All code passing TypeScript checks and LSP diagnostics with no errors
- Build process tested and working correctly (vite build + esbuild for backend)
- Application fully functional and ready for development

**Previous Replit Import Setup (October 1, 2025):**
- Successfully imported GitHub repository to Replit environment
- Configured workflow "Start application" to run `npm run dev` on port 5000 with webview output
- Verified Vite configuration has `allowedHosts: true` for Replit proxy compatibility
- Set up deployment configuration for autoscale with build and start scripts
- Confirmed server is correctly binding to 0.0.0.0:5000 for frontend access
- All code passing LSP diagnostics with no errors

**Brand and Visual Updates:**
- Integrated new DecoBlu USA logo (image_1759294885448.png) in navigation and hero sections
- Updated tagline from "Transforming Interiors" to "Transforming Surfaces"
- Removed statistics section (15+ years experience, 5000+ surfaces, etc.)
- Removed "Leading Enhancement Specialists" badge

**Hero Component Updates:**
- Implemented show-once animation that plays only on first visit (session-based)
- Added zoom in/out effect on background image during scroll using Framer Motion
- Updated button text: "Get a Quote" → "Contact Us", "View Catalog" → "View Products"

**Navigation Updates:**
- Replaced text logo with dual logo setup: icon logo (decoblu_1759298644827.png) on left + text logo (decoblu text logo_1759298657179.png) on right
- Removed separate contact link from navigation menu
- Changed "Get Quote" button to "Contact Us" with routing to contact page
- Enhanced mobile menu with slide-in animations using AnimatePresence

**Home Page Product Section Update (October 1, 2025):**
- Replaced the "Line of Products INFeel" slideshow section (ServicesGrid component) with detailed product cards
- Now displays the same comprehensive product information as the dedicated Products page
- Shows product lines with logos, descriptions, key features, benefits, and catalog downloads:
  - INFeel Architectural Finish Films
  - DecoBlu Luxury Vinyl Flooring
  - DecoBlu Window Films
  - POV Window Films
  - Woven by Elite (added October 1, 2025)
- Each product card includes alternating gradient backgrounds and detailed feature lists
- Includes "Download Catalog" buttons for products with available catalogs

**Woven by Elite Product Addition (October 1, 2025):**
- Added new product line: Woven by Elite vinyl floor covering
- Logo: image_1759322882406.png
- Product images: image_1759322783228.png, image_1759322907527.png, image_1759322910212.png, image_1759322912547.png, image_1759322929278.png
- Features woven fabric finish with lightweight PVC foam base layer
- Multiple backing types for different applications: Comfort rear for tiles, PVC backing for rolls, Foamed PVC backing for carpets, No backing for walls, Thin PVC backing for walls
- Product appears on both Home page and Products page with full carousel and details

**Catalog Download Updates (October 1, 2025):**
- Updated all product catalog buttons to open Google Drive links in new tabs
- INFeel, Woven, Flooring, POV Window Films, and DecoBlu Window Films now link to their respective Google Drive catalogs

**Mobile and Desktop Navigation Fixes (October 1, 2025):**
- Fixed navigation links to properly scroll to sections on the same page (mobile and desktop)
- Fixed "View Products" button in hero section to scroll to products section when on home page
- Added smooth scroll behavior for hash links (#products, #about) on all devices
- Navigation now properly closes mobile menu after selecting a section link
- All scrollbars hidden across the website while maintaining scroll functionality

**UI Component Updates (October 1, 2025):**
- Removed white container background from About Us section logo/image - now displays as clean image
- Removed Card component containers from Testimonials section for cleaner, minimal styling
- Reduced footer padding from py-16 to py-10 (main section) and py-6 to py-4 (bottom section) for more compact footer

**Smart Navbar Behavior (October 1, 2025):**
- Implemented intelligent navbar scroll behavior for both mobile and desktop
- Navbar now shows when scrolling up at any point on the page
- Navbar automatically appears when near the bottom of the page (within 300px from bottom/last section)
- Navbar hides when scrolling down and not near bottom for cleaner viewing experience
- Smooth slide-in/slide-out animations using CSS transforms for professional UX
- Always visible at the top of the page and when mobile menu is open

**Site Configuration Updates (October 1, 2025):**
- Set DecoBlu icon logo (decoblu_1759298644827.png) as the site favicon
- Removed Replit dev banner from the application for cleaner appearance
- Redesigned 404 page to match website style with Navigation, Footer, and brand-consistent styling
- 404 page now includes circular alert icon, large "404" text, helpful message, and "Back to Home" button

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The application uses a modern React-based architecture with TypeScript for type safety. The frontend is built using Vite as the build tool and bundler, providing fast development and optimized production builds. The component structure follows a modular approach with reusable UI components and page-specific components.

**Key Frontend Decisions:**
- **React with TypeScript**: Chosen for component-based architecture and type safety
- **Vite**: Selected for fast development server and optimized builds
- **Wouter**: Lightweight routing solution instead of React Router for smaller bundle size
- **Component Organization**: Clear separation between UI components, page components, and examples

### Styling and Design System
The application implements a comprehensive design system based on Tailwind CSS with custom theming capabilities.

**Design System Components:**
- **Tailwind CSS**: Utility-first CSS framework for rapid UI development
- **Shadcn/ui Components**: Pre-built, accessible UI components with consistent styling
- **Custom Theme Provider**: Light/dark mode support with CSS custom properties
- **Design Guidelines**: Specific color palette inspired by monsterwraps.co.uk with blue branding
- **Responsive Design**: Mobile-first approach with breakpoint-based layouts

**Typography and Visual Elements:**
- **Google Fonts**: Montserrat for headings, Open Sans for body text
- **Animation System**: Framer Motion for smooth scroll animations and transitions
- **Color Scheme**: Blue-focused palette (Brand Blue: 220 100% 45%, Deep Blue: 220 80% 35%)

### State Management and Data Flow
The application uses a combination of React Query for server state and React Context for client state management.

**State Management Decisions:**
- **TanStack React Query**: Handles API requests, caching, and server state synchronization
- **React Context**: Theme management and global UI state
- **Local Component State**: Form handling and component-specific interactions

### Backend Architecture
The backend follows a minimal Express.js architecture with a modular storage interface.

**Backend Structure:**
- **Express.js Server**: RESTful API with middleware for logging and error handling
- **Storage Interface**: Abstracted storage layer with in-memory implementation
- **Development Setup**: Vite integration for seamless development experience

**Storage Design:**
- **IStorage Interface**: Defines CRUD operations for data persistence
- **MemStorage Implementation**: In-memory storage for development and testing
- **Database Ready**: Architecture supports easy migration to persistent databases

### Development and Build System
The project uses modern development tooling for efficient development and deployment.

**Build Configuration:**
- **TypeScript Configuration**: Strict type checking with path aliases for clean imports
- **Vite Configuration**: Optimized for both development and production
- **Replit Integration**: Special plugins for Replit development environment
- **Asset Management**: Organized asset structure with proper aliasing

## External Dependencies

### Core Framework Dependencies
- **@vitejs/plugin-react**: React support for Vite build system
- **express**: Node.js web framework for backend API
- **typescript**: Type safety and development tooling

### UI and Design Dependencies
- **@radix-ui/***: Comprehensive set of accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **framer-motion**: Animation library for smooth UI transitions
- **class-variance-authority**: Type-safe variant management for components
- **clsx & tailwind-merge**: Utility functions for conditional classes

### State Management Dependencies
- **@tanstack/react-query**: Server state management and caching
- **wouter**: Lightweight routing solution
- **react-hook-form**: Form handling with validation

### Database and Storage Dependencies
- **drizzle-orm**: Type-safe ORM for database operations
- **drizzle-kit**: Database migration and schema management tools
- **@neondatabase/serverless**: Serverless PostgreSQL database adapter
- **connect-pg-simple**: PostgreSQL session store for Express

### Development Dependencies
- **@replit/vite-plugin-***: Replit-specific development enhancements
- **postcss & autoprefixer**: CSS processing and vendor prefixing
- **date-fns**: Date manipulation utilities

### Asset Dependencies
The application includes a curated collection of catalog images and stock photos stored in the attached_assets directory, featuring Infeel V17 digital catalog pages and modern interior design imagery to showcase architectural vinyl applications.