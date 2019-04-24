---
title: PidLidIsException 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315450"
---
# <a name="pidlidisexception-canonical-property"></a>PidLidIsException 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
例外 (孤立インスタンスを含む) を表すオブジェクトを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |LID_IS_EXCEPTION  <br/> |
|プロパティセット:  <br/> |PSETID_Meeting  <br/> |
|ロング ID (LID):  <br/> |0x0000000A  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>解説

値が FALSE の場合、定期的なアイテムまたは単一のインスタンスを表すオブジェクトを示します。 任意のオブジェクトに対してこのプロパティが存在しない場合は、TRUE の値を持つ例外埋め込みメッセージを除き、FALSE の値が指定されています。
  
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

