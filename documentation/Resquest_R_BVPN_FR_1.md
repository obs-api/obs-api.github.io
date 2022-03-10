

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


| id         | Type     | Required     |Description |
|--------------|:-----------:|:-----------:|------------|
| `servicePoint.id`| `string`     | (1) | Orange Single Identifier of the Service Point. This information can be found in the API Core Information in the resource _servicePoints_..       |
| `servicePoint.customerReference`      |  `string`  | (1) | Customer Reference of the Service Point.       |
| `servicePoint.reference`      |  `string`   | (1) | Commercial Reference of the Service Point.       |
| `contacts.primary.title`      |  `string`   | required |  Title of the primary contact.        |
| `contacts.primary.firstName`      |  `string`   |required  |  First name of the primary contact.        |
| `contacts.primary.lastName`      |  `string`   | required |  Last name of the primary Contact.     |
| `contacts.primary.email`      |  `string`   | required | E-mail of of the primary contact.       |
| `contacts.primary.phone`      |  `string`    | required| Phone number of the primary contact.        |
| `contacts.primary.mobile`      |  `string`    |required |Mobile number of the primary contact.         |
| `contacts.secondary.title`      |  `string`    | optional | Title of the secondary contact.       |
| `contacts.secondary.firstName`      |  `string`     | optional  | First name of the secondary contact.       |
| `contacts.secondary.lastName`      |  `string`   | optional | Last name of the secondary Contact.       |
| `contacts.secondary.email`      |  `string`    | optional |  E-mail of of the secondary contact.      |
| `contacts.secondary.phone`      |  `string`   | optional |  Phone number of the secondary contact.         |
| `contacts.secondary.mobile`      |  `string`   | optional | Mobile number of the secondary contact.       |

(1) One of these attributes must be specified `servicePoint.id`, `servicePoint.reference`, `servicePoint.customerReference`. The API can accept the request only one Service/Product per request. By using `servicePoint.customerReference`, several Services/Products can match the value, in this case an error will be returned. 


<br>


###  Constraints



All fields of `contacts.primary` . primary contact is mandatory and the secondary contact is optional.


##  Business Errors

This section describes only specific errors for this request.

The HTTP status code is 422 for all these errors

| code         | message     | Description |
|--------------|:-----------:|------------|
| 3610 | Several Products identified    | A disconnection request can be accepted only on one Service/Product. The current criterias    |
| 3611| RequestedAt not Valid    | The requestedAt date must be 20 days minimum and must be a working day in France.  |
| -| -    | ----  |

##  Common Errors

This section describes only specific errors for this request.

The HTTP status code is 422 for all these errors

| status  | code         | message     | Description |
|:--------------:|:-----------:|-----------|------------|
| 401 | - | -     | ---.    |
| 412|65| Precondition failed   | The mandatory field 'xxx' is missing. |
| -|-| -    | ----  |

##  Full Example

Example of a full body for a disconnection request for the BVPN site with the customerReference "INT-AA001-001"

```
{
    "requestedAt": "2022-06-01",
    "type": "R_BVPN_FR_1",
    "customerReference": "WAN-AAT-AA001-001",
    "contract": "256060",
    "properties": {
        "servicePoint": {
            "customerReference": "AAT-AA001-001"
        },
        "contracts":
        {
            "primary":
            {
                "title": "M",
                "firstName": "Paul",
                "lastName": "LANGEL",
                "phone":  "+33401010101",
                "mobile": "+33600200200",
                "email": "paul.langel@mycompany.com"
            }
        }
    }
}

```


##  Relation with Core Information API

`id`, `name`, `customerReference` of the Service Point section can be retrieve in the Core Information API
