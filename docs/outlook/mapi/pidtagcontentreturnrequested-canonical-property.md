---
title: PidTagContentReturnRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentReturnRequested
api_type:
- HeaderDef
ms.assetid: f86f7c59-42ab-4ac0-80fe-c985103e6bd6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c6e3cd64f667298570823832b25e24f9882af6a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583528"
---
# <a name="pidtagcontentreturnrequested-canonical-property"></a>PidTagContentReturnRequested 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを非送信レポートと一緒に返す必要がある場合は TRUE を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_RETURN_REQUESTED  <br/> |
|識別子:  <br/> |0x000A  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |レポート  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが設定されていない場合、MAPI は TRUE 値を持つプロパティとして扱います。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

