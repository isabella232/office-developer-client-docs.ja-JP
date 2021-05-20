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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437309"
---
# <a name="pidtagpstpathhint-canonical-property"></a>PidTagPstPathHint 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構成ダイアログ ボックスに対して、ユーザーが編集できる個人用ストレージ テーブル (.pst ファイル) 名を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PST_PATH_HINT、PR_PST_PATH_HINT_A、PR_PST_PATH_HINT_W  <br/> |
|識別子:  <br/> |0x6771  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |個人用ストレージ テーブル (.pst) 内部  <br/> |
   
## <a name="remarks"></a>注釈

代わりに **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) プロパティを使用すると、構成ダイアログ ボックスが開きますが、ユーザーはパスや他の多くのプロパティを編集できません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]] 
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

