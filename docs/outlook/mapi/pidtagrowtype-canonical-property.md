---
title: PidTagRowType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6722d02f549979381e20a5179b573c027773e72b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599559"
---
# <a name="pidtagrowtype-canonical-property"></a>PidTagRowType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の行の種類を示す値を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROW_TYPE  <br/> |
|識別子:  <br/> |0x0FF5  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、コンテンツ テーブルにのみ表示されます。 カテゴリは、アイテムがある場合にのみ存在します。
  
このプロパティには、次のいずれかの値を指定できます。
  
TBL_LEAF_ROW 
  
> カテゴリ行ではなく、実際のデータを表します。
    
TBL_EMPTY_CATEGORY 
  
> 現在使用されていない。
    
TBL_EXPANDED_CATEGORY 
  
> カテゴリが展開されます。通常、ユーザー インターフェイスには、マイナス記号 ( - ) が横に表示されます。
    
TBL_COLLAPSED_CATEGORY 
  
> カテゴリは折りたたみ込みです。通常、ユーザー インターフェイスには、プラス記号 (+) が横に表示されます。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> コア テーブル オブジェクトに対して許容される操作が含まれます。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagRowid 標準プロパティ](pidtagrowid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

