Fri, Feb 23﻿ It looks like there is already a modal option with Ivory Search!

Mon, Feb 26﻿ Testing to see if I can change the search results template through Theme Builder before actually making a new search results template | succeeded in having a simple results page that takes the current search query and returns somewhat relevant posts | still need to improve the search results appearance as well as the actual search results (with Ivory Search Plugin)

Thu, Mar 28﻿ Your goal is to make the Avantier search bar as pretty and as intuitive as the Edmund Optics search bar!

Mon, Apr 1﻿ I confirmed that the second search icon on the main page is related to Ivory Search after temporarily deactivating the Ivory Search plugin | the second search icon is INSIDE the menu! | Ivory Search -> Menu Search (I can display search form on Primary Menu location) | I can adjust the CSS to make it look better | I need to find a way to remove the search bar from "top-menu"

Tue, Apr 2﻿ Tweaked the top menu to make the search icon in line with the rest of the menu

Improve the appearance of the search results page ﻿Thu, Apr 4 - Sat, Apr 6

Diagnose the issue with the search forms (appearance on main page, appearance of search results, quality of search results, intuitiveness of search bar) ﻿Tue, Apr 2 - Wed, Apr 3

Fri, Apr 26﻿ Finished up my consulting presentation slidedeck and set up the opportunity to actually present this to the team

Tue, May 14﻿ Restarted the actual implementation process for the search bar feature, starting with improving the actual search results

Thu, Jun 6﻿ Decided to cancel my idea of putting the search bar above the navigation menu, and decided to continue with the idea of the modal search bar instead

Present your improvements ﻿Wed, Jun 12

Mon, Jun 17﻿ Setup the UI for the filtering functionality using the HTML block, and moved on to tweak the JS code and php code

Tue, Jun 18﻿ Ran into a roadblock regarding the AJAX request as a result of clicking the radio buttons.

Deal with the issues and concerns brought up by the team's feedback ﻿Mon, Jun 24 - Wed, Jun 26

1) Make the modal search bar look bigger

2) Do search results only show 10 items at a time? Can there be a second or third page to display more results?

3) simplifying the actual result of each item (removing excess data)

(June 2024) Past documentation

Process: filter UI elements -> hidden inputs -> JS updates hidden inputs and triggers search -> PHP code in child theme modifies the search query to include the filter values

Troubleshooting - radio buttons aren't working properly (category won't stay after AJAX reload)

There is a discrepancy between the UI and the html "checked" values on the radio buttons

Elementor might be re-rendering the search form during the AJAX update, causing the radio button states to be reset

Thu, Jul 11﻿ After conducting a bunch of incremental tests during development, I managed to take care of several aspects of the search bar filtering functionality: HTML buttons, hidden value input, radio button event triggering, and the changing of the hidden input value in the search form | also figured out getting the correct AJAX request and response after clicking the radio buttons | also got the correct updating of the HTML (search-results-container) element | what's next is the PHP filtering

Tentative action steps
Project setup and requirements

Choose a CMP (content management platform)

Confirm GTM (Google Tag Manager)

Define requirements:

Consent types (just for cookies)

Banner design (small enough that it doesn’t bother people)

Consent language (no preference)

Geographic scope (no preference)

Setup your tests (on testing environment - AVT experimental branch)

Consent state

Banner interaction

Tag firing

Tools to use: GTM preview mode, browser developer tools, GA DebugView

CMP integration and GTM configuration

Integrate CMP

Create GTM tags (CMP tag and Google Tags)

Create GTM triggers (consent initialization and consent update)

Custom JS and consent logic

Set default consent state

Handle consent updates

Create GTM variables to store consent states and any other data needed for your consent logic

Testing and refinement

Use GTM's preview mode to test your implementation

Deployment and monitoring

Monitor on GTM, Google Analytics, and CMP

10/21/24

Tested out installing the CookieBot CMP plugin on the AVT experimental branch

10/22/24

I set up a free trial account for CookieBot (https://admin.cookiebot.com/domain-groups/88629886-c442-428a-a23d-17cbd54f9bcb/domains/fd4cb0f3-140e-4948-8658-53645eeb5570)

It took me a while to figure out why the banner wasn’t showing up on the page, but then I simply added the script directly to the top of ‘header.php’ and it worked!

I need to set up using Google Tag Manager so that I don’t have to stick to this temporary solution | also so that it makes sure that tags fire only after the user has given consent (especially with more advanced consent settings)

“Built-in Consent Checks: Some Google tags (like Google Analytics and Google Ads) have built-in consent checks. This means they automatically adjust their behavior based on the consent status provided by Cookiebot. You don't need to add extra triggers for these tags.”

11/5/24 -

We purchased the Premium Medium subscription and I connected the plugin with our CookieBot account

For some reason, though, the banner isn’t showing up on the AVT website. I’ll need to deal with that later.

11/6/24 -

Somehow now the banner works but only on incognito mode
