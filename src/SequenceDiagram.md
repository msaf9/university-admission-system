```mermaid
sequenceDiagram
  participant Applicant
  participant Administrator
  participant Visitor
  
  par Inquiry details
        Applicant->>Administrator: Inquiry Question
        Administrator -->>Applicant: Reply Inquiry
  end
  
  par Admission form filling
        Applicant->>Administrator: Fill Admission Form
        Administrator->>Administrator: Check for existing Applicant's ID
        Administrator -->>Applicant: Applicant ID and Password
  end
```
