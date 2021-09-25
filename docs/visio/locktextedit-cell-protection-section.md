---
title: '[LockTextEdit] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
ms.localizationpriority: medium
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: 図形のテキストをロックして、編集できないようにします。
ms.openlocfilehash: c7bac80327894c17f05d0895849a0a19e2028fde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573944"
---
# <a name="locktextedit-cell-protection-section"></a>[LockTextEdit] セル ([Protection] セクション)

図形のテキストをロックして、編集できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストを編集できません。  <br/> |
| FALSE  <br/> | テキストを編集できます。  <br/> |
   
## <a name="remarks"></a>注釈

ロックされている場合でも、[**テキスト**] ダイアログ ボックスでスタイルを適用することにより、テキストの書式設定を行うことはできます (このダイアログ ボックスを開くには、[**ホーム**] タブで、[**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockTextEdit] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockTextEdit  <br/> |
   
プログラムから、インデックスによって [LockTextEdit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockTextEdit** <br/> |
   

