---
title: PidTagParentDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9d71c3e62148ac47b51985510ab45fd605fbdb6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555224"
---
# <a name="pidtagparentdisplay-canonical-property"></a>PidTagParentDisplay 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索中にメッセージが見つかったフォルダーの表示名を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PARENT_DISPLAY、PR_PARENT_DISPLAY_A、PR_PARENT_DISPLAY_W  <br/> |
|識別子:  <br/> |0x0E05  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、どのオブジェクトにも含めではありません。 検索結果フォルダーのコンテンツ テーブルにのみ表示できます。
  
これらのプロパティと **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) プロパティは、互いに関連付けではありません。 これらは、完全に異なるコンテキストに属します。
  
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

