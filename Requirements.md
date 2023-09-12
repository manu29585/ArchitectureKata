## Functional requirements

* User should be able to add an existing trip information manually
* User should be able to modify an existing trip information manually
* User should be able to view an existing trip information manually
* User should be able to delete an existing trip information manually
* User should be able to add individual hotel to a trip
* User should be able to add individual car rental to a trip
* User should be able to add individual air ticket to a trip
* User should be able to get latest updates on the schedule for the associated booking
* User should be able to share the trip details to targeted user.
* User should be able to share the trip details on social media.
* User should be able to view the trip status (Not started, Ongoing, Completed and dashboard)
* User should have an option to automatically archive the trip information once it completes
* User should be able to share the trip details in associated social media platform
* User should be able to create a report from all the trip by selecting a time period
* User should be able to choose the set of available metrics that can be used for generating the report
* User should be able to automatically add trip information from emails without additional user intervention
* User should get car rental information (car location, registration number, driver details) as soon as the flight lands?
* To be clarified: User should be able to filter and whitelist emails from specific travel agency
* To be clarified: User gets notifications on whitelisted emails and has an option to add it to the trip
* To be clarified: Various purpose?

* To be clarified: Summary reports with wide range of metrics? What all needs to be considered?
* Dashboard should be language agnostic. Internalization should be supported?

* As a user, I want to be able to raise problems/issues and get issue resolution updates

## Non-Functional requirements

* When the air travel gets delayed the dashboard shall update within 5 mins
* Should be able to automatically update app without additional user intervention
* Should be able to handle sudden spike in peak days ( friday)
* Application should be available all the time ( availability)
* Application should have active users backup in time of downtime ( availability)
* Auditing functionality to track the activity of user(delete /modify)
* Load Handling -should be able to handle 2million concurrent request and response with out significant delay
* Horizontal scaling
* Should have rich UI for the dashboard/summary report(Usability)
* Travel reservation notification/updates should be quick (Performance)
* Is it going to have any influence on underlying mobile/web platform Ex: Android/ios/windows or support different web browser (Compatibility & Portable)?
* Should be able to have access to mails to filter out travel reservation information(Security)
