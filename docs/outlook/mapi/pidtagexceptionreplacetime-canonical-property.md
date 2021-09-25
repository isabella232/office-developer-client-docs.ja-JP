---
title: PidTagExceptionReplaceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExceptionReplaceTime
api_type:
- HeaderDef
ms.assetid: bd4d1311-15e4-4275-a967-c6d11d2e48d2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d8e0120969700974bdf387e65cafe5adc5b96783
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563603"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a>PidTagExceptionReplaceTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
繰り返しパターンのインスタンスが例外ではない場合に発生した元の日時を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXCEPTION_REPLACETIME  <br/> |
|識別子:  <br/> |0x7FF9  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |メッセージ クラス定義の送信不可  <br/> |
   
## <a name="remarks"></a>注釈

この値は、協定世界時 (UTC) で指定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
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

