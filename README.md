## UI/UX Developer Code Test

# Overview

This project is a Vue 3-based frontend implementation of a dental record management interface, built as a response to a UI/UX Developer Code Test. The goal was to replicate a provided Figma design with responsive behavior, accessibility, and interactivity in mind.

# 🔧 Project Setup

*Prerequisites*

   Node.js >= 16
   npm >= 8

*Install Dependencies*

    npm install
    Run in Development Mode
    npm run dev
    Build for Production
    npm run build

*Optional Deployment (Recommended)*

Deployed via Vercel. For local builds, use npm run build and deploy the dist/ folder via your preferred static host (Vercel, Netlify, GitHub Pages).

## 🚩 Assumptions and Decisions

1. Tech Stack Choice

Initially planned to use Tailwind CSS v4, but due to technical limitations and compatibility issues, reverted to SCSS for styling.
Used Vue 3 with <script setup> composition API for clean and modern component structuring.

2. Design Interpretation

The Figma file only provided the desktop layout. Responsive layouts for tablet and mobile were created based on standard UX principles.
Colors, spacing, and layout approximations were manually adjusted to maintain fidelity where explicit Figma instructions were missing.

3. Code Structure

Component-based layout:
Sidebar, PatientCard, TimelinePanel, BreadcrumbNav, etc.
Utility mixins and SCSS partials are used for breakpoints and reusable styling.
Angular-inspired structure (due to prior experience) was applied to routing logic and component breakdown.

## 📦 Dependencies Used

vue ^3.4

vite ^5.0

sass ^1.62

@vitejs/plugin-vue

Optional/Dev:

eslint + prettier for linting

vite-plugin-svg-icons for handling SVGs (if configured)


## 💡 Future Improvements

🔬 Code-Level Improvements (Planned but Skipped for Deadline)

Move tag selectors out of .button styles for clearer UI semantics

Input fields to support form validation and readonly vs. edit mode separation

Convert breadcrumb navigation into a dynamic component with route awareness

Improve form field grouping with proper ARIA labels

## 🎯 UX Suggestions for Future

Use side drawer instead of breadcrumb trail for section navigation

Break long forms into collapsible sections or accordions

Avoid using emojis or colorful icons in timeline unless semantically required

Improve spacing for mobile by stacking form fields and reducing padding

🚀 How to Improve Further

🔍 Performance Optimizations

Lazy load heavy components like TimelinePanel

Code split dynamic views (e.g., default placeholder vs. patient view)

Minimize external asset sizes (e.g., compress SVGs and gifs)

# Accessibility Compliance

Add aria-labels, roles, and alt tags to all interactive components

Ensure color contrast meets WCAG AA standards

Replace div clickables with button or a where appropriate

Keyboard navigation support (e.g., for timeline entries)

# Interactivity & Usability

Animate timeline expand/collapse with <Transition>

Add hover/focus effects on buttons and tags

Use toast/snackbar messages for actions like save, update, etc.

Animate tab switching or content loading