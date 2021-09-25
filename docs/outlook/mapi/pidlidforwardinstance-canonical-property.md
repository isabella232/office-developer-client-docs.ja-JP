---
title: PidLidForwardInstance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e1d9b7f3a87c8c4fbc6614921640eb2cf11acfe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630370"
---
# <a name="pidlidforwardinstance-canonical-property"></a>PidLidForwardInstance 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会議出席依頼が定期的なシリーズの例外を表し、開催者から送信された招待ではなく、(開催者によって転送された場合でも) 転送されたかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidFwrdInstance  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000820A  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値が FALSE の場合は、会議出席依頼が転送されたインスタンスではないかどうかを示します。 このプロパティは必須ではありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

