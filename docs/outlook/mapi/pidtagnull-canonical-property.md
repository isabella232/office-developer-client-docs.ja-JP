---
title: PidTagNull 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329268"
---
# <a name="pidtagnull-canonical-property"></a>PidTagNull 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティの null 値または設定を表す、または配列スペースを予約します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NULL  <br/> |
|識別子:  <br/> |0x0000  <br/> |
|データの種類 :   <br/> |PT_NULL  <br/> |
|エリア:  <br/> |共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、SPropValue](spropvalue.md) 構造体の配列内の領域を予約するために使用されます。 [SPropTagArray](sproptagarray.md)構造体の配列で使用して、返される **SPropValue** 構造体の配列にスペースを予約するメソッドを指定します。 これにより、計算されたプロパティを安価な方法で入力できます。 
  
詳細については、「MAPI プロパティの [種類の概要」を参照してください](mapi-property-type-overview.md)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

