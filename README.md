InkSpark — Local-first build
This is a fresh rebuild based on the full InkSpark requirements, not a patch to the earlier prototype ZIPs.
Run
Extract the ZIP and open index.html in a modern browser. No package installation is needed for this local-first version.
Included
Responsive mobile/desktop interface: Home, Discover/Search, Library, Leaderboards, Author Studio, Profile, Settings, and reading view.
First-run local profile setup: username, password verification hash (PBKDF2), optional profile picture; profile editing includes display name, bio, banner themes, and frame.
Story create/edit and full chapter authoring. A story cannot be saved until at least one chapter contains text. No story or chapter samples are seeded.
Reading navigation, local progress, chapter completion, library, local XP/levels.
Reader font, size, line spacing, themes, browser speech synthesis (where supported).
Export/import JSON backups.
Honest empty states for public followers, rankings, reads, reactions, and author analytics.
Important limits
This is a local-first app, not a cloud backend. Profile/story/progress data and a salted PBKDF2 password verifier are stored in this browser's localStorage; the plain password is not stored. This is only a local convenience and is not a substitute for secure server authentication. It cannot sign you in on another device because that device has no copy of the local profile/verifier. Per your plan, the backend will later add secure username/password authentication, cross-device sync, database storage, media uploads, public community, comments/reactions, moderation, notifications, server-authoritative XP and leaderboards.
Browser data can be cleared, and large stories/images can exceed localStorage limits. Use Settings → Export local data for backups. Do not rely on this as the only copy of important writing.
No fake content policy
There are zero seeded stories, fake readers, fake reads, fake reactions, fake follower counts, fake analytics, or invented rankings. Only user-entered story text is displayed as content. Publish only original or properly licensed material.
