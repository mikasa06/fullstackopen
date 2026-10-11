```mermaid
sequenceDiagram
    
    participant Browser
    participant Server
    

    Browser->>Server: Get ./spa
    activate Server
    Server-->>Browser: HTML Document
    deactivate Server

    Browser->>Server: Get ./main.css 
    activate Server
    Server-->>Browser: CSS Files
    deactivate Server

    Browser->>Server: Get ./spa.js
    activate Server
    Server-->>Browser: JavaScript Files
    deactivate Server

    Note right of Browser: While running JS, needs to get JSON Files
    Browser->>Server: Get ./data.json
    activate Server
    Server-->>Browser: JSON Files
    deactivate Server
```