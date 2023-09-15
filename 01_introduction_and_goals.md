# Introduction and Goals

"The Road Warrior" is an online trip management company which allows travelers to see all the of their existing reservations organized by the trip. Below is the list of key features which this application provides:

- User-Friendly Dashboard: Provides an intuitive and user-friendly dashboard that allows travelers to easily view, manage, and organize their reservations.

- Reservation Aggregation: The core functionality is aggregating reservations from various sources, including flights, hotels, car rentals etc.

- Trip Organization: Allow users to organize their reservations into trips. This could involve creating tags for each trip, making it easy for users to access the details of a specific journey.

- Booking Management: Enables users to make changes to their reservations directly through the dashboard, such as modifying flight dates or hotels.

- Real-Time Updates: Ensures that the dashboard provides real-time updates on flight statuses, gate changes, delays, and other relevant information.

- Notification System: Implements a notification system that alerts users about upcoming trips, booking confirmations, or changes to their reservations.

## Stakeholders (Target users)

- System Admin: Responsible for overall system administrator
- Traveller: End user who will use the web/mobile application to organize his trip details
- Product Manager: Interested in getting latest insights on the usage of application by various users to take further business decisions

## Business Context

In today's world when you plan for a trip, there are a lot of things to consider. It starts from booking the flight to the destination, to then booking a hotel for your stay. But how do you go from Airport to Hotel? Oh yes, you need car rentals as well.

There are lot of options out there which provides the travelers the best possible options to do all the booking mentioned above like Expedia, Thomas Cook, MakeMyTrip and so on.

Now, if there are already so many option available, why do we need yet another travel website?
First of all, "The Road Warrior" is not just another travel website. It's a travel aggregation solution for all the travel needs.

Let's think of one scenario, where as a user, you have booked your flight ticket from Expedia, booked your stay in Airbnb and have booked the car in Uber. On the day of travel you have to continuously keep switching between different apps to check your bookings.

Well no longer, this is where "The Road Warrior" comes in. We will aggregate all your booking under one trip so you will never have to bother about checking the status of your booking in multiple applications.

I know what you might be thinking, I have already gone through the hassle of booking the travel from multiple applications, I don't want to go through the trouble of adding these details to another app to get the updates. Don't worry, "The Road Warrior" has got you covered.

Our app will automatically look for for travel booking and will add these under a single trip.
We also provide data insights on the basis on past travel history and recommend accordingly.
"The Road Warrior" is your  travel buddy.

### Business Constraints

- Data Integration: Road Warriors rely on real-time data from multiple sources, such as airlines, hotels, car rental companies, and booking platforms. Integrating and updating this data can be challenging due to variations in data formats and availability.
- Competitive Landscape: Established travel aggregators dominate the market. Entering this competitive space can be difficult, and you'll need a compelling value proposition to attract users and partners.
- Data Security: Managing customer data securely is paramount. Travel aggregators handle sensitive personal and payment information, making them attractive targets for cyber attacks. Security measures must be robust.

### Business risks

- Data analytics performed on user behavior without anonymization
- Funding for the startup is unavailable
- Cyber attacks on the system

### Assumptions

- High API availability with 3rd party external integrations
- Cloud deployments strategy with blue-green should address downtime requirements
- User explicitly grants authorization to scrape emails
- Cloud deployment costs is acceptable and there is enough funding for business continuity

### Business Considerations

- Data Privacy and Security
- Monetization
- Global Reach
- Travel Recommendations
- Customer Support
- Scaling

### Environment

Environments: In this phase we define the environment which impact the design such as Existing Systems, Budget, Timelines etc.

- All the teams developing the software with the decided technologies are well trained and will be available until the MMP/MVP completion
- Cloud deployment costs is acceptable and there is enough funding for business continuity
- Software itself will developed in an incremental approach, planned releases every "Quarter" (Quarterly Releases - QR) and relevant MMP/MVP will be derived for the relevant QR by the product management

## High level requirements

- A new startup wants to build the next generation online trip management dashboard to allow travelers to see all of their existing reservations
organized by trip either online (web) or through their mobile device.
- System shall support traffic of 2 million active users/week
- System shall support handling 15 million user accounts

## Detailed Requirements from user point of view

The requirements are defined here [Requirements](Requirements.md)

## Target Product

- System shall provide user with an option to authorize Road Warrior application to poll email for travel-related emails
- System shall support to filter and whitelist travel email so that the trip details are imported from whitelisted emails automatically
- System shall interface with the agency’s existing airline, hotel, and car rental interface system to update travel details (delays, cancellations, updates, gate changes, etc.).
- System shall provide an user with the updates in less than 5 min to any of the changes in flight, hotel or car
- System shall provide an option to enter the trip details manually using the PNR
- System shall display the details grouped by trip, and once the trip is complete, the items should automatically be removed from the dashboard
- System shall provide an option for the user to share the trip details in preferred social media platforms.
- System shall provide option to export end-of-year summary reports with a wide range of metrics about their travel usage
- System shall also gather analytical data from users trips for various purposes - travel trends, locations, airline and hotel vendor preferences, cancellation and update frequency.

| S. No  | Characteristics | Status | Rationale |
| ----------- | -----------| ----------- | ----------- |
| 1) | Scalability |  [x] | The system needs to support multiple users from across the globe. In order to achieve this we should be able to scale our systems (components) horizontally. |
| 2) | Performance |  [x] | The system needs to support multiple users which means there will be high traffic and some of the scenarios (like gate change, cancellation) are time critical. In order to achieve this we should enforce/ define some architecture functions. |
| 3) | Availability |  [x] | The system needs to be available at all times (as the max downtime for the system is just 5 mins). |
| 4) | Usability |  [x] | As the system should have rich UI for the dashboard/summary report we should make sure that we have arch functions defined for usability. |
| 5) | Upgradeability |  [x] | We should be able to update and upgrade the system with additional feature. |
| 6) | Extensibility |  [x] | As the system might have multi vendor, multi service support, we need to make sure that there is no vendor lock-in and the system is easily extensible. |
| 7) | Security |  [x] | As this system stores user information we need to define architecture functions to handle security. Authenticity of the distributed software must be ensured. All the servers shall be protected by device guard|

Other topics to consider

Cost: Since we are talking about having multiple services and these services will be deployed across the continents. The cost is something we need to keep in mind.  
Configurable:
Confidentiality:
Integrity:
Authentication
