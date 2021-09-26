---
title: ISTHEMED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: 図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。
ms.openlocfilehash: 56fdbe781f8178bc7a388ff2d0540b8d3f0c1dc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612569"
---
# <a name="isthemed-function"></a>ISTHEMED 関数

図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **ISTHEMED**()
  
## <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>注釈

> [!NOTE]
> 2013 年Visio **ISTHEMED** 関数は、以前のバージョンの **CELLISTHEMED** 関数を置き換Visio。 
  
**ISTHEMED** 関数を使用すると、テーマの書式設定の適切な部分を図形に割り当て、テーマの書式設定の他の部分を手動で適用した書式で上書きする機能を保持できます。 その後テーマを再適用すると、手動で書式設定が上書きされ、図形がテーマのすべての書式設定を受け取る。 
  
 図形の [[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md)] セルが 0 より大きい場合、**ISTHEMED** は TRUE と評価されます。 セルが 0 と等しい場合は、**ISTHEMED** は FALSE と評価されます。 DocumentSheet と PageSheet のテーマは、シェイプシートで使用される **ISTHEMED** 関数の値には影響しません。 **ISTHEMED** 関数が PageSheet に表示される場合にのみ、ページのテーマが重要になります。 
  
## <a name="example"></a>例

||||
|:-----|:-----|:-----|
|Cell  <br/> |式  <br/> |結果  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |図形に適用されたテーマがある場合、図形のテキストはテーマのフォント書式設定を受け入れます。 図形を使用しない場合、図形のテキストは "Calibri" フォントで書式設定されます。  <br/> |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |図形に色を適用している場合、図形の線の色は赤です。 図形を使用しない場合、図形の線の色は緑になります。  <br/> |
   

