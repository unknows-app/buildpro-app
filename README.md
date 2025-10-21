# BuildPro Construction - Professional Construction Company Platform

A comprehensive web platform for a modern construction company featuring both a public marketing website and an administrative dashboard.

## Features

### Public Website
- **Home Page**: Hero section, featured services, recent projects, testimonials
- **About Page**: Company story, team, values, certifications
- **Services Page**: Detailed service offerings with descriptions
- **Projects Page**: Portfolio gallery with project details and case studies
- **Contact Page**: Contact form, location map, business information

### Admin Dashboard
- **Projects Management**: CRUD operations for project portfolio
- **Services Management**: Service offerings management
- **Media Library**: Image/video upload and organization
- **Lead Management**: Contact form submissions and lead tracking
- **Testimonials**: Customer review management
- **Settings**: Site configuration and company information

## Tech Stack

- **Framework**: Next.js 15 with App Router
- **Language**: TypeScript (strict mode)
- **Styling**: Tailwind CSS
- **Database**: MySQL with Prisma ORM
- **Authentication**: NextAuth.js with credentials
- **Animations**: Framer Motion
- **Icons**: Lucide React

## Getting Started

### Prerequisites

- Node.js 18+ 
- MySQL database
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd eridev-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   # Database
   DATABASE_URL="mysql://root:@localhost:3306/buildpro_construction"

   # NextAuth.js
   NEXTAUTH_URL="http://localhost:3000"
   NEXTAUTH_SECRET="your-secret-key-here"

   # Admin Credentials (for initial setup)
   ADMIN_EMAIL="admin@buildpro.com"
   ADMIN_PASSWORD="admin123"
   ```

4. **Set up the database**
   ```bash
   # Generate Prisma client
   npx prisma generate

   # Run database migrations
   npx prisma db push

   # (Optional) Seed the database with initial data
   npx prisma db seed
   ```

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## Project Structure

```
src/
├── app/                    # Next.js App Router pages
│   ├── admin/             # Admin dashboard pages
│   ├── api/               # API routes
│   ├── about/             # Public pages
│   ├── contact/
│   ├── projects/
│   ├── services/
│   └── layout.tsx         # Root layout
├── components/            # Reusable components
│   ├── layout/           # Layout components
│   └── providers/        # Context providers
├── lib/                  # Utility libraries
│   ├── auth.ts          # NextAuth configuration
│   └── prisma.ts        # Prisma client
├── types/               # TypeScript type definitions
└── middleware.ts        # Next.js middleware
```

## Database Schema

The application uses the following main models:

- **User**: Admin users with authentication
- **Project**: Construction projects with details
- **Service**: Company services and offerings
- **Lead**: Contact form submissions and inquiries
- **Testimonial**: Customer reviews and testimonials
- **Media**: File uploads and media management
- **Setting**: Site configuration and settings

## Admin Access

### Default Admin Credentials
- **Email**: admin@buildpro.com
- **Password**: admin123

**Important**: Change these credentials after first login!

### Admin Features
- Dashboard with project statistics
- Project management (CRUD operations)
- Service management
- Lead tracking and management
- Testimonial management
- Media library
- Site settings and configuration

## API Endpoints

- `POST /api/contact` - Handle contact form submissions
- `GET/POST /api/auth/[...nextauth]` - Authentication endpoints

## Deployment

### Environment Variables for Production
```env
DATABASE_URL="your-production-database-url"
NEXTAUTH_URL="https://your-domain.com"
NEXTAUTH_SECRET="your-production-secret"
```

### Build for Production
```bash
npm run build
npm start
```

## Customization

### Styling
The application uses Tailwind CSS for styling. You can customize:
- Color scheme in `tailwind.config.js`
- Component styles in individual component files
- Global styles in `src/app/globals.css`

### Content
- Update company information in the admin settings
- Add/modify services through the admin dashboard
- Upload and manage projects and testimonials
- Customize SEO settings

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions, please contact the development team or create an issue in the repository.

---

**BuildPro Construction** - Building Dreams, Creating Reality