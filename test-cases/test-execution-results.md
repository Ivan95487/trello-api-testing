Test Execution Results — Trello API
Project Information
Project: Trello API Testing
Tool: Postman
Collection: TrelloApi
Request: card Copy
Test type: API Testing
Execution status: 5/5 Postman assertions passed
Automated Test Results
ID Test Check Expected Result Actual Result Status
1 HTTP Status Code 200 OK 200 OK PASS
2 Response Time Less than 3000 ms Within the limit PASS
3 Card ID Response contains an ID ID is present PASS
4 Card Name Name is a non-empty string Name is present PASS
5 Card List Assignment Card belongs to the requested list List ID matches PASS
Execution Summary
Total automated assertions: 5
Passed: 5
Failed: 0
Notes
All five Postman assertions passed during the recorded execution of the card Copy request.
These results apply only to this request execution. They do not mean that all ten Jira test cases have been executed.
Next Steps
Execute the remaining Jira test cases.
Add negative API scenarios.
Document actual results and defects, if any

TC-03 — Invalid List ID
Result: Passed
HTTP Status: 400 Bad Request
Postman Assertions: 5/5 Passed
Actual Result: The API rejected the request with an invalid list ID.
Expected Result: The API should reject the invalid list ID and return an error response.
Status: Passed

TC-04 — Request without authorization
Result: Passed
HTTP Status: 401 Unauthorized
Postman Assertions: 3/3 Passed
Actual Result: The API rejected the request without an authorization token.
Expected Result: The API should reject requests without a valid authorization token.
Status: Passed

TC-05 — Repeat Request
Result: Needs Investigation
First Request: 200 OK
Second Request: 400 Bad Request
Postman Assertions: 5/5 Passed
Actual Result: The first request succeeded, while the repeated request returned HTTP 400.
Expected Result: The API should handle repeated requests according to the operation's expected behavior.
Status: Needs Investigation

TC-06 — Single Card
Result: Passed
HTTP Status: 200 OK
Postman Assertions: 5/5 Passed
Actual Result: The API successfully processed the request for a list containing one card.
Expected Result: The API should successfully process the request for a list containing one card.
Status: Passed

TC-07 — Multiple Cards
Result: Passed
HTTP Status: 200 OK
Postman Assertions: 5/5 Passed
Actual Result: The API successfully processed the request for a list containing multiple cards.
Expected Result: The API should successfully process the request for a list containing multiple cards.
Status: Passed
