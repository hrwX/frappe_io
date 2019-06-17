<!-- base_template: frappe_io/www/frappe/frappe_base.html --><!-- add-breadcrumbs -->
# Google Contacts Integration

Frappe provides an integration with Google Contacts in order for all users to synchronize their Contacts.


## Setup

In order to allow a synchronization with Google Contacts you need to authorize Frappe to get Contacts data from Google. Google Contacts Integration is set up in the following steps:

1. Create a new project on Google Cloud Platform and generate new OAuth 2.0 credentials.
<img class="screenshot" src="/docs/assets/img/google_contacts_project_reation.gif">
2. Add `https://{yoursite}` to Authorized JavaScript origins.
3. Add `https://{yoursite}?cmd=frappe.integrations.doctype.google_contacts.google_contacts.google_callback` as an authorized redirect URI.
<img class="screenshot" src="/docs/assets/img/google_contacts_project_oauth.gif">
4. Add your Client ID and Client Secret in the Google Settings in `Modules > Integrations > Google Settings`
5. Create a new Google Contacts, enter the Google Account Email you want to sync and then save it. Now click on `Authorize Contacts Access` to authorize Frappe to get Contacts data from Google.
6. Once Authorized, you can manually sync Google Contacts or let Frappe sync Google Contacts daily.


## Features

1. Creation of a Contacts in Frappe from Google Contacts
	- All the Contacts present in Google Contacts will be synchronised in Frappe Framework.
	- If any of the Google Contact have multiple Email Ids associated with them, new Contact will be created in Frappe for each Email Id.