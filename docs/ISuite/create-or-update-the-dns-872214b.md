<!-- loio872214b6b3c84c86b24b6f5c3cf0dd97 -->

# Create or Update the DNS

Learn how to create or update the Domain Name Server \(DNS\).



<a name="loio872214b6b3c84c86b24b6f5c3cf0dd97__prereq_nbs_lth_vlb"/>

## Prerequisites

To determine the external IP address of the deployed solution, run the following command:

> ### Sample Code:  
> ```
> kubectl -n istio-system get service istio-ingressgateway
> ```

The `EXTERNAL-IP` value was assigned by the platform service load balancer. The IP address \(for Azure\) or hostname \(for AWS\) is used for DNS mapping.



## Context

After you've deployed the Edge Integration Cell, perform the following steps:



## Procedure

1.  In your DNS service, create a new entry that associates the domain that you previously defined with the back-end address assigned to the ingress gateway.

    > ### Note:  
    > Propagating the domain through the DNS can take some time because, if DNS records are cached, they require time to expire. Wait for several minutes for your DNS records to take effect.

2.  After the domain is propagated through the DNS, Edge Integration Cell is accessible in the browser using the defined Fully Qualified Domain Name \(FQDN\). To verify if FQDN is accessible, in your browser, open `https://<FQDN>`. A valid browser response is: `{"error":{"code":"apiProxyNotFound","message":"API proxy not found for the given host and path"}}`.


