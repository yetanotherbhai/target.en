---
description: Information to help you manage hosts and environments (host groups,) including setting the default host for reporting, creating whitelists, changing an environment's name, moving a host to another environment, and deleting a host or environment.
keywords: host;hosts;host group;environment;default host;whitelist;blacklist
seo-description: Information to help you manage hosts and environments (host groups,) including setting the default host for reporting, creating whitelists, changing an environment's name, moving a host to another environment, and deleting a host or environment.
seo-title: Manage Hosts and Environments
solution: Target
title: Manage Hosts and Environments
topic: Standard
uuid: 12ba9afc-407f-41a9-9619-693033a3bf3e
index: y
internal: n
snippet: y
translate: y
---

# Manage Hosts and Environments

To access the [!UICONTROL  Hosts] list, click ** [!UICONTROL  Setup] ** > ** [!UICONTROL  Hosts] **. 

![](/migration-test-20180813/assets/hosts_list.png) 

This section contains the following information: 


* [ Filter, Sort, or Search the Hosts List](c_hosts-manage-hosts-and-host-groups.md#section_068B23C9D8224EB78BC3B7C8580251B0)
* [ Select Multiple Hosts](c_hosts-manage-hosts-and-host-groups.md#section_EF3B458475184B7EA997C3559714397C)
* [ Create an Environment](c_hosts-manage-hosts-and-host-groups.md#section_32097D0993724DF3A202D164D3F18674)
* [ Set the Default Host for Reporting](c_hosts-manage-hosts-and-host-groups.md#section_4F8539B07C0C45E886E8525C344D5FB0)
* [ Create Whitelists that Specify Hosts That are Authorized to Send...](c_hosts-manage-hosts-and-host-groups.md#section_0AF7F56C386A42C381AF704DEF08D5CC)
* [ Change the Name of an Environment](c_hosts-manage-hosts-and-host-groups.md#section_9F5F94285F8E495E9CE69810CE94CA08)
* [ Move a Host to a Different Environment](c_hosts-manage-hosts-and-host-groups.md#section_9F52549958BD485EB74FE78C32773D2A)
* [ Delete a Host](c_hosts-manage-hosts-and-host-groups.md#section_F56355BA4BC54B078A1A8179BC954632)
* [ Delete an Environment](c_hosts-manage-hosts-and-host-groups.md#section_737F8869612047868D03FC755B1223D3)


## Filter, Sort, or Search the Hosts List {#section_068B23C9D8224EB78BC3B7C8580251B0}

To filter the [!UICONTROL  Hosts] lists by environment, click the ** [!UICONTROL  All] ** drop-down list, then select the desired environment (Production, Staging, Development, or a custom environment you have created). 

To sort the [!UICONTROL  Hosts] list, click any column header (Name, Environment, or Last Requested) to sort the list in ascending or descending order. 

To search the [!UICONTROL  Hosts] list, type a search term in the Search box. 

## Select Multiple Hosts {#section_EF3B458475184B7EA997C3559714397C}

To select multiple hosts, select the check boxes next to the [!UICONTROL  Name] column for the desired hosts. You can then move or delete all selected hosts. 

## Create an Environment {#section_32097D0993724DF3A202D164D3F18674}


1. From the [!UICONTROL  Hosts] list, click the ** [!UICONTROL  Environments] ** tab. 

1. Click ** [!UICONTROL  Create Environment] **. 

1. Specify a descriptive name for the environment. 

1. Specify the desired active mode for the environment: [!UICONTROL  Active Activities] or [!UICONTROL  Active and Inactive Activities]. 

1. Click ** [!UICONTROL  Save] **. 



## Set the Default Host for Reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

You can select the environment you want to use as the default for all activity reports. 

If you use Production as your default, all unknown hosts automatically are added here and report data from there is included in the default report view. Instead, creating a "clean" environment ensures only your core sites/domains are included. 

To set the default environment for reporting: 


1. From the [!UICONTROL  Hosts] list, click the ** [!UICONTROL  Settings] ** tab. 

1. Select the default host from the ** [!UICONTROL  Environment Settings] ** drop-down list. 

1. Click ** [!UICONTROL  Save] **. 




>[!NOTE]
>
>[!DNL  Recommendations] users must rebuild their behavior database and product database if hosts switch host groups. 



## Create Whitelists that Specify Hosts That are Authorized to Send mbox Calls to Target. {#section_0AF7F56C386A42C381AF704DEF08D5CC}

You can create a whitelist that specifies hosts (domains) that are authorized to send mbox calls to [!DNL  Target]. All other hosts generating calls will get a commented-out authorization error response. By default, any host that contains an mbox call registers with [!DNL  Target] in the Production environment and has access to all active and approved activities. If this is not the desired approach, you can instead use the whitelist to record specific hosts that are eligible to make mbox calls and receive [!DNL  Target] content. All hosts will continue to display in the [!UICONTROL  Hosts] list, and environments can still be used to group these hosts and assign different levels to each, such as whether the host can see active and/or inactive campaigns. 

To create a whitelist: 


1. From the [!UICONTROL  Hosts] list, click the ** [!UICONTROL  Settings] ** tab. 

1. Select ** [!UICONTROL  Enable Authorized Hosts for Content Delivery] ** checkbox. 

1. Add the desired hosts in the ** [!UICONTROL  Host Contains] ** box, as desired. 

   Multiple hosts can be listed, each on its own line. 

1. Click ** [!UICONTROL  Save] **. 



If an mbox call is made on an unauthorized host, the call will respond with ` /* no display - unauthorized mbox host */`. 

The whitelist takes precedence over environments. You should clear out all hosts before using the whitelist feature, then only the hosts allowed by the whitelist appear in your hosts list. You can then move the hosts into the desired environment. 

Sometimes domains from other sites appear in your environments. A domain appears in the list if the domain makes a call to your ` mbox.js`. For example, if somebody copies one of your web pages to their server, that domain appears in your environment. You might also see domains from spider engines, language translator sites, or local disk drives. 

In cases where ` mboxHost` is passed in an API call, conversion is recorded for the environment that is passed in. If no environment is passed, the host in the call defaults to Production. 

You can also create a blacklist that specifies hosts (domains) than cannot send mbox calls to [!DNL  Target] by adding the desired hosts in the [!UICONTROL  Host Does Not Contain] box. 

## Change the Name of an Environment {#section_9F5F94285F8E495E9CE69810CE94CA08}


1. From the [!UICONTROL  Hosts] list, click the ** [!UICONTROL  Environments] ** tab. 

1. Hover over the desired environment, then click the ** [!UICONTROL  Edit] ** icon (  ![](/migration-test-20180813/assets/icon_edit.png) ). 

1. Change the environment name. 

1. Click ** [!UICONTROL  Save] **. 



## Move a Host to a Different Environment {#section_9F52549958BD485EB74FE78C32773D2A}


1. From the [!UICONTROL  Hosts] list, hover over the host you want to move. 

1. Click the ** [!UICONTROL  Move] ** icon (  ![](/migration-test-20180813/assets/icon_move.png) ). 

1. Select the desired environment from the drop-down list, then click the check mark icon. 



## Delete a Host {#section_F56355BA4BC54B078A1A8179BC954632}

You can delete a host when it is no longer needed. 


1. From the [!UICONTROL  Hosts] list, hover over the host you want to delete. 

1. Click the ** [!UICONTROL  Delete] ** icon (  ![](/migration-test-20180813/assets/icon_delete.png) ). 

1. Click ** [!UICONTROL  Delete] ** to confirm the deletion. 




>[!NOTE]
>
>The host will be listed again if anyone browses to an mboxed page on the host.



## Delete an Environment {#section_737F8869612047868D03FC755B1223D3}

You can delete an environment when it is no longer needed. 


1. From the [!UICONTROL  Hosts] list, click the ** [!UICONTROL  Environments] ** tab. 

1. Hover over the environment you want to delete. 

1. Click the ** [!UICONTROL  Delete] ** icon (  ![](/migration-test-20180813/assets/icon_delete.png) ). 

1. Click ** [!UICONTROL  Delete] ** to confirm the deletion. 




>[!NOTE]
>
>You cannot delete the Production environment, but you can rename it.


