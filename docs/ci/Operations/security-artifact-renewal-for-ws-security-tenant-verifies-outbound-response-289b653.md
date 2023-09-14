<!-- loio289b653631d241d88fc3344be384f3ba -->

# Security Artifact Renewal for WS-Security \(Tenant Verifies Outbound Response\)

This use case covers all situations where private keys used by a sender to sign response messages sent to the tenant are changed.

The WS-Security verifier uses a public key to verify a WS-Security response payload.

The following figure illustrates the communication path for this use case.

![](images/SAP_HCI_Security_Renewal_-_WS_Security_Outbound_Response_Verify_516df31.png)

> ### Note:  
> It depends on the **operating model** whether the tenant administrator and the integration developer are at the customer or at SAP. In the **customer-managed operating model**, the tenant administrator and integration developer tasks are performed by the customer. In the **SAP-managed operating model**, these tasks are performed by SAP.

1.  Receiver administrator: Creates a new key pair/certificate.
2.  Receiver administrator: Provides the tenant administrator with the new certificate.
3.  Tenant administrator: Adds the new certificate to the tenant keystore.
4.  Tenant administrator: Informs the receiver administrator that payloads signed with the new key can be sent.
5.  Receiver administrator: Configures receiver system to send payloads signed with the new private key from now on.
6.  Receiver administrator: Removes the old key pair/certificate.
7.  Receiver administrator: Informs the tenant administrator that the receiver system sends payloads signed with the new key.
8.  Tenant administrator: Removes the old certificate from the keystore after a certain time period \(which must be at least the guaranteed delivery time\).

    This time period is necessary to make sure that payloads signed with the old key are no longer in the system.


The participants have to make sure that old keys are kept for at least 90 days after they have been exchanged for new ones. This is to ensure that messages can still be decrypted with the old keys for a period of time.

**Related Information**  


[How WS-Security Works](../ConnectionSetup/how-ws-security-works-2f9a038.md "Messages can be protected according to the WS-Security standard.")

[Involved Roles](involved-roles-3968091.md "The security artifact renewal process requires that different persons perform a sequence of steps in a coordinated way on each side of the communication. The exact sequence depends on the kind of security material which is renewed and on the use case.")

