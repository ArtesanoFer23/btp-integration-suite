<!-- loio49f487ec05c54861a0f970e9bdc529e5 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Component Monitor

Get information on the components.

The *Component Monitor* tile shows you the most important information regarding your components at a glance. Out of all components for Edge Integration Cell, the tile always shows either those components in status *Error* or the status of the top three components, *Policy Engine*, *Worker*, and *Solace* \(Message Service\) in status *OK*.

Choose the tile to view the full list of your deployed components and learn more about them. On the *Component Monitor* overview page, you can see a table with the following information:


<table>
<tr>
<th valign="top">

Field

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*Name*

</td>
<td valign="top">

The name of the component \(the list is in alphabetical order\).

</td>
</tr>
<tr>
<td valign="top">

*Status*

</td>
<td valign="top">

The status of the component's resources: *OK*, *Error* or *Warning*

This column shows the combined state of all pods and is calculated based on the **Ready** and **Pod Status** information. For the Status to be **OK** all pods'**Pod Status** must be **Running**, and their current value must equal the expected value in the **Ready** column.

</td>
</tr>
<tr>
<td valign="top">

*Pod Name*

</td>
<td valign="top">

The technical name of the pod.

</td>
</tr>
<tr>
<td valign="top">

*Ready*

</td>
<td valign="top">

The number of resources for each component.

The values \(<number\> of <max. number\>\) indicate how many containers are ready in a pod out of the configured target number of containers.

</td>
</tr>
<tr>
<td valign="top">

*Pod Status* 

</td>
<td valign="top">

The status of the component's recent pod events. It can be any of the following:

-   *Evicted* 

-   *Running*

-   *CrashLoopBackOff* 

    *Completed* 

-   *Pending*

-   *Terminating*




</td>
</tr>
<tr>
<td valign="top">

*Restarts*

</td>
<td valign="top">

The number of times a pod has restarted after it was initialized.

> ### Note:  
> These restarts are common in Kubernetes and are nothing to worry about. However, a high number of restarts indicate that a component has a problem.



</td>
</tr>
</table>

If the pod status indicates an error for one of the components, you can view the specific details of the pod events. To do so, select the component in the table and the option **View Pod Events** \(<span class="SAP-icons-V5"></span> View Pod Events\) becomes available. There's no exhaustive list of all pod events, but the Kubernetes documentation provides some examples. For more information, see [https://kubernetes.io/docs/reference/kubernetes-api/cluster-resources/event-v1/\#Event.](https://kubernetes.io/docs/reference/kubernetes-api/cluster-resources/event-v1/#Event.) 

When you select an individual component, the grayed-out option **View Runtime Parameters** also becomes available. This leads you to the screen **Runtime Parameters** \(also accessible through the **Quick Links** card in the **Operations Cockpit**\), which provides more detailed information on the runtime parameters of the selected component. For more information, see: [Runtime Parameters](runtime-parameters-63c5276.md).

**Related Information**  


[Operations Cockpit](operations-cockpit-ec0fc95.md "The Operations Cockpit is the central control point for operating edge integration cells and allows the Edge Integration Cell administrator to monitor and adjust system configurations and resources.")

[Job Management](job-management-4146fa5.md "Organize and schedule your existing system jobs, such as data store entries cleanup or trace entries cleanup, or add jobs manually.")

[Runtime Parameters](runtime-parameters-63c5276.md "Get information about the runtime parameters of the components of your Edge Integration Cell.")

