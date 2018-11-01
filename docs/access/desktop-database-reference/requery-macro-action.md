---
title: "'Requery/再クエリ' マクロ アクション"
TOCTitle: Requery Macro Action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e8e5a25b8770f3542fade53d206ff20400ebf350
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885942"
---
# <a name="requery-macro-action"></a><span data-ttu-id="44fad-102">"Requery/再クエリ" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="44fad-102">Requery Macro Action</span></span>


<span data-ttu-id="44fad-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="44fad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44fad-104">**アクション**を使用すると、コントロールのソースを再クエリ アクティブ オブジェクトの指定されたコントロール内のデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="44fad-104">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control.</span></span> <span data-ttu-id="44fad-105">コントロールを指定しない場合は、オブジェクト自体のソースを再クエリします。</span><span class="sxs-lookup"><span data-stu-id="44fad-105">If no control is specified, this action requeries the source of the object itself.</span></span> <span data-ttu-id="44fad-106">アクティブ オブジェクトやそのコントロールの表示データを最新のものにするには、このアクションを使います。</span><span class="sxs-lookup"><span data-stu-id="44fad-106">Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="44fad-107">設定値</span><span class="sxs-lookup"><span data-stu-id="44fad-107">Setting</span></span>

<span data-ttu-id="44fad-108">**アクション**には、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="44fad-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44fad-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="44fad-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="44fad-110">説明</span><span class="sxs-lookup"><span data-stu-id="44fad-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44fad-111"><strong>コントロール名</strong></span><span class="sxs-lookup"><span data-stu-id="44fad-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="44fad-112">更新するコントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="44fad-112">The name of the control you want to update.</span></span> <span data-ttu-id="44fad-113">[マクロ ビルダー] ウィンドウの [<strong>コントロール名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションで、コントロールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="44fad-113">Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="44fad-114">完全修飾識別子ではなく、コントロールの名前だけを使用する必要があります (<strong>フォーム</strong>!<em>formname</em>!<em>controlname</em>)。</span><span class="sxs-lookup"><span data-stu-id="44fad-114">You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>).</span></span> <span data-ttu-id="44fad-115">この引数はアクティブ オブジェクトのソースを再クエリするのには空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="44fad-115">Leave this argument blank to requery the source of the active object.</span></span> <span data-ttu-id="44fad-116">アクティブ オブジェクトがデータシートまたはクエリの結果のかどうか、設定する必要がありますこの引数を指定しません。</span><span class="sxs-lookup"><span data-stu-id="44fad-116">If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="44fad-117">解説</span><span class="sxs-lookup"><span data-stu-id="44fad-117">Remarks</span></span>

<span data-ttu-id="44fad-118">**再クエリ**アクションは、次のいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="44fad-118">The **Requery** action does one of the following:</span></span>

  - <span data-ttu-id="44fad-119">指定したコントロールやオブジェクトの基になるクエリの再実行。</span><span class="sxs-lookup"><span data-stu-id="44fad-119">Reruns the query on which the control or object is based.</span></span>

  - <span data-ttu-id="44fad-120">コントロールやオブジェクトの基になるテーブルで追加、変更、または削除されたレコードの反映。</span><span class="sxs-lookup"><span data-stu-id="44fad-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>


> [!NOTE]
> <P><span data-ttu-id="44fad-121"><STRONG>再クエリ</STRONG>アクションは、レコード ポインターの位置には影響しません。</span><span class="sxs-lookup"><span data-stu-id="44fad-121">The <STRONG>Requery</STRONG> action does not affect the position of the record pointer.</span></span></P>



<span data-ttu-id="44fad-122">クエリやテーブルに基づくコントロールには次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="44fad-122">Controls based on a query or table include:</span></span>

  - <span data-ttu-id="44fad-123">リスト ボックスとコンボ ボックス。</span><span class="sxs-lookup"><span data-stu-id="44fad-123">List boxes and combo boxes.</span></span>

  - <span data-ttu-id="44fad-124">サブフォーム コントロール。</span><span class="sxs-lookup"><span data-stu-id="44fad-124">Subform controls.</span></span>

  - <span data-ttu-id="44fad-125">グラフなどの OLE オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="44fad-125">OLE objects, such as charts.</span></span>

  - <span data-ttu-id="44fad-126">**DSum** などの定義域集計関数が含まれるコントロール。</span><span class="sxs-lookup"><span data-stu-id="44fad-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="44fad-127">指定されたコントロールがクエリまたはテーブルに基づいていない場合、このアクションによってコントロールの再計算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="44fad-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="44fad-p103">"Control Name/コントロール名" 引数を指定しない場合、"Requery/再クエリ" アクションの動作は、オブジェクトにフォーカスがあるときに Shift キーを押しながら F9 キーを押した場合と同じです。サブフォーム コントロールにフォーカスがある場合は、そのサブフォームのソースのみが再クエリされます (この動作も、Shift キーを押しながら F9 キーを押した場合と同じです)。</span><span class="sxs-lookup"><span data-stu-id="44fad-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>


> [!NOTE]
> <P><span data-ttu-id="44fad-130">コントロールやオブジェクトのソースを再<STRONG>クエリを再実行</STRONG>します。</span><span class="sxs-lookup"><span data-stu-id="44fad-130">The <STRONG>Requery</STRONG> action requeries the source of the control or object.</span></span> <span data-ttu-id="44fad-131">対照的に、 <STRONG>RepaintObject</STRONG>アクションは、指定したオブジェクト内のコントロールを再描画がしないデータベースの再クエリを実行または新しいレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="44fad-131">In contrast, the <STRONG>RepaintObject</STRONG> action repaints controls in the specified object but doesn't requery the database or display new records.</span></span> <span data-ttu-id="44fad-132"><STRONG>解除</STRONG>だけでなく、アクティブなオブジェクトを再クエリが、<STRONG>アクション</STRONG>の操作を行いますが、適用されたフィルターが削除されます。</span><span class="sxs-lookup"><span data-stu-id="44fad-132">The <STRONG>ShowAllRecords</STRONG> action not only requeries the active object, but it also removes any applied filters, which the <STRONG>Requery</STRONG> action doesn't do.</span></span></P>



<span data-ttu-id="44fad-133">アクティブ オブジェクトにないコントロールを再クエリする場合は、**アクション**または**DoCmd**オブジェクトの対応する、 **Requery**メソッドではない、(VBA) モジュールの Visual Basic for Applications の**Requery**メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44fad-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="44fad-134">**Requery**メソッドを VBA では、**アクション**または**DoCmd.Requery**メソッドよりも高速です。</span><span class="sxs-lookup"><span data-stu-id="44fad-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="44fad-135">さらに、**アクション**または**DoCmd.Requery**メソッドを使用すると、Microsoft Access クエリを閉じるし、データベースから再読み込みしていますが、アクセスが終了して、再読み込みすることがなくクエリを再度実行、 **Requery**メソッドを使用する場合。</span><span class="sxs-lookup"><span data-stu-id="44fad-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="44fad-136">ActiveX データ オブジェクト (ADO) の**Requery**メソッドが、Access の**Requery**メソッドと同じように動作する注意してください。</span><span class="sxs-lookup"><span data-stu-id="44fad-136">Note that the ActiveX Data Object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

