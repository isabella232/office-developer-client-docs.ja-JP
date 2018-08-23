---
title: '[Ask] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: ユーザーが図形のインスタンスを作成したときや、図形を複製またはコピーしたときに、図形データの入力をユーザーに対して問い合わせるかどうかを指定します。
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804770"
---
# <a name="ask-cell-shape-data-section"></a>[Ask] セル ([図形データ] セクション)

ユーザーが図形のインスタンスを作成したときや、図形を複製またはコピーしたときに、図形データの入力をユーザーに対して問い合わせるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |
          [**図形データの定義**] ダイアログ ボックスで図形データを入力するようユーザーに求めます。
  <br/> |
|FALSE  <br/> |
          ユーザーにデータの入力を求めません。
  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**図形データの定義**] ダイアログ ボックスの [**ドロップ時に確認**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、図形を右クリックし、[**データ**] をポイントして、[**図形データの定義**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Ask] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |プロペラです。*名*です。確認して、プロペラします。 *名前*は、カスタム プロパティ行の名前です。  <br/> |
   
プログラムから、インデックスによって [Ask] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionProp** <br/> |
|行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0、1、2、.  <br/> |
|セル インデックス:  <br/> |**visCustPropsAsk** <br/> |
   

