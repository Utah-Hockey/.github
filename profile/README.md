# Utah Hockey

Welcome to the GitHub home for University of Utah Hockey’s technology projects.

We build and maintain the systems behind the Utah Hockey website, mobile app, statistics, schedules, media, and game-day broadcast. Most of this work supports a volunteer-driven organization, so our goal is to keep the stack reliable, affordable, secure, and easy for future contributors to understand.

## How It Fits Together

```text
HockeyTech / LeagueStat -> API Plugin -> WordPress site (theme), mobile app, broadcast graphics
```

The API Plugin is the single integration point for HockeyTech data. The theme, mobile app, and broadcast tools read its normalized REST API rather than calling HockeyTech directly.

## Repositories

| Repository | What it is |
|---|---|
| [UtahHockey-Modern-Theme](https://github.com/Utah-Hockey/UtahHockey-Modern-Theme) | The live WordPress theme for the website. Presentation only; data comes from the plugins. |
| [API-Plugin](https://github.com/Utah-Hockey/API-Plugin) | WordPress plugin that normalizes HockeyTech data into a REST API and renders Game Center and player profiles. Settings live under **Custom API Settings** (API, Mobile App, and Holiday & Event Overlays tabs). |
| [Apparel-Plugin](https://github.com/Utah-Hockey/Apparel-Plugin) | WordPress plugin for the Team Store: the apparel marketing image and the featured apparel scheduler used by the homepage and mobile app. Split out of API-Plugin. |
| [mu-plugins](https://github.com/Utah-Hockey/mu-plugins) | Must-use WordPress plugins for behavior that has to load no matter which theme is active. |
| [UtahHockey-MobileApp](https://github.com/Utah-Hockey/UtahHockey-MobileApp) | Flutter app with news, tickets, schedules, standings, rosters, Game Center, video, and a historical archive. iPadOS, macOS, and watchOS versions are in progress. |
| [CaptivateScripts](https://github.com/Utah-Hockey/CaptivateScripts) | Planned Google Sheets / Captivate client for broadcast graphics, built on the API Plugin. |
| [UtahHockey-UpdateAndMigration-2026](https://github.com/Utah-Hockey/UtahHockey-UpdateAndMigration-2026) | Infrastructure, migration automation, release notes, and the cross-repository backlog for the 2026 platform update. |

Most project repositories are private to organization members.

## Project Priorities

We try to build systems that are:

- **Reliable** — stable enough for game days, announcements, and public traffic
- **Maintainable** — documented clearly so volunteers can pick up the work later
- **Cost-conscious** — designed for nonprofit and volunteer budgets
- **Accessible** — usable across devices and friendly to all site visitors
- **Secure** — respectful of user accounts, admin access, and operational data

## Current Focus

The 2026 website cutover to the new theme and AWS hosting is complete. Current work includes:

- Retiring the remaining legacy plugin and content dependencies
- Moving temporary MU plugin styling into the theme
- Finishing roster, history, and Game Center cleanup
- Building the Captivate broadcast client on the API Plugin
- Bringing the mobile app to iPad, Mac, and Apple Watch

## Contributing

Utah Hockey technology work is volunteer-supported. Contributions should be practical, documented, and respectful of the live production site.

1. Read the repository README and open issues.
2. Work from a feature branch and open a pull request against the repository’s default branch.
3. Keep changes focused and easy to review.
4. Document anything that affects deployment, data, forms, plugins, or AWS resources.
5. Never commit secrets, API keys, database dumps, or production credentials.

Merging to the default branch of the theme and plugin repositories deploys to production automatically, so test changes before you merge.

---

Built by volunteers for the Utah Hockey community.
