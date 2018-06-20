---
title: メッセージ ストアのテーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801649"
---
# <a name="message-store-tables"></a>メッセージ ストアのテーブル

  
  
**適用されます**: Outlook 
  
メッセージ ストアのテーブルには、現在のプロファイルで、メッセージ ストア プロバイダーに関する情報が含まれています。 MAPI セッションごとに MAPI によって実装され、クライアントによって使用されるメッセージ ストアの 1 つのテーブルがあります。 クライアントは、特定のプロバイダーのすべてのインスタンスを検索する、または特定のメッセージ ストアを検索するのには次の表を使用できます。 
  
メッセージ ストアのテーブルは、動的です。 クライアント アプリケーションのユーザーは、プロファイルを編集する場合は、 **PR_DEFAULT_STORE**の値など、既定のメッセージ ストアを変更する影響を受けるメッセージ ストアのプロパティをすぐに更新されます。 
  
クライアントは、 [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを呼び出して、メッセージ ストアのテーブルをアクセスします。 
  
次のプロパティは、メッセージ ストアのテーブルの設定の必要な列を構成します。
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE**([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

