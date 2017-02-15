---
title: Organizations and organizational hierarchies | Microsoft Docs
description: An organization is a group of people who are working together to carry out a business process or achieve a goal. Organizational hierarchies represent the relationships between the organizations that make up your business.
author: sericks007
manager: AnnBe
ms.date: 2015-12-04 17:25:25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: 71
ms.suite: Released- Dynamics AX 7.0.0
ms.custom: 17291
ms.assetid: 175691e2-5bb6-41d8-a0cb-06d4a4a75e7d
ms.region: Global
ms.author: sericks
translationtype: Human Translation
ms.sourcegitcommit: 744ac447b01dee241043ba27e3b1ffdcb0022a1b
ms.openlocfilehash: b0ee957fc6c846cb1f29ec6288d8b266ebffcd3e


---

# <a name="organizations-and-organizational-hierarchies"></a>Organizations and organizational hierarchies

An organization is a group of people who are working together to carry out a business process or achieve a goal. Organizational hierarchies represent the relationships between the organizations that make up your business.

<a name="organizations"></a>Organizations
-------------

In Microsoft Dynamics 365 for Operations, you can define the following types of internal organizations: legal entities, operating units, and teams.

All internal organizations are types of the **Party** entity. Therefore, these organizations use the address book to store address and contact information. A party, which can be either a person or an organization, can belong to one or more address books.
### <a name="legal-entities"></a>Legal entities

A legal entity is an organization that has a registered or legislated legal structure. Legal entities can enter into legal contracts and are required to prepare statements that report on their performance. A company is a type of legal entity. In this release of Microsoft Dynamics 365 for Operations, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID. This association exists because some functional areas in the program use a company ID, or DataAreaId, in their data models. In these functional areas, companies are used as a boundary for data security. Users can access data only for the company that they are currently logged on to.

### <a name="operating-units"></a>Operating units

An operating unit is an organization that is used to divide the control of economic resources and operational processes in a business. People in an operating unit have a duty to maximize the use of scarce resources, improve processes, and account for their performance. In Microsoft Dynamics 365 for Operations, the types of operating units include cost centers, business units, value streams, departments, and retail channels. The following table provides more information about each type of operating unit.
| Operating unit type | Description                                                                                                                                    | Purpose                                                                                                                                 |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cost center         | An operating unit in which managers are accountable for budgeted and actual expenditures.                                                      | Used for the management and operational control of business processes that span legal entities.                                         |
| Business unit       | A semi-autonomous operating unit that is created to meet strategic business objectives.                                                        | Used for financial reporting that is based on industries or product lines that the organization serves independently of legal entities. |
| Value stream        | An operating unit that controls one or more production flows.                                                                                  | Commonly used in lean manufacturing to control the activities and flows that are required to supply a product or service to consumers.  |
| Department          | An operating unit that represents a category or functional part of an organization that performs a specific task, such as sales or accounting. | Used to report on functional areas. A department may have profit and loss responsibility, and may consist of a group of cost centers.   |
| Retail channel      | An operating unit that represents a brick and mortar store, an online store or an online marketplace.                                          | Used for the management and operational control of one or more stores within or across legal entities.                                  |

### <a name="teams"></a>Teams

A team is an organization in which the members share a common responsibility, interest, or objective. Teams cannot be used in organizational hierarchies.
Organizational hierarchies
--------------------------

Set up organizational hierarchies to view and report on your business from different perspectives. For example, you can set up a hierarchy of legal entities for tax, legal, or statutory reporting. Set up a hierarchy that is based on operating units to report financial information that is not legally required, but that is used for internal control. For example, you can create a purchasing hierarchy to control purchasing policies, rules, and business processes. Each hierarchy is assigned a purpose in Microsoft Dynamics 365 for Operations. The purpose of a hierarchy determines the types of organizations that can be included in the hierarchy. The purpose also determines which application scenarios a hierarchy can be used in. Organizations in a hierarchy can share parameters, policies, and transactions. An organization can inherit or override the parameters of its parent organization. However, shared master data, such as products and address books, applies to the whole organization and cannot be overridden for individual organizations. Creating organizations and hierarchies requires careful planning. For more information, see [Plan the organizational hierarchy](https://docs.microsoft.com/en-us/dynamics365/operations/core/organization-administration/plan-the-organizational-hierarchy).






<!--HONumber=Feb17_HO3-->


