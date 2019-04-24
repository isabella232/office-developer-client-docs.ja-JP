---
title: PidTagSendRichInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342519"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>PidTagSendRichInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者がリッチテキスト形式 (RTF) およびオブジェクトのリンクと埋め込み (OLE) オブジェクトを含む、すべてのメッセージのコンテンツを受信できる場合は、TRUE が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEND_RICH_INFO  <br/> |
|識別子:  <br/> |0x3a40  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>解説

配布リストとメッセージングユーザーオブジェクトがこのプロパティを公開することをお勧めします。 
  
このプロパティは、送信者が受信者の MAPI が有効であると判断するかどうかを示します。 
  
このプロパティが TRUE に設定されている場合、トランスポートとゲートウェイは RTF および OLE オブジェクトを含む、メッセージの完全なコンテンツを送信できます。 トランスポートプロバイダーとゲートウェイは、トランスポートニュートラルカプセル化形式 (TNEF) を使用して、関連するすべてのメッセージングシステムにネイティブではないすべてのプロパティをカプセル化する必要があります。 
  
このプロパティが FALSE に設定されている場合、トランスポートプロバイダーとゲートウェイは、ネイティブクライアントが使用できないメッセージの内容を自由に破棄できます。 たとえば、クライアントが RTF をサポートしていない場合、トランスポートプロバイダーはプレーンテキストのみを送信できます。 
  
このプロパティが設定されていない場合、既定の動作は、トランスポートプロバイダー、メッセージ転送エージェント (MTA)、またはゲートウェイの実装によって決まります。 アドレス帳プロバイダーは、このプロパティをサポートする必要はありません。 たとえば、密結合のアドレス帳とトランスポートプロバイダーは、TNEF を送信することはできますが、RTF は使用しません。 
  
クライアントは、トランスポートプロバイダーとゲートウェイが独自のイニシアチブで TNEF を使用することを想定してはなりません。 tnef をサポートする一部のトランスポートプロバイダーおよびゲートウェイは、このプロパティの値を考慮せずにメッセージを送信しますが、TRUE に設定されていない場合は、tnef の作成や送信を拒否します。 
  
> [!NOTE]
> このプロパティの設定とその値に基づいた決定は、受信者ごとに行われます。 
  
既定では、MAPI は値を TRUE に設定します。 [IAddrBook:: createoneoff](iaddrbook-createoneoff.md)または[imapisupport:: createoneoff](imapisupport-createoneoff.md)を呼び出しているクライアントは、 _ulflags_パラメーターで**MAPI_SEND_NO_RICH_INFO**ビットを設定することができます。これにより、MAPI でこのプロパティが FALSE に設定されます。 ユーザーインターフェイスによって作成された1回目の一時は、作成するテンプレートで指定された値を使用します。 
  
[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドへの呼び出しでは、名前を解決できないにもかかわらず、インターネットアドレス (SMTP) として解釈される場合、このプロパティは FALSE に設定されます。 インターネットアドレスとして解釈されるようにするには、未解決のエントリの表示名を X @ Y の形式にする必要があります。Z ("pete@pinecone.com" など)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトへ。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[PidTagAttachDataObject 標準プロパティ](pidtagattachdataobject-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

