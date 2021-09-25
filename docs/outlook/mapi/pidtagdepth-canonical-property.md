---
title: PidTagDepth 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: af1d9746677308834f3758d9f5ab8da7e50cb769
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563673"
---
# <a name="pidtagdepth-canonical-property"></a>PidTagDepth 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
階層テーブル内のオブジェクトのインデントまたは深度の相対レベルを表す整数を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEPTH  <br/> |
|識別子:  <br/> |0x3005  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティでは、コンテンツ テーブル内の行の分類レベル、または階層テーブルの階層深度を指定することもできます。 深度は 0 から始め、0 は左端のカテゴリを表します。 すべての場合、プロパティ値は絶対値ではなく相対値を表します。 たとえば、階層テーブルの深度値は、階層テーブルが取得されたコンテナーを基準にしています。 深度は、ルート コンテナーからの絶対深度を表すのではありません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> コア テーブル オブジェクトに対して許容される操作が含まれます。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagObjectType 標準プロパティ](pidtagobjecttype-canonical-property.md)
  
[PidTagSelectable 標準プロパティ](pidtagselectable-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

