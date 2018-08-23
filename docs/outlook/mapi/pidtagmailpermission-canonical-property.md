---
title: PidTagMailPermission 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571193"
---
# <a name="pidtagmailpermission-canonical-property"></a>PidTagMailPermission 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージングのユーザーがメッセージを送信する許可されている場合 TRUE が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MAIL_PERMISSION  <br/> |
|識別子:  <br/> |0x3A0E  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが設定されていない MAPI により真の価値を持つものとして扱います。 
  
一部のエントリがいない、メールが有効な企業のディレクトリに false を指定するには、このプロパティを設定します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

