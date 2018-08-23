---
title: TNEF の属性から MAPI プロパティへのマッピング
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 810895836ea4d9e4aa82c189f68d13eefd409163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568729"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>TNEF の属性から MAPI プロパティへのマッピング

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
TNEF の実装および MAPI プロパティへのマッピングで定義されているすべての属性を次の表に一覧します。 場合によっては、複数の MAPI プロパティは、1 つの属性としてエンコードされます。 いくつかの属性は、このセクションで後述する説明を拡張してきました。
  
|**TNEF の属性**|**MAPI プロパティまたはプロパティ**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID**([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN**([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**attAttachment** <br/> |このマッピングの詳細については、 [TNEF の属性](tnef-attributes.md)を参照してください。  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING**([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME**([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME**([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**attBody** <br/> |**PR_BODY**([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY**([PidTagConversationKey](pidtagconversationkey-canonical-property.md))このプロパティは Microsoft Exchange Server で推奨されていません。 使用が引き続き発生する Outlook でのみ、IPM の**を検索するためです。MessageManager**メッセージです。  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE**([PidTagEndDate](pidtagenddate-canonical-property.md))詳細については、 [attDate 属性](attdate-attributes.md)を参照してください。  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME**詳細については、 [attDate 属性](attdate-attributes.md)を参照してください。  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))詳細については、 [attDate 属性](attdate-attributes.md)を参照してください。  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME**([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))詳細については、 [attDate 属性](attdate-attributes.md)を参照してください。  <br/> |
|**attDateStart** <br/> |**単に PR_START_DATE**([PidTagStartDate](pidtagstartdate-canonical-property.md))詳細については、 [attDate 属性](attdate-attributes.md)を参照してください。  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID**([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) と**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |この属性の詳細については、 [attMAPIProps](attmapiprops.md)を参照してください。  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**attMessageID** <br/> |**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))[X.400 ゲートウェイおよび配送で TNEF 相関関係](tnef-correlation-in-x-400-gateways-and-transports.md)を参照してください。  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |[AttOwner](attowner.md)を参照してください。  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY**(**PidTagParentKey**)このプロパティは廃止されました。 詳細については、[このエディションでは、API 要素の削除](api-elements-deprecated-in-this-edition.md)を参照してください。  <br/> |
|**attPriority** <br/> |**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED**([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**attSubject** <br/> |**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

