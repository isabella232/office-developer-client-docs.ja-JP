---
title: If...Then...Else マクロ ブロック
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: fe8336d95a0982379621a7dd798113fbf882499c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562637"
---
# <a name="ifthenelse-macro-block"></a>If...Then...Else マクロ ブロック


**適用先**: Access 2013、Office 2013

式の値に応じた条件に基づいてアクションのグループを実行するには、If マクロ ブロックを使用します。

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

**If** および **Else If** の両方に次の引数が必要です。

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
<td><p>テストする条件です。True または False のいずれかに評価できる式でなければなりません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈


            **If** マクロブロックを選択すると、テキストボックスが表示され、テストする条件を示す式を入力することができます。さらにコンボ ボックスが表示され、マクロ アクションを入力できます。その下に、"End If" というテキストが自動的に表示されます。If と End If が囲む領域の中で、一連のアクション (ブロック) を指定します。入力した式が真である場合にのみ、そのブロックが実行されます。

1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。

If ブロックには **Else If** ブロックをいくつでも追加できます。

オプションの **Else** ブロックを挿入するには、 **Add Else** をクリックします。この場合、 **Else** の下に挿入したアクションが **Else** ブロックを形成します。このブロックは、これより上にあるアクションが実行されない場合にのみ実行されます。 **If** ブロックには 1 つの **Else** ブロックのみを追加できます。

次のコード例では、1 つ目のブロックのマクロ アクションは、\[[Status]\] の値が 0 より大きい場合に実行されます。\[[Status\] の値が 0 より大きくない場合は、**Else If** に続く式が評価されます。 **Else If** ブロックのマクロ アクションは、\[[状態]\] の値が 0 の場合に実行されます。最後に、1 つ目のブロックも 2 つ目のブロックも実行されない場合、 **Else** ブロックのアクションが実行されます。

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

**if** ブロックを入れ子にすることができます。最初の式が True のときに 2 番目の式を評価する場合は、**If** ブロックを **If** ブロック内に入れ子にすることを検討してください。次のコード例では、内部 **If** ブロックは、\[状態\] の値が 0 *を超え、* 100 より大きい場合にのみ実行されます。

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
