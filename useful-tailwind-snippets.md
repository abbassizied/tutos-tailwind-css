# 🧩 Tailwind CSS Snippets

**A collection of reusable and customizable UI components built with Tailwind CSS.**
> All components are mobile-first and built using utility-first Tailwind CSS classes. Customize spacing, color, typography, and responsiveness as needed.

## Some Useful Links

- [A free repository for community components using Tailwind CSS](https://www.creative-tim.com/twcomponents)
- [Tailwind CSS Components Library](https://tailwindflex.com/)
- [Tailwind CSS UI Components, Blocks and Templates to Build Faster!](https://tailgrids.com/components)

- [Cheat sheet](https://cheatsheet-tailwindcss.vercel.app/)
- [Vs extension](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)
 
---

## 📦 Core Components

* **Button**
  Primary, secondary, icon, ghost, and toggle variants with support for disabled and loading states.
```css
/* button.css */
.btn {
  @apply inline-flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium transition-all duration-150 disabled:opacity-50 disabled:cursor-not-allowed;
}
.btn-primary {
  @apply bg-blue-600 text-white hover:bg-blue-700 focus:ring-2 focus:ring-blue-400;
}
.btn-secondary {
  @apply bg-gray-200 text-gray-800 hover:bg-gray-300 focus:ring-2 focus:ring-gray-400;
}
.btn-ghost {
  @apply bg-transparent text-gray-700 hover:bg-gray-100 focus:ring-2 focus:ring-gray-200;
}
.btn-icon {
  @apply p-2 rounded-full text-gray-600 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-300;
}
```

```html
<!-- Base styles for all buttons -->
<button class="inline-flex items-center justify-center gap-2 px-4 py-2 rounded-lg text-sm font-medium transition-all duration-150 disabled:opacity-50 disabled:cursor-not-allowed">
  Button
</button>

<!-- Primary Button -->
<button class="bg-blue-600 text-white hover:bg-blue-700 focus:ring-2 focus:ring-blue-400 focus:outline-none disabled:opacity-50 disabled:cursor-not-allowed inline-flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium transition-all duration-150">
  Primary
</button>

<!-- Secondary Button -->
<button class="bg-gray-200 text-gray-800 hover:bg-gray-300 focus:ring-2 focus:ring-gray-400 focus:outline-none disabled:opacity-50 disabled:cursor-not-allowed inline-flex items-center gap-2 px-4 py-2 rounded-lg text-sm font-medium transition-all duration-150">
  Secondary
</button>

<!-- Just icon -->
<button class="p-2 rounded-full hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-300 text-gray-600 disabled:opacity-50">
  <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
    <path d="M5 12h14M12 5l7 7-7 7" />
  </svg>
</button>

<!-- Icon + Text -->
<button class="inline-flex items-center gap-2 px-4 py-2 rounded-lg bg-blue-600 text-white hover:bg-blue-700 focus:ring-2 focus:ring-blue-400 disabled:opacity-50">
  <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
    <path d="M5 12h14M12 5l7 7-7 7" />
  </svg>
  Next
</button>

<!--  Ghost Button (transparent, subtle) -->
<button class="bg-transparent text-gray-700 hover:bg-gray-100 focus:ring-2 focus:ring-gray-200 px-4 py-2 rounded-lg transition disabled:opacity-50">
  Ghost
</button>

<!-- Loading State (with spinner) -->
<button class="relative inline-flex items-center gap-2 px-4 py-2 rounded-lg bg-blue-600 text-white hover:bg-blue-700 disabled:opacity-50" disabled>
  <svg class="animate-spin h-4 w-4 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8v8z"></path>
  </svg>
  Loading...
</button>

<!-- 💡 Optional: Component Classes (Tailwind + DRY) -->
<button class="btn btn-primary">Save</button>
<button class="btn btn-secondary">Cancel</button>
<button class="btn btn-ghost">Ghost</button>
<button class="btn-icon">
  <svg class="w-5 h-5">...</svg>
</button>
```

* **Badge**
  Small visual indicators for status, notifications, or labels (e.g., "New", "99+", "Beta").
```css
/* badge.css */
.badge {
  @apply inline-block px-2 py-0.5 text-xs font-medium rounded-full;
}
.badge-success {
  @apply bg-green-100 text-green-800;
}
.badge-danger {
  @apply bg-red-100 text-red-800;
}
.badge-info {
  @apply bg-blue-100 text-blue-800;
}
.badge-warning {
  @apply bg-yellow-100 text-yellow-800;
}
.badge-dot {
  @apply h-2 w-2 rounded-full;
}
```

```html
<span class="inline-block px-2 py-0.5 text-xs font-medium bg-green-100 text-green-800 rounded-full">
  Active
</span>

<span class="inline-block px-2 py-0.5 text-xs font-medium bg-blue-100 text-blue-800 rounded-full">
  Info
</span>

<span class="inline-block px-2 py-0.5 text-xs font-medium bg-yellow-100 text-yellow-800 rounded-full">
  Pending
</span>

<span class="inline-block px-2 py-0.5 text-xs font-medium bg-red-100 text-red-800 rounded-full">
  Error
</span>

<span class="inline-flex items-center justify-center min-w-[1.5rem] h-5 px-1.5 text-xs font-bold bg-red-600 text-white rounded-full">
  99+
</span>

<span class="badge badge-success">Success</span>
```

* **Chips**
  Compact elements for tags, filters, or actions, optionally with dismiss icons.

* **Icon**
  Scalable, inline-friendly icons (e.g., using Heroicons or Lucide).

* **Divider**
  Visual separators to group content vertically or horizontally.

* **Toolbar**
  Flexible container for tool-based UI like topbars or command bars.

---

## 🧱 Layout & Structure

* **Container**
  Centered, constrained wrapper to organize page content with consistent padding and responsive width.
```css
  .app-container {
    @apply mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl;
  }
```

```html
<!-- Simple Responsive Container -->
<div class="container mx-auto px-4">
  <!-- Your page content here -->
</div>

<!-- Custom Utility Class (Reusable Container) -->
<div class="app-container">
  <!-- Consistent layout across pages -->
</div>
```

* **Card Component**
  Flexible, shadowed boxes ideal for grouping content like text, images, or interactive elements.

* **Colored Message Blocks**
  Use contextual colors (info, success, warning, error) to highlight messages or sections.
```css
  .msg-info {
    @apply bg-blue-600 text-white;
  }
  .msg-success {
    @apply bg-green-600 text-white;
  }
  .msg-warning {
    @apply bg-yellow-500 text-white;
  }
  .msg-error {
    @apply bg-red-600 text-white;
  }
  .msg-block {
    @apply p-4 rounded-md mb-4 text-sm font-medium;
  }
```

```html

<!-- Basic Colored Message Blocks -->
<div class="p-4 rounded-md text-white bg-blue-600 mb-4">
  <p class="text-sm font-medium">Info: This is an informational message.</p>
</div>

<!-- With Icon and Close Button -->
<div class="flex items-center p-4 mb-4 rounded-md bg-blue-600 text-white">
  <svg class="w-5 h-5 mr-2 flex-shrink-0" fill="none" stroke="currentColor" stroke-width="2"
       viewBox="0 0 24 24" aria-hidden="true">
    <path stroke-linecap="round" stroke-linejoin="round" d="M13 16h-1v-4h-1m1-4h.01M12 2a10 10 0 100 20 10 10 0 000-20z" />
  </svg>
  <p class="flex-grow text-sm font-medium">Info: This is an informational message with icon.</p>
  <button class="ml-4 text-white hover:text-gray-200 focus:outline-none" aria-label="Close">
    <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
    </svg>
  </button>
</div>
 
<!-- Reusable Utility Classes for Variants -->
<div class="msg-block msg-info">Info message</div>
<div class="msg-block msg-success">Success message</div>
<div class="msg-block msg-warning">Warning message</div>
<div class="msg-block msg-error">Error message</div>
```

* **Notification / Alert Blocks**
  Bold, attention-grabbing alerts for user feedback, status updates, or important notices.
  
* **Menu**
  Dropdown or context menu for triggering actions or navigating.

* **Sidenav (Drawer)**
  Collapsible side navigation menu with overlay or inline modes.

* **Tabs**
  Tabbed interface to organize content into sections.

---

## 🧭 Navigation && 🎨 UI Elements

* **Navbar**
  Responsive horizontal navigation with support for branding, links, dropdowns, and buttons.
```html
  <nav class="bg-white shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">
        <!-- Brand -->
        <div class="flex-shrink-0 flex items-center">
          <span class="text-xl font-bold text-indigo-600">MyBrand</span>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden md:block">
          <div class="ml-10 flex items-baseline space-x-4">
            <a href="#" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-indigo-600 hover:bg-indigo-50 transition-colors duration-200">Home</a>
            <a href="#" class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-indigo-600 hover:bg-indigo-50 transition-colors duration-200">Features</a>
            <div class="relative group">
              <button class="px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:text-indigo-600 hover:bg-indigo-50 transition-colors duration-200 flex items-center">
                Dropdown
              </button>
              <div class="absolute left-0 mt-2 w-48 bg-white shadow-lg rounded-md py-1 hidden group-hover:block z-10">
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Item One</a>
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Item Two</a>
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Item Three</a>
              </div>
            </div>
            <a href="#" class="px-3 py-2 rounded-md text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 transition-colors duration-200">Get Started</a>
          </div>
        </div>

        <!-- Mobile menu button -->
        <div class="md:hidden flex items-center">
          <button type="button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-indigo-600 hover:bg-indigo-50 focus:outline-none">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu (Hidden by default) -->
    <div class="md:hidden hidden">
      <div class="pt-2 pb-3 space-y-1 sm:px-3">
        <a href="#" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-indigo-600 hover:bg-indigo-50">Home</a>
        <a href="#" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-indigo-600 hover:bg-indigo-50">Features</a>
        <div class="px-3 py-2 rounded-md text-base font-medium text-gray-700">
          <button class="w-full text-left">Dropdown</button>
          <div class="mt-1 pl-4 space-y-1">
            <a href="#" class="block text-sm text-gray-700 hover:bg-gray-100 hover:text-indigo-600 px-3 py-2 rounded-md">Item One</a>
            <a href="#" class="block text-sm text-gray-700 hover:bg-gray-100 hover:text-indigo-600 px-3 py-2 rounded-md">Item Two</a>
            <a href="#" class="block text-sm text-gray-700 hover:bg-gray-100 hover:text-indigo-600 px-3 py-2 rounded-md">Item Three</a>
          </div>
        </div>
        <a href="#" class="block px-3 py-2 rounded-md text-base font-medium text-white bg-indigo-600 hover:bg-indigo-700">Get Started</a>
      </div>
    </div>
  </nav>
```

* **Pagination**
  Clean and adaptable pagination component for navigating between multiple content pages.
```html
  <nav aria-label="Pagination" class="inline-flex flex-wrap gap-2 items-center">
    <!-- Previous Button -->
    <a href="#" class="px-3 py-2 text-sm font-medium text-gray-700 bg-white border border-gray-300 rounded-l-md hover:bg-gray-50 focus:outline-none transition-colors duration-200">
      ← Previous
    </a>

    <!-- Page Numbers -->
    <div class="flex gap-1 flex-wrap">
      <a href="#" class="px-3 py-2 text-sm font-medium text-indigo-600 bg-indigo-50 border border-indigo-200 rounded-md hover:bg-indigo-100 focus:outline-none">
        1
      </a>
      <a href="#" class="px-3 py-2 text-sm font-medium text-gray-700 bg-white border border-gray-300 hover:bg-gray-50 focus:outline-none">
        2
      </a>
      <a href="#" class="px-3 py-2 text-sm font-medium text-gray-700 bg-white border border-gray-300 hover:bg-gray-50 focus:outline-none">
        3
      </a>
      <span class="px-3 py-2 text-sm font-medium text-gray-400 bg-white border border-gray-300">…</span>
      <a href="#" class="px-3 py-2 text-sm font-medium text-gray-700 bg-white border border-gray-300 hover:bg-gray-50 focus:outline-none">
        10
      </a>
    </div>

    <!-- Next Button -->
    <a href="#" class="px-3 py-2 text-sm font-medium text-gray-700 bg-white border border-gray-300 rounded-r-md hover:bg-gray-50 focus:outline-none transition-colors duration-200">
      Next →
    </a>
  </nav>
```

* **Headers & Footers**
  Standard top and bottom sections of a page with navigation, branding, or links. 
```html
  <!-- Header -->
  <header class="bg-white shadow-sm sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
      <!-- Brand -->
      <div class="flex-shrink-0">
        <span class="text-xl font-bold text-indigo-600">MyBrand</span>
      </div>

      <!-- Navigation -->
      <nav class="hidden md:flex space-x-6">
        <a href="#" class="text-sm font-medium text-gray-700 hover:text-indigo-600 transition-colors duration-200">Home</a>
        <a href="#" class="text-sm font-medium text-gray-700 hover:text-indigo-600 transition-colors duration-200">Features</a>
        <a href="#" class="text-sm font-medium text-gray-700 hover:text-indigo-600 transition-colors duration-200">Pricing</a>
        <a href="#" class="text-sm font-medium text-gray-700 hover:text-indigo-600 transition-colors duration-200">Contact</a>
      </nav>

      <!-- Mobile Menu Button -->
      <button class="md:hidden text-gray-500 hover:text-indigo-600 focus:outline-none">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </div>
  </header>

  <!-- Main Content -->
  <main class="flex-grow py-12 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
    <h1 class="text-3xl font-bold mb-6">Welcome to My Website</h1>
    <p class="text-lg text-gray-700 leading-relaxed">
      This is the main content area. You can replace this text with your own content.
    </p>
  </main>

  <!-- Footer -->
  <footer class="bg-white border-t border-gray-200 py-8 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-8">
      <!-- Brand & Description -->
      <div class="flex flex-col items-start">
        <span class="text-xl font-bold text-indigo-600">MyBrand</span>
        <p class="text-sm text-gray-500 mt-1">A simple and beautiful website template built with Tailwind CSS.</p>
      </div>

      <!-- Quick Links -->
      <div class="flex flex-col md:flex-row gap-6">
        <div>
          <h3 class="font-semibold text-gray-700 mb-2">Company</h3>
          <ul class="space-y-1 text-sm text-gray-500">
            <li><a href="#" class="hover:text-indigo-600 transition-colors">About</a></li>
            <li><a href="#" class="hover:text-indigo-600 transition-colors">Careers</a></li>
            <li><a href="#" class="hover:text-indigo-600 transition-colors">Blog</a></li>
          </ul>
        </div>
        <div>
          <h3 class="font-semibold text-gray-700 mb-2">Support</h3>
          <ul class="space-y-1 text-sm text-gray-500">
            <li><a href="#" class="hover:text-indigo-600 transition-colors">Help Center</a></li>
            <li><a href="#" class="hover:text-indigo-600 transition-colors">Terms of Service</a></li>
            <li><a href="#" class="hover:text-indigo-600 transition-colors">Privacy Policy</a></li>
          </ul>
        </div>
      </div>

      <!-- Social Icons -->
      <div class="flex space-x-4">
        <a href="#" aria-label="Twitter" class="text-gray-400 hover:text-indigo-600 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
          </svg>
        </a>
        <a href="#" aria-label="GitHub" class="text-gray-400 hover:text-indigo-600 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
          </svg>
        </a>
        <a href="#" aria-label="LinkedIn" class="text-gray-400 hover:text-indigo-600 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.454C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"/>
          </svg>
        </a>
      </div>
    </div>

    <!-- Copyright -->
    <div class="mt-8 pt-6 border-t border-gray-200 text-center text-sm text-gray-500">
      © 2025 MyBrand. All rights reserved.
    </div>
  </footer>
```
 
---

## 🧩 Form Controls

* **Input Field**
  Text inputs with support for states (focused, error, disabled), icons, and labels.

* **Textarea**
  Multiline input with responsive resizing and validation styling.

* **Checkbox**
  Custom styled checkboxes with label support and toggle animations.

* **Radio Button**
  Custom radio inputs grouped by field name with full keyboard accessibility.

* **Select**
  Styled dropdown menus with optional search or multi-select features.

* **Autocomplete**
  Type-ahead input with filtered suggestion dropdown.

* **Datepicker**
  Input with a popover calendar for date selection.

* **Timepicker**
  Input for selecting time via dropdown or slider interface.

* **Form Field Wrapper**
  Common layout for labels, inputs, hints, and error messages.

---

## 🔐 Forms & Authentication

* **Sign-In Form**
  Minimal and secure login form with input fields for email/username and password.
```html
  <div class="max-w-md w-full bg-white rounded-lg shadow-md p-6 sm:p-8 space-y-6">
    <div>
      <h2 class="text-2xl font-bold text-gray-900">Sign in to your account</h2>
      <p class="mt-2 text-sm text-gray-600">Enter your email and password below to access your dashboard.</p>
    </div>

    <form class="space-y-6">
      <!-- Email/Username -->
      <div>
        <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email or Username</label>
        <input
          type="text"
          id="email"
          class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 transition-colors duration-200"
          placeholder="you@example.com"
          required
        />
      </div>

      <!-- Password -->
      <div>
        <label for="password" class="block text-sm font-medium text-gray-700 mb-1">Password</label>
        <div class="relative">
          <input
            type="password"
            id="password"
            class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 transition-colors duration-200"
            placeholder="••••••••"
            required
          />
          <button
            type="button"
            class="absolute inset-y-0 right-0 pr-3 flex items-center text-gray-400 hover:text-gray-600"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Remember Me & Forgot Password -->
      <div class="flex items-center justify-between">
        <label class="flex items-center">
          <input
            type="checkbox"
            class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded"
          />
          <span class="ml-2 text-sm text-gray-600">Remember me</span>
        </label>
        <a href="#" class="text-sm text-indigo-600 hover:text-indigo-800">Forgot password?</a>
      </div>

      <!-- Submit Button -->
      <div>
        <button
          type="submit"
          class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 transition-colors duration-200"
        >
          Sign in
        </button>
      </div>

      <!-- Alternative Option -->
      <p class="text-center text-sm text-gray-500">
        Don't have an account?
        <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">Sign up</a>
      </p>
    </form>
  </div>
```

* *(Optional additions: Sign-Up Form, Password Reset, 2FA Input)*

---

## 📊 Data Display

* **Table**
  Responsive, styled tables for listing structured data with optional sorting or zebra striping.
```html
<div class="max-w-7xl mx-auto bg-white shadow rounded-lg overflow-hidden">
    <!-- Table Title -->
    <div class="px-4 py-3 border-b border-gray-200">
      <h2 class="text-lg font-semibold text-gray-800">User List</h2>
    </div>

    <!-- Table Container -->
    <div class="overflow-x-auto">
      <table class="min-w-full divide-y divide-gray-200">
        <thead class="bg-gray-50">
          <tr>
            <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
              Name
            </th>
            <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
              Email
            </th>
            <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
              Role
            </th>
            <th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
              Status
            </th>
            <th scope="col" class="relative px-6 py-3">
              <span class="sr-only">Actions</span>
            </th>
          </tr>
        </thead>
        <tbody class="divide-y divide-gray-200">
          <tr class="hover:bg-gray-50 transition-colors duration-150">
            <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
              Jane Cooper
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
              jane.cooper@example.com
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
              Admin
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-100 text-green-800">
                Active
              </span>
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
              <button class="text-indigo-600 hover:text-indigo-900 mr-3">Edit</button>
              <button class="text-red-600 hover:text-red-900">Delete</button>
            </td>
          </tr>
          <tr class="hover:bg-gray-50 transition-colors duration-150">
            <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
              Michael Jordan
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
              michael.jordan@example.com
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
              User
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-yellow-100 text-yellow-800">
                Inactive
              </span>
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
              <button class="text-indigo-600 hover:text-indigo-900 mr-3">Edit</button>
              <button class="text-red-600 hover:text-red-900">Delete</button>
            </td>
          </tr>
          <tr class="hover:bg-gray-50 transition-colors duration-150">
            <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
              Robert Fox
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
              robert.fox@example.com
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">
              Guest
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-100 text-green-800">
                Active
              </span>
            </td>
            <td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
              <button class="text-indigo-600 hover:text-indigo-900 mr-3">Edit</button>
              <button class="text-red-600 hover:text-red-900">Delete</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
```


* *(Optional additions: Empty states, Loading skeletons, Filters)*

---
