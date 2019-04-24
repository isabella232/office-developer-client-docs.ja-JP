---
title: '[Shape Data] 行 ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
localization_priority: Normal
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: 図形に関連付けられた1つの図形データ項目に関する情報を格納します。 図形には、図形データ項目ごとに1つの図形データ行が含まれています。図形データ行には Prop.name という名前が付けられ、次のセルが含まれています。 詳細については、各セルに関連する項目を参照してください。
ms.openlocfilehash: 058f8f180a2eca4736d06dfcc533d81f45150c86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326216"
---
# <a name="shape-data-row-shape-data-section"></a>[Shape Data] 行 ([Shape Data] セクション)

図形に関連付けられた1つの図形データ項目に関する情報を格納します。 図形には、図形データ項目ごとに1つの図形データ行が含まれています。図形データ行には Prop.name という名前が付けられ、次のセルが含まれています。 詳細については、各セルに関連する項目を参照してください。
  
|**Cell**|**Description**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに表示されるラベルを指定します。  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |項目を選択したときに [**図形データ**] ダイアログ ボックスまたはウィンドウに表示される説明または手順を示すテキストを指定します。  <br/> |
|[Type](type-cell-shape-data-section.md) <br/> |図形データ項目値のデータ型を指定します。データ型には、文字列 (0)、固定リスト (1)、数値 (2)、ブール演算型 (3)、可変リスト (4)、日付/時刻 (5)、期間 (6)、通貨 (7) があります。  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |図形データ項目の書式を指定します。  <br/> |
|[値](value-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに入力した項目の値が格納されています。  <br/> |
|[[sortkey]](sortkey-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウの項目を一覧表示する場合に使用するキーを指定します。  <br/> |
|[可視](invisible-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに、図形データ項目を表示するかどうかを指定します。 TRUE = 非表示、FALSE = 表示 を示します。  <br/> |
|[依頼](ask-cell-shape-data-section.md) <br/> |インスタンスを作成したときや、図形を複製またはコピーしたときに、図形データ情報の入力をユーザーに求めるかどうかを指定します。  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |図形データ項目の値を表示するための言語を指定します。  <br/> |
|[Calendar](calendar-cell-miscellaneous-section.md) <br/> |図形データ項目の [Type] の値が "日付" のときに、使用するカレンダーの種類を指定します。  <br/> |
   
## <a name="remarks"></a>解説

 任意の数の Prop を追加できます。 必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。 既存の [Shape Data] セクションに図形データ項目を追加するには、行を右クリックして、ショートカット メニューの [**行の挿入**] をクリックします。 
  
これらのセルを行名で参照できます。これは、シェイプシートウィンドウに赤いテキストで表示されます。 わかりやすい名前を Prop に割り当てることができます。行の*名前*を入力し、[*価格*] などの名前を入力します。たとえば、行名 Prop を作成します。 その後、[ラベル] セルを参照するには、"Prop." というラベルを使用します。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

