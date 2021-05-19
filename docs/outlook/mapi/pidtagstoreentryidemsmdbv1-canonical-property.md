---
title: PidTagStoreEntryIdEmsmdbV1 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415153"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>PidTagStoreEntryIdEmsmdbV1 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Exchange Server 2010 または Exchange Server 2013 メッセージ ストアのエントリ識別子の古いスタイル (Microsoft Outlook 2002 以前のバージョン) が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|識別子:  <br/> |0x65F60102  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Outlook 2003 から、サーバー FQDN はエントリの ID に統合され、参照用の RPC が追加されるのを回避しました。 ただし、これによりエントリの ID が長くなり、2 つのエントリの ID が同等かどうかを判断するために **CompareEntryIDs** メソッドを使用する必要があるシナリオが多くなります。 PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) プロパティは、Microsoft Outlook 2002 (Microsoft Office XP) および以前のバージョンで使用されている Exchange Server エントリ ID の古い形式にアクセスします。 これにより、スペースを節約し、エントリの ID が等しいかどうかを判断するために必要な **CompareEntryIDs** 呼び出しの数も削減できます。 古いエントリの ID を使用してメールボックスを開く場合、参照が必要な場合は、追加の RPC が発生する場合があります。 
  
キャッシュ モードで PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドで MAPI_NO_CACHE フラグを使用してキャッシュをバイパスする必要があります。 この **PR_STORE_ENTRYID_EMSMDB_V1** 使用できない場合は、コードは自動的にPR_STORE_ENTRYID。 2003 Outlook 2003 Microsoft Outlook 2013プロパティPR_STORE_ENTRYID_EMSMDB_V1します。 
  
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId 標準プロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

