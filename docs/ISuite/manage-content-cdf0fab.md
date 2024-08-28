<!-- loiocdf0fabfc91a4cdab97643e7b6e5069a -->

# Manage Content

As a content administrator, you can create products that includes APIs from different business systems and manage the content that application developers can view on the catalog.

To illustrate the benefits of this feature, let's consider an example. Imagine you work for XYZ company and you are tasked with building an application. To accomplish this, you need to utilize APIs such as the sales order or CRM APIs from S4HANA, payroll APIs from SuccessFactors, and marketing solution APIs from SAP Marketing Cloud. Using this feature you can enhance the extensibility of these APIs and leverage them to build your application and address any challenges you encounter.

![](images/ABHE_DEV_Edition_3b25f9f.png)

The block diagram illustrates the process of adding and registering business systems in the System Landscape within Business Technology Platform \(BTP\). Once a business system is added and registered, it can be found in the API business hub enterprise. To discover the APIs within these systems, the content admin creates products and publishes them, making the products visible in the catalog. They can incorporate pertinent API documentation and ensure that this catalog is readily available to developers. Once they appear in the catalog, developers can explore and utilize these APIs to develop applications.Please note that these are unmanaged APIs.

To achieve these objectives, your *Global Account Administrator* needs to register these systems in your system landscape. This action establishes a connection between the SAP system and SAP BTP. Following system registration, these systems appear on the *Manage Content* page in API business hub enterprise. For more information, see [Discover APIs within Integration Suite from Various Business Systems](discover-apis-within-integration-suite-from-various-business-systems-0cea56f.md).

> ### Note:  
> At present, you can only register and add S/4 HANA Cloud business systems.

**Related Information**  


[Discover APIs within Integration Suite from Various Business Systems](discover-apis-within-integration-suite-from-various-business-systems-0cea56f.md "As a content administrator, you can make your APIs available on the API business hub enterprise catalog by discovering and publishing them from various business systems.")

[Make APIs Available in the Catalog](make-apis-available-in-the-catalog-f148690.md "As a content administrator, make your APIs available to developers in your organization by publishing them on API business hub enterprise.")

[Manage Products](manage-products-4dd3d90.md "As a content administrator, you have the ability to manage a product once it has been created.")

[Manage Scheduled Requests](manage-scheduled-requests-7236981.md "Monitor and manage all requests for product creation and updates.")
