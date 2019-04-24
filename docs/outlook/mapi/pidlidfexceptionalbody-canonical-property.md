---
title: PidLidFExceptionalBody 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327462"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a>PidLidFExceptionalBody 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
例外の埋め込みメッセージオブジェクトに、定期的な予定表オブジェクトとは異なる本文があることを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidfexceptionalbody  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008206  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値が TRUE の場合、例外の埋め込みメッセージオブジェクトには本文が必要です。 このプロパティの値が FALSE の場合、またはプロパティが存在しない場合は、クライアントまたはサーバーは、定期的な予定表オブジェクトから本文を取得する必要があります。
  
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

