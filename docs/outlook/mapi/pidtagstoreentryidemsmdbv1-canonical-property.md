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
  
microsoft exchange server 2010 または exchange server 2013 のメッセージストアのエントリ識別子の古いスタイル (microsoft Outlook 2002 以前のバージョン) が格納されています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|識別子:  <br/> |0x65f60102  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Outlook 2003 以降では、サーバー fqdn がエントリ id に統合されているため、参照用の rpc が追加されることはありません。 ただし、これによりエントリ id が長くなり、2つのエントリ id が等しいかどうかを判断するために**compareentryids**メソッドを使用する必要があるシナリオが増えます。 PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) プロパティは、microsoft Outlook 2002 (microsoft Office XP) および以前のバージョンで使用されていた Exchange Server エントリ ID の古い形式にアクセスします。 これにより、スペースを節約したり、エントリ id が等しいかどうかを判断するために必要な**compareentryids**呼び出しの数を減らしたりすることもできます。 古いエントリ id を使用してメールボックスを開くと、参照が必要な場合に追加の rpc が発生する可能性があることに注意してください。 
  
キャッシュモードで PR_STORE_ENTRYID_EMSMDB_V1 プロパティにアクセスするには、MAPI_NO_CACHE フラグと[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用してキャッシュをバイパスする必要があります。 **PR_STORE_ENTRYID_EMSMDB_V1**が使用できない場合は、コードを PR_STORE_ENTRYID に戻す必要があります。 PR_STORE_ENTRYID_EMSMDB_V1 プロパティをサポートしているのは、outlook 2003 ~ Microsoft outlook 2013 のみです。 
  
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId 標準プロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

