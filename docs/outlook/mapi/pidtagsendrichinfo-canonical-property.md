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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386440"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>PidTagSendRichInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者がリッチ テキスト形式 (RTF) およびオブジェクトのリンクと埋め込み (OLE) オブジェクトを含む、すべてのメッセージの内容を受信できる場合は TRUE を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEND_RICH_INFO  <br/> |
|識別子:  <br/> |0x3A40  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>備考

配布リストとメッセージのユーザー オブジェクトがこのプロパティを公開することをお勧めします。 
  
このプロパティでは、送信者が受信者に MAPI を有効にすると見なされるかどうかを示します。 
  
このプロパティは TRUE に設定、トランスポートおよびゲートウェイは RTF と OLE オブジェクトを含むメッセージの完全なコンテンツを送信できます。 トランスポート プロバイダーが、ゲートウェイは、すべてのメッセージング ・ システムにネイティブではない任意のプロパティをカプセル化するのには、トランスポート ニュートラル カプセル化形式 (TNEF) を使用する必要があります。 
  
このプロパティは FALSE に設定、トランスポート プロバイダーが、ゲートウェイは、ネイティブのクライアントが使用できないメッセージの内容を破棄するのには無料です。 など、クライアントでは、rtf 形式をサポートしていないと、トランスポート プロバイダーはプレーン テキストのみを送信できます。 
  
このプロパティが設定されていない場合、既定の動作は、トランスポート プロバイダー、メッセージ転送エージェント (MTA) またはゲートウェイの実装によって決定されます。 アドレス帳プロバイダーは、このプロパティをサポートする必要はありません。 たとえば、密結合のアドレス帳とトランスポート プロバイダーは、TNEF を送信する rtf 形式を使用しない選択できます。 
  
トランスポート プロバイダーを考えないで、クライアントとゲートウェイでは、TNEF を使用して、自分の責任では。 いくつかのトランスポート プロバイダーと TNEF をサポートするゲートウェイは、このプロパティの値に関係なく転送が構築または TRUE に設定されていない場合は、TNEF を送信する他のユーザーを拒否します。 
  
> [!NOTE]
> 受信者ごとの単位では、このプロパティと、その値に基づく意思決定の設定です。 
  
既定では、MAPI は、値を TRUE に設定します。 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)または[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)を呼び出して、プロバイダーを呼び出すクライアントは、 _ulFlags_パラメーターを FALSE にこのプロパティを設定するのには MAPI に**MAPI_SEND_NO_RICH_INFO**ビットを設定できます。 ユーザー インターフェイスによって作成される一時アドレスは、作成するテンプレートで指定された値を使用します。 
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドの呼び出しの名前が解決することはできませんが、インターネット アドレス (SMTP) として解釈できる場合、このプロパティは FALSE に設定します。 インターネット アドレスとして解釈されます、未解決のエントリの表示名は、X@Y の形式である必要があります。Z では、"pete@pinecone.com"などです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクトをインターネット メールの標準的な規則。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagAttachDataObject 標準プロパティ](pidtagattachdataobject-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

