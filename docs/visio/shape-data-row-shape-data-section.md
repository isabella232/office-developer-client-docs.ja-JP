---
title: '[Shape Data] 行 ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
ms.localizationpriority: medium
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: 図形に関連付けられた、単一の図形データ項目の情報を格納します。図形には、各図形データ項目に対して 1 つの [Shape Data] 行があります。[Shape Data] 行の名前は Prop.name で、次のセルが含まれます。詳細については、各セルに関連する項目を参照してください。
ms.openlocfilehash: d488c181912f924a49ed7a42bf0e25a66fa16b7d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559571"
---
# <a name="shape-data-row-shape-data-section"></a>[Shape Data] 行 ([Shape Data] セクション)

図形に関連付けられた、単一の図形データ項目の情報を格納します。図形には、各図形データ項目に対して 1 つの [Shape Data] 行があります。[Shape Data] 行の名前は Prop.name で、次のセルが含まれます。詳細については、各セルに関連する項目を参照してください。
  
|**Cell**|**Description**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに表示されるラベルを指定します。  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |項目を選択したときに [**図形データ**] ダイアログ ボックスまたはウィンドウに表示される説明または手順を示すテキストを指定します。  <br/> |
|[種類](type-cell-shape-data-section.md) <br/> |図形データ項目値のデータ型を指定します。データ型には、文字列 (0)、固定リスト (1)、数値 (2)、ブール演算型 (3)、可変リスト (4)、日付/時刻 (5)、期間 (6)、通貨 (7) があります。  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |図形データ項目の書式を指定します。  <br/> |
|[値](value-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに入力した項目の値が格納されています。  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウの項目を一覧表示する場合に使用するキーを指定します。  <br/> |
|[非表示](invisible-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに、図形データ項目を表示するかどうかを指定します。TRUE = 非表示、FALSE = 表示 を示します。<br/> |
|[Ask](ask-cell-shape-data-section.md) <br/> |インスタンスを作成したときや、図形を複製またはコピーしたときに、図形データ情報の入力をユーザーに求めるかどうかを指定します。  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |図形データ項目の値を表示するための言語を指定します。  <br/> |
|[Calendar](calendar-cell-miscellaneous-section.md) <br/> |図形データ項目の [Type] の値が "日付" のときに、使用するカレンダーの種類を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

 Prop を追加できます。  *必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。 既存の [Shape Data] セクションに図形データ項目を追加するには、行を右クリックして、ショートカット メニューの [**行の挿入**] をクリックします。 
  
これらのセルは行名で参照できます。これは、赤いテキストの ShapeSheet ウィンドウに表示されます。 Prop.name rows *にわかりやすい*  名前を割り当てるには、行をクリックし、  *たとえば*  Price などの名前を入力して、Prop.Price という行名を作成します。 その後、Prop.Price.Label を使用して [ラベル] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

