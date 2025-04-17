# From Zero to One: Build Your First Software Project

Welcome to this beginner-friendly guide that will take you from zero coding experience to deploying your first web projects. This tutorial is divided into two sections:

- **1-Hour Portfolio Project**: Create and deploy a simple personal portfolio site using GitHub Pages
- **6-Hour Web App Project**: Build a full web application with modern tools and deploy it online

Let's begin your journey into software development!

## Table of Contents

- [1-Hour Portfolio Project](#1-hour-portfolio-project)
  - [Creating a GitHub Account](#creating-a-github-account)
  - [Creating a Git Repository](#creating-a-git-repository)
  - [Pulling the Repository Locally](#pulling-the-repository-locally)
  - [Setting Up VSCode/Cursor](#setting-up-vscodecursor)
  - [Creating and Editing Markdown Files](#creating-and-editing-markdown-files)
  - [Uploading to GitHub Pages](#uploading-to-github-pages)
  - [Setting Up GitHub Pages URL](#setting-up-github-pages-url)
- [6-Hour Web App Project](#6-hour-web-app-project)
  - [Planning Your Web App UI](#planning-your-web-app-ui)
  - [Setting Up a NextJS Project](#setting-up-a-nextjs-project)
  - [Using AI Tools to Accelerate Development](#using-ai-tools-to-accelerate-development)
  - [Implementing ShadCN Design](#implementing-shadcn-design)
  - [Creating Environment Variables](#creating-environment-variables)
  - [Optional: Setting Up Supabase Authentication](#optional-setting-up-supabase-authentication)
  - [Deploying to Vercel](#deploying-to-vercel)
  - [Buying a Domain from DNSSimple](#buying-a-domain-from-dnssimple)
  - [Configuring Your Domain on Vercel](#configuring-your-domain-on-vercel)
- [Next Steps and Resources](#next-steps-and-resources)

---

# 1-Hour Portfolio Project

This section will guide you through creating a simple portfolio website hosted on GitHub Pages. This is perfect for showcasing your resume, projects, or personal information.

## Creating a GitHub Account

GitHub is a platform that hosts code and allows for version control using Git.

1. Go to [GitHub's website](https://github.com/).
2. Click "Sign Up" in the top right corner.
3. Enter your email, create a password, and choose a username.
4. Verify your account (you may need to solve a puzzle).
5. Select your preferences when prompted.
6. Verify your email address by clicking the link sent to your inbox.

**Tip**: Choose a professional username as it will be visible in your portfolio URL.

## Creating a Git Repository

A repository (repo) is like a project folder that stores all your code.

1. Once logged in to GitHub, click the "+" icon in the top right corner.
2. Select "New repository."
3. Name your repository `username.github.io` (replace "username" with your GitHub username).
   - This special naming convention tells GitHub this will be your GitHub Pages site.
4. Add an optional description.
5. Keep the repository public.
6. Check the box that says "Add a README file."
7. Click "Create repository."

**Important**: The repository name **must** follow the format `username.github.io` for the GitHub Pages to work correctly with your username.

## Pulling the Repository Locally

"Pulling" means downloading the repository to your computer to work on it locally.

First, you need to install Git:

1. Download Git from [git-scm.com](https://git-scm.com/downloads).
2. Install it with default settings.

Then, clone your repository:

1. On your repository page, click the green "Code" button.
2. Copy the HTTPS URL shown.
3. Open Terminal (Mac/Linux) or Command Prompt/PowerShell (Windows).
4. Navigate to where you want to store your project:
   ```bash
   cd Documents
   ```
5. Clone the repository:
   ```bash
   git clone https://github.com/username/username.github.io.git
   ```
   (Replace the URL with the one you copied)
6. Navigate into the repository folder:
   ```bash
   cd username.github.io
   ```

## Setting Up VSCode/Cursor

VSCode (Visual Studio Code) is a popular code editor, and Cursor is an AI-enhanced version of VSCode.

1. Download and install [VSCode](https://code.visualstudio.com/) or [Cursor](https://cursor.sh/).
2. Open the application.
3. Go to File > Open Folder.
4. Navigate to and select your repository folder.
5. The folder will open in the editor's Explorer panel.

**Recommended Extensions**:
- Markdown All in One (for Markdown preview and editing)
- GitHub Theme (for GitHub-style syntax highlighting)
- Live Server (to preview your site locally)

To install extensions:
1. Click the Extensions icon in the sidebar (or press Ctrl+Shift+X).
2. Search for the extension name.
3. Click "Install."

## Creating and Editing Markdown Files

Markdown is a simple formatting syntax that converts to HTML.

1. In VSCode/Cursor, right-click in the Explorer panel and select "New File."
2. Name it `index.md` (this will be your homepage).
3. Add content to your file. Here's a sample portfolio template:

```markdown
# Your Name

## About Me
A brief introduction about yourself and your interests.

## Skills
- Skill 1
- Skill 2
- Skill 3

## Projects
### Project 1
Description of project 1.

### Project 2
Description of project 2.

## Contact
- Email: your.email@example.com
- LinkedIn: [Your Name](https://linkedin.com/in/yourprofile)
- GitHub: [Your Username](https://github.com/yourusername)
```

4. Save the file (Ctrl+S or Cmd+S).

You can preview your markdown by:
- Right-clicking in the editor and selecting "Open Preview"
- Or pressing Ctrl+Shift+V (or Cmd+Shift+V on Mac)

## Uploading to GitHub Pages

After creating your content, you need to upload (push) it to GitHub:

1. Open Terminal/Command Prompt in VSCode by pressing `` Ctrl+` `` (backtick).
2. Make sure Git knows who you are:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
3. Stage your changes:
   ```bash
   git add .
   ```
4. Commit your changes:
   ```bash
   git commit -m "Add portfolio content"
   ```
5. Push to GitHub:
   ```bash
   git push origin main
   ```
   (You might be prompted to enter your GitHub credentials)

## Setting Up GitHub Pages URL

Now, you'll activate GitHub Pages to make your site live:

1. Go to your repository on GitHub.
2. Click "Settings" in the top menu.
3. Scroll down to "Pages" in the left sidebar.
4. Under "Source," select "Deploy from a branch."
5. In the "Branch" dropdown, select "main" and "/root" folder, then click "Save."
6. Wait a few minutes for your site to deploy.
7. Refresh the GitHub Pages settings page, and you should see a message saying "Your site is published at https://username.github.io."

Congratulations! Your portfolio is now live on the internet!

**Optional**: To customize your site further, you can add a `_config.yml` file to use GitHub Pages themes. Here's a simple example:

```yaml
theme: jekyll-theme-minimal
title: Your Name's Portfolio
description: A showcase of my projects and skills
```

Save this file in your repository, commit, and push it to apply the theme.

---

# 6-Hour Web App Project

Now that you've got a basic portfolio, let's build something more complex: a web application with modern tools.

## Planning Your Web App UI

Before writing code, it's good to plan your user interface:

1. Go to [Excalidraw](https://excalidraw.com/).
2. Use the tools to sketch your app's layout and features.
3. Consider designing:
   - A homepage
   - Navigation menu
   - Content sections
   - Interactive elements
4. Export your design as an image (File > Export).
5. Save this in your project folder for reference.

**Tips for UI Planning**:
- Focus on user flow: how will people navigate your app?
- Keep it simple for your first project
- Label components and their functions
- Note any interactive elements and what they should do

## Setting Up a NextJS Project

Next.js is a React framework that makes creating web applications easier.

First, ensure you have Node.js installed:
1. Download from [nodejs.org](https://nodejs.org/).
2. Install with default settings.

Then create your Next.js project:

1. Open Terminal/Command Prompt.
2. Navigate to where you want to create your project:
   ```bash
   cd Documents
   ```
3. Create a new Next.js app:
   ```bash
   npx create-next-app@latest my-web-app
   ```
4. Answer the setup questions:
   - Would you like to use TypeScript? → Yes
   - Would you like to use ESLint? → Yes
   - Would you like to use Tailwind CSS? → Yes
   - Would you like to use the `src/` directory? → Yes
   - Would you like to use App Router? → Yes
   - Would you like to customize the default import alias? → No
5. Navigate into your new project:
   ```bash
   cd my-web-app
   ```
6. Open it in VSCode/Cursor:
   ```bash
   code .
   ```
   (or open manually from the editor)

## Using AI Tools to Accelerate Development

AI tools like Claude or ChatGPT can help generate code for specific features. Here's how to use them effectively:

1. Define what you need clearly (e.g., "I need a navigation bar with Home, About, and Contact links").
2. Ask the AI to generate the code:
   ```
   Create a React component for a navigation bar with Home, About, and Contact links using Tailwind CSS in a Next.js project.
   ```
3. Copy the generated code.
4. Paste it into the appropriate file in your project.
5. Modify as needed to fit your design.

**Example Files to Create/Modify**:

1. Create a navigation component:
   - Create `src/components/Navbar.tsx`
   - Paste AI-generated navigation code

2. Modify the home page:
   - Open `src/app/page.tsx`
   - Replace with your own content or AI-generated code

3. Create additional pages:
   - Create `src/app/about/page.tsx`
   - Create `src/app/contact/page.tsx`

## Implementing ShadCN Design

ShadCN provides beautiful, accessible UI components for React applications.

1. Initialize ShadCN in your project:
   ```bash
   npx shadcn-ui@latest init
   ```

2. Follow the prompts:
   - Would you like to use TypeScript? → Yes
   - Which style would you like to use? → Default
   - Which color would you like to use as base color? → Slate
   - Where is your global CSS file? → src/app/globals.css
   - Do you want to use CSS variables? → Yes
   - Where is your tailwind.config.js located? → tailwind.config.js
   - Configure the import alias? → @/components

3. Install components you want to use, for example:
   ```bash
   npx shadcn-ui@latest add button
   npx shadcn-ui@latest add card
   npx shadcn-ui@latest add input
   ```

4. Use these components in your pages:

```tsx
// Example usage in src/app/page.tsx
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from "@/components/ui/card";

export default function Home() {
  return (
    <main className="flex min-h-screen flex-col items-center justify-between p-24">
      <Card className="w-full max-w-md">
        <CardHeader>
          <CardTitle>Welcome to My App</CardTitle>
          <CardDescription>This is my first Next.js application.</CardDescription>
        </CardHeader>
        <CardContent>
          <p>This card is built with ShadCN components.</p>
        </CardContent>
        <CardFooter>
          <Button>Get Started</Button>
        </CardFooter>
      </Card>
    </main>
  );
}
```

## Creating Environment Variables

Environment variables store sensitive information like API keys:

1. Create a `.env.local` file in your project root:
   ```
   NEXT_PUBLIC_SITE_NAME=My Awesome App
   # Add other public variables with NEXT_PUBLIC_ prefix
   
   # Private variables (server-side only)
   API_SECRET_KEY=your_secret_key_here
   ```

2. Access these variables in your code:
   ```tsx
   // For client-side (must start with NEXT_PUBLIC_)
   const siteName = process.env.NEXT_PUBLIC_SITE_NAME;
   
   // For server-side
   // This must be in a Server Component or API route
   const apiKey = process.env.API_SECRET_KEY;
   ```

3. Add `.env.local` to your `.gitignore` file to keep secrets safe.

**Important**: Never commit sensitive keys or tokens to GitHub. Always use environment variables for secrets.

## Optional: Setting Up Supabase Authentication

Supabase is an open-source Firebase alternative that provides authentication services.

1. Create a Supabase account at [supabase.com](https://supabase.com/).
2. Create a new project.
3. Go to Settings > API to find your API keys.
4. Install Supabase in your Next.js project:
   ```bash
   npm install @supabase/supabase-js
   ```

5. Create a Supabase client file `src/lib/supabase.ts`:
   ```typescript
   import { createClient } from '@supabase/supabase-js';

   const supabaseUrl = process.env.NEXT_PUBLIC_SUPABASE_URL || '';
   const supabaseKey = process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY || '';

   export const supabase = createClient(supabaseUrl, supabaseKey);
   ```

6. Add Supabase keys to your `.env.local` file:
   ```
   NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

7. Create a simple login component:

```tsx
// src/components/LoginForm.tsx
'use client';

import { useState } from 'react';
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { supabase } from '@/lib/supabase';

export default function LoginForm() {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');
  const [loading, setLoading] = useState(false);
  const [message, setMessage] = useState('');

  const handleLogin = async (e: React.FormEvent) => {
    e.preventDefault();
    setLoading(true);
    setMessage('');

    try {
      const { error } = await supabase.auth.signInWithPassword({
        email,
        password,
      });

      if (error) throw error;
      setMessage('Logged in successfully!');
    } catch (error: any) {
      setMessage(error.message || 'An error occurred during login');
    } finally {
      setLoading(false);
    }
  };

  return (
    <form onSubmit={handleLogin} className="space-y-4 w-full max-w-md">
      <div>
        <Input
          type="email"
          placeholder="Email"
          value={email}
          onChange={(e) => setEmail(e.target.value)}
          required
        />
      </div>
      <div>
        <Input
          type="password"
          placeholder="Password"
          value={password}
          onChange={(e) => setPassword(e.target.value)}
          required
        />
      </div>
      <Button type="submit" className="w-full" disabled={loading}>
        {loading ? 'Logging in...' : 'Log In'}
      </Button>
      {message && <p className="text-sm text-center">{message}</p>}
    </form>
  );
}
```

8. Add this component to a login page:

```tsx
// src/app/login/page.tsx
import LoginForm from '@/components/LoginForm';

export default function Login() {
  return (
    <main className="flex min-h-screen flex-col items-center justify-center p-24">
      <div className="w-full max-w-md space-y-4">
        <h1 className="text-2xl font-bold text-center">Log In</h1>
        <LoginForm />
      </div>
    </main>
  );
}
```

## Deploying to Vercel

Vercel is the easiest platform to deploy Next.js applications:

1. Create a GitHub repository for your project:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. Create a new repository on GitHub:
   - Go to GitHub and click "New repository"
   - Name it (e.g., "my-web-app")
   - Make it public or private
   - Don't initialize with any files

3. Connect your local project:
   ```bash
   git remote add origin https://github.com/yourusername/my-web-app.git
   git branch -M main
   git push -u origin main
   ```

4. Go to [Vercel](https://vercel.com/) and sign up/log in with GitHub.

5. Click "Add New" > "Project".

6. Select your repository from the list.

7. Configure your project:
   - Framework Preset: Next.js
   - Root Directory: ./
   - Build Command: next build
   - Output Directory: .next

8. Add environment variables from your `.env.local` file.

9. Click "Deploy".

10. Wait for deployment to complete.

## Buying a Domain from DNSSimple

A custom domain looks more professional than a vercel.app subdomain:

1. Go to [DNSSimple](https://dnsimple.com/).

2. Sign up for an account.

3. Search for your desired domain name.

4. Follow the checkout process:
   - Choose the registration period
   - Fill in your contact information
   - Complete the payment

5. After purchase, you'll manage the domain from DNSSimple's dashboard.

## Configuring Your Domain on Vercel

Now connect your domain to your Vercel project:

1. In your Vercel project dashboard, go to "Settings" > "Domains".

2. Enter your domain name (e.g., "mywebapp.com") and click "Add".

3. You'll see DNS configuration instructions. There are two options:
   
   **Option 1: Using Vercel as your nameserver**
   - In DNSSimple, go to "DNS" > "Name Servers"
   - Update the nameservers to the ones provided by Vercel
   - Wait for DNS propagation (up to 48 hours)
   
   **Option 2: Adding DNS records in DNSSimple**
   - In DNSSimple, go to "DNS" > "Records"
   - Add the records shown in Vercel's instructions (usually a CNAME record)

4. Back in Vercel, wait for domain verification.

5. Once verified, your site will be available at your custom domain!

---

# Next Steps and Resources

Congratulations on completing your first web development projects! Here are some suggestions for continuing your learning journey:

## Enhance Your Projects
- Add a blog to your portfolio
- Implement more advanced features in your web app
- Improve accessibility and responsive design

## Learn More
- [Next.js Documentation](https://nextjs.org/docs)
- [React Documentation](https://react.dev/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [ShadCN UI Components](https://ui.shadcn.com/)
- [Supabase Documentation](https://supabase.com/docs)

## Practice and Build
- Create personal projects that solve real problems
- Contribute to open-source projects
- Join coding challenges and hackathons

## Connect with the Community
- Join Discord servers for web development
- Participate in Reddit communities like r/webdev
- Attend local or virtual meetups

Remember, the best way to learn is by building. Keep creating, and don't be afraid to make mistakes along the way!

---

*This tutorial was created to help beginners get started with web development. If you find any issues or have suggestions for improvements, please open an issue on the GitHub repository.*
