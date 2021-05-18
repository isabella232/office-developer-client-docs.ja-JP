---
title: TNEF 属性と MAPI プロパティのマッピング
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 25647a6488fec9a39f8b41441fe9afc4c4aa0a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405024"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>TNEF 属性と MAPI プロパティのマッピング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の表に、TNEF 実装で定義されている属性と MAPI プロパティへのマッピングを示します。 場合によっては、複数の MAPI プロパティが 1 つの属性としてエンコードされます。 一部の属性では、このセクションの後半で説明が拡張されています。
  
|**TNEF 属性**|**MAPI プロパティまたはプロパティ**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID** ([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**attAttachment** <br/> |このマッピングの詳細については [、「TNEF Attributes」を参照してください](tnef-attributes.md)。  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md) **)** 、 PR_RENDERING_POSITION ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**attBody** <br/> |**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY** ([PidTagConversationKey](pidtagconversationkey-canonical-property.md)) このプロパティは Microsoft Exchange Server で非推奨です。IPM を検索するために、Outlook でのみ使用が保持されます **。MessageManager** メッセージ。  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) の詳細については [、「attDate Attributes」](attdate-attributes.md) を参照してください。  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME** 詳細 [については、「attDate Attributes」](attdate-attributes.md) を参照してください。  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) 詳細については [、「attDate Attributes」](attdate-attributes.md) を参照してください。  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) 詳細については [、attDate 属性を](attdate-attributes.md) 参照してください。  <br/> |
|**attDateStart** <br/> |**PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) の詳細については [、「attDate Attributes」](attdate-attributes.md) を参照してください。  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) **および** PR_SENDER_NAME ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |この属性の詳細については [、「attMAPIProps」を参照してください](attmapiprops.md)。  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**attMessageID** <br/> |**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) [X.400 ゲートウェイとトランスポートの TNEF の相関関係を参照してください](tnef-correlation-in-x-400-gateways-and-transports.md)。  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |**PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |[attOwner を参照してください](attowner.md)。  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY** (**PidTagParentKey**) このプロパティは廃止されました。 詳細 [については、「このエディションで廃止された API 要素](api-elements-deprecated-in-this-edition.md) 」を参照してください。  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED** ([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**attSubject** <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

