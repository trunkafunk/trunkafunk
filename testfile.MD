##This is a testfile


```mermaid
sequenceDiagram
    participant Client
    participant Twix
    participant SVR
    Client->>Twix: InitiatePhoneNumberVerification 
    Client->>Twix: VerifyPhoneNumber
    Note left of Client: Login Token is Granted. If New user, Access token is granted
    Note left of Client: If Existing User:
    Client->>Twix: InitiateEmailAddressVerification
    Client->>Twix: VerifyEmailAddress
    Client->>Client: Check Login Status
    
    
    participant AccountServices
    participant ContactDiscovery
    
    ContactDiscovery->>iframe: html & javascript

    iframe->>dotcom: iframe ready
    dotcom->>iframe: set mermaid data on iframe
    iframe->>iframe: render mermaid
```
