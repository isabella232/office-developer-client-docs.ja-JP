---
title: PidTagTransportMessageHeaders 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e37035729c81301c6b43fe40e500a407f4750f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550296"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a>PidTagTransportMessageHeaders 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート固有のメッセージ エンベロープ情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TRANSPORT_MESSAGE_HEADERS、PR_TRANSPORT_MESSAGE_HEADERS_A、PR_TRANSPORT_MESSAGE_HEADERS_W  <br/> |
|識別子:  <br/> |0x007D  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

トランスポート プロバイダーは、受信メッセージのメッセージ ヘッダー情報を生成できます。
  
これらのプロパティは、トランスポート メッセージ ヘッダー情報を破棄するか、メッセージ テキストに事前に保留する代わりに使用できます。 クライアントは、情報を表示するかどうかを選択できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagBody 標準プロパティ](pidtagbody-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

