---
title: '[ButtonFace] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804937"
---
# <a name="buttonface-cell-actions-section"></a>[ButtonFace] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[ButtonFace] セルに含まれる文字列は Microsoft Office のボタン イメージの ID を表します。値ゼロ (0) または空白は、アイコンが表示されないことを示します。 
  
ButtonFace] セルに使用できる Id は、 **CommandBarButton**オブジェクトの**FaceID**プロパティで使用される Id と同じです。 これらの Id の詳細については、MSDN の「コマンド バー ボタンのイメージを使用する」を検索してください。 
  
取得する ButtonFace] セルへの参照の名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |**アクション**です。  *名*です。 **ButtonFace**で**動作**します。  *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 **i** = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionButtonFace** <br/> |
   

