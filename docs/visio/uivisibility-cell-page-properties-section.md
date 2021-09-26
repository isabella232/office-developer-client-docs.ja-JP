---
title: '[UIVisibility] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
ms.localizationpriority: medium
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
ms.openlocfilehash: 564cb13d5b8e1cf1394787bba1d5bdab82a9c85a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603229"
---
# <a name="uivisibility-cell-page-properties-section"></a>[UIVisibility] セル ([Page Properties] セクション)

ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |UI 内にページ名を表示します (既定値)。  <br/> |**visUIVNormal** <br/> |
|1  <br/> |UI 内にページ名を表示しません。  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>注釈

[UIVisibility] セルを **visUIVHidden** に設定すると、ページ名を含む文字列を表示する UI のどの部分にも、ページが表示されなくなります。 たとえば、[**ドローイング エクスプローラー**] 内、または [ページ] タブ上で、ページがオプションとして表示されなくなります。 ただし、ページ名を含めないオートメーションパスまたは UI パス (印刷コマンドなど) を使用する場合、ページは **引き続きアクセス可能** です。 
  
 このセルは、図面ページ専用であり、校正履歴のオーバレイ ページ用ではありません。既定では [UIVisibility] セルが **visUIVHidden** に設定されますが、この値を変更しないでください。 
  
> [!NOTE]
> ドキュメントの [印刷] コマンドからページを非表示にする場合は、背景ページ **(Type** プロパティは **visTypeBackground)** にし、どのページでも背景として使用されません (背景ページの図形は、背景として使用するページを印刷するときに印刷されます)。 ドキュメントの [印刷] **コマンド** はインデックス付きページでのみ機能し、背景ページはインデックス付けされません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UIVisibility] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |UIVisibility  <br/> |
   
プログラムから、インデックスによって [UIVisibility] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageUIVisibility** <br/> |
   

