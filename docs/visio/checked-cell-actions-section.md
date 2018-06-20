---
title: '[Checked] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805025"
---
# <a name="checked-cell-actions-section"></a>[Checked] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |チェック マークが表示されます。  <br/> |
|FALSE  <br/> |チェック マークが付いていない (既定値) を表示します。  <br/> |
   
## <a name="remarks"></a>備考

取得するの [Checked] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。オンになっているアクション。 *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Checked] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0、1、2、.  <br/> |
|セル インデックス:  <br/> |**visActionChecked** <br/> |
   

