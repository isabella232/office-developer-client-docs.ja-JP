---
title: '[ClippingPath] セル ([外部イメージの情報] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: イメージを限定しているパスの図形座標への参照を格納します。
ms.openlocfilehash: 6f65317c014435dd90cb293766e59bd5f1818589
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577984"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>[ClippingPath] セル ([外部イメージの情報] セクション)

イメージを限定しているパスの図形座標への参照を格納します。 
  
## <a name="remarks"></a>注釈

[**ClippingPath**] セルが有効なパスを示している場合、イメージがクリップされるため、イメージはパス内で描画されます。[**ClippingPath**] セルが空か、無効なエントリが格納されている場合は、イメージは、スケール値とオフセット値を使用した角形のクリップで描画されます。  
  
> [!NOTE]
> イメージの ShapeSheet の [[Geometry]](geometry-section.md) セクションで定義されたパスだけが **、ClippingPath** セルの有効なエントリです。 イメージのクリッピング パスの定義に、シート間参照は使用できません。 
  
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
   
## <a name="example"></a>例

次の操作を実行して、イメージの境界図形を楕円に変更できます。
  
- 描画キャンバスに図を挿入します。
    
- 図を右クリックして、[**シェイプシートの表示**] をクリックします。
    
- シェイプシート上を右クリックして、[**Insert Section**] を選択します。
    
- [**セクションの挿入**] ダイアログ ボックスで、[**図形座標**] を選択して [**OK**] をクリックします。
    
- 新しい [Geometry] セクション (例: "Geometry2") で、1 行を含むすべての行を削除します。
    
- 残りの行を右クリックして、[**図形要素の変更**] をクリックします。
    
- [**図形要素の変更**] ダイアログ ボックスで、[**楕円**] を選択して [**OK**] をクリックします。
    
- [外部 **イメージ] セクション** で **、[ClippingPath]** セルの数式を設定し  `="Geometry2.Path"` 、数式を受け入れる。 
    

