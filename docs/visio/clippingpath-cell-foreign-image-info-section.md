---
title: '[ClippingPath] セル ([外部イメージの情報] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: イメージを限定しているパスの図形座標への参照を格納します。
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341861"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>[ClippingPath] セル ([外部イメージの情報] セクション)

イメージを限定しているパスの図形座標への参照を格納します。 
  
## <a name="remarks"></a>解説

[**ClippingPath**] セルが有効なパスを示している場合、イメージがクリップされるため、イメージはパス内で描画されます。 [**ClippingPath**] セルが空か、無効なエントリが格納されている場合は、イメージは、スケール値とオフセット値を使用した角形のクリップで描画されます。 
  
> [!NOTE]
> イメージのシェイプシートの [ [Geometry](geometry-section.md) ] セクションで定義されているパスのみが、 **[clippingpath]** セルの有効なエントリです。 イメージのクリッピング パスの定義に、シート間参照は使用できません。 
  
別の数式によって、**Cell** エレメントの **N** 属性の値から、または **CellsU** プロパティを使用したプログラムから、名前によって [**ClippingPath**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [clippingpath]  <br/> |
   
プログラムから、インデックスによって [**ClippingPath**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>例

次の操作を実行して、イメージの境界図形を楕円に変更できます。
  
- 描画キャンバスに図を挿入します。
    
- 図を右クリックして、[**シェイプシートの表示**] をクリックします。
    
- シェイプシート上を右クリックして、[**Insert Section**] を選択します。
    
- [**セクションの挿入**] ダイアログ ボックスで、[**図形座標**] を選択して [**OK**] をクリックします。
    
- [新しい Geometry] セクション (例: "Geometry2") で、1行を除くすべてを削除します。
    
- 残りの行を右クリックして、[**図形要素の変更**] をクリックします。
    
- [**図形要素の変更**] ダイアログ ボックスで、[**楕円**] を選択して [**OK**] をクリックします。
    
- [**外部イメージ**] セクションで、 **[clippingpath]** セルの数式をに`="Geometry2.Path"`設定して、その数式を確定します。 
    

