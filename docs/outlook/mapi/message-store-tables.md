---
title: メッセージ ストア テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 324696284976d599f4a3fd465a4c3c2433dba059
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551073"
---
# <a name="message-store-tables"></a>メッセージ ストア テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア テーブルには、現在のプロファイルのメッセージ ストア プロバイダーに関する情報が含まれる。 MAPI セッションごとに 1 つのメッセージ ストア テーブルがあります。MAPI によって実装され、クライアントによって使用されます。 たとえば、クライアントは、このテーブルを使用して、特定のプロバイダーのすべてのインスタンスを検索したり、特定のメッセージ ストアを検索したりできます。 
  
メッセージ ストア テーブルは動的です。 クライアント アプリケーションのユーザーがプロファイルを編集し、既定のメッセージ ストア (たとえば、影響を受けるメッセージ ストアの **PR_DEFAULT_STORE** プロパティの値) を変更すると、すぐに更新されます。 
  
クライアントは [、IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) メソッドを呼び出してメッセージ ストア テーブルにアクセスします。 
  
次のプロパティは、メッセージ ストア テーブルで必要な列セットを構成します。
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

