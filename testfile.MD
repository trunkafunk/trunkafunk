
New User Flow

```mermaid
sequenceDiagram
    participant Client
    participant AuthenticationService
    participant AccountService
    participant SVR
    Client->>SVR: GetEncryptedKey
    Client->>AccountService: GetSVRToken()???
    Client->>AuthenticationService: InitiatePhoneNumberVerification() 
    Client->>AuthenticationService: VerifyPhoneNumber()
    
    Note left of Client: Login Token is Granted. Access token is granted
    Client->>Client: Check Login Status
    Note left of Client: If invited or Active(?)
    Client->>Client: createWallet()
    Client->>AccountService: BackupWords()

    Client->>AccountService:SetWalletAddressRequest()
    Note left of Client: Backup SVR Record    
    
    participant AccountServices
    participant ContactDiscovery
    


```




Existing User Flow
```mermaid
sequenceDiagram
    participant Client
    participant Twix
    participant SVR
    Client->>SVR: GetSVRToken()

    Client->>Twix: InitiatePhoneNumberVerification() 
    Client->>Twix: VerifyPhoneNumber()
    Note left of Client: Login Token is Granted. Access token is granted
    Client->>Twix: InitiateEmailAddressVerification
    Client->>Twix: VerifyEmailAddress    
    Client->>Twix: getEncryptedBackup    
    
    
    
    
    
    participant AccountServices
    participant ContactDiscovery
    

```

