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
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437330"
---
# <a name="uivisibility-cell-page-properties-section"></a>[UIVisibility] セル ([Page Properties] セクション)

ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |UI 内にページ名を表示します (既定値)。  <br/> |**visUIVNormal** <br/> |
|1   <br/> |UI 内にページ名を表示しません。  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>注釈

[UIVisibility] セルを **visUIVHidden** に設定すると、ページ名を含む文字列を表示する UI のどの部分にも、ページが表示されなくなります。 たとえば、[**ドローイング エクスプローラー**] 内、または [ページ] タブ上で、ページがオプションとして表示されなくなります。 ただし、ページ名を含まないオートメーションまたは UI パス (たとえば、[**印刷**] コマンド) を使用する場合は、ページにアクセスできます。 
  
 このセルは、図面ページ専用であり、校正履歴のオーバレイ ページ用ではありません。既定では [UIVisibility] セルが **visUIVHidden** に設定されますが、この値を変更しないでください。 
  
> [!NOTE]
> ページをドキュメントの**印刷**コマンドから非表示にするには、背景ページ (**Type**プロパティは**visTypeBackground** ) を使用して、どのページでも使用されていない (背景ページ上の図形を背景として使用するページで印刷する)印刷されます)。 ドキュメントの [**印刷**] コマンドはインデックスが作成されたページでのみ動作し、背景ページにインデックスは作成されません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UIVisibility] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[uivisibility]  <br/> |
   
プログラムから、インデックスによって [UIVisibility] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**vispageuivisibility** <br/> |
   

