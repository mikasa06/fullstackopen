```mermaid
sequenceDiagram
    
    participant Browser
    participant Server
    

    Browser->>Server: POST ./new_note_spa
    activate Server
    Server-->>Browser: 201 created
    deactivate Server

    Note right of Browser: No more redirects

```