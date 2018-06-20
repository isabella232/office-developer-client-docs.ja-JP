---
title: '[Disabled] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: 図面ウィンドウに、アクション タグを表示するかどうかを示します。
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805226"
---
# <a name="disabled-cell-action-tags-section"></a>[Disabled] セル ([Action Tags] セクション)

図面ウィンドウに、アクション タグを表示するかどうかを示します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | アクション タグは無効です。  <br/> |
| FALSE  <br/> | アクション タグは有効です (既定値)。  <br/> |
   
## <a name="remarks"></a>備考

アクション タグを無効にすると、有効にするまで表示されません。 
  
取得する、[Disabled] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。無効になっているスマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Disabled] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagDisabled** <br/> |
   

