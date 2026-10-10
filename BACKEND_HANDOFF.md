InkSpark backend handoff
Current state
This is a standalone, browser-run front end. It does not connect to CloudPages or any other backend, and it is not yet a production public release.
Backend capabilities needed for public release
Secure sign-up/sign-in and account recovery (server-side password hashing; never store raw passwords in the browser)
Database for users, profiles, stories, chapters, library, reading progress, follows, comments, reactions, reports, and moderation records
Object storage and image processing for profile pictures, banners, and story covers
Server-authoritative XP, anti-abuse controls, seasonal reader and author leaderboards, and rewards
Search/indexing, pagination, rate limits, audit logs, backups, monitoring, and privacy/deletion workflows
Content moderation, copyright reporting, terms, privacy policy, and age-appropriate safety controls
Integration approach
Keep UI components independent from persistence. Replace the loadDB / saveDB localStorage functions in app.js with a repository layer that calls authenticated API endpoints. Do not put private service keys in browser JavaScript. The backend should calculate ranks and XP grants rather than trusting client-supplied values.
CloudPages connection
No CloudPages project URL, API documentation, access token, or connector was supplied, and no CloudPages-specific connector was available in the current app connections. Therefore no live connection has been made. Once the actual provider/product URL and API details are known, adapt the repository layer to that backend.
