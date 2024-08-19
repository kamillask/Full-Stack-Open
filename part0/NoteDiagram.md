```mermaid

sequenceDiagram
	participant browser
	participant server

	browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
	activate server
	server->>browser: GET request to /notes
	deactivate server

	browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
	activate server
	server->>browser: HTML document
	deactivate server

	browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
	activate server
	server->>browser: CSS file
	deactivate server

	browser->> server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
	activate server
	server->>browser: JavaScript file
	deactivate server

	browser--> server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
	activate server
	server->>browser: {content: "asdasdasd", date: "2024-08-18T22:04:41.740Z"}
	deactivate server


	