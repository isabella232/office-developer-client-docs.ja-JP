---
title: PidLidNonSendCcTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383178"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a>PidLidNonSendCcTrackStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**DispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) のプロパティに記載されている各出席者の値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidNonSendCcTrackStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008544  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

**DispidNonSendableCC**プロパティが設定されている場合にのみ、このプロパティが必要です。 このプロパティの値の数は、 **dispidNonSendableCC**内の値の数に等しくなければなりません。 このプロパティでは、各 PT_LONG 値は、同じインデックス位置にある**dispidNonSendableCC**プロパティに出席者に対応します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

