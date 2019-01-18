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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721060"
---
# <a name="showallrecords-macro-action"></a><span data-ttu-id="b7e6e-102">ShowAllRecords マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b7e6e-102">ShowAllRecords macro action</span></span>


<span data-ttu-id="b7e6e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b7e6e-104">" **ShowAllRecords/全レコードの表示** " アクションを使用すると、作業中のテーブル、クエリの結果セット、またはフォームに適用されているフィルターを解除して、テーブルまたは結果セットのすべてのレコード、またはフォームの基になっているテーブルまたはクエリのすべてのレコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-104">You can use the **ShowAllRecords** action to remove any applied filter from the active table, query result set, or form, and display all records in the table or result set or all records in the form's underlying table or query.</span></span>

## <a name="setting"></a><span data-ttu-id="b7e6e-105">設定</span><span class="sxs-lookup"><span data-stu-id="b7e6e-105">Setting</span></span>

<span data-ttu-id="b7e6e-106">" **ShowAllRecords/全レコードの表示** " アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-106">The **ShowAllRecords** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e6e-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b7e6e-107">Remarks</span></span>

<span data-ttu-id="b7e6e-p101">このアクションを使用すると、テーブル、クエリの結果セット、またはフォームのすべてのレコード (変更されたレコードまたは新しいレコードを含む) が表示されます。このアクションにより、フォームまたはサブフォームに対してレコードの再クエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-p101">You can use this action to ensure that all records (including any changed or new records) are displayed for a table, query result set, or form. This action causes a requery of the records for a form or subform.</span></span>

<span data-ttu-id="b7e6e-110">また、このアクションを使用して、" **ApplyFilter/フィルターの実行** " アクション、[ **ホーム**] タブの [ **フィルター**] コマンド、または " **OpenForm/フォームを開く** " アクションの " **Filter Name/フィルター名** " または " **Where Condition/Where 条件式** " 引数で適用されたフィルターを解除することもできます。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-110">You can also use this action to remove any filter that was applied with the **ApplyFilter** action, the **Filter** command on the **Home** tab, or the **Filter Name** or **Where Condition** argument of the **OpenForm** action.</span></span>

