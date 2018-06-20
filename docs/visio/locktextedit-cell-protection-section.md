---
title: '[LockTextEdit] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: 図形のテキストをロックして、編集できないようにします。
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805776"
---
# <a name="locktextedit-cell-protection-section"></a>[LockTextEdit] セル ([Protection] セクション)

図形のテキストをロックして、編集できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストを編集できません。  <br/> |
| FALSE  <br/> | テキストを編集できます。  <br/> |
   
## <a name="remarks"></a>注釈

テキストの書式設定**テキスト**] ダイアログ ボックスでスタイルを適用することができますもする ([**ホーム**] タブで、[**フォント**の矢印] をクリック) します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockTextEdit] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockTextEdit  <br/> |
   
プログラムから、インデックスによって [LockTextEdit] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockTextEdit** <br/> |
   

