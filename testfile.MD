
##New User Flow

```mermaid
sequenceDiagram
    participant Client
    participant Twix
    participant SVR
    Client->>Twix: InitiatePhoneNumberVerification 
    Client->>Twix: VerifyPhoneNumber
    
    Note left of Client: Login Token is Granted. Access token is granted
    Client->>Client: Check Login Status
    
    
    participant AccountServices
    participant ContactDiscovery
    


```




##Existing User Flow
```mermaid
sequenceDiagram
    participant Client
    participant Twix
    participant SVR
    Client->>Twix: InitiatePhoneNumberVerification 
    Client->>Twix: VerifyPhoneNumber
    Note left of Client: Login Token is Granted. Access token is granted
    Client->>Twix: InitiateEmailAddressVerification
    Client->>Twix: VerifyEmailAddress    
    
    participant AccountServices
    participant ContactDiscovery
    

```

