# What is Web Security? HTML & JavaScript Review
Video: https://www.youtube.com/watch?v=5JJrJGZ_LjM

## What is web security?
- Browser security
  - Browser enforces certain rules
  - Same Origin Policy
    - Isolate webpages from each other
- Server app security
  - Servers arent in control of what the client is doing on the client machine
  - Attackers can run arbitrary HTTP clients; can send anything to the server
- Client app security
  - Prevent user from being attacked while using web app locally
  - XSS - Cross site scripting
- Protect the user
  - From social engineering
  - From trackers, private data being leaked

## Why is web security hard?
- We're trying to run untrusted code securely - extremely ambitious goal
- Different site interacting in the same tab (mashups)
- Low-level features and hardware access
- Desire for high performance 
- APIs were not designed from first principles; it evolved over time - we have a different model for the web now vs when it was create
- Strict backwards compatibility requirements (dont break the web)
- Modern web apps are built on a tangle of technologies that have been developed over time then haphazardly pieced together.  Every piece of the web app stack, from HTTP requests to browser-side scripts, comes with important yet subtle security consequences.  To keep users safe, it is essential for developers to confidently navigate this landscape 
- The browser has an impossible task
  - Sites, even malicious ones, can
    - downlad content from anywhere
    - spawn worker processes
    - open sockets to a server or even another users browser
    - display media in a huge number of formats
    - run custom code on the GPU
    - save/read data from the filesystem
- Differing visions for the web
  - Simple document viewer
  - Powerful application platform
- The web is robust
  - Its all too easy to criticize, lament, and create paranoid scenarios about the 'unsound security foundations' of the web.  Truth is, all of that criticism is true, and yet the web has proven to be an incredibly robust platform

# This course
- Part 1: Browser security model, same origin policy
- Part 2: Client security: attacks, defense
- Part 3: Server security: attacks, defense, authentication, TLS
- Part 4: Writing secure code

# HTML
## Ways to specify a URL
- Full URL `<a href='http://stanford.edu/news/2019/'>2019 News</a>`
- Relative URL `<a href='september'>September news</a>` 
  - same as `https://stanford.edu/news/2019/september`
- Absolute URL `<a href='/events'>Events</a>`
  - same as `https://stanford.edu/events`
  - goes to root directory and starts building path from there
- Fragment URL: `<a href='#section3'>Jump to section 3</a>`
  - Tacks on a fragment and takes you to a specific element