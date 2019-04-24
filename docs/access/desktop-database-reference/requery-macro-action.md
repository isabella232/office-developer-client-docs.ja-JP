---
title: Requery マクロ アクション
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8b90af8d1cda073ffa37022bb5db5e8cf8e3b978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306707"
---
# <a name="requery-macro-action"></a><span data-ttu-id="dad4b-102">Requery マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="dad4b-102">Requery macro action</span></span>

<span data-ttu-id="dad4b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="dad4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dad4b-p101">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.</span><span class="sxs-lookup"><span data-stu-id="dad4b-p101">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="dad4b-107">Setting</span><span class="sxs-lookup"><span data-stu-id="dad4b-107">Setting</span></span>

<span data-ttu-id="dad4b-108">"Requery/再クエリ" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dad4b-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dad4b-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="dad4b-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dad4b-110">説明</span><span class="sxs-lookup"><span data-stu-id="dad4b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dad4b-111"><strong>Control Name/コントロール名</strong></span><span class="sxs-lookup"><span data-stu-id="dad4b-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dad4b-112">更新するコントロールの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="dad4b-112">The name of the control you want to update.</span></span> <span data-ttu-id="dad4b-113">[マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>コントロール名</strong>] ボックスに、コントロール名を入力します。</span><span class="sxs-lookup"><span data-stu-id="dad4b-113">Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="dad4b-114">完全修飾識別子ではなく、コントロールの名前のみを使用する必要があります ( <strong>Forms</strong>! など)。<em>formname</em>!<em>controlname</em>)</span><span class="sxs-lookup"><span data-stu-id="dad4b-114">You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>).</span></span> <span data-ttu-id="dad4b-115">アクティブオブジェクトのソースを再クエリするには、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="dad4b-115">Leave this argument blank to requery the source of the active object.</span></span> <span data-ttu-id="dad4b-116">アクティブオブジェクトがデータシートまたはクエリの結果セットの場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="dad4b-116">If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dad4b-117">注釈</span><span class="sxs-lookup"><span data-stu-id="dad4b-117">Remarks</span></span>

<span data-ttu-id="dad4b-118">"Requery/再クエリ" アクションは、次のいずれかの処理を行います。</span><span class="sxs-lookup"><span data-stu-id="dad4b-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="dad4b-119">指定したコントロールやオブジェクトの基になるクエリの再実行。</span><span class="sxs-lookup"><span data-stu-id="dad4b-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="dad4b-120">コントロールやオブジェクトの基になるテーブルで追加、変更、または削除されたレコードの反映。</span><span class="sxs-lookup"><span data-stu-id="dad4b-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="dad4b-121">The **Requery** action does not affect the position of the record pointer.</span><span class="sxs-lookup"><span data-stu-id="dad4b-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="dad4b-122">クエリやテーブルに基づくコントロールには次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="dad4b-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="dad4b-123">リスト ボックスとコンボ ボックス。</span><span class="sxs-lookup"><span data-stu-id="dad4b-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="dad4b-124">サブフォーム コントロール。</span><span class="sxs-lookup"><span data-stu-id="dad4b-124">Subform controls.</span></span>

- <span data-ttu-id="dad4b-125">グラフなどの OLE オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="dad4b-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="dad4b-126">**DSum** などの定義域集計関数が含まれるコントロール。</span><span class="sxs-lookup"><span data-stu-id="dad4b-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="dad4b-127">指定されたコントロールがクエリまたはテーブルに基づいていない場合、このアクションによってコントロールの再計算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="dad4b-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="dad4b-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span><span class="sxs-lookup"><span data-stu-id="dad4b-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="dad4b-p104">The **Requery** action requeries the source of the control or object. In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records. The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span><span class="sxs-lookup"><span data-stu-id="dad4b-p104">The **Requery** action requeries the source of the control or object. In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records. The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="dad4b-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="dad4b-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="dad4b-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span><span class="sxs-lookup"><span data-stu-id="dad4b-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="dad4b-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span><span class="sxs-lookup"><span data-stu-id="dad4b-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="dad4b-136">ActiveX データオブジェクト (ADO) **requery**メソッドは、Access **requery**メソッドと同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="dad4b-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

