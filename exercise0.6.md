sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Success json returned with message: "note created"
    deactivate server

    Note right of browser: The browser executes the callback function that pushes only the new note to notes
      and rerenders only the notes list