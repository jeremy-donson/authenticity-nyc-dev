## AuthentiCity-NYC Project: Dev Repo
- Core Assignment Target = Jekyll Event Template: "Calendars Have Many Events."
  - Context: We run [multiple FB groups](https://linktr.ee/authenticitynyc) where venues and performers promote local jazz events in NYC.
---
### Project Reqs TOC
- [Static Web Site Project Setups](#static-web-site-project-setups)
- AuthentiCity-NYC [Version 1](#version-1)
- AuthentiCity-NYC [Version 2](#version-2)
---
#### Static Web Site Project Setups
  - Clarify version 1 static site project specs: AuthentiCity-NYC
  - Configure and document code pipeline through approvals in qa environment.
  - Smooth the workflow of finalizing and testing template specs.
  - Configure and document subdomain hosting for qa and prod environments.
  - Verify best practices for [jekyll + ghub pages](https://github.com/carpentries-incubator/jekyll-pages-novice).
  - Migrate to github organization account: urbanspectra-nyc
  - Look at [github actions](https://socsieng.github.io/blogging/2020/09/07/using-github-actions-over-github-pages.html) to support a more flexible build and deploy tool set.
  - Look at [using gitpod with jekyll](https://talk.jekyllrb.com/t/new-video-develop-jekyll-or-github-pages-using-docker-containers/7199) for realtime team dev collaboration.
  - Review entire process for Static Site Project Setups towards automation using terraform, vagrant and docker.

#### Version 1
  - [Site Map](#site-map)
  - [Info Achitecture](#info-architecture)
  - [Jekyll Site Map Plug-In](https://github.com/jekyll/jekyll-sitemap)
  - Support [ICS File Format Spec](https://docs.fileformat.com/email/ics/)
  - Support [FB Event Posts](https://www.facebook.com/events/3310363792539939) => Note that we can export an ics file from a FB event.
  - Support [Calendar Sharing API](https://developers.google.com/calendar/api)
  - Support [EventBrite API](https://www.eventbrite.com/platform/docs/api-basics)
  - [Calendar Service Event Aggregation Support Testing](https://talk.jekyllrb.com/t/how-to-fetch-an-ics-icalendar-response-and-show-it-in-jekyll/5723)

#### Site Map
- NOTE: We plan to use this [jekyll theme.](https://www.fourkitchens.com/blog/article/jekyll-event-schedule/)
- HOME PAGE
  - About Pages
  - Site Map Page
  - Event Locations Page
  - 


- Create repos for code pipeline => [ dev => qa => prod ]
- Consider domains and launch hosting options.
- Push me to organize the repos and issues.
- Separate v1 from v2 requirements.

#### Version 2
  - [Site Map](#site-map)
  - [Info Achitecture](#info-architecture)
