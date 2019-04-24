---
title: �㗝�l�A�N�Z�X
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336737"
---
# <a name="delegate-access"></a><span data-ttu-id="961a9-103">代理人アクセス</span><span class="sxs-lookup"><span data-stu-id="961a9-103">Delegate Access</span></span>

  
  
<span data-ttu-id="961a9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="961a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="961a9-p101">Delegate access refers to the user's ability to send a message as another user or receive a message for another user. Delegate access is a service provider-independent feature of MAPI that transport providers can support if they choose. However, no provider is required to do so. Delegate access is valuable when it is necessary for a user to send messages as, or filter incoming messages for, another user or when a user must access another user's message store. Before allowing a delegate user to connect to another user's store, the message store provider must verify that the delegate user has the proper authority.</span><span class="sxs-lookup"><span data-stu-id="961a9-p101">Delegate access refers to the user's ability to send a message as another user or receive a message for another user. Delegate access is a service provider-independent feature of MAPI that transport providers can support if they choose. However, no provider is required to do so. Delegate access is valuable when it is necessary for a user to send messages as, or filter incoming messages for, another user or when a user must access another user's message store. Before allowing a delegate user to connect to another user's store, the message store provider must verify that the delegate user has the proper authority.</span></span> 
  
<span data-ttu-id="961a9-110">�㗝�l�A�N�Z�X��T�|�[�g���邽�߂Ɏg�p����v���p�e�B�� 2 �̃O���[�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="961a9-110">There are two groups of properties that are used to support delegate access:</span></span>
  
 <span data-ttu-id="961a9-111">**PR_SENT_REPRESENTING_ADDRTYPE**([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS**([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-113">**PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-114">**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-115">**PR_SENT_REPRESENTING_SEARCH_KEY**([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-116">**PR_RCVD_REPRESENTING_ADDRTYPE**([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS**([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-118">**PR_RCVD_REPRESENTING_ENTRYID**([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-119">**PR_RCVD_REPRESENTING_NAME**([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="961a9-120">**PR_RCVD_REPRESENTING_SEARCH_KEY**([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="961a9-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span></span> 
  
<span data-ttu-id="961a9-p102">On outgoing messages, the **PR_SENT_REPRESENTING** properties identify the messaging user that should act as the sender. Clients can set these properties as an option. If the **PR_SENT_REPRESENTING** properties are not set by the time the message reaches a transport provider that supports delegate access, it is the provider's responsibility to set them along with the **PR_SENDER** properties.</span><span class="sxs-lookup"><span data-stu-id="961a9-p102">On outgoing messages, the **PR_SENT_REPRESENTING** properties identify the messaging user that should act as the sender. Clients can set these properties as an option. If the **PR_SENT_REPRESENTING** properties are not set by the time the message reaches a transport provider that supports delegate access, it is the provider's responsibility to set them along with the **PR_SENDER** properties.</span></span> 
  
<span data-ttu-id="961a9-p103">��M���b�Z�[�W�ɂ́A **PR_RCVD_REPRESENTING**�v���p�e�B�́A��M�҂Ƃ��ċ@�\����K�v������܂����[�U�[����肵�܂��B�㗝�l�̃��b�Z�[�W��z�M����ӔC�g�����X�|�[�g �v���o�C�_�[�́A **PR_RCVD_REPRESENTING**�� **PR_RECEIVED_BY**�̗����̃v���p�e�B��ݒ肷��K�v������܂��B�N���C�A���g�́A�㗝�l�̃��b�Z�[�W���M�́A�Ή����� **PR_RCVD_REPRESENTING**�v���p�e�B�� **PR_SENT_REPRESENTING**�v���p�e�B�̒l��R�s�[����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="961a9-p103">On incoming messages, the **PR_RCVD_REPRESENTING** properties identify the user that should act as the recipient. Transport providers responsible for delivering delegate messages must set both the **PR_RCVD_REPRESENTING** and **PR_RECEIVED_BY** properties. Clients receiving a delegate message should copy the values of the **PR_SENT_REPRESENTING** properties to the corresponding **PR_RCVD_REPRESENTING** properties.</span></span> 
  
<span data-ttu-id="961a9-p104">���Ƃ��΁A�T���[���x�ɒ��ɁAJohn �� Sally �̃��b�Z�[�W����M����Ƃ��܂��B **PR_RCVD_REPRESENTING**�v���p�e�B�́A�㗝�l�̈���Ƃ��� John ����肵�܂��BJohn Sally �̔ގ�M�������b�Z�[�W�ւ̕ԐM�𑗐M���郁�b�Z�[�W�� **PR_SENDER**�v���p�e�B�́A���o�l�Ƃ��� John ����肵�܂��BJohn Sally ��\�����A���邽�߂ɁA **PR_SENT_REPRESENTING**�v���p�e�B�� Sally ����肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="961a9-p104">For example, suppose John is receiving Sally's messages while Sally is on vacation. The **PR_RCVD_REPRESENTING** properties identify John as the delegate recipient. When John sends a reply to a message that he has received for Sally, the message's **PR_SENDER** properties identify John as the sender. Because John is representing Sally, the **PR_SENT_REPRESENTING** properties identify Sally.</span></span> 
  
<span data-ttu-id="961a9-p105">Transport providers handling incoming delegate messages should usually deliver these messages as the messaging user identified by the **PR_SENT_REPRESENTING** properties rather than as the user identified by the **PR_SENDER** properties. The exception to this rule is when it is necessary to match access privilege and transport types. In this case, a transport provider can choose a sending identity.</span><span class="sxs-lookup"><span data-stu-id="961a9-p105">Transport providers handling incoming delegate messages should usually deliver these messages as the messaging user identified by the **PR_SENT_REPRESENTING** properties rather than as the user identified by the **PR_SENDER** properties. The exception to this rule is when it is necessary to match access privilege and transport types. In this case, a transport provider can choose a sending identity.</span></span> 
  
<span data-ttu-id="961a9-p106">If the **PR_SENT_REPRESENTING** properties are unavailable for an incoming delegate message, the transport provider handling delivery must set them, using the values of the corresponding **PR_SENDER** properties. If the **PR_SENT_REPRESENTING** properties are available but the transport provider does not support delegate access, it can use the **PR_SENDER** properties for delivery.</span><span class="sxs-lookup"><span data-stu-id="961a9-p106">If the **PR_SENT_REPRESENTING** properties are unavailable for an incoming delegate message, the transport provider handling delivery must set them, using the values of the corresponding **PR_SENDER** properties. If the **PR_SENT_REPRESENTING** properties are available but the transport provider does not support delegate access, it can use the **PR_SENDER** properties for delivery.</span></span> 
  

