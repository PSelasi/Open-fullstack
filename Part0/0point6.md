```mermaid
sequenceDiagram
participant user
participant browser
participant server

user->>browser: Inputs new note and clicks save

browser->>server: Sends a POST request for the new note in JSON format

activate server
server->>browser: Updates database with the new note and sends 201 Created
deactivate server
Note right of server: Server saves the new note to the database

browser->>user: Displays the new note
