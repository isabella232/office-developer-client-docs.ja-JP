---
title: '[UIVisibility] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806742"
---
# <a name="uivisibility-cell-page-properties-section"></a>[UIVisibility] セル ([Page Properties] セクション)

ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |UI 内にページ名を表示します (既定値)。  <br/> |**visUIVNormal** <br/> |
|1  <br/> |UI 内にページ名を表示しません。  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>備考

UIVisibility セルを**visUIVHidden**に設定すると、ページでページ名を含む文字列が表示される UI の任意の場所に表示できなくなります。 などのページが、**ドローイング エクスプ ローラー]** または [ページ] タブのオプションとして表示はされません。 ページのアクセスは可能ただし、ページ名、たとえば、 **[印刷**] コマンドが含まれていないオートメーションまたは UI パスを使用する場合。 
  
 このセルは、ドキュメントのページを使用UIVisibility のセルを**visUIVHidden**にデフォルトで設定しているマークアップ オーバーレイのページで使用するためのものではありませんし、変更しないようにします。 
  
> [!NOTE]
> ドキュメントの**印刷**] コマンドを非表示に使用すれば、背景ページ (**Type**プロパティは、 **visTypeBackground** ) で任意のページ (ページは印刷時に背景として使用するページは、背景上の図形の背景として使用されていません。印刷)。 ドキュメントの **[印刷**] コマンドは、インデックス付きのページでのみ機能し、背景ページのインデックスは作成されません。 
  
取得する、[UIVisibility] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |UIVisibility  <br/> |
   
プログラムから、インデックスによって [UIVisibility] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageUIVisibility** <br/> |
   

