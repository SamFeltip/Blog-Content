---
tags: [sharrowvale, technology/programming]
---

# Astro Pagefind

## Requirements

Pagefind API support for on Astro SSR

Potential Existing support for SSR with template UI.[^1] Upon further reading, this component renders the required code to run pagefind client side.

We need to be able to call the static pagefind api from the Astro backend. This would let us render search components in Astro and send responses [[htmx]] style.

## Research

You can run pagefind as a separate server. Could this be used to easily connect two services?

You can also run pagefind on node.[^2] Its unclear if this is just for indexing, or for searching too. Will need to test this with astro.

Found a GitHub issue for running pagefind in node.[^3] This is pretty clearly what would be needed before an Astro version of pagefind was possible. It would certainly be the required step for working on this.

## Proposal

1. Run pagefind search api within Node.js
2. Run this pagefind search api within an Astro component
3. Make use of pagefind search api within Astro component to serve search in Astro SSR
4. Support Astro features such as pagination in pagefind queries

[^1]: https://github.com/shishkin/astro-pagefind?tab=readme-ov-file#pre-filled-search-query
[^2]: https://pagefind.app/docs/node-api/
[^3]: https://github.com/CloudCannon/pagefind/issues/519
