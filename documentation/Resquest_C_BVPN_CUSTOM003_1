# Request to Creation of BPVN Site

The objective of this request is to request the deployment of a new BVPN site based on the template 003.


Please contact your Orange Representative to verify if you can use this type of request.


### TYPE = C_BVPN_CUSTOM003_1

<br>
<br>

###  Structure of the `properties` section

<br>


| id         | Type     | required | Description |
|--------------|:-----------:|:-----------:|------------|
| `network.id`      |  `string` | (1) |Orange Single identifier of the Network where the new BVPN site must be assigned.    |
| `network.name`      |  `string`  |(1) | Name of the Network where the new BVPN site must be assigned.    |
| `billingAccount.id`      |  `string`  |(2) | Billing Account Number for invoicing the service.   |
| `billingAccount.code`      |  `string`  |(2) | Sub Billing Account Number for invoicing the service.    |
| `profile`| `string`     | required | Name of the Profile.<br>Possible values: _FDJ CONNECT OPTIMA 8M_, _FDJ CONNECT OPTIMA 18M_, _FDJ CONNECT FTTH_,   _FDJ CONNECT ULTIME_, _FDJ CONNECT CELL_   |
| `location.name`      |  `string`  | required |  Name of the location where the service must be installed. |
| `location.localCompany`      |  `string`  | optional | Name of the Local Company  |
| `location.localCompanyLegalNumber`      |  `string`  | optional | Number of the Local Company corresponding to the SIREN.  |
| `location.address.street`      |  `string`  | required | Main street information. |
| `location.address.extendedStreet`      |  `string`  | optional | Complementary information allowing to facilitate the elligibily of the Offer.  |
| `location.address.postalCode`      |  `string`  | required | Postal Code of the Location. For France, must be a 5 digits number.  |
| `location.address.city`      |  `string`  | required | Name of the City  |
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
| `options.bandwidth`      |  `string`  | optional | *Débit*<br>Possible values: _8M_, _1M_, _Extended_       |
| `options.wifi`      |  `string`  | optional | *Wifi complémentaire*    Todo Check Quantity  |
| `options.multicast`      |  `string`  | optional | *Multicast*    |
| `options.quickstart`      |  `string`  | optional |*Quickstart*       |
| `options.ethernet`      |  `string`  | optional |*Ethernet complémentaire*       |
| `options.internal_antenna`      |  `string`  | optional |*Antenne mobile intérieure*     |
| `options.external_antenna`      |  `string`  | optional |*Antenne mobile extérieure*     |


<br>

(1)

(2)

(3)

(4)

<br>
<br>
<br>


###  Constraints

You can use the servicePoint.customerReference, only if it is assigned to one service. 


###  Business Errors

The HTTP status code is 422 for all these errors

| code         | message     | Description |
|--------------|:-----------:|------------|
| -| -    | The current address is not valid. |
| -| -    | The current address is not enough precize to determin the offer eligibility. Please, fill-in the extendedStreet field.  |
| -| -    | ----  |
