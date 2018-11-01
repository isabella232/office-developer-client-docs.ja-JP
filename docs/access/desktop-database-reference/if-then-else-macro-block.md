---
title: If...Then...Else マクロ ブロック
TOCTitle: If...Then...Else Macro Block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7c6842e8463250f6575cfc85364ec3bff7aba1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876044"
---
# <a name="ifthenelse-macro-block"></a>If...Then...Else マクロ ブロック


**適用されます**Access 2013、Office 2013。

式の値に応じた条件に基づいてアクションのグループを実行するには、 **If** マクロ ブロックを使用します。

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a>設定

**場合**との両方に**一致しない場合**、次の引数が必要です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Expression</strong></p></td>
<td><p>テストする条件です。True または False に評価される式を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

**If** マクロ ブロックを選択するとテキスト ボックスが表示されるので、そこにテストする条件を表す式を入力します。さらに、マクロ アクションを挿入できるコンボ ボックスも表示されます。マクロ アクションの下に、"End If" というテキストが自動的に表示されます。If と End If は、アクションのグループ (ブロック) を入力できる領域を囲みます。ブロックは、入力した式が True の場合にのみ実行されます。

1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。

If ブロックには、任意の数の **Else If** ブロックを追加できます。

オプションの **Else** ブロックを挿入するには、 **Add Else** をクリックします。この場合、 **Else** の下に挿入したアクションが **Else** ブロックを形成します。このブロックは、これより上にあるアクションが実行されない場合にのみ実行されます。 **If** ブロックには 1 つの **Else** ブロックのみを追加できます。

場合に次のコード例では、最初のブロックのマクロ アクションの実行の値\[ステータス\]が 0 より大きい。 場合の値\[ステータス\]が 0 より大きい、**それ以外の場合**式が評価されます。 **Else If**ブロック内のマクロ アクションが実行される場合の値\[ステータス\]が 0 です。 最後に、1 つ目のブロックも 2 つ目のブロックも実行されない場合、 **Else** ブロックのアクションが実行されます。

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

**場合**のブロックを入れ子にすることができます。 最初の式が True の場合に、2 番目の式を評価する場合は、 **If**ブロック内の**If**ブロックを入れ子にする必要があります。 コード例を次に、内側のブロックの**場合**にのみする際に実行の値\[ステータス\]が両方とも 0*と*100 を超える値を超える。

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
