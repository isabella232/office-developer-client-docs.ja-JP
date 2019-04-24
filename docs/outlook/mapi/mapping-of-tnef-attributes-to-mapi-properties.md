---
title: TNEF 属性から MAPI プロパティへのマッピング
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 25647a6488fec9a39f8b41441fe9afc4c4aa0a7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357653"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>TNEF 属性から MAPI プロパティへのマッピング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の表に、TNEF 実装で定義されているすべての属性と、それらの MAPI プロパティへのマッピングを示します。 場合によっては、複数の MAPI プロパティが1つの属性としてエンコードされることがあります。 一部の属性には、このセクションで後述する拡張の説明があります。
  
|**TNEF 属性**|**MAPI プロパティまたはプロパティ**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID**([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**添付 attachcreatedate** <br/> |**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**/添付データ** <br/> |**PR_ATTACH_DATA_BIN**([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**添付ファイル** <br/> |このマッピングの詳細については、「 [TNEF 属性](tnef-attributes.md)」を参照してください。  <br/> |
|**/添付ファイルメタファイル** <br/> |**PR_ATTACH_RENDERING**([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**添付 attachmodifydate** <br/> |**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**添付添付タイトル** <br/> |**PR_ATTACH_FILENAME**([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**/添付ファイル名** <br/> |**PR_ATTACH_TRANSPORT_NAME**([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**添付本文** <br/> |**PR_BODY**([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY**([PidTagConversationKey](pidtagconversationkey-canonical-property.md))このプロパティは、Microsoft Exchange Server で廃止されました。この使用法は、IPM を検索する場合にのみ、Outlook で使用できます。 **MessageManager**メッセージ。  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE**([PidTagEndDate](pidtagenddate-canonical-property.md))詳細については、「[属性](attdate-attributes.md)」を参照してください。  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME**詳細については、「[属性](attdate-attributes.md)」を参照してください。  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))詳細については、「[属性](attdate-attributes.md)」を参照してください。  <br/> |
|**添付 (エンタープライズ)** <br/> |**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))詳細については、「[属性](attdate-attributes.md)」を参照してください。  <br/> |
|**添付の開始** <br/> |**PR_START_DATE**([PidTagStartDate](pidtagstartdate-canonical-property.md))詳細については、「[属性](attdate-attributes.md)」を参照してください。  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) および**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |この属性の詳細については、「 [attMAPIProps](attmapiprops.md)」を参照してください。  <br/> |
|**/添付メッセージング** <br/> |**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**添付 messageid** <br/> |**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))「 [x. ゲートウェイとトランスポート」の「TNEF 相互関係](tnef-correlation-in-x-400-gateways-and-transports.md)」を参照してください。  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |[attOwner](attowner.md)を参照してください。  <br/> |
|**「添付」** <br/> |**PR_PARENT_KEY**(**PidTagParentKey**)このプロパティは廃止されました。 詳細については、[このエディションで廃止](api-elements-deprecated-in-this-edition.md)された API 要素を参照してください。  <br/> |
|**attPriority** <br/> |**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**添付の添付** <br/> |**PR_RESPONSE_REQUESTED**([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**添付件名** <br/> |**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

