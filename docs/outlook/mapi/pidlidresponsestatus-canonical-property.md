---
title: PidLidResponseStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345760"
---
# <a name="pidlidresponsestatus-canonical-property"></a>PidLidResponseStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
出席者の応答状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidresponsestatus  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008218  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>解説

応答の状態は、次の表に示す値のいずれかである必要があります。
  
|**応答状態**|**値**|**説明**|
|:-----|:-----|:-----|
|[火炎なし]  <br/> |0x00000000  <br/> |このオブジェクトに対する応答は必要ありません。 これは、予定オブジェクトおよび会議の応答オブジェクトに当てはまります。  <br/> |
|開催  <br/> |0x00000001  <br/> |この会議は開催者に帰属します。  <br/> |
|仮承諾  <br/> |0x00000002  <br/> |出席者の会議でこの値を指定すると、出席者が会議出席依頼を仮承諾したことが示されます。  <br/> |
|受付  <br/> |0x00000003  <br/> |出席者が会議出席依頼を承諾したことを出席者の会議 t に表示する値です。  <br/> |
|辞退  <br/> |0x00000004  <br/> |出席者の会議でこの値を指定すると、出席者が会議出席依頼を辞退したことが示されます。  <br/> |
|火炎 not応答  <br/> |0x00000005  <br/> |出席者が会議に応答していないことを示します。 この値は、会議出席依頼、会議の更新、および会議の取り消しに対応しています。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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

