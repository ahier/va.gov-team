# Intiative Briefing: New VA.gov Mobile Header

## Outcome Summary
Since the launch of VA.gov in late 2018, the site has featured one responsive Global header element that was **not optimized for Mobile view.**  
As a result, for our growing base of Mobile users, issues with the current header include:

- Consumes too much space, pushing down the most important element on the page (based on usage): the top tasks links (Proven during Veteran Research Study)
- Some of the exposed navigational elements cause user confusion -- e.g. the Crisis Line logo was mistaken for a hamburger menu on mobile per user research
- Too many chevrons in the top right corner with all acting differently, causing confusion
- Top spacing and inconsistent search engagement. 

## The Problem to be Solved

* Problem Defined: How might we make the Mobile version of VA.gov easier to scan and use, while preserving important links in an intuitive way?

* Evidence to support Prolem: Mobile usage is up, however site navigation via mobile is low to include mobile search, during a recent wayfinding research study it was idenfied that certain pain points existed on Mobile that could be enhanced to improve the UX.  A full comparison of Desktop Vs. Mobile is vaualble in determining common tasks across each device, along with what top tasks lend themselves more to desktop (e.g. form completion) and those on mobile (e.g. navigation). 

* Why do you think the problem is occurring? Other reasons why this might be occurring?
     * This is occuring likely due to the context rich pages in the benefit hubs that are likely creating "content roadblocks" for Veterans to complete intented tasks. In addition to the large left hand navigational menu (mega menu) as it was proven that the smaller navigational menu is easier to navigate and provides a quicker path for users to interact with and follow.  
     * [Baseline analytics](https://github.com/department-of-veterans-affairs/va.gov-team/issues/28225) 
     * Veterans were asked in a recent research wayfinding session what they didn't like about VA.gov, almost half of the participants said that it was difficult to find what you need, especially when it isn't in the "top 4" boxes. "A lot of things I can't find on mobile".  
      
 
* How does this initiative help further OCTO-DE's mission and goals?
     * VA North Star: Increase the usage and throughput of VA services 
     * VA North Star: Increase the quality and reliability of VA services 

<!--
## Desired User Outcomes
- *Why would a user want to use this?*
- *With this problem solved, what should users be able to do/achieve that they couldn't before?*

## Undesired User Outcomes
## Desired Business Outcomes

- *Why would your business want this to exist?*
- *With this problem solved, what should your business be able to do/achieve that they couldn't before?*

## Undesired Business Outcomes
-->

---
## Measuring Success

### Key Performance Indicators (KPIs)

- **Findability:** Increase top task link clicks by 10% that lend to mobile usage (See Bet for details) (Currently 2.3% of all unique clicks from top tasks) with an overal top task stretch goal of 15% increase over a six month usage benchmark. 
    - BET: Elevating VA.gov Mobile header through cleaner interface will decrease confusion and allow for a greater view and usage of top tasks links on mobile. Some tasks present more of a mobile friendly experience (i.e. Menu, Sign-in, search, find a VA location) and others more to Desktop experience (I.e. form completion, direct deposit, dependent change, footer elements). We anticipate that by increasing visiability on "mobile" freindly tasks could result in an increase in both usage and confidence for mobile users. 
- **Service Completion:** Increase mobile sign-ins by 10% (Currently 4.3% of all sign-ins are mobile) with an overal top task stretch goal of 15% increase over a six month usage benchmark.
    - BET: Improving UX via bringing the sign-in element to a more visible location for mobile users functionality and findability should increase sign-ins on mobile making a more efficient funnel to Tier 1 benefit actions for mobile users.
- **Ease of use:** Increase mobile usage by 2.5% (Currently sitting at 1.7% of total usage) 
    - Eliminating navigational confusion through streamlined design elements and exposing critical items such as sign-in and top tasks links users will be more confident in using mobile/tablet to learn, access and apply for benefits. 
- **Trust/Satisfaction:** Achieve a Medallia score of 2.0 to 2.5 satisfaction as a messure of success for mobile. 
    - BET: Currently CSAT is not being measured on the homepage, however we are working with customer contact team to impliment user satisfaction rating element on the homepage for tracking: Improved UI will result in increased CSAT score as a measure of increased satisfaction and truth through use of new mobile interface. 
 
---

## Discovery
### Assumptions/Risks

- **Value Risks** (will people use it): 
  - There is measurable value to Veterans through an optimized mobile experience.  With an enhacnced VA.gov mobile header user experience could increase usage of Top Task links on the Home Page without significantly impacting discoverability/usage of Search from that navigational component.  Essentially changing design aspects that have been proven through user research to be confusion and low value user experiences would give mobile users a shorter path to the benefits they deserve.   
  - The biggest technical risk is in breaking functionality, especially anything tied to the redux state when we break out the components in the [SearchHelpSignIn component](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/platform/site-wide/user-nav/components/SearchHelpSignIn.jsx), but we can mitigate this risk with E2E testing
- **Usability Risks** (can people figure out how to use it):
  -  A snapshot of VA.gov click-through analytics and user research conducted in May 2021 indicates there is relatively modest engagement of the navigational elements in the global header by mobile users, with the exception of the VA Benefits and Health Care menu item and to a lesser extent Search.
  -  Scoping mobile navigational paths to be "three-click rule" compliant could help user find itended supporting content that would lead to an informed benefit action providing a clear conversion paths from the benefit hubs to the benefit action spoke. 
  -  Some of the exposed navigational elements cause user confusion -- e.g. the Crisis Line logo was mistaken for a hamburger menu on mobile per user research
  -  Too many chevrons in the top right corner with all acting differently, user causing confusion and degrading user experience.
- **[Technical] Feasibility Risks** (can we build it with available tech/data):
  - This page will be easy to refactor, All of suggested design changes can be done by removing/updating assets and elements with minimal risk.  [Refer to Technical analysis for additional details](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/public-websites/home-page/new-mobile-header/Initiative%20Briefing.md#technical-analysis)  
- **Viability Risks/Constraints** (will there be a positive organizational impact):
  - This optimization will apply some much needed streamlining for navigational strategies along with user flow and conversion paths for mobile users that are currently struggling to complete critical tasks via mobile platform. Risk/constraint to consideer will be ensuring no disruptions to the current veteran expereince in VA.gov home page via mobile while we optimize (servicability needs to remain stead and active).  A secondary contraint will be to ensure user flow and mobile enhancmenets are fully tested with Veterans through a slow production release to 5% of users and test and measure effectiveness against defined KPIs to ensure success criteria is being achieved and intended user experience is achieved before increasing phased roll-out.   

### Solution Scope
**In Scope**
- Mobile enhancements only (Not affecting Desktop experience)
- Auth and Unauth elements as outlined in Deisgn specs
- Defined roll out plan to 5% prod, test & measure before increasing roll out percentage/scope 

**Not In Scope**
- No Desktop enhancements (Mobile only)
--- 

## Launch Planning
### Collaboration Cycle
> 💡 *Use for any Collab Cycle tracking, questions.*

- Kickoff ticket

### Go-to-market 

|Date| Decision |
|--|--|
| TBD |  Dave Conlon to review initiatives briefing and validate |
| TBD |  Determine KPIs and Success Measures and validate |
| TBD |  Complete VSP Collaboration Cycle events  |
| TBD |  Complete Release Plan per action items |

### Timeline 
> *Describe any major milestones for this initiative including organizational, legislative, etc. constraints.*

* [Link to Release Plan for this Initiative](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/platform/product-management/release-plan-template.md)

#### Initiative Launch Dates
- *Target Launch Date*
  - tbd
- *Actual Launch Date* 
  - tbd

---
   
## Screenshots
- [Sketch Designs](https://www.sketch.com/s/63193c20-04fc-4d4f-8b54-abf698c48636/a/Vr8Zzrw) 

---

#### Communications
Primary communication for this initiative will be via #VSA-Public-Websites slack channel. 

<details>

- Team Name: Public Websites 
- GitHub Label(s): VSA-Public-Websites 
- Slack channel: #vsa-public-wesbites
- Product POCs: David Conlon (PO), Brian Lloyd (PM)

</details>

#### Technical Analysis 
- Review product outline and provide a technical analysis on implementation
  - Many of the changes in the product outline are cosmetic including:
    - Updating the "Official..." banner to consume less space
    - Removing the "crisis line" logo
    - Use a simplified version of the VA logo
    - Add th hamburger icon to the Menu button
    - Remove the Home page item in the menu"
    - "Contact us" moves to the bottom spot on the expanded menu
    - Wrap "Close menu" with the expanded menu
    - Authenticated user drop down menu moves to the top
  - All of these changes can be done by removing/updating assets and elements with minimal risk
  - Some changes will involve relocating existing components 
    - Sign in stays persistent in the header
    - Search is now usable in the expanded menu
    - Currently these are part of the [SearchHelpSignIn component](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/platform/site-wide/user-nav/components/SearchHelpSignIn.jsx), but would need to be broken up into individual components so we can relocate the individual UI pieces
- Provide best recommendations for optimized UX/UI
  - Earlier comments mentioned building out 2-4 components 1 for each combination of Unauth/Auth + Desktop/Mobile, but it looks as though the distinction between unauth and auth at the component level is already done for us [here](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/platform/site-wide/user-nav/components/SearchHelpSignIn.jsx#L36-L66), so we can mostly copy the [MegaMenu](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/platform/site-wide/mega-menu/components/MegaMenu.jsx) to a `MobileMegaMenu` component that can be combined with the [MobileMenuButton](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/platform/site-wide/mobile-menu-button/containers/Main.jsx)
  - We should consider moving the mobile mega menu out of `content-build` entirely and having it render by react so it can sit below the menu button within the dom, making it easier to have connect the background/border of the menu and button
- Include risks and ideas to mitigate risks for implementation
  - The biggest risk is in breaking functionality, especially anything tied to the redux state when we break out the components in the [SearchHelpSignIn component](https://github.com/department-of-veterans-affairs/vets-website/blob/master/src/platform/site-wide/user-nav/components/SearchHelpSignIn.jsx), but we can mitigate this risk with E2E testing
- Add questions for PO/PM/Lead Designer for follow up and determination during future planning and grooming sessions
  - None at this time

#### Stakeholders
Design - Ryan T.
PO - Dave Conlon 

<details>
  
- Office/Department: N/A
- Contact(s): N/A
 
</details>

---
<sup>1</sup> [VA.gov Analytics - KPI Framework](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/platform/analytics/Analytics%20Playbook/va-gov-platform-analytics-kpi-framework.pdf)\
<sup>2</sup> [SVPG: The Four Big Risks](https://svpg.com/four-big-risks/)
