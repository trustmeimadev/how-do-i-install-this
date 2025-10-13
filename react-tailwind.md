# React + Tailwind Setup for the Cognitively Impaired

### Step 1: Installing React with Vite (Because You're Too Cool for Create-React-App)

Congratulations, you've chosen Vite. How original. Run this command and try not to mess it up:

```bash
npm create vite
```

Follow the prompts like a good little developer. Pick React, pick TypeScript if you have any self-respect left, and try not to name your project "my-app" like every other unimaginative code monkey.

### Step 2: Install Tailwind CSS (For When You Can't Write Real CSS)

Because writing actual CSS is apparently too hard for modern developers:

```bash
npm install tailwindcss @tailwindcss/vite
```

### Step 3: Configure the Vite Plugin (Copy-Paste Like Your Life Depends On It)

Open your `vite.config.js` file and replace whatever garbage is in there with this:

```js
import { defineConfig } from 'vite';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [tailwindcss()],
});
```

Don't ask me why this works. It just does. Moving on.

### Step 4: Import Tailwind (The Final Nail in Your CSS Skills' Coffin)

Find your `globals.css` or `index.css` file (it's probably right there, genius) and slap this at the top:

```css
@import 'tailwindcss';
```

That's it. You're now officially a Tailwind developer. Congratulations on joining the ranks of developers who think `className="flex justify-center items-center"` is peak engineering.

---

**Still Confused?** (Of Course You Are)

Check these links before bothering me:

- [Vite Guide](https://vite.dev/guide/) - Read it. Seriously.
- [Tailwind with Vite](https://tailwindcss.com/docs/installation/using-vite) - The official docs that you should have read first

**Pro Tip:** If this doesn't work, you probably typed something wrong. Check your spelling, check your file paths, and question your life choices that led you to web development.