<span data-ttu-id="b7e6e-111">このアクションの動作は、[ **ホーム**] タブの [ **フィルターの切り替え**] をクリックするか、フォーム ビュー、レイアウト ビュー、またはデータシート ビューでフィルターが適用されたフィールドを右クリックして [ **フィルターのクリア**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-111">This action has the same effect as clicking **Toggle Filter** on the **Home** tab, or right-clicking the filtered field and clicking **Clear filter from...** in Form view, Layout view, or Datasheet view.</span></span>

<span data-ttu-id="b7e6e-112">Visual Basic for Applications (VBA) モジュールで " **ShowAllRecords/全レコードの検索** " アクションを実行するには、 **DoCmd** オブジェクトの **ShowAllRecords** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-112">To run the **ShowAllRecords** action in a Visual Basic for Applications (VBA) module, use the **ShowAllRecords** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="b7e6e-113">例</span><span class="sxs-lookup"><span data-stu-id="b7e6e-113">Example</span></span>

<span data-ttu-id="b7e6e-114">**マクロによるフィルターの適用**</span><span class="sxs-lookup"><span data-stu-id="b7e6e-114">**Apply a filter by using a macro**</span></span>

<span data-ttu-id="b7e6e-p102">次のマクロでは、一連のアクションを使用して、"顧客電話帳" フォームの各レコードにフィルターを適用します。このマクロでは、" **ApplyFilter/フィルターの実行** " アクション、" **ShowAllRecords/全レコードの表示** " アクション、および " **GoToControl/コントロールの移動** " アクションの使い方を示します。また、フォームでオプション グループのどのトグル ボタンが選択されたかを判断するための条件の使い方も示します。アクションの各行は、レコードセットを選択するトグル ボタンに関連付けられており、たとえば、ア行、カ行、サ行などから始まるレコードや、すべてのレコードを選択します。このマクロは、[会社名フィルター] オプション グループの " **AfterUpdate/更新後処理** " イベントに設定します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-p102">The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7e6e-120">条件</span><span class="sxs-lookup"><span data-stu-id="b7e6e-120">Condition</span></span></p></th>
<th><p><span data-ttu-id="b7e6e-121">アクション</span><span class="sxs-lookup"><span data-stu-id="b7e6e-121">Action</span></span></p></th>
<th><p><span data-ttu-id="b7e6e-122">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="b7e6e-122">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b7e6e-123">コメント</span><span class="sxs-lookup"><span data-stu-id="b7e6e-123">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7e6e-124">[会社名フィルター] =1</span><span class="sxs-lookup"><span data-stu-id="b7e6e-124">[Company Name Filters] =1</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-125"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="b7e6e-125"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e6e-126"><strong>Where 条件式</strong>: [会社名] と同じように&quot;[AÀÁÂÃÄ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="b7e6e-126"><strong>Where Condition</strong>: [Company Name] Like &quot;[AÀÁÂÃÄ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-127">ア行で始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-127">Filter for company names that start with A, À, Á, Â, Ã, or Ä.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e6e-128">[会社名フィルター] =2</span><span class="sxs-lookup"><span data-stu-id="b7e6e-128">[Company Name Filters] =2</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-129"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="b7e6e-129"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e6e-130"><strong>Where 条件式</strong>: [会社名] と同じように&quot;B \*&quot;</span><span class="sxs-lookup"><span data-stu-id="b7e6e-130"><strong>Where Condition</strong>: [Company Name] Like &quot;B\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-131">カ行またはガ行で始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-131">Filter for company names that start with B.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e6e-132">[会社名フィルター] =3</span><span class="sxs-lookup"><span data-stu-id="b7e6e-132">[Company Name Filters] =3</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-133"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="b7e6e-133"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e6e-134"><strong>Where 条件式</strong>: [会社名] と同じように&quot;[CÇ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="b7e6e-134"><strong>Where Condition</strong>: [Company Name] Like &quot;[CÇ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-135">サ行またはザ行で始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-135">Filter for company names that start with C or Ç.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e6e-136">タ、ダ行からワ行までのアクション行についても、ア行からサ、ザ行までと同じ形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-136">... Action rows for D through Y have the same format as A through C ...</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e6e-137">[会社名フィルター] =26</span><span class="sxs-lookup"><span data-stu-id="b7e6e-137">[Company Name Filters] =26</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-138"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="b7e6e-138"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e6e-139"><strong>Where 条件式</strong>: [会社名] と同じように&quot;[ZÆØÅ] \*&quot;</span><span class="sxs-lookup"><span data-stu-id="b7e6e-139"><strong>Where Condition</strong>: [Company Name] Like &quot;[ZÆØÅ]\*&quot;</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-140">アルファベットで始まる会社名を抽出します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-140">Filter for company names that start with Z, Æ, Ø, or Å.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e6e-141">[会社名フィルター] =27</span><span class="sxs-lookup"><span data-stu-id="b7e6e-141">[Company Name Filters] =27</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-142"><strong>ShowAllRecords</strong></span><span class="sxs-lookup"><span data-stu-id="b7e6e-142"><strong>ShowAllRecords</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b7e6e-143">全レコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-143">Show all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e6e-144">[RecordsetClone] です。[RecordCount]&gt;0</span><span class="sxs-lookup"><span data-stu-id="b7e6e-144">[RecordsetClone].[RecordCount]&gt;0</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-145"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b7e6e-145"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b7e6e-146"><strong>Control Name/コントロール名</strong>: 会社名</span><span class="sxs-lookup"><span data-stu-id="b7e6e-146"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="b7e6e-147">選択した文字で始まるレコードが抽出されたら、[会社名] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="b7e6e-147">If records are returned for the selected letter, move focus to the CompanyName control.</span></span></p></td>
</tr>
</tbody>
</table>

