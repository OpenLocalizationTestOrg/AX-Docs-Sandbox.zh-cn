---
title: Electronic signature overview
description: This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Operations.
author: maertenm
manager: AnnBe
ms.date: 2015-12-02 21 - 19 - 12
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 31905da33ce0a752032ffeb186fad139b372a084
ms.lasthandoff: 02/22/2017


---

# <a name="electronic-signature-overview"></a>Electronic signature overview

This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Operations.

<a name="what-is-an-electronic-signature"></a>What is an electronic signature?
--------------------------------

An electronic signature confirms the identity of a person who is about to start or approve a computing process. In some industries, an electronic signature is as legally binding as a handwritten signature. Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense. They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States. **Note:** An electronic signature by itself isn't the same as a digital signature. An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures. A digital signature can help identify whether another user or process has tampered with the data. A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data. As described below, electronic signatures in Microsoft Dynamics 365 for Operations have built-in digital signature functionality.

## <a name="electronic-signatures-in-dynamics-365-for-operations"></a>Electronic signatures in Dynamics 365 for Operations
In Dynamics 365 for Operations, you can use electronic signatures for critical business processes. Some processes have built-in electronic signature capabilities. You can also create custom signature requirements for any database table and field. Electronic signatures have built-in digital signature functionality. Every user who signs documents must obtain a valid cryptographic certificate. When a document is signed, the private key that is associated with that certificate is validated. Dynamics 365 for Operations records electronic signature information in a log to provide an audit trail. To set up electronic signatures, see [Set up electronic signatures](http://ax.help.dynamics.com/en/wiki/set-up-electronic-signatures/).

## <a name="users-who-require-access-to-electronic-signatures"></a>Users who require access to electronic signatures
Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.

### <a name="electronic-signature-administrator"></a>Electronic signature administrator

The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified. By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.

### <a name="signer"></a>Signer

A signer provides electronic signatures for documents and processes that require signatures. By default, a user who belongs to the **System user** security role has permission to sign documents electronically. **Note:** The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed. A user who changes data and must then sign for those changes must have permission to change the data. A user who signs on behalf of another user might not require access to the data. An example of this kind of user is a supervisor who signs for an employee's changes.

### <a name="electronic-signature-auditor"></a>Electronic signature auditor

The electronic signature auditor reviews the database log and the signature review log that is available from the database log. By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures. If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:

-   View electronic signature failures
-   View database log

## <a name="signing-documents-electronically"></a>Signing documents electronically
### <a name="get-a-certificate"></a>Get a certificate

Before you sign documents electronically in Dynamics 365 for Operations, you must request a certificate. **Note:** Dynamics 365 for Operations uses Microsoft SQL Server features to create certificates and enable electronic signing. No additional certificate or public key infrastructure (PKI) is required. When you request a certificate, a public key and a private key are created for you in the Dynamics 365 for Operations database. The private key is encrypted by using a password that is known only to you. When you sign a document electronically, your identity is verified when you enter the password. To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**. You must enter and confirm the password that you will use for signing. The password is used to protect your private key and authorize the use of your certificate. This password isn't stored in the database, and it isn't available to anyone else, not even to the Dynamics 365 for Operations administrator. If you forget the password that is connected with your certificate, that certificate must be reset. If you reset the certificate, you don't affect documents that you signed by using the previous certificate. To reset the certificate, on the **Options** page, click **Reset certificate**.

### <a name="sign-a-document-electronically"></a>Sign a document electronically

The **Sign document** page is displayed when you make a change that requires an electronic signature.

1.  On the **Sign document** page, click the **Document** tab to review the changes to the document.
2.  On the **Signature** tab, select a reason code.
3.  Enter a comment, if a comment is required.
4.  If your user ID doesn't appear in the **Signer** field, select it in the list.
5.  Enter your location, if this information is required.
6.  Click **OK**.

### <a name="sign-for-another-users-changes"></a>Sign for another user's changes

Occasionally, you might want a user to sign for another user's changes. For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM). Use this procedure to designate a Dynamics 365 for Operations user as a signer for another user. **Note:** When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change. The user can't save the change until the signature has been provided. To designate approvers, follow these steps.

1.  On the **Options** page, on the **Accounts** tab, click **Designate approver**.
2.  In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.
3.  In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.



