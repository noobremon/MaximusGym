# 💪 Unisex Gym - Modern Fitness Platform

A feature-rich, responsive gym management and booking platform built with modern web technologies. This application provides a seamless experience for gym members to explore facilities, book classes, manage memberships, and connect with professional trainers.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![React](https://img.shields.io/badge/React-18.3.1-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.6.3-blue.svg)](https://www.typescriptlang.org/)

---

## ✨ Key Features

- 🏋️ **Membership Management** - Three-tier membership plans (Basic, Premium, Elite) with detailed feature comparisons
- 📅 **Class Booking System** - Real-time class scheduling with availability tracking and instant booking
- 👨‍🏫 **Professional Trainers** - Browse trainer profiles with specialties and social media links
- 🏢 **Facility Showcase** - Interactive gallery of gym facilities and equipment
- 💬 **Testimonials** - Real member success stories with ratings and achievements
- 📧 **Contact Form** - Integrated email system for inquiries (EmailJS)
- 🗺️ **Location Maps** - Interactive maps using Leaflet and Google Maps API
- 🎨 **3D Gym Scene** - Immersive 3D visualization powered by Three.js
- 🌓 **Dark Theme** - Beautiful dark-themed UI with modern animations
- 📱 **Fully Responsive** - Mobile-first design that works on all devices
- ⚡ **Fast Performance** - Optimized with Vite and React Query for caching
- 🎭 **Smooth Animations** - Framer Motion for delightful user interactions

---

## 🛠️ Tech Stack

### Frontend
- **Framework:** React 18.3.1 with TypeScript 5.6.3
- **Build Tool:** Vite 5.4.14
- **Routing:** Wouter 3.3.5 (lightweight React router)
- **Styling:** Tailwind CSS 3.4.17 + shadcn/ui components
- **State Management:** Zustand 5.0.3
- **Data Fetching:** TanStack React Query 5.60.5
- **Forms:** React Hook Form 7.55.0 + Zod 3.24.2 validation
- **Animations:** Framer Motion 11.13.1
- **3D Graphics:** Three.js 0.175.0
- **Icons:** React Icons 5.4.0, Lucide React 0.453.0
- **Maps:** Leaflet 1.9.4, React Leaflet 4.2.1, Google Maps API

### Backend & Database
- **Database:** PostgreSQL
- **ORM:** Drizzle ORM
- **Schema Validation:** Zod

### Additional Libraries
- **Email Service:** EmailJS-com 3.2.0
- **Date Handling:** date-fns 3.6.0
- **Theme Management:** next-themes 0.4.6
- **UI Components:** Radix UI (Headless component library)

### Deployment
- **Hosting Options:** Netlify / Vercel
- **Build Configuration:** Both netlify.toml and vercel.json included

---

## 📁 Folder Structure

```
Gymmmmm/
│
├── client/                          # Frontend application
│   ├── src/
│   │   ├── components/              # React components
│   │   │   ├── ui/                  # Reusable UI components (shadcn/ui)
│   │   │   ├── ClassSection.tsx     # Classes overview section
│   │   │   ├── ContactSection.tsx   # Contact form section
│   │   │   ├── FacilitySection.tsx  # Facilities showcase
│   │   │   ├── Footer.tsx           # Site footer
│   │   │   ├── GymScene.tsx         # 3D Three.js scene
│   │   │   ├── Hero.tsx             # Landing hero section
│   │   │   ├── MembershipPlans.tsx  # Membership cards
│   │   │   ├── Navbar.tsx           # Navigation bar
│   │   │   ├── TestimonialSection.tsx # Customer reviews
│   │   │   └── TrainerSection.tsx   # Trainer profiles
│   │   │
│   │   ├── pages/                   # Route pages
│   │   │   ├── home.tsx             # Homepage (combines all sections)
│   │   │   ├── booking.tsx          # Class booking interface
│   │   │   ├── classes.tsx          # Class listings
│   │   │   ├── contact.tsx          # Contact page
│   │   │   ├── facilities.tsx       # Facility details
│   │   │   ├── membership.tsx       # Membership plans page
│   │   │   ├── trainers.tsx         # Trainer profiles page
│   │   │   └── not-found.tsx        # 404 page
│   │   │
│   │   ├── store/                   # State management
│   │   │   └── gym-store.ts         # Zustand store (auth, bookings)
│   │   │
│   │   ├── hooks/                   # Custom React hooks
│   │   │   ├── use-mobile.tsx       # Mobile detection hook
│   │   │   └── use-toast.ts         # Toast notification hook
│   │   │
│   │   ├── lib/                     # Utility libraries
│   │   │   ├── queryClient.ts       # React Query configuration
│   │   │   └── utils.ts             # Helper functions
│   │   │
│   │   ├── assets/                  # Static assets
│   │   ├── App.tsx                  # Main app component
│   │   ├── main.tsx                 # Entry point
│   │   └── index.css                # Global styles
│   │
│   ├── public/                      # Public static files
│   │   └── images/                  # Image assets
│   └── index.html                   # HTML template
│
├── shared/                          # Shared types and schemas
│   └── schema.ts                    # Zod schemas and TypeScript types
│
├── migrations/                      # Database migrations (Drizzle)
│
├── drizzle.config.ts                # Drizzle ORM configuration
├── vite.config.ts                   # Vite build configuration
├── tailwind.config.ts               # Tailwind CSS configuration
├── tsconfig.json                    # TypeScript configuration
├── postcss.config.js                # PostCSS configuration
├── netlify.toml                     # Netlify deployment config
├── vercel.json                      # Vercel deployment config
├── theme.json                       # Theme configuration
└── package.json                     # Dependencies and scripts
```

---

## 🚀 Installation Steps

### Prerequisites
- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **PostgreSQL** database (local or cloud)

### Step 1: Clone the Repository
```bash
git clone https://github.com/noobremon/Unisex-Gym.git
cd Unisex-Gym
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Set Up Environment Variables
Create a `.env` file in the root directory:

```env
# Database Configuration
DATABASE_URL=postgresql://username:password@localhost:5432/gym_db

# Optional: Email Service (EmailJS)
# Configure these in EmailJS dashboard
VITE_EMAILJS_SERVICE_ID=your_service_id
VITE_EMAILJS_TEMPLATE_ID=your_template_id
VITE_EMAILJS_PUBLIC_KEY=your_public_key

# Optional: Google Maps API
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_key
```

### Step 4: Set Up Database
Run Drizzle migrations to set up your database schema:

```bash
# Generate migrations
npx drizzle-kit generate

# Run migrations
npx drizzle-kit push
```

---

## 🔧 Environment Variables Setup

| Variable | Description | Required | Example |
|----------|-------------|----------|---------|
| `DATABASE_URL` | PostgreSQL connection string | ✅ Yes | `postgresql://user:pass@localhost:5432/gym_db` |
| `VITE_EMAILJS_SERVICE_ID` | EmailJS service ID for contact form | ⚠️ Optional | `service_abc123` |
| `VITE_EMAILJS_TEMPLATE_ID` | EmailJS template ID | ⚠️ Optional | `template_xyz789` |
| `VITE_EMAILJS_PUBLIC_KEY` | EmailJS public key | ⚠️ Optional | `pub_key_123` |
| `VITE_GOOGLE_MAPS_API_KEY` | Google Maps API key | ⚠️ Optional | `AIza...` |

> **Note:** The application will work without optional variables, but some features (email, maps) will be limited.

---

## 💻 How to Run Locally

### Development Mode
```bash
npm run dev
```
The application will be available at `http://localhost:5173`

### Production Preview
```bash
# Build the application
npm run build

# Preview the production build
npm run preview
```

---

## 📦 Build / Deployment Instructions

### Build for Production
```bash
npm run build
```
This creates an optimized production build in the `dist/public/` directory.

### Deploy to Netlify
1. **Push code to GitHub**
2. **Connect repository to Netlify**
3. **Configure build settings:**
   - Build command: `npm run build`
   - Publish directory: `dist/public`
4. **Add environment variables** in Netlify dashboard
5. **Deploy**

Alternatively, use Netlify CLI:
```bash
npm install -g netlify-cli
netlify deploy --prod
```

### Deploy to Vercel
1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Deploy:**
   ```bash
   vercel --prod
   ```

3. **Add environment variables** in Vercel dashboard

The `vercel.json` configuration is already included for seamless deployment.

---

## 🌐 API Endpoints

> **Note:** This is currently a frontend-focused application with mock data. Backend API endpoints are referenced but not fully implemented. Below is the expected API structure for future backend integration:

### Class Management
- `GET /api/classes` - Fetch all gym classes
- `GET /api/class-schedules?day={day}` - Get schedules for specific day
- `POST /api/book-class` - Book a class session
  ```json
  {
    "userId": 1,
    "scheduleId": 5
  }
  ```

### Membership
- `GET /api/memberships` - Get all membership plans
- `POST /api/register-membership` - Register for a membership
  ```json
  {
    "userId": 1,
    "planId": 2
  }
  ```

### Trainers & Facilities
- `GET /api/trainers` - Fetch all trainers
- `GET /api/facilities` - Get facility information
- `GET /api/testimonials` - Fetch customer testimonials

### Contact
- `POST /api/contact` - Submit contact form
  ```json
  {
    "name": "John Doe",
    "email": "john@example.com",
    "subject": "Inquiry",
    "message": "Message content"
  }
  ```

---

## 🎯 Usage Examples

### Booking a Class
1. Navigate to the **Booking** page (`/booking`)
2. Select a day of the week from the tabs
3. Browse available classes with time slots
4. Click **"Book Class"** to reserve your spot
5. Receive instant confirmation via toast notification

### Choosing a Membership
1. Go to **Membership** page (`/membership`)
2. Toggle between **Monthly** and **Yearly** plans
3. Compare features across Basic, Premium, and Elite tiers
4. Click **"Choose Plan"** to select your membership
5. Complete the registration process

### Contacting the Gym
1. Visit the **Contact** page (`/contact`)
2. Fill in your name, email, subject, and message
3. Submit the form
4. Email is sent via EmailJS integration

### Exploring Trainers
1. Navigate to **Trainers** page (`/trainers`)
2. View trainer profiles with specialties
3. Connect via social media links (Instagram, Facebook, Twitter)

---

## 📸 Screenshots Section

> Add screenshots here to showcase your application:

### Homepage Hero Section
![Hero Section](./screenshots/hero.png)

### Class Booking Interface
![Booking Page](./screenshots/booking.png)

### Membership Plans
![Membership Plans](./screenshots/membership.png)

### Trainer Profiles
![Trainers](./screenshots/trainers.png)

---

## 🏗️ Architecture Overview

### Component Architecture
```
App (Root)
├── ThemeProvider (Dark theme support)
├── TooltipProvider (UI tooltips)
├── Toaster (Notifications)
├── Navbar (Persistent navigation)
├── Router
│   ├── Home Page
│   │   ├── Hero (3D scene + CTA)
│   │   ├── MembershipPlans
│   │   ├── ClassSection
│   │   ├── TrainerSection
│   │   ├── FacilitySection
│   │   ├── TestimonialSection
│   │   └── ContactSection
│   ├── Booking Page (Schedule management)
│   ├── Classes Page (Class catalog)
│   ├── Membership Page (Plan comparison)
│   ├── Trainers Page (Trainer grid)
│   ├── Facilities Page (Facility gallery)
│   ├── Contact Page (Contact form + map)
│   └── 404 Page
└── Footer
```

### Data Flow
```
User Interaction
      ↓
React Components
      ↓
Zustand Store (State Management)
      ↓
React Query (API Calls + Caching)
      ↓
Backend API (Future)
      ↓
PostgreSQL Database (via Drizzle ORM)
```

### State Management Flow
- **Zustand Store** manages:
  - User authentication state
  - Selected day/class/membership
  - Booking history
  - Login/logout actions
- **React Query** handles:
  - Server state caching
  - Background data synchronization
  - Optimistic updates for bookings

### Key Design Patterns
- **Component Composition:** Reusable UI components from shadcn/ui
- **Custom Hooks:** Abstracted logic (use-toast, use-mobile)
- **Route-based Code Splitting:** Vite optimizes bundle sizes
- **Schema Validation:** Zod ensures type safety across client/server
- **Mock Data Strategy:** Development mode uses inline mock data

---

## 🤝 Contribution Guidelines

We welcome contributions! Follow these steps:

### 1. Fork the Repository
```bash
git clone https://github.com/your-username/Unisex-Gym.git
```

### 2. Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### 3. Make Your Changes
- Follow the existing code style
- Use TypeScript for type safety
- Write descriptive commit messages
- Test your changes thoroughly

### 4. Commit Your Changes
```bash
git add .
git commit -m "feat: add new feature description"
```

### 5. Push to Your Branch
```bash
git push origin feature/your-feature-name
```

### 6. Open a Pull Request
- Provide a clear description of your changes
- Reference any related issues
- Wait for code review

### Code Style Guidelines
- Use **TypeScript** for all new code
- Follow **ESLint** rules
- Use **Prettier** for formatting
- Write meaningful component and variable names
- Add comments for complex logic

### Commit Message Convention
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code style changes (formatting)
- `refactor:` Code refactoring
- `test:` Adding tests
- `chore:` Maintenance tasks

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2026 Unisex Gym

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🚀 Future Improvements

### Backend Development
- [ ] Build complete REST API with Express.js or Fastify
- [ ] Implement JWT-based authentication
- [ ] Add user profile management
- [ ] Create admin dashboard for gym management

### Enhanced Features
- [ ] **Payment Integration** - Stripe/PayPal for membership payments
- [ ] **Real-time Chat** - WebSocket support for trainer-member communication
- [ ] **Progress Tracking** - Member workout logs and progress charts
- [ ] **Mobile App** - React Native version for iOS/Android
- [ ] **Video Streaming** - Online workout classes (HLS/DASH)
- [ ] **AI Workout Planner** - Personalized workout recommendations
- [ ] **Nutrition Tracking** - Meal planning and calorie tracking
- [ ] **QR Code Check-in** - Contactless gym entry system
- [ ] **Push Notifications** - Class reminders and updates
- [ ] **Social Features** - Member community forum

### Performance & SEO
- [ ] Server-Side Rendering (SSR) with Next.js migration
- [ ] Progressive Web App (PWA) capabilities
- [ ] Image optimization with next/image
- [ ] SEO metadata optimization
- [ ] Lighthouse performance score 95+

### Testing & Quality
- [ ] Unit tests with Vitest
- [ ] Integration tests with React Testing Library
- [ ] E2E tests with Playwright
- [ ] Accessibility audits (WCAG 2.1 AA compliance)
- [ ] CI/CD pipeline with GitHub Actions

### Analytics & Monitoring
- [ ] Google Analytics integration
- [ ] Error tracking with Sentry
- [ ] Performance monitoring
- [ ] User behavior analytics

---

## 👨‍💻 Developer Notes

### Getting Help
- Check existing [issues](https://github.com/noobremon/Unisex-Gym/issues)
- Read the [documentation](./docs)
- Join our community discussions

### Useful Commands
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linter (if configured)
npm run lint

# Format code (if configured)
npm run format
```

### Project Status
🟢 **Active Development** - This project is actively maintained and open for contributions.

---

## 🙏 Acknowledgments

- **shadcn/ui** - Beautiful component library
- **Radix UI** - Accessible headless components
- **Unsplash** - High-quality fitness images
- **Three.js** - 3D graphics library
- **Framer Motion** - Animation library

---

## 📞 Contact

For questions or support, reach out:

- **GitHub Issues:** [Report a bug](https://github.com/noobremon/Unisex-Gym/issues)
- **Email:** support@unisexgym.com
- **Website:** [www.unisexgym.com](https://www.unisexgym.com)

---

<div align="center">

**Built with ❤️ by the Unisex Gym Team**

⭐ Star this repo if you find it helpful!

</div>
