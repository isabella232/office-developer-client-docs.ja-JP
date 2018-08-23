---
title: PidTagStoreEntryIdEmsmdbV1 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 505ea9ba5d7105f20f335035e42286fdab1cb1aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576324"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>PidTagStoreEntryIdEmsmdbV1 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
以前の形式 (Microsoft Outlook 2002 およびそれ以前のバージョン) の Microsoft Exchange Server 2010 または Exchange Server 2013 のメッセージ ・ ストアのエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|識別子:  <br/> |0x65F60102  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Outlook 2003 以降では、エントリ Id、参照の追加の Rpc を回避するためにサーバーの Fqdn が統合されています。 ただし、このエントリ Id が長いなりかどうかについて 2 つのエントリ Id と同じ**CompareEntryIDs**メソッドを使用する必要がある複数のシナリオを紹介します。 PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) のプロパティは古い形式の Microsoft Outlook 2002 (Microsoft Office XP) と以前のバージョンで使用されている Exchange Server のエントリ ID にアクセスします。 領域を節約でき、 **CompareEntryIDs**呼び出しのエントリ Id が等しいときに判断するために必要な数を減らしてもこのことができます。 ある古いエントリ Id を使用してメールボックスを開くにかかる可能性がありますいくつか追加の Rpc の紹介が必要な場合に注意してください。 
  
キャッシュ モードでの PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには、MAPI_NO_CACHE フラグを使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用してキャッシュをバイパスする必要があります。 **PR_STORE_ENTRYID_EMSMDB_V1**を使用できない場合、コードする必要がありますに戻る PR_STORE_ENTRYID。 Microsoft Outlook 2013 で Outlook 2003 のみでは、PR_STORE_ENTRYID_EMSMDB_V1 プロパティをサポートします。 
  
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId 標準プロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

