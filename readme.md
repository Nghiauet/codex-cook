# Next.js Beginner Tutorial (Step by Step)

This guide walks you through building your first Next.js app with **zero prior React or frontend experience**. Each step is short, clear, and hands-on.

## 0) Install Node.js (Required)
Next.js runs on Node.js.

1. Visit **https://nodejs.org**
2. Download and install the **LTS** version
3. Verify in your terminal:

```bash
node -v
npm -v
```

---

## 1) Create a New Next.js Project
Run this in your terminal:

```bash
npx create-next-app@latest my-first-next-app
```

When prompted, choose:
- **TypeScript?** No
- **ESLint?** Yes
- **Tailwind?** No
- **App Router?** Yes
- **Use src/ directory?** Yes
- **Import alias?** Yes

---

## 2) Start the Development Server
```bash
cd my-first-next-app
npm run dev
```

Open your browser at:
```
http://localhost:3000
```
You should see the default Next.js page.

---

## 3) Your First Change (Edit the Homepage)
Open:
```
src/app/page.js
```
Replace its content with:

```jsx
export default function Home() {
  return (
    <main>
      <h1>Hello, Next.js Beginner!</h1>
      <p>This is my first page.</p>
    </main>
  );
}
```

Save and refresh the browser to see your new text.

---

## 4) Add a Second Page
Create a new file:
```
src/app/about/page.js
```

Add:

```jsx
export default function About() {
  return (
    <main>
      <h1>About Me</h1>
      <p>I’m learning Next.js!</p>
    </main>
  );
}
```

Visit:
```
http://localhost:3000/about
```

---

## 5) Add a Link Between Pages
Edit `src/app/page.js`:

```jsx
import Link from "next/link";

export default function Home() {
  return (
    <main>
      <h1>Hello, Next.js Beginner!</h1>
      <p>This is my first page.</p>
      <Link href="/about">Go to About Page</Link>
    </main>
  );
}
```

---

## 6) Add Simple Styling
Edit:
```
src/app/globals.css
```

Add:

```css
main {
  font-family: Arial, sans-serif;
  padding: 2rem;
}

h1 {
  color: #0070f3;
}
```

---

## 7) What You Learned
✅ Create pages
✅ Navigate with links
✅ Edit components
✅ Apply basic styling

---

## Next Steps (Optional)
- Add images in `/public`
- Learn React basics (props, state)
- Create reusable components
- Deploy on Vercel
