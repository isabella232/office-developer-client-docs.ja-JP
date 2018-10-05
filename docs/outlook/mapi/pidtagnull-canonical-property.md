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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400797"
---
# <a name="pidtagnull-canonical-property"></a>PidTagNull 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配列の領域を予約または、null 値またはプロパティの設定を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NULL  <br/> |
|識別子:  <br/> |0x0000  <br/> |
|データの種類 :   <br/> |PT_NULL  <br/> |
|エリア:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>備考

[SPropValue](spropvalue.md)構造体の配列の領域を予約するのにはこのプロパティを使用します。 **SPropValue**構造体の返される配列内の領域を予約する方法を指示する[SPropTagArray](sproptagarray.md)構造体の配列で使用されます。 安価な方法で設定されるプロパティを計算できます。 
  
詳細については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許可されている操作のプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

