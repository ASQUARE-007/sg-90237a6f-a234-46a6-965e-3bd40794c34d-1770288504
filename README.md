# Softgen Starter Project

A modern Next.js application built with TypeScript, React 18, and Tailwind CSS.

## 🚀 Tech Stack

- **Framework:** Next.js 15.2 (Pages Router)
- **Language:** TypeScript 5
- **Styling:** Tailwind CSS 3.4
- **UI Components:** Shadcn/UI with Radix UI primitives
- **Animations:** Framer Motion
- **Form Handling:** React Hook Form + Zod validation
- **Theme:** next-themes for dark mode support
- **Icons:** Lucide React

## 📦 Features

- ⚡ Next.js 15 with Turbopack for fast development
- 🎨 Pre-configured Shadcn/UI component library
- 🌓 Dark mode support with theme switching
- 📱 Fully responsive design
- ♿ Accessibility-first components
- 🔒 Type-safe with TypeScript
- 🎭 Smooth animations with Framer Motion
- 📋 Advanced form handling with validation

## 🛠️ Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd <project-directory>
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.local.example .env.local
```
Edit `.env.local` with your configuration.

4. Start the development server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

## 📜 Available Scripts

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint

## 📁 Project Structure

```
src/
├── components/     # React components
│   ├── ui/        # Shadcn/UI components
│   ├── SEO.tsx    # SEO meta tags component
│   └── ThemeSwitch.tsx
├── contexts/      # React context providers
├── hooks/         # Custom React hooks
├── lib/           # Utility functions
├── pages/         # Next.js pages (routing)
│   ├── api/       # API routes
│   └── fonts/     # Font files
└── styles/        # Global styles and Tailwind config
```

## 🎨 Customization

### Colors & Theme

Edit `src/styles/globals.css` to customize color variables:

```css
:root {
  --background: ...;
  --foreground: ...;
  /* Add your custom colors */
}
```

Update `tailwind.config.ts` to sync with your color system.

### Typography

Fonts are configured in `src/pages/_document.tsx` and `src/styles/globals.css`. 
Update font imports and CSS variables to use your preferred typefaces.

## 🔧 UI Components

This project includes a full suite of Shadcn/UI components:

- Forms: Input, Textarea, Select, Checkbox, Radio, Switch
- Overlays: Dialog, Sheet, Drawer, Popover, Tooltip
- Navigation: Navigation Menu, Menubar, Breadcrumb, Tabs
- Feedback: Alert, Toast, Progress, Skeleton
- Data Display: Table, Card, Avatar, Badge, Calendar
- And many more...

Import components from `@/components/ui/*`:

```tsx
import { Button } from "@/components/ui/button";
import { Card } from "@/components/ui/card";
```

## 🌐 SEO

The project includes a reusable SEO component. Use it in your pages:

```tsx
import { SEO } from "@/components/SEO";

export default function Page() {
  return (
    <>
      <SEO 
        title="Page Title"
        description="Page description"
        image="/og-image.png"
      />
      {/* Your content */}
    </>
  );
}
```

## 🚀 Deployment

### Vercel (Recommended)

Click the button below to deploy to Vercel:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

Or use the Vercel CLI:

```bash
npm i -g vercel
vercel
```

### Other Platforms

Build the production bundle:

```bash
npm run build
```

Then deploy the `.next` folder to your hosting platform.

## 📝 Environment Variables

Create a `.env.local` file with the following variables:

```bash
# Add your environment variables here
# NEXT_PUBLIC_API_URL=
# DATABASE_URL=
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is built with [Softgen](https://softgen.ai) - AI-powered software development.

## 🆘 Support

For issues and questions:
- Check the [Next.js documentation](https://nextjs.org/docs)
- Visit [Shadcn/UI documentation](https://ui.shadcn.com)
- Contact [Softgen Support](https://softgen.ai/support)

---

Built with ❤️ using [Softgen](https://softgen.ai)