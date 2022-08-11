## AuthentiCity-NYC Project: Dev Repo
- Core Assignment Target = Jekyll Event Template: "Calendars Have Many Events."
  - [Diagram](https://tinyurl.com/AuthentiCityNYC-v1)
  - Context: We run [multiple FB groups](https://linktr.ee/authenticitynyc) where venues and performers promote local jazz events in NYC.
  - Current Process:
    - Gather venue calendars in local group zipcodes.
    - Gather artist calendars in local group zipcodes.
    - Scrape calendar or request gCal events streams from venue owners and artists to AuthentiCityNYC@gmail.com
    - Target recurring events, as they are easiest to promote over time.
    - Create fb event in local group => includes many features worth listing.
    - Share that fb group event link out => create friendly event post url alias.
    - Share that fb group event link URL alias out to MANY places => "free event post boosts"
    - Track impressions and conversions.  Use this info to inform montly promo campaigns.
---
There is no formal monthly campaign cycle right now.  With this site we will work towards a monthly promo campaign cycle.
Evolving a template from proposed to final is an iterative process.
The specs for v1 include [ics file format]() + fb group events + gCal ics stream reads.
Version 1 has some goals for ics+ format.
Version 2 has other goals for ics+ format.

- We will both aggregate and syndicate event data and content:
  - aggregate: from gCal
  - syndicate: to FaceBook Group Events
---
### Project Reqs TOC
- AuthentiCity-NYC [Version 1](#version-1)
- AuthentiCity-NYC [Version 2](#version-2)
- [Static Web Site Project Setups](#static-web-site-project-setups)
---
#### Version 1
  - [V1 Site Map](#v1-site-map)
  - [V1 Information Achitecture](#v1-information-architecture)
  - Support [ICS File Format Spec](https://docs.fileformat.com/email/ics/)
  - Support latest version of [ICS File Format Spec](https://icalendar.org/)
  - Support [FB Event Posts](https://www.facebook.com/events/3310363792539939) => Note that we can export an ics file from a FB event.
  - ![curl-or-selenium](https://user-images.githubusercontent.com/34130568/183911688-cbe75714-52f5-49eb-9072-2db3b55a25a6.png)
    - [Compressed Sample ICS File](https://github.com/jeremy-donson/authenticity-nyc-dev/files/9300497/e757019095504419.ics.zip)
    - That ics file was exported from this [fb event post](https://www.facebook.com/events/757019095504419/).
    - Focus on group events:  https://developers.facebook.com/docs/graph-api/reference/event/
  - Support [Calendar Sharing API](https://developers.google.com/calendar/api) => Who-Why-When-What-Where-How
  - Support [EventBrite API](https://www.eventbrite.com/platform/docs/api-basics)
  - [Calendar Service Event Aggregation Support Testing](https://talk.jekyllrb.com/t/how-to-fetch-an-ics-icalendar-response-and-show-it-in-jekyll/5723)
  - Automation tools: https://github.com/topics/facebook-event

- FB Testing:
  - GET ics file from FB api => ics+
  - POST ics+ to FB as a group event. => methods... curl, selenium, ??
  - Consider singleton and batch options.
  - Target other FB event api data points to scrape, like: geo, venue, band, event post images

- gCal Testing:
  - GET ics file from gCal api => ics+. Two test gmail accounts will support this.
  - Identify any missing data points.
  - Identify any missing data values.
  - Consider singleton and batch options.

- Other apis to eval:
  - meetup
  - eventbrite
  - github api has a nice i18n setup for jekyll doc => https://docs.github.com/en/rest

- Those docs are all translated into:
  - 简体中文
  - 日本語
  - Español
  - Português do Brasil

#### Site Map
- We plan to use this [jekyll theme](https://www.fourkitchens.com/blog/article/jekyll-event-schedule/).
- HOME PAGE MAIN NAVS
  - Return2Home
  - About Pages: [FB Groups](https://linktr.ee/authenticitynyc) + Jazz Venues + Musical Artists + Community Pillars + Sponsors + Alliances
  - Site Map Page Using [Jekyll Site Map Plug-In](https://github.com/jekyll/jekyll-sitemap)
  - Calendars => Calendars Landing Page => Calendar of Events => Event Detail Page
  - Event Locations Page By Date

#### Information Architecture
  - Calendars have many events.
  - Event landing pages show many related events.
  - We will need to query FB API for extended event post data and 
  - Local events count.  Events by zipcodes.
  - ICS format syncs => Pull from FB Event Post / Push to FB Event Post => singleton + batch
  - Other API's:  gcal + eventbrite + meetup + ??
  - API GET calls are easy.  POST calls are not!!  Curl or [Selenium](https://github.com/ethanXWL/Python-Selenium-Facebook-group-auto-poster/blob/master/README.md)?

---
### Project Candidate Requirements
- In General
  - Candidate must have strong written and spoken english. => Accents are NO PROBLEM!!
  - Candidate must have github id + ssh commit proof. => We can help you get setup on github if needed.
  - Use zoom and signal for secure communication where we can reach clarity the fastest.
  - Hours of regular availability for work and for meetings are to be clarified, including timezone considerations.

- Project-Specific Skills
  - Main tasks require jekyll templates from project specs and completed html.
  - Knowledge of Facebook Graph API Queries.

- To Get Started:
  - Local system machine + OS info + IP.
  - Connect via email.
  - Review github project specs (README.md).
  - Ask for simplest first small assignment.  Determine exact deliverables prior to order being created.
---
#### Version 2
  - [Site Map](#v2-site-map)
  - [Info Achitecture](#v2-info-architecture)

- https://mincong.io/en/jekyll-i18n/
- https://www.klaasnotfound.com/2017/02/16/proper-multilingual-site-with-github-pages-and-jekyll/

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
  - Remember to test URLs for proper seo + [object graph tags](https://ogp.me/#types).  [Jekyll og info](https://gist.github.com/davidensinger/5431869).
  - Consider [jekyll i18n tools](https://polyglot.untra.io/).
---


#### References
- [Docs: Github Pages Using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)
- [Docs: Jekyll](https://jekyllrb.com/docs/)
- [Jekyll GHub Pages Dev Info](https://github.com/carpentries-incubator/jekyll-pages-novice)
