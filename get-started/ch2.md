## Chapter 2: Surveying Freshworks Apps

A lot of us are usually exposed to software those are B2C products. For example, ordering food online, booking a cab online and also shopping online. We interact with android apps and web applications. So we know app needs to have a catalogue, menu bar, shopping cart, login, register and so on.

But rarely we are involved in B2B products. Infact there might be some of them you might be using without even realizing. Slack and Jira are good examples. They help teams to be more productive. It is worth knowing that a any business would have different units belonging to sales, marketing, HR, support, IT and engineering. Freshworks ships SaaS software for those units and enable them offer better customer experience, IT service and cultivate customer relationships.

In this chapter, let's discuss to get a perspective of what kind of problems teams like those face day to day and as developers how we do our bit to can solve them. Freshworks by it's nature of offering SaaS applications, it is never one product fits every business requirement.

### Customer Experience

1. Freshdesk displays tickets in a list. So teams prefer them to be in Kanban style.See how [Kanban Board](https://www.freshworks.com/apps/freshdesk/kanban_board) app can help.
2. Customer facing teams talk to customers who have different native languages. There could [be an app that help agent translate](https://www.freshworks.com/apps/freshdesk/translate_buddy) the text.
3. Some teams use Hubspot CRM to manage contacts. An [app](https://www.freshworks.com/apps/freshdesk/hubspot_crm) can get the contact details from Hubspot and render them inside Freshdesk to help the Freshdesk user with context.
4. Writing support articles is a lot helpful to customers to refer to and solve the problem. But which of top support articles? Which articles should I be writing next to help customer? An app like [Google Analytics](https://www.freshworks.com/apps/freshdesk/google_analytics/) can help.
5. If there is poor internet connection when website visitor is chatting with the agent and chat disconnects; isn't it a poor experience? An [app](https://www.freshworks.com/apps/freshchat/airecomms_-_twilio_sms) to send a good old SMS is gold.
6. There could be instance if that specific customer facing team has unique problem. They might want to sync some information with their inhouse tool. There's no app available. You can build one!

### IT service

1. A lot of businesses use Microsoft Office 365. How about an [app](https://www.freshworks.com/apps/freshservice/office365-freshservice) to help IT team manage details of tasks, changes and meetings?
2. Some times emails exchange happens for months and there could be a long email thread. There could some attachments those go missing. How about an [app](https://www.freshworks.com/apps/freshservice/attachments_viewer) to avoid that?
3. Maybe IT service team has decided to ship couple of items as employees go work from home. Let's help IT team [with an app](https://www.freshworks.com/apps/freshservice/it_resource_management) to be able to choose criticle products from service catalog and map them under WFH kit.
4. Like wise, IT teams may have very unique problems pertaining to supporting employees, if there not one relavant in on Marketplace, developer can build one herself.

### Customer Relationship Management

1. There could be sales teams who might have been using Docusign. An [app](https://www.freshworks.com/apps/freshworks_crm/docusign_fsales) could help them easily send documents to contacts and have them signed.
2. When replying to Leads within CRM, there should be an app that can pull additional details from Ticketing tool that sales team already uses.
3. There can be a sync that always happens every 24 hours to sync data from CRM with an internal system. An app can of help.
4. Every integration that can happen with Marketing and Sales software like Mailchip. Google Analytics, Quick Books, Trello and Asana are great examples.

As a B2B app developer on Freshworks developer platform above are the usecases that teams belonging to any organisation would need help with. Yet, so far, we've only discussed the parts those don't go into implementation details.

However all of these usecases are not always require app platform to have them solved.

- Apps those use App SDK and let our platform handle Infrastrucure and provide platform for app's run time. These types of apps are Freshworks Apps.
  - These apps if intended to publish on marketplace, they are referred to Marketplace Apps.
  - If apps are built to be used specifically for a customer/business/team depending their unique requirement; these apps are referred to as **Custom Apps.**
- Some apps may consume only REST APIs. Developer by preference would host server and web app themselves and take API key from the user. These apps are referred **external apps** at Freshworks.

Both of those apps can be published via App management portal. Visit types of apps section in any App SDK documentation.
