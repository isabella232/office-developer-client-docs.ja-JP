---
title: '[ObjectKind] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: テキスト フィールドの種類を示します。
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438513"
---
# <a name="objectkind-cell-text-fields-section"></a>[ObjectKind] セル ([Text Fields] セクション)

テキスト フィールドの種類を示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | 標準  <br/> |**visTFOKStandard** <br/> |
| 1   <br/> |縦中横  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>注釈

テキスト フィールドは、次のいずれかの種類に該当します。
  
- 標準 : フィールド カテゴリ別に挿入された横書きテキストであることを示すフィールドです。
    
- 縦中横 : 縦書きテキストの内部に設定された横書きテキストであることを示すフィールドです。
    
別の数式または **CellsU** を使用したプログラムから、名前によって [ObjectKind] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Fields. objectkind [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [ObjectKind] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visFieldObjectKind** <br/> |
   

