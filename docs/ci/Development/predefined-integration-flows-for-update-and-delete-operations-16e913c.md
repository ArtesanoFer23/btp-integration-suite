<!-- loio16e913c349c548ea91207369033452b6 -->

# Predefined Integration Flows for Update and Delete Operations

![](images/Predefined_iFlow_-_Update_and_Delete_b460ea6.png)

This integration flow is autogenerated for Update and Delete operations. In order to complete the binding to the data source, you have to edit at least the Request Mapping element.

To understand this integration flow, let's look at an example of an Update operation.



## Example

You open an app on your smartphone to extend your stay in a hotel room in the city of New York. This application sends the booking information to a hotel booking system. The hotel booking system receives this data with the help of a SOAP Web service and updates it.

The mobile application communicates with the hotel booking system by calling a URI to update a booking record and passes the booking information as the payload. When the OData sender receives the request, it passes it to the Request Mapping element. This mapping element contains information that maps the fields from the OData structure to the SOAP structure and passes the update request to the SOAP receiver.

The SOAP receiver processes the request and updates the booking record in the back-end. The status of the update operation is then sent to the OData sender. The OData sender in turn sends it to the mobile application.
