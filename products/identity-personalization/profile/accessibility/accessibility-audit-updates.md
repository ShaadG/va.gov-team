# Accessibility audit & updates

**Last updated: September 6, 2022**

_We should consolidate all accessibility feedback we've gotten, review it, and determine next steps. Tasks run from full-on projects (eg. moving edit from in-line to another page) to smaller tasks we can knock out as time allows._

- [Current open Profile and 508/Accessibility GitHub tickets ](https://github.com/department-of-veterans-affairs/va.gov-team/issues?q=is%3Aopen+is%3Aissue+label%3A508%2FAccessibility+label%3Aprofile)
- See [Profile screen reader walk-through](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/profile/product/screen-reader-walkthrough.md) - **May 3, 2022**

## Findings

### 508-defect-0
- ❗️ Potentially Harmful. Must be fixed immediately.

---

### 508-defect-1
- ❗️ Critical. Must be fixed before launch.

#### Connected Apps
-   Screen reader user is not aware of most content
	-   Headings can be changed to improve this page
	-   **Recommendations:**
		-   Angela suggested having an H2 that says Connected Apps with the rest of the headings (app names) as H3, so a screen reader could easily skip down to Veteran programs and services
	-   **Next steps:** TBD
-   Minor heading level change in featured content ([ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/37363))

---

### 508-defect-2
- ⚠️ Serious. Should be fixed in 1-2 sprints post-launch.

#### Sidebar nav position 
`508-defect-2`
- Currently below the H1 and creating confusion for screen reader users ([ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/40593))
- [Slack thread](https://dsva.slack.com/archives/C909ZG2BB/p1651153191682419)
-   **Next steps:**  Needs team grooming


#### Direct deposit, routing and account number information is unclear to screen reader users

-   [NEW 508-defect-2](https://github.com/department-of-veterans-affairs/va.gov-team/issues/46614) 
-    related to focus management and screen reader announcement on the Direct Deposit Information content area. After clicking the **EDIT** button to edit direct deposit information for disability compensation and pension bank information, the focus is set to the routing number field. This causes screen reader users to miss the informative content that appears above it that includes an image and descriptive text noting to users where to find their bank's routing and account numbers. 
   -   There are also instances where after clicking the **EDIT** button, and then clicking on the expandable-collapsible area for "Where can I find these numbers?", the caption that should appear following the image is missing.
---

### 508-defect-3
- ⚠️ Moderate. Should be fixed in 1-3 sprints post-launch.

#### Buttons are styled to look like links
-   In the address validation flow, we still have edit buttons that look like links in the alerts and next to the address entered by the user 
-   ([ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/43095#issuecomment-1228599039))
-   _Consideration:_ This could be a non-issue if we move to a one thing per page flow for this UX
-   **Next steps:** team grooming, likely needs design re-work
---

### 508-defect-4
- ✔️ Trivial. Consider fixing or exploring in 2-4 sprints post-launch.

#### Notification Settings: No announcement of the type of telephone number (mobile) being read aloud
-   [NEW 508-defect-4](https://github.com/department-of-veterans-affairs/va.gov-team/issues/46609) - related to missing descriptive text within the Notification Settings content area. Near the top of the content, the Veteran’s mobile number is listed, followed by a link to update their mobile phone number. The text content listed beforehand does not truly indicate what type of phone number is being read aloud by screen readers. Users may be able to guess that this is their mobile number, but the lack of specific callout text may create confusion.

#### Field "headings" / lists (i.e. Mailing address and Home address)
`508-defect-4`
-   Some changes are needed for the field names/headings
-   Concern also raised during BAI pilot session with Angela
-   **Recommendations:**
	-   It would be better if "Mailing address" were H3 instead of a list item, with paragraph text then used for the hint text
	-   Same applies to Phone numbers and other similar fields in Profile
- **_Possible contradictory item:_** Previously recommended to use unordered list and headings pattern ([ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/19618))
 	- Accessibility concluded that it would be better to use an unordered list and headings pattern for the profile
-   **Next steps:** Needs team grooming

#### Phone number screen reader improvement
- The phone number is not that accessible. The screen reader reads out the number as a regular number rather than a phone number. ([ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/44534))
- **Next steps:** Sprint planning

#### Notification settings
- The legend element should be the first child of the fieldset for notification preferences ([ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/31449))
- **Next steps:** [Ticket in icebox](https://github.com/department-of-veterans-affairs/va.gov-team/issues/37041)

#### "Are you sure?" modal, editing profile
- Wording might need to be revisited
- **Recommendations:**
	- Maybe instead of Continue and Cancel, the modal could be Are you Sure? with Yes/No buttons
- On the other hand, as is might be better for those with cognitive disabilities
- **Next steps:** Created ticket [#46788](https://github.com/department-of-veterans-affairs/va.gov-team/issues/46788) collaborate with content folks on improving this.
---

### Issues that need more work

#### Hubless spoke
- [Mural](https://app.mural.co/t/vsa8243/m/vsa8243/1653404244021/d2fdb4d36539e09705429286accaf119db765664?invited=true&sender=u28f508d646c449cc1afe4873) 
- Concerns presented by accessibility folks regarding current challenges due to the lack of a true landing page
- Initial meeting held with Josh Kim, David Kennedy, and Matt Dingee
- [Slack thread](https://design.va.gov/patterns/forms/sub-task)
- **Next steps:** Needs ticket + a11y defect level, team grooming
	-   *Shared Support - a11y defect level suggestion*: More assessment/research needed


#### Address validation 
-   Address validation is a considerably difficult flow for screen reader users
-   Concern raised during BAI pilot session with Angela
-   **Next steps:** Needs ticket + a11y defect level for prioritzation
	-   *Shared Support - a11y defect level suggestion*: `508-defect-2`
-   **Considerations:** What percentage of users end up going through this flow? Knowing this could help us prioritize.

#### Name tag
-   Currently, nametag is hiding above the first heading and there's a good chance a screen reader user wouldn't catch this (unless a beginner)
-   **Recommendations:**
	-   Angela considers this like "basic information," which could be displayed right below the H1 under an H2 heading that says “basic information” 
	-   Or for less priority, it could be at the bottom of the page
	-   In order to make it visible to the screen reader, it would need to be under a new H2 heading under the H1
	-   If we put it above H1, we might not need to display it on each page, as it could get redundant. Instead, the nametag could be included and read out on Personal information only
-   **Next steps:** Needs ticket, a11y defect level, team grooming
	-   *Shared Support - a11y defect level suggestion*: `508-defect-3`

#### TTY (Direct Deposit)
-   The help phone number is ok for the screen reader, but 711 is not. TTY is not part of the aria label and needs to be. Angela would put TTY prior to the 711 in actual link text
-   **Next steps:** _Resolved?_
	-   *Shared Support - a11y defect level suggestion*: `508-defect-2`
	-   [Related TTY ticket](https://github.com/department-of-veterans-affairs/va.gov-team/issues/46195)


#### Account Security
-   If navigating by heading, it's easy to skip all main fields
-   Headings can be changed to improve this page
-   **Recommendations:**
	-   Angela: "You can put the email address change at the top under H1 under an H2 and then another that says completed tasks (H2) - or put the email part somewhere else and then get rid of the rest"
-   **Next steps:** Needs ticket, a11y defect level, team grooming
	-   *Shared Support - a11y defect level suggestion*: `508-defect-3`

#### In-line error message when editing in profile
-   Focuses on wrong thing with error - not keeping focus on update button. (Note: this might need more looking into, I'm not sure what the specific focus needs are)
-   Also does not tell screenreader about all the errors shown, just one. This is likely a form system problem, opened a bug assuming that's the case [#46731](https://github.com/department-of-veterans-affairs/va.gov-team/issues/46731)
-   **Recommendations:**
	-   Angela suggested that the best thing to do is to have a list of errors together
-   **Next steps:** Determine where focus should go, get a11y defect level
	-   *Shared Support - a11y defect level suggestion*: `508-defect-2`
	-   *Additional suggestion*: If an error summary is available, place focus on the heading within this area. Otherwise, if an error summary is not available, place focus within the first error field. Be sure to include descriptive error messages for screen readers and other users to determine what needs to be corrected.

#### One-per-page editing
-   Consider moving from in-line editing to one-per-page editing
-   Can one-per-page editing help with any of the above concerns?
-   Some research has been done by other teams
-   **Next steps:** Create ticket to assess the above items.
	-   *Shared Support - a11y defect level suggestion*: More assessment/research needed  

## Shared Support Accessibility Audit Summary - September 2022

An additional accessibility audit was completed August 31, 2022 by the PTEMS Shared Support team. Testing of keyboard navigation, color contrast, magnification, Axe browser scan and screen reader testing with JAWS, NVDA and VoiceOver were completed and focused on the following higher traffic content areas:
-   Personal Information
-   Contact Information
-   Direct Deposit Information
-   Notification Settings

### Audit Notes

Overall, all of the accessibility issues identified aligned with the earlier screen reader findings mentioned in this document. Two additional issues were found and have been added to the appropriate defect level secvtion above.  Additional notes:

-   Color Contrast - not a defect, but more of something spotted regarding consistency with some areas having a combination of black and light gray text versus similar content where all black text is used.
-   Error handling -  [a broader discussion happened with the Forms Library team](https://github.com/department-of-veterans-affairs/va-forms-system-core/issues/557), but essentially this is regarding when error messaging is triggered as a user navigates


## Resolved items & updates

_Document resolved issues so we can learn from them_

-   When we have character maximums, the ideal, no-magic solution is to include text next to the label without a modal alert (25 characters maximum)
-   Avoid conditional reveal when possible
