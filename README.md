# NBA-Analytics-Optimisation-Engine
A sports analytics platform for the NBA, built as our COMS3011A project at Wits. You can look up players and teams, see game predictions, and build a fantasy lineup. Every stat on the site is calculated from play-by-play data.

Links
Live app: sportsanalytics.pages.dev
Project documentation: Innovation Documentation Website
What it does

The core of the app is player and team lookup, game predictions using Elo ratings and the Four Factors model, and a fantasy lineup optimizer built on mixed-integer linear programming (MILP). You can lock players into the optimizer and ask it for alternative lineups.

Around that we added player comparison, postseason and advanced stats, custom statistics, all-time leaders, injury reports, Player Archetypes, and a Live tab. Each page has a short tutorial for first-time users.

For developers, the API comes with Swagger UI documentation, API keys with rate limits and quotas, and response caching. Paid features sit behind a Become Pro tier.

On the admin side, event corrections are logged with an audit trail, new data goes through a review step before ingestion, and dataset releases are versioned. There is a built-in bug tracker and a privacy notice with POPIA controls.

How we built it

We worked in four sprints. Sprint 1 set up the foundation: Google sign-in, data ingestion, predictions, and the optimizer. Sprint 2 added comparison tools, advanced stats, and our first user survey (11 responses). Sprint 3 covered the admin, API, and Pro features. Sprint 4 added archetypes, the Live tab, and changes based on eighteen pieces of user feedback.

Tech stack
Frontend: React, hosted on Cloudflare Pages
Backend: NestJS API, hosted on Render
Database: Supabase
Data ingestion: nba_api
API docs: Swagger UI
Source control and project management: Gitea

The full breakdown is on the Tech Stack page of the docs.

Documentation

The documentation site is built from the docs/ folder in this repository and redeploys on every push to main. It covers:

Product: feature tiers, UI overview, the Become Pro valuation model, Player Archetypes, and the roadmap
Architecture: ERD, data ingestion, API design and reference, performance, security, and architecture decision records (database, auth, hosting, caching, and play-by-play storage)
Process: sprint log, scrum meetings, Git methodology, definition of done, coding conventions, CI/CD, testing, and an AI usage ledger
Users and stakeholders: client meetings, the stakeholder log, survey results, user interviews, and the improvements we made from them

If you're marking or reviewing the project, start with the Rubric Quick Links and the Demo Guide on the docs home page.
