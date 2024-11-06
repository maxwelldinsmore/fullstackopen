sequenceDiagram
    participant browser
    participant server

    browser->>server: Put https://studies.cs.helsinki.fi/exampleapp/spa
    browser-->>browser: user adds information to form

    browser-->server: clicks save button
    activate server
    server->>browser: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server->>browser: sent as json data
    deactivate server

    