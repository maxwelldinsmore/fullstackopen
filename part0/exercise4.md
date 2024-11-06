sequenceDiagram
    participant browser
    participant server

    browser->>server: Put https://studies.cs.helsinki.fi/exampleapp/notes
    browser-->>browser: user adds information to form



    browser-->server: clicks save button
    activate server
    server->>browser: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    deactivate server

    Note: No more specifics since /new_note isn't viewable