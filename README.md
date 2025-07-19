# Cape May Golf Carts - Official Website

A comprehensive website for Cape May Golf Carts, serving Cape May County, New Jersey with premium DENAGO and EVOLUTION electric golf carts.

## Features

- **12 Town-Specific Pages** - Dedicated landing pages for Cape May, Wildwood, Avalon, Stone Harbor, Ocean City, Sea Isle City, North Wildwood, Wildwood Crest, Cape May Point, Rio Grande, Middle Township, and Lower Township
- **Complete Vehicle Inventory** - 24+ golf cart models from DENAGO and EVOLUTION brands
- **Mobile-Responsive Design** - Optimized for all devices with Tailwind CSS
- **SEO Optimized** - Comprehensive sitemap, business schema, and structured data
- **Contact & Service Forms** - Professional contact handling with database integration

## Technology Stack

- **Frontend:** React 18 + TypeScript + Vite
- **Backend:** Node.js + Express + TypeScript
- **Database:** PostgreSQL with Drizzle ORM
- **Styling:** Tailwind CSS + shadcn/ui components
- **State Management:** TanStack Query (React Query)
- **Routing:** Wouter
- **Form Handling:** React Hook Form + Zod validation

## Quick Start

### Prerequisites
- Node.js 18+ 
- PostgreSQL database
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/cape-may-golf-carts.git
cd cape-may-golf-carts
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your database URL and other configurations
```

4. Set up the database:
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
├── client/               # React frontend
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Route components
│   │   └── lib/          # Utilities and configurations
├── server/               # Express backend
│   ├── data/            # Static data files
│   └── routes.ts        # API endpoints
├── shared/              # Shared types and schemas
├── public/              # Static assets and SEO files
└── attached_assets/     # Product images and media
```

## Key Features

### Town-Specific Landing Pages
- Unique content for each Cape May County location
- Local SEO optimization with area-specific keywords
- Interactive maps and location details
- Consistent branding with location-specific customization

### Vehicle Inventory
- **DENAGO Models:** EV City, EV Nomad, EV Nomad XL, EV Rover series
- **EVOLUTION Models:** Classic, Carrier, D5 Maverick/Ranger, D6 Max, Forester, Turfman
- Detailed specifications, pricing, and feature lists
- High-quality product images and descriptions

### SEO & Performance
- Comprehensive sitemap.xml with all pages and images
- Business schema markup for local search
- Google My Business integration ready
- Optimized loading with lazy loading and image compression

## API Endpoints

- `GET /api/golf-carts` - Fetch all golf carts
- `GET /api/golf-carts/:id` - Fetch specific golf cart
- `GET /api/golf-carts/slug/:slug` - Fetch by URL slug
- `POST /api/contact` - Submit contact form
- `GET /api/services` - Fetch available services
- `GET /api/testimonials` - Fetch customer testimonials

## Database Schema

The application uses Drizzle ORM with PostgreSQL. Key tables include:
- `golf_carts` - Vehicle inventory and specifications
- `contact_forms` - Customer inquiries and contact submissions
- `services` - Available services and pricing
- `testimonials` - Customer reviews and feedback

## Deployment

### Environment Variables Required:
```
DATABASE_URL=your_postgresql_connection_string
NODE_ENV=production
PORT=5000
```

### Build Commands:
```bash
npm run build    # Build both frontend and backend
npm start        # Start production server
```

## SEO Files

- `/sitemap.xml` - Complete site structure for search engines
- `/robots.txt` - Search engine crawling guidelines
- `/business-schema.json` - Business information for local search
- `/google-business-verification.html` - Google My Business verification

## Support

For technical support or business inquiries:
- Email: info@capemaygolfcarts.com
- Phone: 1-844-844-6638
- Website: https://capemaygolfcarts.com

## License

© 2025 Cape May Golf Carts. All rights reserved.

---

**Cape May County's Premier Golf Cart Dealer**
*Serving Cape May, Wildwood, Avalon, Stone Harbor, Ocean City, Sea Isle City, and surrounding areas.*