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
- All project setups
  - Clarify version 1 static site project specs: AuthentiCity-NYC
  - Configure and document code pipeline through approvals in qa environment.
  - Provision dev access to github repos.  Start to use github issues and project board.
  - Smooth the workflow of finalizing and testing template specs.
  - Configure and document subdomain hosting for qa and prod environments.  Consider [Netlify hosting](https://www.netlify.com/).
  - Verify best practices for [jekyll + ghub pages](#references).
  - Migrate to github organization account: urbanspectra-nyc
  - Look at [github actions](https://socsieng.github.io/blogging/2020/09/07/using-github-actions-over-github-pages.html) to support a more flexible build and deploy tool set.
  - Look at [using gitpod with jekyll](https://talk.jekyllrb.com/t/new-video-develop-jekyll-or-github-pages-using-docker-containers/7199) for realtime team dev collaboration.
  - We will use [postman](https://www.tecmint.com/install-postman-on-linux-desktop/) and [selenium](https://medium.com/@fortheloveoftech/automating-facebook-events-with-python-and-selenium-dca4c52e2513) for testing
  - Review entire Static Site Project Setup process towards automation using terraform, vagrant and docker.
  - Remember to test URLs for proper [object graph tags](https://ogp.me/#types).  [Jekyll og info](https://gist.github.com/davidensinger/5431869).
  - Consider [jekyll i18n tools](https://polyglot.untra.io/).
---
#### Version 1
  - [Site Map](#site-map)
  - [Info Achitecture](#info-architecture)
  - [Jekyll Site Map Plug-In](https://github.com/jekyll/jekyll-sitemap)
  - Support [ICS File Format Spec](https://docs.fileformat.com/email/ics/)
  - Support [FB Event Posts](https://www.facebook.com/events/3310363792539939) => Note that we can export an ics file from a FB event.
  - Support [Calendar Sharing API](https://developers.google.com/calendar/api) => Who-Why-When-What-Where-How
  - Support [EventBrite API](https://www.eventbrite.com/platform/docs/api-basics)
  - [Calendar Service Event Aggregation Support Testing](https://talk.jekyllrb.com/t/how-to-fetch-an-ics-icalendar-response-and-show-it-in-jekyll/5723)

#### Site Map
- We plan to use this [jekyll theme](https://www.fourkitchens.com/blog/article/jekyll-event-schedule/).

- HOME PAGE NAVS
  - About Pages: [FB Groups](https://linktr.ee/authenticitynyc) + Jazz Venues + Musical Artists + Community Pillars + Sponsors + Alliances
  - Calendars => Calendars Landing Page => Calendar of Events => Event Detail Page
  - Event Locations Page By Date
  - Site Map Page
---

#### Version 2
  - [Site Map](#site-map)
  - [Info Achitecture](#info-architecture)

#### References
- [Docs: Github Pages Using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)
- [Docs: Jekyll](https://jekyllrb.com/docs/)
- [Jekyll GHub Pages Dev Info](https://github.com/carpentries-incubator/jekyll-pages-novice)
