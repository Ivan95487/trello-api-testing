Trello API — Test Cases
Project overview
This document contains test cases for testing the Trello API functionality for archiving all cards in a list.
Testing type: API Testing
Tool: Postman
Test management: Jira
Target functionality: Archive all cards in a Trello list.
Test Cases
TC-01 — Archive all cards in a list
Priority: High
Precondition: A list contains multiple cards.
Steps:
Send a request to archive all cards in the selected list.
Check the response.
Verify the cards’ archived status.
Expected result: All cards in the selected list are archived successfully.
TC-02 — Archive an empty list
Priority: Medium
Precondition: The list contains no cards.
Steps:
Send a request to archive all cards in the empty list.
Check the response.
Expected result: The request is processed without an unexpected server error.
TC-03 — Invalid list ID
Priority: High
Precondition: An invalid list ID is available.
Steps:
Send the request using an invalid list ID.
Check the response status and body.
Expected result: The API returns an appropriate error response.
TC-04 — Request without authorization
Priority: High
Precondition: No valid authorization credentials are provided.
Steps:
Remove the API key and token.
Send the request.
Expected result: The API rejects the unauthorized request.
TC-05 — Archive an already archived list
Priority: Medium
Precondition: The list has already been archived.
Steps:
Send the archive request again.
Check the response.
Expected result: The API handles the repeated request without unexpected errors.
TC-06 — Archive a list containing one card
Priority: Medium
Precondition: The list contains exactly one card.
Steps:
Send the archive request.
Verify the card status.
Expected result: The single card is archived successfully.
TC-07 — Archive a list containing many cards
Priority: Medium
Precondition: The list contains 100 cards, if supported by the API.
Steps:
Send the archive request.
Check the response.
Verify the archived status of the cards.
Expected result: All eligible cards are archived, subject to API limitations.
TC-08 — Verify other lists are not affected
Priority: High
Precondition: The board contains multiple lists with cards.
Steps:
Send the archive request for one selected list.
Check the cards in the other lists.
Expected result: Cards in other lists remain unchanged.
TC-09 — Invalid HTTP method
Priority: Medium
Precondition: The API endpoint is available.
Steps:
Send the request using an unsupported HTTP method.
Check the response.
Expected result: The API returns an appropriate error response.
TC-10 — Missing list ID
Priority: High
Precondition: The request does not contain a list ID.
Steps:
Remove the required list ID.
Send the request.
Check the response.
Expected result: The API returns an appropriate validation error.
Execution Status
Test execution: Not Run
These test cases describe the planned checks. Actual execution results will be documented separately after running each test.
