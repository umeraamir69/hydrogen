---
"@shopify/hydrogen": minor
---

`requestContext.markResponseAsPersonalized(reason)` is now public. Call it when a response holds customer data that Hydrogen can't see, such as a page that renders a cart from `getCart()` or from a separate `/api/cart` request. `requestContext.applyResponseHeaders()` then makes that response private and uncacheable, and removes `Surrogate-Control` and vendor `*-Cache-Control` headers. Responses that you don't mark stay cacheable.
