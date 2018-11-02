---
title: If...Then...Else マクロ ブロック
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c671ced7d3de2ce461af3bcf0a5d832e092bbf17
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922938"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="21f65-102">If...Then...Else マクロ ブロック</span><span class="sxs-lookup"><span data-stu-id="21f65-102">If...Then...Else macro block</span></span>


<span data-ttu-id="21f65-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="21f65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21f65-104">式の値に応じた条件に基づいてアクションのグループを実行するには、 **If** マクロ ブロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="21f65-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="21f65-105">設定</span><span class="sxs-lookup"><span data-stu-id="21f65-105">Setting</span></span>

<span data-ttu-id="21f65-106">**場合**との両方に**一致しない場合**、次の引数が必要です。</span><span class="sxs-lookup"><span data-stu-id="21f65-106">For both **If** and **Else If**, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21f65-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="21f65-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="21f65-108">説明</span><span class="sxs-lookup"><span data-stu-id="21f65-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21f65-109"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="21f65-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="21f65-p101">テストする条件です。True または False に評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="21f65-p101">The condition that you wish to test. It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="21f65-112">備考</span><span class="sxs-lookup"><span data-stu-id="21f65-112">Remarks</span></span>

<span data-ttu-id="21f65-p102">**If** マクロ ブロックを選択するとテキスト ボックスが表示されるので、そこにテストする条件を表す式を入力します。さらに、マクロ アクションを挿入できるコンボ ボックスも表示されます。マクロ アクションの下に、"End If" というテキストが自動的に表示されます。If と End If は、アクションのグループ (ブロック) を入力できる領域を囲みます。ブロックは、入力した式が True の場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="21f65-p102">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="21f65-p103">1 つ目の式が False だった場合に別の式を評価するには、 **Add Else If** をクリックし、オプションの **Else If** ブロックを挿入します。True または False として評価される式を入力する必要があります。1 つ目の式が False で、この式が True の場合のみ、ブロックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="21f65-p103">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="21f65-120">If ブロックには、任意の数の **Else If** ブロックを追加できます。</span><span class="sxs-lookup"><span data-stu-id="21f65-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="21f65-p104">オプションの **Else** ブロックを挿入するには、 **Add Else** をクリックします。この場合、 **Else** の下に挿入したアクションが **Else** ブロックを形成します。このブロックは、これより上にあるアクションが実行されない場合にのみ実行されます。 **If** ブロックには 1 つの **Else** ブロックのみを追加できます。</span><span class="sxs-lookup"><span data-stu-id="21f65-p104">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="21f65-124">場合に次のコード例では、最初のブロックのマクロ アクションの実行の値\[ステータス\]が 0 より大きい。</span><span class="sxs-lookup"><span data-stu-id="21f65-124">In the following code example, the macro actions in the first block execute if the value of \[Status\] is greater than 0.</span></span> <span data-ttu-id="21f65-125">場合の値\[ステータス\]が 0 より大きい、**それ以外の場合**式が評価されます。</span><span class="sxs-lookup"><span data-stu-id="21f65-125">If the value of \[Status\] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="21f65-126">**Else If**ブロック内のマクロ アクションが実行される場合の値\[ステータス\]が 0 です。</span><span class="sxs-lookup"><span data-stu-id="21f65-126">The macro actions in the **Else If** block execute if the value of \[Status\] is equal to 0.</span></span> <span data-ttu-id="21f65-127">最後に、1 つ目のブロックも 2 つ目のブロックも実行されない場合、 **Else** ブロックのアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="21f65-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="21f65-128">**場合**のブロックを入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="21f65-128">You can nest **If** blocks.</span></span> <span data-ttu-id="21f65-129">最初の式が True の場合に、2 番目の式を評価する場合は、 **If**ブロック内の**If**ブロックを入れ子にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="21f65-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="21f65-130">コード例を次に、内側のブロックの**場合**にのみする際に実行の値\[ステータス\]が両方とも 0*と*100 を超える値を超える。</span><span class="sxs-lookup"><span data-stu-id="21f65-130">In the following code example, the inner **If** block only executes when the value of \[Status\] is both greater than 0 *and* greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
