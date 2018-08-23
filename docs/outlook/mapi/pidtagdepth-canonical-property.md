---
title: PidTagDepth 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 100d59a0fd95fcad1976e82aebf6892227c08ec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564914"
---
# <a name="pidtagdepth-canonical-property"></a>PidTagDepth 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
インデント、または階層テーブル内のオブジェクトのレベルの相対レベルを表す整数値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEPTH  <br/> |
|識別子:  <br/> |0x3005  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティでは、内容のテーブル、または階層テーブル内の階層の深さにも行の分類のレベルを指定できます。 深さは、します 0 が一番左のカテゴリを表す、0 から始まる。 すべての場合は、プロパティの値は、絶対値ではなく、相対値を表します。 階層テーブルの深さの値は階層テーブルの取得元となるコンテナーを基準としました。 ルート コンテナーの場合は、深さが絶対の深さを表していません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> テーブルのコア オブジェクトに許容される操作が含まれます。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagObjectType 標準プロパティ](pidtagobjecttype-canonical-property.md)
  
[PidTagSelectable 標準プロパティ](pidtagselectable-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

