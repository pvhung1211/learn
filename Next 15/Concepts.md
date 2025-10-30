
### Parallel Routes
- `@parallel`: (don't use it unless u must) https://www.youtube.com/watch?v=wi8kF8UniUI
	- `@users/settings/page.tsx` => render `@users/settings/page.tsx` on `/settings`
	- `@admin/settings/page.tsx` => render `@admin/settings/page.tsx` on `/settings`
	- `@other/default.tsx` 
		- => render `@other/default.tsx` when redirected to `/settings` by url 
		- => render `@other/page.tsx` when redirected to `/settings` by Next.js routing.

### Catch-all Routes
- `[...catchAll]`: 