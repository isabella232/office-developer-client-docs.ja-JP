---
title: PidLidResponseStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 62e25b6cb9635aa6598ff912f717ba27239fd3be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624781"
---
# <a name="pidlidresponsestatus-canonical-property"></a>PidLidResponseStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
出席者の応答状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidResponseStatus  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008218  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

応答の状態は、次の表の値の 1 つである必要があります。
  
|**応答の状態**|**値**|**説明**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |このオブジェクトには応答は必要ありません。 これは、予定オブジェクトと会議の応答オブジェクトの場合です。  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |この会議は開催者に属します。  <br/> |
|respTentative  <br/> |0x00000002  <br/> |出席者の会議のこの値は、出席者が会議出席依頼を暫定的に承諾したと示します。  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |出席者の会議 t のこの値は、出席者が会議出席依頼を承諾したと示します。  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |出席者の会議のこの値は、出席者が会議出席依頼を拒否したかどうかを示します。  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |出席者の会議のこの値は、出席者がまだ応答していない状態を示します。 この値は、会議出席依頼、会議の更新、および会議のキャンセルです。  <br/> |
   
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

