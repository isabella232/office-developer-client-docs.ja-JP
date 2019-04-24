---
title: PidLidExceptionReplaceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337983"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a>PidLidExceptionReplaceTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
例外が置換する定期的なパターン内の日付と時刻を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispide xceptionreplacetime  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008228  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

値は協定世界時 (UTC) で指定する必要があります。 このプロパティを使用すると、特定のインスタンスに対して exception attachment オブジェクトを検索できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

