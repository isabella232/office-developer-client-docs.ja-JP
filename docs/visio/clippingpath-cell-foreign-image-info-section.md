---
title: '[ClippingPath] セル ([外部イメージの情報] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: イメージを限定しているパスの図形座標への参照を格納します。
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805008"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>[ClippingPath] セル ([外部画像情報] セクション)

イメージを限定しているパスの図形座標への参照を格納します。 
  
## <a name="remarks"></a>Remarks

[**ClippingPath**] セルが有効なパスを示している場合、イメージがクリップされるため、イメージはパス内で描画されます。[**ClippingPath**] セルが空か、無効なエントリが格納されている場合は、イメージは、スケール値とオフセット値を使用した角形のクリップで描画されます。  
  
> [!NOTE]
> イメージのシェイプ シートの[[Geometry](geometry-section.md) ] セクションで定義されたパスだけは、 **ClippingPath**セルの有効なエントリです。 シートの相互参照は、画像クリッピングパスを定義するのには使用できません。 
  
別の数式によって、**Cell** エレメントの **N** 属性の値から、または **CellsU** プロパティを使用したプログラムから、名前によって [**ClippingPath**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ClippingPath  <br/> |
   
プログラムから、インデックスによって [**ClippingPath**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>次の使用例では、テーブルからレコードを削除できないようにします。

次の操作を実行して、イメージの境界図形を楕円に変更できます。
  
- 描画キャンバスに図を挿入します。
    
- 図を右クリックして、[**シェイプシートの表示**] をクリックします。
    
- シェイプシート上を右クリックして、[**Insert Section**] を選択します。
    
- [**セクションの挿入**] ダイアログ ボックスで、[**図形座標**] を選択して [**OK**] をクリックします。
    
- 新しいジオメトリ セクション (例:"Geometry2"など) では、1 つを除くすべての行を削除します。
    
- 残りの行を右クリックして、[**図形要素の変更**] をクリックします。
    
- [**図形要素の変更**] ダイアログ ボックスで、[**楕円**] を選択して [**OK**] をクリックします。
    
- **外部イメージ**セクションで、 **ClippingPath**のセルの数式を設定します`="Geometry2.Path"`し、数式を使用します。 
    

