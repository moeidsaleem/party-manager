# party-manager

So to make the Party manager we need to understand how it works. 
Every person must provide the following 
## Requirements
> Full Name 
>Phone Number
>email 
>Address 
>City 
>CnicNumber*
>UniversityID*



## Functionality 

Public user can sign up into the system. 
Just buy the tickets online from  the system. 
Get the QR Entry pass. 
A user can also buy many tickets on single QR. 
Tickets purchased will be added to the purchase history of the user. 


### Arriving at the event with QRcode ticket 

The authority will scan your QR code with the application which will in execute a POST method on the server sending along the UniqueID, Status of the event Ticket. 
If the ticket status is set to true, then user can enter the event. 



### Managing the Events 

Admin can add as many events to the system. 
Every event will have the following attributes.
Following are steps: 
 eventName  <br />
 eventLocation 
 eventTime 
 eventType 
 eventCover
 eventRate_key :: eventRate_price *
 eventUniqueId: 
 eventDescription
 eventFacebookUrl
 eventTwitterUrl
 eventAuthority_designation :: eventAuthority_name :: eventAuthority_phone 
 eventContact# 
 eventContactEmail
eventContactPhone 
