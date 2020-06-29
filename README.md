# Evergreen OPAC
**https://bugs.launchpad.net/evergreen/+bug/1778972**

**Change opac to opac-old and opac-new to opac in the templates folder to use.**

This is a redesign of the current OPAC in the Evergreen ILS meant to enhance the responsiveness, accessibility and readability of the OPAC.

This change utilizes **Bootstrap 4** for style and responsiveness as well as some custom style changes and updates to the html:

### RESULTS
* Facets changed to it's own settable colors in colors.tt2

* Facets 'more/less' buttons will now snap back to facets after load and scrolls instead of pushing full list to page

* Navigation set in button group

### SUMMARY
* Extra information (Not always needed) hidden and shown by button (+more) with no need for reload (bootstrap collapse)

* "Back To Results" button returns you to the specific record in the results and not to top of list

* All options for item contained into a button group

* 'Awards' extra would just have text "Loading...", this has been enlarged to "'Loading Recommendations' with a loading bar

### MY ACCOUNT
* Pay selected charges displays a dynamic amount in the button totalling the selected payments

* Added front end support for redirecting to Paypal for payment. Functionality pending back end implementation of IPNs

* Language choice added to 'Personal Information' menu

* Modified pending addresses to display INSTEAD of current address if a change is requested for that particular address

* Navbar user item counts and charges now contextual. Has 'zero_count' and 'non_zero_count' color options for when the number is zero and when it is not zero. (Not present on E-Items)

### OTHER
* Many buttons were changed to be contextual ( Green = YES, Red = NO ). The option has been added in colors.tt2 for each of the contextual buttons with comments on what they affect. They currently use Bootstrap 4 styling.

* Created more granularity for colors by adding and modifying some color classes so that one color is less blanketing and more control can be had

* Login opens in modal window instead of redirect.(Redirects to login page on failure)

* Search filters in advanced search modified to follow bootstrap .col and fall in line properly on mobile

* Alert on OPAC changed to bootstrap dismissable alert. The color of the alert is also added as a config option where the message is set in config.tt2. Uses standard bootstrap4

* Created minified versions for all tables to display properly on mobile

* Tables now highlight rows on hover and check a row's box on a row click

* Tooltips updated

### FEEDBACK UPDATES
* White space has been significantly minimized. The OPAC was also set by default to 'Show More' on the results page causing larger results to appear. This has been set back to the default

* The filter/sort options are much smaller. There are quite a few so I mused on an accordian style hide&show but the current layout should be sufficient.

* The facets have been placed back on the right hand side. When I first dealt with the OPAC, I put them under the search results as I interpereted this as a "Can't find what you are looking for? Try these!" and less of a filtering option. On mobile, they will still be below the search results as that just makes sense with the limited screen space.

* Link/Hover effects on mobile have been changed to be more consistent with the rest of the navigation with hovering indication. This was just a 'bug' in the code.

* Items Checked Out - The Call Number position has been moved as, yes, it is a large part of the search

* Selecting Items from search results- I question the necessity of this bar with my iteration as the basket will show on every page. I have fixed this to show the # selected.

* Account Preferences - Language - Another bug in the code that has been fixed and the items fall in line now

* Checkboxes - Most tables can be clicked to select the row. Account preferences shows the selected row on hover now but there is no rows to actually select. Also, on the search results page, the 'Add to basket' large button can be used to select the title. If there are any with just a checkbox as the only option I can surely look into those as it is helpful, as noted, to have a larger clicking surface for a selection.
