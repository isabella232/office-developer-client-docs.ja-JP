---
title: PidTagRecipientProposed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e00f121bf52f2c6fcbe797fb8f6126584444411
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580692"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>PidTagRecipientProposed 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
会議の出席者が反応したかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|識別子:  <br/> |0x5FE1  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |トランスポートにおける受取人  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、出席者が新しい日時を提案することを示します。 値の false の場合、または、このプロパティがない場合は、まだ応答して、参加者がいないか、出席者からの最新の応答は、新しい日付を含める/時間の提案でしたいないを意味します。 この値を TRUE にすることはできません定期的な一連の出席者のために。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

