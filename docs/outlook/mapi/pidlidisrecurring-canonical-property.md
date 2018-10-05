---
title: PidLidIsRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390850"
---
# <a name="pidlidisrecurring-canonical-property"></a>PidLidIsRecurring 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトが定期的に関連付けられているかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |LID_IS_RECURRING  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000005  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

TRUE の値は、オブジェクトが一連の定期的なまたは例外 (孤立したインスタンスを含む) のいずれかを表すことを示します。 値 FALSE、または、このプロパティがない場合は、オブジェクトが 1 つのインスタンスを表すことを示します。 このプロパティは、 **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) のプロパティの違いに注意してください。
  
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

