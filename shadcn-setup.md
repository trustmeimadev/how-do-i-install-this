# Shadcn/ui Setup for Copy-Paste Warriors

### Prerequisites (Read This or Regret It Later)

You need either:
- Vite + React project (see `react-tailwind.md` for the brain-dead version)

Both should already have Tailwind installed. If not, what the hell have you been doing?

### Step 1: Initialize Shadcn (The Magic Command You'll Forget Tomorrow)

Run this in your project root, genius:

```bash
npx shadcn-ui@latest init
```

Answer the prompts like the indecisive developer you are:
- **TypeScript:** Obviously yes, unless you enjoy runtime surprises
- **Style:** Default (because you have no taste anyway)
- **Base color:** Slate (or whatever, it's your bland website)
- **CSS variables:** Yes (trust the process, or don't, I don't care)

### Step 2: Install Your First Component (Baby Steps)

Let's start with a button because that's probably all you can handle:

```bash
npx shadcn-ui@latest add button
```

Congratulations, you now have a fancy button component you didn't write.

### Step 3: Use It Like a Pro (Copy-Paste Champion)

Import and use it in your component:

```tsx
import { Button } from "@/components/ui/button"

export default function YourComponent() {
  return (
    <Button variant="outline">
      Click me (if you can figure out how)
    </Button>
  )
}
```

### Step 4: Add More Components (Because One Wasn't Enough)

Common ones you'll probably need:

```bash
# For forms (because HTML forms are too mainstream)
npx shadcn-ui@latest add input
npx shadcn-ui@latest add label
npx shadcn-ui@latest add textarea

# For layout (because CSS Grid is apparently rocket science)
npx shadcn-ui@latest add card
npx shadcn-ui@latest add separator

# For the inevitable modal popup
npx shadcn-ui@latest add dialog

# For when you need to show off
npx shadcn-ui@latest add dropdown-menu
npx shadcn-ui@latest add badge
```

### Step 5: Configure Your Path Aliases (If You Skipped This Like an Idiot)

Make sure your `tsconfig.json` or `jsconfig.json` has this:

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```

For Next.js, it's usually already there. For Vite, you probably messed it up.

---

**Pro Tips for the Perpetually Confused:**

1. **Browse components:** Visit [ui.shadcn.com](https://ui.shadcn.com) and copy whatever looks shiny
2. **Customization:** Edit the components in `@/components/ui/` - they're yours now
3. **Theming:** Modify `globals.css` CSS variables like a real developer
4. **Variants:** Read the component props, they're actually documented

**Still Broken?** (Color Me Surprised)

- Check your Tailwind config includes the components folder
- Make sure your path aliases work (`@/` should resolve properly)
- Delete `node_modules` and start over (the universal fix)
- Consider a career in accounting

**Final Note:** You're now using a component library built on top of Radix primitives wrapped in Tailwind classes. Congratulations on adding three layers of abstraction to render a button. Modern web development at its finest.