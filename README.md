# SEGB2B
SEG B2B Commerce Implementation

## Author
Pradeep Chary

## Naming Conventions

### Custom Object
| Singular      | Plural        | API           |
| :------------ | :------------ | :------------ |
| Story         | Stories       | B2B_Story     |
| User Story    | User Stories  | B2B_UserStory |

### Custom Field (Standard Object)
| Label         | API               | Description                    |
| :------------ | :---------------- | :----------------------------- |
| Engine Number | B2B_EngineNumber  | B2B - This is so so an purpose |

### Custom Field (Custom Object)
| Label         | API               | Description                    |
| :------------ | :---------------- | :----------------------------- |
| Engine Number | EngineNumber      | B2B - This is so so an purpose |

### Profiles
| Label                                     | Permission        |
| :---------------------------------------- | :---------------- |
| Admin                                     | Read/Edit         |
| B2B Aftermarket User                      | Read/Edit         |
| Customer Community Plus Login User        | Read              |
| SEG Automotive Store Guest Buyer Profile  | Read              |

### Custom Labels
| Name          | Category      |
| :------------ | :------------ |
| CLB2B00005    | B2B Shop Me   |
| CLB2B00011    | B2B Shop Me   |

### Apex Class
| Label                         | Purpose            |
| :---------------------------- | :----------------- |
| B2B_ProductsController        | Name and Logic     |
| B2B_ProductsSelector          | SOQLs              |
| IFv2_DmlController            | DML Operations     |
| IFv2_ExceptionLogs            | Exception Handler  |
| B2B_ProductsControllerTest    | Test Class         |

### Apex Trigger
| Label                             | Purpose            |
| :-------------------------------- | :----------------- |
| B2B_ProductsTrigger               | Trigger Name       |
| B2B_ProductsTriggerHandler        | Trigger Events     |
| B2B_ProductsTriggerHelper         | Logic              |
| IFv2_ExceptionLogs                | Exception Handler  |
| B2B_ProductsTriggerHelperTest     | Test Class         |

### Lightning Web Components
| Name                 |
| :------------------- |
| b2b_productSearch    |
| b2b_footer           |

### Aura Components
| Name                 |
| :------------------- |
| B2B_ProductSearch    |
| B2B_Footer           |

### SOQL Format
```sql
[SELECT
    Id,
    Name,
    EngineNumber
FROM
    Product2
WHERE
    Id = ''
AND
    Name = ''
LIMIT 1000
ORDER BY Name]
```

### File Headers (Apex)
```java
/*******************************************************************************************************
* 
* @ Name            :   IFv2_WorkflowListviewController
* @ Purpose         :   Controller for Workflow Listview
* @ Methods         :   1) fetchWorkflows - Displaying workflows according to profile categorisation
*                           params - sObjectName
*                       2) createRequestRecord - Create Request record
*                           params - WorkflowName
* @ Author          :   Pradeep Chary
* @ Usage           :   1) For displaying workflow list on the workflow page according to the user
*                       2) For creating a request from the workflow page onclick of execute
* @ Test Class Name :   IFv2_WorkflowListviewControllerTest
*
*   Date            |  Developer Name               |  Version      |  Changes
* ======================================================================================================
*   30-10-2018      |  pradeep.chary@absyz.com      |  1.0          |  Initial Version
*   05-11-2018      |  vivek.kothalanka@absyz.com   |  1.1          |  Added Profile Categorization Logic.
*
*******************************************************************************************************/
```

### File Headers (Components)
```html
<!--
* 
* @ Name    :   IFv2_WorkflowListViewCmp
* @ Purpose :   This is a component for displaying the workflow listview
* @ Author  :   Pradeep Chary
*
*   Date            |  Developer Name               |  Version      |  Changes
* ======================================================================================================
*   30-10-2018      |  pradeep.chary@absyz.com      |  1.0          |  Initial Version
*
-->
```

### Variables
| Type          | Naming format         |
| :------------ | :-------------------- |
| String        | strProductName        |
| Integer       | intProductNumber      |
| Boolean       | blnIsProductActive    |
| Object        | objProduct            |
| List          | list_Products         |
| Set           | set_Products          |
| Map           | map_ProductsById      |