# mafch-d-legacy-login

Hi! I'm your first Markdown file in **StackEdit**. If you want to learn about StackEdit, you can read me. If you want to play with Markdown, you can edit me. If you have finished with me, you can just create new files by opening the **file explorer** on the left corner of the navigation bar.


## HEADERS

|       Name   			|	Description										|                    
|-------------------|-------------------------------------------|
|ChannelId			|Is required and corresponds to the system identifier invoked by the API [17091201 for Web or 17189501 for Mobile]|
|sid			|Is required and corresponds to the session id|
|client_id		|Are optional|
|Authorization	|Are optional|
|Accept-Language|Are optional and only support [es, en]|
|Accept			|Are optional and only support [application/json]|
|Content-Type	|Is required and only support [application/json]|
|uuid			|Is required|


## METHOD: POST 
### URI: /api/v1/authorization/authenticateBNE 

The file explorer is accessible using the button in left corner of the navigation bar. You can create a new file by clicking the **New file** button in the file explorer. You can also create folders by clicking the **New folder** button.

### Pre-Requirements

- You need a customer number with active status [21] with his representative and his password

### Request Body

```javascript
{
  "sessionRequired": true,
  "customerCredentials": {
    "customerId": "string",
    "legalRepresentativeId": "string",
    "password": "string",
    "encryptionType": "string",
    "language": "string",
    "clientIp": "string",
    "data": "string"
  }
}
```

### Request Body Specifications
|			Name		|	Description										|
|-------------------|-------------------------------------------|
|"sessionRequired"	|	Contains a logical value and must always be [true] to create the connection with the backend services|
|"customerCredentials"	|	Is the object that contains the information for the customer's logon|
|"customerId"			|	Corresponds to the identifier number of a client of 1-12 numbers
"legalRepresentativeId"	|	Must be 2 digits and can start at 0
"password"				|	Must start with 2 digits and 6 alphanumeric characters
|"language"				|	Must be [es] for Spanish or [en] for English or can be sent empty or null
|"encryptionType"		|	Can be sent empty as they are not currently in use
|"clientIP"				|	Corresponds to the computer´s IP and can be sent empty or null
|"data"					|	Can be sent empty as they are not currently in use

## METHOD: DELETE 

### URI: /api/v1/authorization/authenticateBNE

You can export the current file by clicking **Export to disk** in the menu. You can choose to export the file as plain Markdown, as HTML using a Handlebars template or as a PDF.

### Pre-Requirements

- The "sid" of an active or authenticated session is required

### Request Body

No need request body.

### Request Body Specifications

No need request body.
