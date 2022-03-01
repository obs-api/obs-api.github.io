

# Request to Disconnect of BPVN Site

<br>

### TYPE = R_BVPN_FR_1

This request can be used only by French Market customers.

The objective of this request is to request the disconnection of a BVPN site.

The request is compatible with Standard and customized catalogs.



<br>
<br>

##  Structure of the `properties` section

<br>


| id         | Type     | Description |
|--------------|:-----------:|------------|
| `servicePoint.id`| `string`     | Orange Single Identifier of the Service Point. This information can be found in the API Core Information in the resource _servicePoints_..       |
| `servicePoint.customerReference`      |  `string`  | Customer Reference of the Service Point.       |
| `servicePoint.reference`      |  `string`  | Commercial Reference of the Service Point.       |
| `contacts.primary.firstName`      |  `string`  |  First name of the secondary contact.        |
| `contacts.primary.lastName`      |  `string`  |  Last name of the primary Contact.     |
| `contacts.primary.email`      |  `string`  | E-mail of of the primary contact.       |
| `contacts.primary.phone`      |  `string`  | Phone number of the primary contact.        |
| `contacts.primary.mobile`      |  `string`  |Mobile number of the primary contact.         |
| `contacts.secondary.firstName`      |  `string`  | First name of the secondary contact.       |
| `contacts.secondary.lastName`      |  `string`  | Last name of the secondary Contact.       |
| `contacts.secondary.email`      |  `string`  |  E-mail of of the secondary contact.      |
| `contacts.secondary.phone`      |  `string`  |  Phone number of the secondary contact.         |
| `contacts.secondary.mobile`      |  `string`  | Mobile number of the secondary contact.       |


###  Constraints

You can use the servicePoint.customerReference, only if it is assigned to one service. 
The primary contact is required and the secondary contact is optional.


##  Business Errors

This section describes only specific errors for this request.

The HTTP status code is 422 for all these errors

| code         | message     | Description |
|--------------|:-----------:|------------|
| -| -    | ----  |
| -| -    | ----  |
| -| -    | ----  |


##  Full Example
