This is the 0.6 exercise to show the sequence diagram depicting the user goes to the single-page app
After posting the 
```mermaid
sequenceDiagram
    participant browser
    participant server

    Note When user click button, collect value in "notes_form" element into note variable, adds it to the notes list and then update the page with new notes list. After that sends variable with HTTP POST

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa, payload: [{"note"="new note"}]
    activate server
    server-->>browser: Status 201, payload is {"message":"note created"}
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes
```
