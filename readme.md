```mermaid
  sequenceDiagram
      participant browser
      participant server
  
      browser->>server: POST https://studies.cs.helsinki.fi//exampleapp/new_note
      activate server
      Note left of server: Push to note database
      server-->>browser: URL Redirect
      deactivate server
  
      Note right of browser: HTTP GET request to /notes - Reloads the page
```
