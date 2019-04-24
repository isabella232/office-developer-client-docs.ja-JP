---
title: ISTHEMED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: 図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357513"
---
# <a name="isthemed-function"></a>ISTHEMED 関数

図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **isthemed**()
  
## <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>解説

> [!NOTE]
> visio 2013 の**isthemed**関数は、以前のバージョンの visio の**CELLISTHEMED**関数を置き換えます。 
  
**isthemed**関数を使用すると、テーマの書式の適切な部分を図形に割り当てることができますが、手動で適用した書式設定を使用してテーマの書式設定の他の部分を上書きする機能は保持されます。 後でテーマを再適用すると、手動で書式設定すると、すべてのテーマの書式設定が無効になります。 
  
 図形の [[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md)] セルが 0 より大きい場合、**ISTHEMED** は TRUE と評価されます。 セルが 0 と等しい場合は、**ISTHEMED** は FALSE と評価されます。 documentsheet および PageSheet のテーマは、シェイプシートで使用され**** ている isthemed 関数の値に影響を与えません。 PageSheet で**isthemed**関数が表示されている場合にのみ、ページのテーマに問題があります。 
  
## <a name="example"></a>例

||||
|:-----|:-----|:-----|
|Cell  <br/> |Formula  <br/> |結果  <br/> |
|文字フォント  <br/> |IF (isthemed ()、書式付き eval ()、FONT ("Calibri"))  <br/> |図形に適用されたテーマがある場合、図形のテキストはテーマのフォント書式設定を受け入れます。 図形にテーマが設定されていない場合、図形のテキストには "Calibri" というフォントが適用されます。  <br/> |
|linecolor]  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |図形にテーマが適用されている場合、図形の線の色は赤になります。 図形にテーマが設定されていない場合、図形の線の色は緑になります。  <br/> |
   

