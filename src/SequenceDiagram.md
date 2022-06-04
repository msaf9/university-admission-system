```mermaid
sequenceDiagram
  participant Visitor
  participant Applicant
  participant Administrator
  
  par Inquiry details
        Applicant->>Administrator: Inquiry Question
        activate Administrator 
        Administrator -->>Applicant: Reply Inquiry
        deactivate Administrator
  end
  
  par Admission form filling
        Applicant->>Administrator: Fill Admission Form
        activate Administrator 
        Administrator->>Administrator: Check for existing Applicant's ID
        Administrator -->>Applicant: Applicant ID and Password
        deactivate Administrator
  end
  
  par Login for merit list
        Applicant->>Administrator: Login details
        activate Administrator
        Administrator->>Administrator: Checks Validation
        Administrator -->>Applicant: View Merit List
        deactivate Administrator
  end
  
  par Final admission confirmation
        Applicant->>Administrator: Final Merit Details
        activate Administrator
        Administrator -->>Applicant: Admission Confirmation and reciept
        deactivate Administrator
  end
  
  par Inquiry Registration
        Visitor->>Administrator: Inquiry Details
        activate Administrator
        Administrator->>Administrator: Compare Inquiry IDs
        Administrator-->>Administrator: Checks with already done inquiries
        Administrator -->>Visitor: Send Inquiry ID
        deactivate Administrator
  end
  
  par Inquiry Reply
        Visitor->>Administrator: Inquiry ID
        activate Administrator
        Administrator -->>Visitor: Inquiry Response
        deactivate Administrator
  end
```
