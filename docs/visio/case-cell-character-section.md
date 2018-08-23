---
title: '[Case] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: 図形のテキストでの大文字小文字による区別を指定します。すべて大文字 (1) および先頭文字のみ大文字 (2) を選択した場合、すべてのテキストを大文字で入力すると、テキストの表示状態は変わりません。この 2 つのオプションを有効にするには、テキストを小文字で入力する必要があります。
ms.openlocfilehash: 9acd786b6fa38aec42990f1fd942174367f1135e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804947"
---
# <a name="case-cell-character-section"></a>[Case] セル ([文字] セクション)

図形のテキストでの大文字小文字による区別を指定します。すべて大文字 (1) および先頭文字のみ大文字 (2) を選択した場合、すべてのテキストを大文字で入力すると、テキストの表示状態は変わりません。この 2 つのオプションを有効にするには、テキストを小文字で入力する必要があります。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 通常  <br/> |**visCaseNormal** <br/> |
| 1  <br/> | すべて大文字  <br/> |**visCaseAllCaps** <br/> |
| 2  <br/> | 先頭文字のみ大文字  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Case] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char.Case [ *i* ]、 *i* = < 1 > では、2、3、.  <br/> |
   
プログラムから、インデックスによって [Case] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0、1、2、.  <br/> |
| セル インデックス:  <br/> |**visCharacterCase** <br/> |
   

