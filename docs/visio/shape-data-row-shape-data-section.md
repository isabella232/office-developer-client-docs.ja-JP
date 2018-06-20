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
description: 図形に関連付けられている 1 つの図形データ項目の情報が含まれています。 図形には、各図形データ項目の 1 つの図形データ行が含まれています。図形データ行では、[prop.name] 名前が付けられます、次のセルが含まれています。 詳細については、特定のセルを参照してください。
ms.openlocfilehash: 7bf7eafd1869aa3c3ee03efbde30560cdaaeb302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806375"
---
# <a name="shape-data-row-shape-data-section"></a>[Shape Data] 行 ([Shape Data] セクション)

図形に関連付けられている 1 つの図形データ項目の情報が含まれています。 図形には、各図形データ項目の 1 つの図形データ行が含まれています。図形データ行では、[prop.name] 名前が付けられます、次のセルが含まれています。 詳細については、特定のセルを参照してください。
  
|**Cell**|**説明**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスまたはウィンドウに表示されるラベルを指定します。  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |アイテムが選択されている場合、 **[図形データ**] ダイアログ ボックスまたはウィンドウ内のユーザーに表示される説明や手順のテキストを指定します。  <br/> |
|[型](type-cell-shape-data-section.md) <br/> |図形データ項目値のデータ型を指定します。データ型には、文字列 (0)、固定リスト (1)、数値 (2)、ブール演算型 (3)、可変リスト (4)、日付/時刻 (5)、期間 (6)、通貨 (7) があります。  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |図形データ項目の書式を指定します。  <br/> |
|[値](value-cell-shape-data-section.md) <br/> |**[図形データ**] ダイアログ ボックスまたはウィンドウに入力した項目の値が含まれています。  <br/> |
|[[Sortkey]](sortkey-cell-shape-data-section.md) <br/> |[**図形データ**] ダイアログ ボックスの項目をボックスまたはウィンドウが表示されるキーを指定します。  <br/> |
|[非表示](invisible-cell-shape-data-section.md) <br/> |**[図形データ**] ダイアログ ボックスまたはウィンドウで、図形データ項目が表示されているかどうかを指定します。 True の場合は表示されます。表示されている場合は false です。  <br/> |
|[質問](ask-cell-shape-data-section.md) <br/> |インスタンスを作成したときや、図形を複製またはコピーしたときに、図形データ情報の入力をユーザーに求めるかどうかを指定します。  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |図形データ項目の値を表示するための言語を指定します。  <br/> |
|[予定表](calendar-cell-miscellaneous-section.md) <br/> |図形データ項目の [Type] の値が "日付" のときに、使用するカレンダーの種類を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

 多くのプロペラを追加できます。 *名前*の行、行に意味のある名前を割り当てるし、セルの値を設定します。 既存の [Shape Data] セクションに図形データ項目を追加するには、行を右クリックし、ショートカット メニューの [**行の挿入**] をクリックします。 
  
行名を赤いテキストで、[シェイプ シート] ウィンドウに表示されるが、これらのセルを参照できます。 プロペラにわかりやすい名前を割り当てます。*名*の行は、行をクリックし、付けるを作成するたとえば、*価格*名前を入力します。 行名を使用して、[Label] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

