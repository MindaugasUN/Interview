# Job Interview assignment

Create Rest API for parking solution

# Functional requirements

  - Start API must accept valid vehicle number plate and must contain parking zone 
  - Stop API must provide parking stop timestamp
  - API that returns list of active parking sessions with it's vehicle number plate , start time and parking zone name
  
 # Domain rules
 
 Parking zone can be two types:
 - OnStreet without barrier
 - OffStreet with barrier
 
 ### OnStreet parking zone
 
 - It must have unique zone name
 
 ### OffStreet parking zone
 
  - It must have unique zone name
  - It must have have System property that defines Vendor (vendor can be VendorA or VendorB)
  - During parking stop  Vendor must be informed via REST API (example: HTTP DELETE /vendorA/Stop with payload {Vehicle number plate})
  - If Vendor request fails - mark parking session as failed for future processing by creating Fine record
 
 ### Fine record 
 - Must have timespamp when happen
 - Must have refference to parking session  
 
 ### Parking session 
 
 - Only 1 active session per vehicle number plate
 
 # Bonus task 
 
 Create UI for testing. It can be web or other application type. 


