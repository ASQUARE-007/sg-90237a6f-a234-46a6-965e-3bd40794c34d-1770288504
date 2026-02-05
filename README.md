# Softgen Starter Project

A modern, production-ready Next.js application starter template built with the latest web technologies and best practices.

## ✨ Features

- ⚡ **Next.js 15.2** - Latest features with Pages Router architecture
- 🎨 **Tailwind CSS 3.4** - Utility-first styling with custom design system
- 🧩 **Shadcn/UI** - Beautiful, accessible component library
- 🌓 **Dark Mode** - Built-in theme switching with next-themes
- 📱 **Responsive Design** - Mobile-first approach
- ♿ **Accessibility** - WCAG compliant components
- 🔒 **TypeScript** - Full type safety throughout
- 🎭 **Framer Motion** - Smooth animations and transitions
- 📋 **Form Handling** - React Hook Form with Zod validation
- 🎯 **SEO Ready** - Meta tags and Open Graph support

## 🚀 Tech Stack

### Core
- **Framework:** Next.js 15.2 (Pages Router)
- **Language:** TypeScript 5
- **React:** 18.3

### Styling & UI
- **CSS Framework:** Tailwind CSS 3.4
- **UI Components:** Shadcn/UI + Radix UI
- **Animations:** Framer Motion 12
- **Icons:** Lucide React 0.474

### Forms & Validation
- **Form Library:** React Hook Form 7.54
- **Validation:** Zod 3.24
- **Resolvers:** @hookform/resolvers

### Additional Features
- **Theme Management:** next-themes
- **Date Handling:** date-fns
- **Carousels:** Embla Carousel
- **Payment Integration:** Stripe (ready to use)

## 🛠️ Getting Started

### Prerequisites

- **Node.js** 18.x or higher
- **npm** or **yarn** package manager
- **Git** for version control

### Installation

1. **Clone the repository:**
```bash
git clone <your-repository-url>
cd <project-name>
```

2. **Install dependencies:**
```bash
npm install
```

3. **Set up environment variables:**
```bash
cp .env.local.example .env.local
```

Edit `.env.local` with your configuration values.

4. **Start the development server:**
```bash
npm run dev
```

The application will be available at [http://localhost:3000](http://localhost:3000)

## 📜 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with Turbopack |
| `npm run build` | Create production build |
| `npm start` | Run production server |
| `npm run lint` | Run ESLint code analysis |

## 📁 Project Structure

```
softgen-starter/
├── src/
│   ├── components/          # React components
│   │   ├── ui/             # Shadcn/UI component library
│   │   ├── SEO.tsx         # SEO meta tags component
│   │   └── ThemeSwitch.tsx # Dark mode toggle
│   ├── contexts/           # React Context providers
│   │   └── ThemeProvider.tsx
│   ├── hooks/              # Custom React hooks
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   ├── lib/                # Utility functions
│   │   └── utils.ts
│   ├── pages/              # Next.js pages (file-based routing)
│   │   ├── api/           # API routes
│   │   ├── fonts/         # Font files (Geist)
│   │   ├── _app.tsx       # App wrapper
│   │   ├── _document.tsx  # HTML document structure
│   │   ├── index.tsx      # Home page
│   │   └── 404.tsx        # Custom 404 page
│   └── styles/            # Global styles
│       └── globals.css    # Tailwind + custom CSS
├── public/                # Static assets
│   ├── favicon.ico
│   └── og-image.png
├── components.json        # Shadcn/UI configuration
├── tailwind.config.ts     # Tailwind CSS configuration
├── tsconfig.json          # TypeScript configuration
├── next.config.mjs        # Next.js configuration
└── package.json           # Project dependencies
```

## 🎨 Styling & Customization

### Color System

Edit `src/styles/globals.css` to customize the color palette:

```css
:root {
  --background: 0 0% 100%;
  --foreground: 222.2 84% 4.9%;
  --primary: 222.2 47.4% 11.2%;
  --primary-foreground: 210 40% 98%;
  /* Add your custom colors here */
}

.dark {
  --background: 222.2 84% 4.9%;
  --foreground: 210 40% 98%;
  /* Dark mode variants */
}
```

Update `tailwind.config.ts` to sync with your design system.

### Typography

The project uses Geist fonts (included). To change fonts:

1. Import fonts in `src/styles/globals.css`:
```css
@import url('https://fonts.googleapis.com/css2?family=Your+Font&display=swap');
```

2. Update font configuration in `tailwind.config.ts`:
```ts
fontFamily: {
  sans: ['Your Font', 'sans-serif'],
}
```

### Adding Components

Use Shadcn/UI CLI to add more components:

```bash
npx shadcn@latest add <component-name>
```

Available components: button, card, dialog, form, input, select, and 40+ more.

## 🧩 Using UI Components

Import components from `@/components/ui/*`:

```tsx
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardHeader } from "@/components/ui/card";
import { Input } from "@/components/ui/input";

export default function MyComponent() {
  return (
    <Card>
      <CardHeader>Example Card</CardHeader>
      <CardContent>
        <Input placeholder="Enter text..." />
        <Button>Submit</Button>
      </CardContent>
    </Card>
  );
}
```

## 🌐 SEO Configuration

Use the built-in SEO component for page-level meta tags:

```tsx
import { SEO } from "@/components/SEO";

export default function AboutPage() {
  return (
    <>
      <SEO 
        title="About Us"
        description="Learn more about our company"
        image="/about-og-image.png"
        url="https://yoursite.com/about"
      />
      {/* Your page content */}
    </>
  );
}
```

## 🚀 Deployment

### Deploy to Vercel (Recommended)

1. **One-Click Deploy:**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

2. **Via Vercel CLI:**
```bash
npm i -g vercel
vercel
```

### Deploy to Other Platforms

1. Build the production bundle:
```bash
npm run build
```

2. Start the production server:
```bash
npm start
```

3. Deploy the `.next` folder and `public` directory to your hosting platform.

### Environment Variables

Set up environment variables in your deployment platform:

```bash
# Example variables (add your own)
NEXT_PUBLIC_SITE_URL=https://yoursite.com
# NEXT_PUBLIC_API_URL=
# DATABASE_URL=
# STRIPE_SECRET_KEY=
# STRIPE_PUBLISHABLE_KEY=
```

## 🔧 Configuration Files

- **next.config.mjs** - Next.js configuration including image domains, headers, and build settings
- **tailwind.config.ts** - Tailwind CSS configuration with custom colors, fonts, and plugins
- **tsconfig.json** - TypeScript compiler options and path aliases (`@/*`)
- **components.json** - Shadcn/UI component library configuration

## 📚 Documentation & Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [React Documentation](https://react.dev)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Shadcn/UI Components](https://ui.shadcn.com)
- [TypeScript Handbook](https://www.typescriptlang.org/docs)
- [Framer Motion API](https://www.framer.com/motion)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

- 📖 Check the [Next.js documentation](https://nextjs.org/docs)
- 💬 Visit [Shadcn/UI documentation](https://ui.shadcn.com)
- 🐛 Report issues on GitHub
- 📧 Contact [Softgen Support](https://softgen.ai/support)

## 🙏 Acknowledgments

- Built with [Softgen](https://softgen.ai) - AI-powered software development
- UI components by [Shadcn](https://ui.shadcn.com)
- Icons by [Lucide](https://lucide.dev)
- Fonts by [Vercel](https://vercel.com/font)

---

**Made with ❤️ using [Softgen](https://softgen.ai)**