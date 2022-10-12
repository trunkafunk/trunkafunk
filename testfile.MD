##This is a testfile


```mermaid
sequenceDiagram
    participant Client
    participant Twix
    participant SVR
    Client->>Twix: InitiatePhoneNumberVerification 
    Twix->>Client: InitiatePhoneNumberVerificationResponse
    Client->>Twix: VerifyPhoneNumber
    Twix->>Client: VerifyPhoneNumberResponse
    Note left of Client: Login Token is Granted

    Note left of Client: If Existing User:
    Client->>Twix: InitiateEmailAddressVerification
    Twix->>Client: InitiateEmailAddressVerificationResponse
    Client->>Twix: VerifyEmailAddress
    Twix->>Client: VerifyEmailAddressResponse

    
    
    
    viewscreen->>iframe: html & javascript
    iframe->>dotcom: iframe ready
    dotcom->>iframe: set mermaid data on iframe
    iframe->>iframe: render mermaid
```
