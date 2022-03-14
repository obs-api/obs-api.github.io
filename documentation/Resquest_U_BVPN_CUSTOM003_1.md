# Request to Update of BPVN Site

The objective of this request is to request the update of a BVPN site based on the Template 0003.

Please contact your Orange Representative to verify if you can use this type of request.


The request is compatible with Standard and customized catalogs.

### TYPE = U_BVPN_CUSTOM003_1

<br>
<br>

###  Structure of the `properties` section

<br>

| id         | Type     | Required  | Description|
|--------------|:-----------:|:-----------:|------------|
| `servicePoint.id`| `string`     | (1) |  Orange Single Identifier of the Service Point. This information can be found in the API Core Information in the resource _servicePoints_..       |
| `servicePoint.customerReference`      |  `string`  | (1) | Customer Reference of the Service Point.       |
| `servicePoint.reference`      |  `string`  | (1) |  Commercial Reference of the Service Point.       |
| `contacts.primary.title`      |  `string`  | required |  Title of the person. Authorized Values are: M., Mrs.  |
| `contacts.primary.firstName`      |  `string`  | required | First name of the person.   |
| `contacts.primary.lastName`      |  `string`  | required |  Last name of the person  |
| `contacts.primary.phone`      |  `string`  | required |   Phone Number of the person. The format must be + (TODO) |
| `contacts.primary.mobile`      |  `string`  | required |   Mobile Phone Number of the person. The format must be + (TODO) |
| `contacts.primary.email`      |  `string`  | required |  Email of the person. |
| `contacts.secondary.title`      |  `string`  | optional | Title of the person. Authorized Values are: M., Mrs.    |
| `contacts.secondary.firstName`      |  `string`  | optional |  First name of the person.   |
| `contacts.secondary.lastName`      |  `string`  | optional |Last name of the person   |
| `contacts.secondary.phone`      |  `string`  | optional | Phone Number of the person. The format must be + (TODO)   |
| `contacts.secondary.mobile`      |  `string`  | optional |   Mobile  Phone Number of the person. The format must be + (TODO) |
| `contacts.secondary.email`      |  `string`  | optional | Email of the person.    |
| `profile`| `string`     | required | Name of the Profile.<br>Possible values: _FDJ CONNECT OPTIMA 8M_, _FDJ CONNECT OPTIMA 18M_, _FDJ CONNECT FTTH_,   _FDJ CONNECT ULTIME_, _FDJ CONNECT CELL_   |
| `options.bandwidth`      |  `string`  | required | *Débit*<br>Possible values: _8M_, _1M_, _Extended_       |
| `options.wifi`      |  `string`  |  required | *Wifi complémentaire*   TODO check Quantity???   |
 | `options.multicast`      |  `string`  |required |  *Multicast*    |
 | `options.quickstart`      |  `string`  |required | *Quickstart*       |
 | `options.ethernet`      |  `string`  |required | *Ethernet complémentaire*       |
 | `options.internal_antenna`      |  `string`  | required | *Antenne mobile intérieure*     |
| `options.external_antenna`      |  `string`  | required | *Antenne mobile extérieure*     |

<br>

(1) One of these attributes must be specified `servicePoint.id`, `servicePoint.reference`, `servicePoint.customerReference`. The API can accept the request only one Service/Product per request. By using `servicePoint.customerReference`, several Services/Products can match the value, in this case an error will be returned. 


<br>

 
###  Constraints

You can use the servicePoint.customerReference, only if it is assigned to one service. 


###  Errors

The HTTP status code is 422 for all these errors

| code         | message     | Description |
|--------------|:-----------:|------------|
| -| -    | Several services can match criterias |
| -| -    | ----  |
| -| -    | ----  |
