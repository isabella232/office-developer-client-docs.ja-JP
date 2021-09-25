---
title: PidTagSwappedToDoData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b63e12eb69aff565d3d4ef99b66a5ad364b7cc08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578936"
---
# <a name="pidtagswappedtododata-canonical-property"></a>PidTagSwappedToDoData 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Message オブジェクトのフラグ付き状態に影響しないプロパティ値の 2 番目のセットを保持します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|識別子:  <br/> |0x0E2D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

送信者フラグまたは送信者アラームがサポートされている場合、セカンダリ フラグの保存場所として機能するこの構造は、送信者フラグでサポートされている情報フラグ プロトコルに関連するすべてのプロパティ、および送信者のアラームでサポートされているアラーム 設定 プロトコルに関連するすべてのプロパティを、送信者フラグまたは送信者アラーム情報をメッセージの受信者に公開せずに保存する場所を提供します。
  
同様に、この構造は、以前に送信されたメッセージの受信者アラームでサポートされているリマインダー 設定 プロトコルに関連する受信者フラグとプロパティでサポートされている Informational Flagging Protocol に関連するすべてのプロパティを格納する場所を提供します。
  
このプロパティの詳細については [、「[MS-OXOFLAG] 」を参照してください](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

