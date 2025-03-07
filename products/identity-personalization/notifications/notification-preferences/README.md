# Notification settings: Product outline

Last Updated September 1, 2022

## Table of Contents
- [POCs](#pocs)
- [Overview](#overview)
- [User Outcomes](#user-outcomes)
- [Business Outcomes](#business-outcomes)
- [Measuring Success](#measuring-success)
- [Projects](#projects)
- [How to access and test](#how-to-access-and-test)
- [Backend](#backend)
- [Frontend](#frontend)
- [Design and UX](#design-and-ux)



### POCs

- Slack channel: [#accountexp-authexp](https://dsva.slack.com/channels/accountexp-authexp) [#va-profile](https://dsva.slack.com/channels/va-profile)
 
 ### Roles

[Please refere to the profile product outline for the current VA.gov profile team](https://github.com/department-of-veterans-affairs/va.gov-team/tree/master/products/identity-personalization/profile#roles).

Additionally, we work in partnership with VANotify and VA Profile on this work. Additional partners include:

|Name|Role|Email|
|----|----|-----|
|Beverly Nelson| OCTO lead for VANotify| beverly.nelson@va.gov |
|Melanie Jones | VANotify PM | melanie.jones@oddball.io |
|Mike Richard | VA Profile PM | Michael.Richard2@va.gov |


## Overview

The VA is ramping up their digital communications efforts, specifically through text and email. As a result, veterans need to be able to opt in or out of communications and customize through which channels they prefer to be contacted. To meet these organizational and user needs, the VA.gov profile supports notification settings, which are powered by the [VA Profile backend](https://depo-platform-documentation.scrollhelp.site/developer-docs/external-integrations). This section is also managed in close partnership with [VANotify](https://depo-platform-documentation.scrollhelp.site/developer-docs/VANotify.1885634900.html), which manages all notifications.

More information on the VANotify platform can be found [here](https://github.com/department-of-veterans-affairs/va.gov-team/tree/master/products/va-notify).

### What to Know


This section of profile allows users to:

- Manage text notification preferences.  
- Add or update the mobile phone number where notifications will be sent.

The following data will come through VA Profile's API

- Notification types (appointment reminder, claim update, etc)
- Channels (text/email), groups (e.g. health care)
- User settings (null, true, false) will come through


Currently we support the following notifications:

|Notification Group|Item|
|--------|-----------|
|Health Care|- Appointment Reminders <br />- Prescription Shipping|
|Health Care| - Applications, claims, decision reviews, and appeals|
| Financial | - Payments (future)|

     
## User Outcomes

### Desired user outcomes

- As a veteran, I want to be able to see what types of communications I am eligible to receive.
- As a veteran, I want to be able to select where and how I receive those communication (eg. receive emails for claim updates; receive texts for appointment reminders).
- As a veteran, I only want to have to keep this information updated in one place.


## Business Outcomes

### Desired business outcomes

- Allow veterans to set and manage communication preferences from their VA.gov profile.
- Allow any updates veterans make to their permissions to be saved/accessed across the VA (through VA Profile backend).
- Set up an infrastructure for this functionality that is sustainable and allows us to scale easily over time.


## Measuring success

We are not currently measuring any OKRs or KPIs for notification settings.

For previous OKRs/KPIs:

- [Notification settings MVP project outline](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/notifications/notification-preferences/product/mvp-project-outline.md#measuring-success)

## Projects

|Projects|Launch date|
|--------|-----------|
|[Notification settings MVP project outline](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/notifications/notification-preferences/product/mvp-project-outline.md#measuring-success)| Nov 2021|
|[Notification Communications MVP](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/notifications/notification-preferences/product/communications-permissions-mvp-definition.md)| July 2021|

## How to Access and Test
- [Staging](https://staging.va.gov/profile/notifications)
- Testing documentation
     - [Notification settings test/use cases & users](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/staging-test-accounts-notification-preferences.md)
     - [Notification settings a11y test case documentation](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/Administrative/vagov-users/staging-test-accounts-notification-preferences-a11y.md)
- [Production](https://va.gov/profile/notifications)

## Backend

### Services

- Notification settings come from [VA Profile](https://depo-platform-documentation.scrollhelp.site/developer-docs/external-integrations).
- This section is also managed in close partnership with [VANotify](https://depo-platform-documentation.scrollhelp.site/developer-docs/VANotify.1885634900.html), which manages all notifications.

Additional details can be found [here](https://github.com/department-of-veterans-affairs/va.gov-team-sensitive/blob/master/products/identity-personalization/profile/notification_settings/backend_documentation.md)

### Error Handling

- _Coming soon!_

## Frontend

- [Frontend documentation on how the notification settings UI works](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/notifications/notification-preferences/frontend/display-notes.md)

## Design and UX
- [High level user flow with screenshots](https://www.sketch.com/s/afd69a1f-72d2-430b-9b62-285e9d3f479c/a/v8zKwxQ)
- [Notification settings sketch files](https://www.sketch.com/s/afd69a1f-72d2-430b-9b62-285e9d3f479c)
- [Use cases](https://github.com/department-of-veterans-affairs/va.gov-team/blob/master/products/identity-personalization/notifications/notification-preferences/use-cases/README.md)

