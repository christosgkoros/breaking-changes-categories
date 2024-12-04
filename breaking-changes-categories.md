# Categories
The same breaking changes as a result of modifying a property also apply to modifying parameters or headers.

### Removing a method
Breaks any clients that rely on that specific functionality because the method no longer exists and cannot be invoked.

### Removing a path
This is considered a breaking change because clients that try to access the removed path receive an error, not the expected data or functionality.

### Modifying an endpoint’s behavior or business logic
Disrupts client applications that depend on the existing behavior or an endpoint’s expected results, which affects their functionality.

### Modifying a property’s meaning
Leads to incorrect interpretations and misuse of data. This is because applications that consume the API will use the property as per its old definition.

### Change in Authentication or Authorization requirements
These changes can deny access to clients that were previously able to interact with the API, which leads to functionality failure.

## Input
Removing a property
The API may reject or ignore requests to clients programmed to send the removed property. This leads to functionality or data consistency issues.

### Making an optional property required
The API may reject requests from clients that did not previously send the previously-optional property. This leads to breaking client interactions with the API.

### Modifying a property’s format (decreasing)
Clients sending data in the original format may receive errors or the API may misinterpret their data. This can lead to unintended consequences.
This change includes:
* Decreasing string length
* Decreasing number range
* Decreasing array items count
* Removing enum values

### Modifying a property’s default value
Client applications that rely on the previous default values may experience unexpected behavior changes when they interact with the API.

## Output
### Removing a required property
This can break clients that expect and rely on the property being present in the API’s response.

### Making a required property optional
Causes issues for clients that expect the previously-required property to be present.

### Modifying a property’s format (increasing)
Results in problems if the client application cannot handle increased data size or complexity. This can lead to crashes or data misinterpretation.
This change includes:
* Increasing string length
* Increasing number range
* Increasing array items count
* Adding enum values
