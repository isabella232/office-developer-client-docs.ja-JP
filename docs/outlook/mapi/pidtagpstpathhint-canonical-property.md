---
title: PidTagPstPathHint 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6b71feb6d5967eab3aa490a256825a2803381f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569093"
---
# <a name="pidtagpstpathhint-canonical-property"></a>PidTagPstPathHint 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
構成] ダイアログ ボックスには、ユーザーが編集できる、個人用領域 (.pst ファイル) のテーブル名を提供します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PST_PATH_HINT、PR_PST_PATH_HINT_A、PR_PST_PATH_HINT_W  <br/> |
|識別子:  <br/> |0x6771  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |パーソナル ストレージ表 (.pst) 内部  <br/> |
   
## <a name="remarks"></a>注釈

代わりに**PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) プロパティを使用する場合、[構成] ダイアログ ボックスが開きが、ユーザーは、パスとその他の多くのプロパティを編集するのには使用できません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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

