

1. Application Username / Password is used

2. P6 Web Service URL must be entered and should be in the format
   https://<host>:<port> for SSL
   http://<host>:<port>  without SSL
   https://<host>  when no port is specified

3. Application use must have Web Service module access and access to the business object they want to read or modify.

4. P6 Administrator configuration for Web Service must be modified for on-premise

   Configurations -> Web Services -> Security -> Authentication 
     Mode : Username Token Profile
     Username Token Profile -> Nonce
         Require Nonce: False
     Username Token Profile -> Created
         Require Created: False

   Configurations -> Web Services -> Security -> Message Protection
      Require Timestamp : False
      Require Digital Signatures For Incoming Messages : False
      Require Encryption For Incoming Messages : False

5. Microsoft XML, v3.0 must be installed on the computer to use macros 

6. To modify the data, set CRUD flag value appropriately. Valid CRUD flag values are 
	C = Create
	R = Read (records will be flagged R when data is downloaded)
	U = Update
	D = Delete

5. Certain features are restricted in evaluation copy.