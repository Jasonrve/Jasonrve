# Profile README notes

## Components

- `assets/profile-banner.svg` and `assets/profile-banner-mobile.svg`: local, responsive banners with a slow-moving network graphic and reduced-motion support.
- [capsule-render](https://github.com/kyechan99/capsule-render): animated wave footer.
- [readme-typing-svg](https://github.com/DenverCoder1/readme-typing-svg): rotating typing tagline.
- [Shields.io](https://github.com/badges/shields): hero badges, tech labels, live star counts.
- [Skill Icons](https://github.com/tandpfun/skill-icons): supported stack icons are stored locally in `assets/engineering-stack-{light,dark}.svg` and switched via `<picture>`. Helm, Argo CD, and Vault use labeled Shields badges because Skill Icons omits those IDs.
- [GitHub Readme Streak Stats](https://github.com/DenverCoder1/github-readme-streak-stats): contribution streak card, light/dark via `<picture>`.
- [komarev profile views](https://github.com/antonkomarev/github-profile-views-counter): view counter.

## Dependencies

The header and main skill icon grid are local. The other widgets use third-party endpoints; if one is down the text and links still work. No Actions, no secrets.
`github-readme-activity-graph.vercel.app` was removed: it returned HTTP 402 as of 2026-09-25.

## Featured repositories

VaultLens and Uptime Kuma Operator are featured; "More from my work" links Bifrost Budget using its GitHub description.
Repos without a GitHub description (rancher-mcp, rancher-devops-operator, TerraSec) are left out. Add a description on GitHub, then list them.

## Validation

- All image URLs returned HTTP 200 on 2026-09-25.
- No fabricated metrics: star counts are live Shields badges.
- Local Playwright preview checked at 390px and 1280px on 2026-10-22: images loaded, no horizontal overflow at phone width, and the banner animation stops under reduced-motion preference.
- Engineering stack checked in Playwright at 390px dark and desktop light on 2026-10-22: both local icon grids loaded, the Helm/Argo CD/Vault badges appeared, and the section had no horizontal overflow.
