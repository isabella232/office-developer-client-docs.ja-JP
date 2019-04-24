---
title: ShowAllRecords マクロ アクション
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308646"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="fc7f5-102">ShowAllRecords マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="fc7f5-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="fc7f5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc7f5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="fc7f5-104">"**ShowAllRecords/全レコードの表示**" アクションを使用すると、作業中のテーブル、クエリの結果セット、またはフォームに適用されているフィルターを解除して、テーブルまたは結果セットのすべてのレコード、またはフォームの基になっているテーブルまたはクエリのすべてのレコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="fc7f5-105">Setting</span><span class="sxs-lookup"><span data-stu-id="fc7f5-105">Setting</span></span>

<span data-ttu-id="fc7f5-106">"**ShowAllRecords/全レコードの表示**" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7f5-107">注釈</span><span class="sxs-lookup"><span data-stu-id="fc7f5-107">Remarks</span></span>

<span data-ttu-id="fc7f5-p101">このアクションを使用すると、テーブル、クエリの結果セット、またはフォームのすべてのレコード (変更されたレコードまたは新しいレコードを含む) が表示されます。このアクションにより、フォームまたはサブフォームに対してレコードの再クエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-p101">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form. This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="fc7f5-110">また、このアクションを使用して、" **ApplyFilter/フィルターの実行** " アクション、[ **ホーム**] タブの [ **フィルター**] コマンド、または " **OpenForm/フォームを開く** " アクションの " **Filter Name/フィルター名** " または " **Where Condition/Where 条件式** " 引数で適用されたフィルターを解除することもできます。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="fc7f5-111">このアクションの動作は、[ **ホーム**] タブの [ **フィルターの切り替え**] をクリックするか、フォーム ビュー、レイアウト ビュー、またはデータシート ビューでフィルターが適用されたフィールドを右クリックして [ **フィルターのクリア**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="fc7f5-112">Visual Basic for Applications (VBA) モジュールで " **ShowAllRecords/全レコードの検索** " アクションを実行するには、 **DoCmd** オブジェクトの **ShowAllRecords** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="fc7f5-113">例</span><span class="sxs-lookup"><span data-stu-id="fc7f5-113">Example</span></span>

<span data-ttu-id="fc7f5-114">**マクロによるフィルターの適用**</span><span class="sxs-lookup"><span data-stu-id="fc7f5-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="fc7f5-p102">次のマクロでは、一連のアクションを使用して、"顧客電話帳" フォームの各レコードにフィルターを適用します。このマクロでは、" **ApplyFilter/フィルターの実行** " アクション、" **ShowAllRecords/全レコードの表示** " アクション、および " **GoToControl/コントロールの移動** " アクションの使い方を示します。また、フォームでオプション グループのどのトグル ボタンが選択されたかを判断するための条件の使い方も示します。アクションの各行は、レコードセットを選択するトグル ボタンに関連付けられており、たとえば、ア行、カ行、サ行などから始まるレコードや、すべてのレコードを選択します。このマクロは、[会社名フィルター] オプション グループの " **AfterUpdate/更新後処理** " イベントに設定します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc7f5-120">条件</span><span class="sxs-lookup"><span data-stu-id="fc7f5-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="fc7f5-121">アクション</span><span class="sxs-lookup"><span data-stu-id="fc7f5-121">Action</span></span></p></th>
<th><p><span data-ttu-id="fc7f5-122">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="fc7f5-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="fc7f5-123">Comment</span><span class="sxs-lookup"><span data-stu-id="fc7f5-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc7f5-124">[会社名フィルター] =1</span><span class="sxs-lookup"><span data-stu-id="fc7f5-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="fc7f5-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="fc7f5-126"><strong>Where 条件式</strong>: [会社名] &quot;Like [アイウエオ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="fc7f5-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-127">ア行で始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7f5-128">[会社名フィルター] =2</span><span class="sxs-lookup"><span data-stu-id="fc7f5-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="fc7f5-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="fc7f5-130"><strong>Where 条件式</strong>: [会社名] &quot;B のようになります。&quot;</span><span class="sxs-lookup"><span data-stu-id="fc7f5-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-131">カ行またはガ行で始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc7f5-132">[会社名フィルター] =3</span><span class="sxs-lookup"><span data-stu-id="fc7f5-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="fc7f5-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="fc7f5-134"><strong>Where 条件式</strong>: [会社名] &quot;Like [cç] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="fc7f5-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-135">サ行またはザ行で始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7f5-136">タ、ダ行からワ行までのアクション行についても、ア行からサ、ザ行までと同じ形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc7f5-137">[会社名フィルター] =26</span><span class="sxs-lookup"><span data-stu-id="fc7f5-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="fc7f5-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="fc7f5-139"><strong>Where 条件式</strong>: [会社名] &quot;Like [abcdefghijklmnopqrstuvwxyz] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="fc7f5-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-140">アルファベットで始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7f5-141">[会社名フィルター] =27</span><span class="sxs-lookup"><span data-stu-id="fc7f5-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="fc7f5-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fc7f5-143">全レコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc7f5-144">[RecordsetClone]。RecordCount&gt;0</span><span class="sxs-lookup"><span data-stu-id="fc7f5-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="fc7f5-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="fc7f5-146"><strong>Control Name/コントロール名</strong>: 会社名</span><span class="sxs-lookup"><span data-stu-id="fc7f5-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="fc7f5-147">選択した文字で始まるレコードが抽出されたら、[会社名] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc7f5-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

