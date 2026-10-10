# tinyland-forms (RETIRED)

> **Retired 2026-10-10.** This repository is archived and receives no further
> changes. Its replacement is the SvelteKit remote-function `form()` pattern
> with Effect Schema / Standard Schema validation (estate ruling RU3), which
> `xoxd-ai/site.scaffold` is adopting as the default for every Tinyland site.

`@tummycrypt/tinyland-forms` held reusable Zod schemas, field validators and
`sveltekit-superforms` integration helpers. The estate is replacing
sveltekit-superforms with SvelteKit remote functions (`query` / `form` /
`command`), so these helpers have no future consumer. No live app imports this
package, so it was retired in the 2026-10 estate uplift (rulings RU2/RU7)
rather than moved to the new stack.

- Replacement: declare forms with `form()` from `$app/server` in a
  `*.remote.ts` module and validate with an Effect Schema (Standard Schema)
  value. Upstream docs: https://svelte.dev/docs/kit/remote-functions
- Bazel registry: `tummycrypt_tinyland_forms` 0.2.2 and 0.2.3 in
  [xoxd-ai/bazel-registry](https://github.com/xoxd-ai/bazel-registry) are
  marked `deprecated`. They stay resolvable; nothing is yanked.
- npm: no further versions will be published (RU8). Published versions are not
  unpublished.
- Code: the last released source is tag `v0.2.2`. Copy any schema or validator
  you still need into your own app instead of depending on this package.
