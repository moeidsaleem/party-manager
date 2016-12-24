# Party Managing System 


So to make the Party manager we need to understand how it works. 
Every person must provide the following 
### Requirements
- Full Name 
- Phone Number
- email 
- Address 
- City 
- Gendar
- CnicNumber*
- UniversityID*
- userFacebookUrl
- userTwitterUrl
- userGoogleUrl 
- easyPaisaDetails

## Functionality 

Public user can sign up into the system. 
Just buy the tickets online from  the system. 
Get the QR Entry pass. 
A user can also buy many tickets on single QR. 
Tickets purchased will be added to the purchase history of the user. 


### Arriving at the event with QRcode ticket 

The authority will scan your QR code with the application which will in execute a POST method on the server sending along the UniqueID, Status of the event Ticket. 
If the ticket status is set to true, then user can enter the event. 



## Managing the Events 

Admin can add as many events to the system. 
Every event will have the following attributes.
Following are steps
- eventName  
- eventLocation 
- eventTime 
- eventType 
- eventCover
- eventRate_key :: eventRate_price *
- eventUniqueId: 
- eventDescription
- eventFacebookUrl
- eventTwitterUrl
- eventAuthority_designation :: eventAuthority_name :: eventAuthority_phone 
- eventContact# 
- eventContactEmail
- eventContactPhone 

#### Working of event- GuestList 

Once admin creates a new event and the details are added to the system. The Event will opearte its guestlist to active.
Admin will decide to make the guest list public or private though public will be able to see the number of inviting people to the party. 
Guestlist will show three types of guest.
- Bookings - Those who have made reservation but not paid.
- Purchased - Those who have paid and confirmed the reservation. 

Also, users will be able to the profile of the guests coming to the event Except personal information. 



### Ticket Generator 

Ticket is generated for those who have already made booking and Ticket payment status is cleared. 
The system generates a QR-Code that contain the information with a Ticket Unique ID, made up complex encrpytion upto 9 number.
000-000-00-0

first three Number will be eventId encrpted, 
Next Three number will be User uId encrpyted, 
next two number will be ticketSerial encrpyed.
last number will show the status of the ticket. (paid or not) 


# User Inteface (UI) 

For User Inteface , the system will have the following panels. 
1. Admin Panel  - Can CRUD Events,users.
2. User Panel  - Can see event,purchase tickets. See transaction history. 
3. Merchant Panel (Optional) 

### Admin Panel 
See how admin will work. 
##### Admin Workflow 
Admin login to the system-->Admin can CRURD users | Admin can CRUD Events | Admin can manage ads Campaign (optional) | 

:Admin CRUD Users:Admin CRUD Events:Admin CRUD AdsCampaign:

###### Required modules 
- Admin Authentication
- Admin Profile 
- Admin CRUD users.
- Admin CRUD Events.
- Admin Statistics.


### Users Panel
This is how a normal user will work.
##### Users Workflow

User sign up --> user login to the system -->  Manage Profile | Search event --> Place booking --> Checkout -->purchased | Booking history | 

###### Required modules 
- User Authentication
- User Porfile 
- Event Booking 


### Ticketing 

Whenever a event is created a eventId will be generated with it. Admin (creator) can CRUD Ticket types and set prices. 
The ticket will be booked by the users(logged in) , and can purchase upto atleat <b> 10 Tickets on there Account per event. 
Though for couple tickets maximum limit 3 is allowed.

Once the ticket is confirmed a QR-Code with confirmation id will be genarated. Confirmation id will hold details of the userDetails, eventDetails and TicketInformation. 
The QR Scanner will post the request to the server where POST Will be handled in a way that system will search for the ConfirmationLog if the id exist. 

