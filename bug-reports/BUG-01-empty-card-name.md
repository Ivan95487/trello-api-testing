BUG-01: Trello API allows a card to have an empty name
Bug ID: BUG-01
Title: API allows updating an existing card with an empty name
Module: Trello Cards API
Endpoint: PUT /1/cards/{id}
Severity: Medium
Priority: Medium
Status: New
Preconditions
• An existing Trello card is available.
• A valid Trello API key and token are configured in Postman.
Steps to Reproduce
1. Open Postman.
2. Create a PUT request to /1/cards/{id}.
3. Specify a valid card ID.
4. Add valid API key and token.
5. Add the name parameter with an empty value.
6. Send the request.
7. Check the HTTP response and the card on the Trello board.
Expected Result
The API should reject an empty card name and return a validation error. The existing card name should remain unchanged.
Actual Result
The API returns 200 OK.
The card is updated with an empty name and appears without a title on the Trello board.
Test Data
• HTTP method: PUT
• Parameter: name
• Parameter value: Empty
• HTTP response: 200 OK
Environment
• API: Trello REST API
• Tool: Postman
• Application: Trello Web
Attachments
• Postman response screenshot
• Trello board screenshot showing the card with an empty name
Notes
The behavior should be reviewed against the product requirements for card name validation.
