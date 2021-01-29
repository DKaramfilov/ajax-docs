---
title: Run the RadScheduler in Anonymous Authorization Disabled Environment
page_title: Run the RadScheduler in Anonymous Authorization Disabled Environment - RadScheduler
description: Check our Web Forms article about Run the RadScheduler in Anonymous Authorization Disabled Environment.
slug: scheduler/troubleshootings/run-the-radscheduler-in-anonymous-authorization-disabled-environment
tags: run,the,radscheduler,in,anonymous,authorization,disabled,environment
published: True
position: 2
---

# Run the RadScheduler in Anonymous Authorization Disabled Environment



This article shows how to configure the WCF service in order to run the **RadScheduler** in anonymous authorization disabled environment.

## Troubleshooting

In order to run the **RadScheduler** in anonymous authorization disabled environment you have to enable the **CredentialsTransportation** within the WCF configuration.

Example 1: Configure WCF service to enable the CredentialsTransportation.

````XML
<system.servicemodel>
	<bindings>
	  <basicHttpBinding>
		<binding>
		  <security mode="TransportCredentialOnly">
			<transport clientCredentialType="Windows" />
		  </security>
		</binding>
	  </basicHttpBinding>
	  <webHttpBinding>
		<binding>
		  <security mode="TransportCredentialOnly">
			<transport clientCredentialType="Windows" />
		  </security>
		</binding>
	  </webHttpBinding>
	</bindings>
</system.servicemodel>
````


