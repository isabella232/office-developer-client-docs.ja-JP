---
title: PidTagParentDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 910a62a660ea17992aa391d7453919d9fbb53c86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580433"
---
# <a name="pidtagparentdisplay-canonical-property"></a>PidTagParentDisplay 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
検索時にメッセージがあるフォルダーの表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PARENT_DISPLAY、PR_PARENT_DISPLAY_A、PR_PARENT_DISPLAY_W  <br/> |
|識別子:  <br/> |0x0E05  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、任意のオブジェクトではありません。 のみ検索結果フォルダーの内容の表に表示されることができます。
  
これらのプロパティおよびプロパティの**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) は、互いに関係ありません。 まったく異なるコンテキストに属しているとします。
  
## <a name="related-resources"></a>関連リソース

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

