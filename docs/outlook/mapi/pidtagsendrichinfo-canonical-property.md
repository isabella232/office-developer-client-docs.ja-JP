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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342519"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>PidTagSendRichInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者がリッチ テキスト形式 (RTF) やオブジェクト リンクおよび埋め込み (OLE) オブジェクトを含むすべてのメッセージ コンテンツを受信できる場合は TRUE を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEND_RICH_INFO  <br/> |
|識別子:  <br/> |0x3A40  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

配布リストとメッセージング ユーザー オブジェクトでこのプロパティを公開する必要があります。 
  
このプロパティは、送信者が受信者を MAPI が有効と見なすかどうかを示します。 
  
このプロパティを TRUE に設定すると、トランスポートとゲートウェイは RTF オブジェクトや OLE オブジェクトを含むメッセージの完全なコンテンツを送信できます。 トランスポート プロバイダーとゲートウェイは、トランスポート ニュートラル カプセル化形式 (TNEF) を使用して、関連するすべてのメッセージング システムにネイティブではないプロパティをカプセル化する必要があります。 
  
このプロパティを FALSE に設定すると、トランスポート プロバイダーとゲートウェイは、ネイティブ クライアントが使用できないメッセージ コンテンツを自由に破棄できます。 たとえば、クライアントが RTF をサポートしていない場合、トランスポート プロバイダーはプレーン テキストのみを送信できます。 
  
このプロパティを設定しない場合、既定の動作は、トランスポート プロバイダー、メッセージ転送エージェント (MTA)、またはゲートウェイの実装によって決まります。 アドレス帳プロバイダーは、このプロパティをサポートする必要はありません。 たとえば、緊密に結合されたアドレス帳とトランスポート プロバイダーは、TNEF の送信を選択できますが、RTF は使用されません。 
  
クライアントは、トランスポート プロバイダーとゲートウェイが独自のイニシアチブで TNEF を使用すると想定すべきではありません。 TNEF をサポートする一部のトランスポート プロバイダーとゲートウェイは、このプロパティの値に関係なく送信しますが、TNEF が TRUE に設定されていない場合は、TNEF の作成や送信を拒否する場合があります。 
  
> [!NOTE]
> このプロパティの設定と、その値に基づく決定は、受信者ごとに行われます。 
  
既定では、MAPI は値を TRUE に設定します。 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)を呼び出すクライアントまたは [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)を呼び出すプロバイダーは _、ulFlags_ パラメーターで **MAPI_SEND_NO_RICH_INFO** ビットを設定できます。これにより、MAPI は、このプロパティを FALSE に設定します。 ユーザー インターフェイスによって作成された 1 回のオフは、作成テンプレートで指定された値を使用します。 
  
名前を解決できないが、インターネット アドレス (SMTP) として解釈できる場合に [IAddrBook::ResolveName](iaddrbook-resolvename.md) メソッドを呼び出す場合、このプロパティは FALSE に設定されます。 インターネット アドレスとして解釈するには、未解決のエントリの表示名は、次の形式X@Y。Z ("pete@pinecone.com" など)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトまで。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagAttachDataObject 標準プロパティ](pidtagattachdataobject-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

