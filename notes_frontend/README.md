# Personal Notes Frontend (Astro)

Ocean Professional themed web UI to create, edit, view, and organize personal notes.

Features
- Home page list with search and tag filter
- Create, edit, delete notes
- Note detail page with inline editing and duplicate
- Tags support with quick filters
- LocalStorage persistence via a data service abstraction
- Responsive layout: sidebar, topbar, main content
- Smooth transitions, rounded corners, subtle shadows
- No external keys required

Tech
- Astro 5
- TypeScript for types and service layer
- Client-side interactivity with minimal vanilla JS

Run
- Install: npm install
- Dev: npm run dev (served on port 3000 per astro.config.mjs)
- Build: npm run build
- Preview: npm run preview

Structure
- src/styles/theme.css: Ocean Professional theme styles
- src/components/: Topbar, Sidebar, NoteItem, NoteEditor, TagPills
- src/pages/index.astro: Notes list, search, filter, quick create
- src/pages/note/[id].astro: Note detail/edit
- src/lib/types.ts: Note/NoteInput types
- src/lib/storage.ts: SSR-safe localStorage wrapper
- src/lib/notesService.ts: Async CRUD/search abstraction (prep for API swap)

Future backend
- Swap implementations inside src/lib/notesService.ts to call HTTP endpoints.
- Keep async signatures to drop-in replace.

Accessibility
- Semantic labels on inputs, buttons have aria labels, focus rings via :focus styles.

```env
# No env vars required. If adding a backend later:
# NOTES_API_URL=https://api.example.com
```
