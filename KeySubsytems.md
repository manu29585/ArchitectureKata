# Key Sub systems

[To go back](./README.md)

todo delete old plntuml [Subsystems-Interaction](./.media/Subsystems-Interaction.png)

![Subsystems-Interaction](./.media/RoadWarrior_SubSystems-Subsystems_And_Interactions.jpg)
* Email Service:
![Email Service](./.media/RoadWarrior_SubSystems-Email_Polling_And_Whitelisting.jpg)
  * Interfaces with different mailing services to get and scrape the user mails. Works as an aggregator for all the mail service provider.
* Travel Service Provider: 
![Travel Service Provider](./.media/RoadWarrior_SubSystems-Travel_Service_Provider.jpg)
* Interfaces with 3rd party travel providers{eg. make my trip} and air,hotel, car rental service provider. To get
  * more details on PNR.
  * updates etc
* TripOrganizer:
![Trip Organizer](./.media/RoadWarrior_SubSystems-Add-Update-Delete.jpg)
  * Key component on the dashboard using which trip details are managed (Add/Modify/delete)
  * PNR Handling
* Road Warrior DashboardManager
  * Overarching component which encapsulates different service on the UI
* DataAnalyticsManagement
  * Used for user behavior tracking
* Trip Summary Provider 
 ![Trip Summary Provider](./.media/RoadWarrior_SubSystems-Trip_Summary_Provider.jpg)
  * Provides analytical options (What are the different data mining options available for traveler) to UI
  * Generates reports
* Vendor Management :
 ![Vendor Management](./.media/RoadWarrior_SubSystems-Vendor_Management.jpg)
  * Onboard/Adds/Removes third part vendors which provide booking services such as Airlines, Cars and Hotels
* Identity Management (Authentication & Authorization)
 ![Identity Management](./.media/RoadWarrior_SubSystems-Login-Registration.jpg)
  * OAuth2 integration
  * User Management
* Social Media Service :
 ![Social Media Service](./.media/RoadWarrior_SubSystems-Share_Trip_details.jpg)
  * Interface with various social media providers
  * Enables user of the RW Dashboard to share the trip info
* UserConfigurationManagement
  * User related settings like whitelisting emails
* Data Management : Encapsulates storage and retrieval of Trip/Booking/User information.
  * Also handles quick reads
  * caching of recent user data
  * Secure write/updates
  * Will be used by other services in RW backend
* TripSyncManager:
  * Get the live data (real world updates) from the travel service provider.
* NotificationManager:
 ![Notification Manager](./.media/RoadWarrior_SubSystems-TripNofiication.jpg)
  * Handles the notification to the user for changes and updates in itinerary
  * Broadcast messaging to all users (e.g. ads [ads may need to be as per user profiles], emergency updates)
* EventHub/CommunicationMgr
  * Handles communications across services and components
* UserManagement
  * Used for new user registration
* API Gateway :
  * Manages routing, load balancing etc and wil be the entry point for the UI layer for Web and Mobile app
* CustomerServiceAndHelpdeskManagement
 ![CustomerServiceAndHelpdeskManagement](./.media/RoadWarrior_SubSystems-Helpdesk_Management.jpg)
  * Integrates to various travel aggregators helpdesk

## Usecases illustrated
The interactions between these subsystems are detailed by the major usecases below

### Register new user
![001 Register new user](./.media/001-Register-new-user.png)
### Login
![002 Login](./.media/002-Login.png)
### Add Email Whitelist/filters
![004 Add Email Whitelistfilters](./.media/004-Add-Email-Whitelist-filters.png)
### User AdReUp Trips
![005 User AdReUp Trips](./.media/005-User-AdReUp-Trips.png)
### Auto update via E-mail polling
![006 Auto update via E-mail polling](./.media/006-Auto-update-via-E-mail-polling.png)

### Adding new Vendor interfaces

### Updates via 3rd party travel services

### Notifications to user

### Analytics and End of Year Summary report

### Raising helpdesk calls

***

### [To go back](./README.md)