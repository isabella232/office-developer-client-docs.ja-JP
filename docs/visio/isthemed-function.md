---
title: ISTHEMED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: 図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805646"
---
# <a name="isthemed-function"></a>ISTHEMED 関数

図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。 
  
## <a name="version-information"></a>バージョン情報

Visio 2013 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

 **ISTHEMED**()
  
## <a name="return-value"></a>�߂�l

ブール型
  
## <a name="remarks"></a>Remarks

> [!NOTE]
> Visio 2013 には、 **ISTHEMED**関数は、Visio の以前のバージョンから**CELLISTHEMED**関数を置き換えます。 
  
**ISTHEMED**はテーマの書式設定の適切な部分を図形に割り当てることで機能しますが、テーマの書式を手動で適用される書式の他の部分を上書きする機能を保持します。 後でテーマを再適用する場合手動で書式設定がオーバーライドされ、図形にはテーマの書式設定のすべて。 
  
 **ISTHEMED**は、図形内の[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md)セルが 0 より大きい場合は TRUE に評価されます。 このセルが 0 の場合は、 **ISTHEMED**を評価し、false を指定します。 DocumentSheet と PageSheet のテーマは、シェイプ シートで使用する**ISTHEMED**関数の値に影響はありません。 **ISTHEMED**関数が表示される場合にのみ、PageSheet はページのテーマだけにします。 
  
## <a name="example"></a>次の使用例では、テーブルからレコードを削除できないようにします。

||||
|:-----|:-----|:-----|
|セル  <br/> |Formula  <br/> |結果  <br/> |
|Char.Font  <br/> |IF(ISTHEMED()、THEMEVAL()、FONT("Calibri"))  <br/> |図形にテーマを適用する場合、図形のテキストは、テーマのフォントを受け入れます。 図形がテーマではない場合は、「Calibri」フォントを使用して図形のテキストが書式設定されます。  <br/> |
|線の色  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |図形にテーマを適用する場合、図形の線の色は赤色です。 図形がテーマではない場合は、図形の線の色は緑です。  <br/> |
   

