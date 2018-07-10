---
title: PidTagStoreEntryIdEmsmdbV1 の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803591"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>PidTagStoreEntryIdEmsmdbV1 の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
以前の形式 (Microsoft Outlook 2002 およびそれ以前のバージョン) の Microsoft Exchange Server 2010 または Exchange Server 2013 のメッセージ ・ ストアのエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|識別子:  <br/> |0x65F60102  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>備考

Microsoft Outlook 2003 以降では、エントリ Id、参照の追加の Rpc を回避するためにサーバーの Fqdn が統合されています。 ただし、このエントリ Id が長いなりかどうかについて 2 つのエントリ Id と同じ**CompareEntryIDs**メソッドを使用する必要がある複数のシナリオを紹介します。 PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) のプロパティは古い形式の Microsoft Outlook 2002 (Microsoft Office XP) と以前のバージョンで使用されている Exchange Server のエントリ ID にアクセスします。 領域を節約でき、 **CompareEntryIDs**呼び出しのエントリ Id が等しいときに判断するために必要な数を減らしてもこのことができます。 ある古いエントリ Id を使用してメールボックスを開くにかかる可能性がありますいくつか追加の Rpc の紹介が必要な場合に注意してください。 
  
キャッシュ モードでの PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには、MAPI_NO_CACHE フラグを使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用してキャッシュをバイパスする必要があります。 **PR_STORE_ENTRYID_EMSMDB_V1**を使用できない場合、コードする必要がありますに戻る PR_STORE_ENTRYID。 Microsoft Outlook 2013 で Outlook 2003 のみでは、PR_STORE_ENTRYID_EMSMDB_V1 プロパティをサポートします。 
  
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId の標準的なプロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
