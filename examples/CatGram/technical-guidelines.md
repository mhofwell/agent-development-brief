# Technical Guidelines

Defines the technology stack, architectural constraints, and system requirements that you must work within. This ensures the agent using chosen tools and respects performance/integration requirements, while leaving implementation details flexible.

## Tech Stack (Required)

- **Frontend:** Next.js 14+ with App Router
- **Styling:** Tailwind CSS + shadcn/ui components
- **Authentication & Database:** Supabase (Postgres)
- **Backend APIs:** Node.js/Express with TypeScript
- **Deployment:** Railway.app
- **Icons:** Lucide React

## Architecture Constraints

- Use Server Actions instead of API routes where appropriate
- Database queries through Supabase client
- TypeScript throughout - no JavaScript files
- Environment variables for all API keys and secrets

## Performance Requirements

- Photo upload within 30 seconds typical case
- Feed loads within 2 seconds on mobile
- Images optimized for mobile viewing
- Responsive design works on all common mobile browsers

## Integration Requirements

- Image storage and CDN through Supabase Storage
- Real-time updates for likes/comments (consider Supabase realtime)
- Image resizing and optimization pipeline
- Basic content moderation hooks

## Development Standards

- ESLint + Prettier configured
- Component-first architecture
- Error boundaries for image upload failures
- Graceful degradation when images fail to load
- Basic logging for debugging production issues

## Known Limitations

- No video uploads in MVP
- No advanced photo editing
- Basic text-only comments (no image replies)
- Single photo per post only
- No photo filters or effects