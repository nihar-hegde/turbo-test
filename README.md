# Turborepo with Next.js, Tailwind CSS, and shadcn/ui

A monorepo setup using Turborepo with a Next.js application configured with Tailwind CSS and shadcn/ui components.

## Project Structure

- **Apps**: Contains the main Next.js application
  - `apps/valtro-app` - Main Next.js application
- **Packages**: Shared packages and UI components
  - `packages/ui` - Shared UI component library with shadcn/ui setup

## Adding New Components

When adding new shadcn/ui components to the shared UI package, follow these steps:

### 1. Generate Component
Run the CLI command to add new components to `packages/ui`. This will automatically add the component to `packages/ui/src/components/ui/`.

### 2. Update Import Paths
After generation, manually update the import path for utils in the new component:
- Change: `@/lib/utils`
- To: `../../lib/utils`

### 3. Export Component
Add the component export to `packages/ui/src/components/ui/index.ts` to make it available for use in the main application.

## Usage

Once the above steps are completed, the component will be available for import and use in the main application (`apps/valtro-app`).