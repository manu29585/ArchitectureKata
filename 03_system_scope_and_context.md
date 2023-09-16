# System Scope and Context {#section-system-scope-and-context}

## Domain Model

![Entities](.media/Entities.png)

![SystemDomainModel](.media/DomainModel.png)

## High level User Interaction and Use Cases

![UserInteractionAndUseCases](.media/UserInteractionAndUseCases.png)

## Sub-system interaction

![Subsystems-Interaction](./.media/RoadWarrior_SubSystems-Subsystems_And_Interactions.png)

## Use case illustrations

The interactions between these subsystems are detailed by the major use cases below

### Register new user

![001 Register new user](./.media/001-Register-new-user.png)

### Login

![002 Login](./.media/002-Login.png)

* On the Login/Authenticate call Identity Management checks User credentials with User Management
* Inform Dashboard Mgr of active user [will be useful for further use cases...]
* Return valid bearer token
* Valid bearer token is must for all further use case calls

**NOTE**: ApiGateway will reject all subsequent calls with invalid bearer tokens
Also for simplicity sake in below diagrams The API Gateway is not explicitly shown

### Add Email Whitelist/filters

![004 Add Email Whitelist filters](./.media/004-Add-Email-Whitelist-filters.png)

1. User config management has the responsibility to add/update/get email and filter information

**NOTE**: Use of User Config Management Service is illustrated in next interaction

### Auto update via E-mail polling

![006 Auto update via E-mail polling](./.media/006-Auto-update-via-E-mail-polling.png)

1. Dashboard Manager activates Email Service for polling and scraping emails
2. Email Service get users whitelist/filters thru User Config Management
3. Informs Trip Organizer of trip/booking data from E-mail. E.g. data extracted PNR
4. Trip Organizer will check if data is newer and commit

**NOTE**: Trip Organizer also works with Trip Service Provider to get more details on the Trip/Booking
![005-Get-All-Details-Thru3rd-Party](./.media/005-Get-All-Details-Thru3rd-Party.png)

### User manually adds/updates Trips

In this interaction Dashboard Manager directly interacts with Trip Organizer
![005 User AdReUp Trips](./.media/005-User-AdReUp-Trips.png)

## Subsystem Details

* Email Service
![Email Service](./.media/RoadWarrior_SubSystems-Email_Polling_And_Whitelisting.jpg)
  * Interfaces with different mailing services to get and scrape the user mails. Works as an aggregator for all the mail service provider.

* Travel Service provider
![Travel Service Provider](./.media/RoadWarrior_SubSystems-Travel_Service_Provider.jpg)
* Interfaces with 3rd party travel providers{eg. make my trip} and air,hotel, car rental service provider. To get
  * more details on PNR.
  * updates etc

* TripOrganizer
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

* Vendor Management
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
