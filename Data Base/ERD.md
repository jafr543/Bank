```mermaid
erDiagram
    Countries {
        int CountryID PK
        string CountryName
    }

    People {
        int PersonID PK
        string FirstName
        string LastName
        string Email
        string PhoneNumber
        int CountryID FK
        date DateOfBirth
    }

    Clients {
        int ClientID PK
        int PersonID FK
    }

    Accounts {
        int AccountID PK
        int ClientID FK
        string AccountNumber
        decimal Balance
        datetime CreatedDate
        boolean IsClose
    }

    Transactions {
        int TransactionID PK
        int TransactionGroupID
        int CreatedByUserID FK
        string Type
        datetime CreatedDate
        int AccountID FK
        decimal Amount
    }

    Users {
        int UserID PK
        int PersonID FK
        string UserName
        string Passwordhash
        int Permissions
        boolean IsActive
        datetime CreatedDate
    }

    LoginSessions {
        int LoginID PK
        int UserID FK
        string RefreshTokenHash
        datetime ExpiresAt
        datetime RevokedAt
        datetime CreatedAt
    }

    AuditLogs {
        int AuditLogID PK
        int UserID FK
        string Action
        datetime PerformedAt
        string Status
        string IPAddress
    }

    Countries ||--o{ People : "contains"
    People ||--o{ Clients : "is"
    People ||--o{ Users : "is"
    Clients ||--o{ Accounts : "owns"
    Accounts ||--o{ Transactions : "has"
    Users ||--o{ Transactions : "creates"
    Users ||--o{ LoginSessions : "has"
    Users ||--o{ AuditLogs : "generates"
