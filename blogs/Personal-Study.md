---
description: Blog updates from my personal research and study
icon: display-code
---

# Personal Research and Study


## Differences between Server-side and Client-side Rendering

Server-Side Rendering (SSR) and Client-Side Rendering (CSR) are two approaches for rendering web pages. They differ in when and where the HTML is generated and delivered to the user’s browser.

**Client-Side Rendering (CSR)**

- **How It Works**: 
  - In CSR, the initial HTML sent by the server is mostly empty or contains a minimal shell (like a `<div id="root">` for React apps). 
  - The browser then downloads the JavaScript bundle, which contains the code for rendering the UI, and the app is rendered dynamically on the client side (the user's browser). 
  - The app fetches data and dynamically populates the UI, making it interactive once the JavaScript execution is complete.

**Server-Side Rendering (SSR)**

- **How It Works**: 
  - In SSR, the HTML is generated on the server based on the request. When a user requests a page, the server fetches the necessary data and renders the full HTML page, which is then sent to the user's browser.
  - The browser receives the fully rendered HTML, which can be displayed immediately. Afterward, the JavaScript is loaded to make the page interactive, a process known as "hydration."

| Feature               | Client-Side Rendering (CSR)                 | Server-Side Rendering (SSR)                 |
|-----------------------|---------------------------------------------|--------------------------------------------|
| **Initial Load Speed** | Slower (HTML rendered after JS is executed) | Faster (HTML rendered and sent by server)  |
| **Subsequent Navigation** | Fast (no full page reloads)               | Slower (can involve server round trips)    |
| **SEO**               | Challenging (requires workarounds)          | Better (full HTML available for crawlers)  |
| **Server Load**       | Lower (serves static assets and APIs)       | Higher (renders HTML for each request)     |
| **Complexity**        | Simpler (no server-side rendering logic)    | More complex (requires handling on server) |
\