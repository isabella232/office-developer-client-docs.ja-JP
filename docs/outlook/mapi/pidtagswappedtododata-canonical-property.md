---
title: PidTagSwappedToDoData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359137"
---
# <a name="pidtagswappedtododata-canonical-property"></a>PidTagSwappedToDoData 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Message オブジェクトのフラグ付き状態に影響しないプロパティ値の2番目のセットを保持します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|識別子:  <br/> |0x0e2d  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI ノンノンアウトテーブル  <br/> |
   
## <a name="remarks"></a>解説

第2のフラグの格納場所として機能送信者フラグまたは送信者事前通知がサポートされている場合、この構造では、sender フラグでサポートされている情報フラグ設定プロトコルに関連するすべてのプロパティを格納する場所を提供します。送信者のフラグまたは送信者の事前通知情報をメッセージの受信者に公開せずに、送信者の事前通知でサポートされている、アラーム設定プロトコルに関連するプロパティ。
  
同様に、この構造体には、受信者フラグでサポートされている情報フラグ設定プロトコルに関連するすべてのプロパティと、受信者でサポートされているアラーム設定プロトコルに関連するプロパティが格納される場所があります。以前に送信されたメッセージのアラーム。
  
このプロパティの詳細については、「 [[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)」を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

