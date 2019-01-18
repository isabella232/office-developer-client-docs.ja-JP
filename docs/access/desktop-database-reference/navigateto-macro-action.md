---
title: NavigateTo マクロ アクション
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704141"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="2f6e9-102">NavigateTo マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2f6e9-102">NavigateTo macro action</span></span>

<span data-ttu-id="2f6e9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f6e9-104">**移動**操作を使用するには、ナビゲーション ウィンドウでデータベース オブジェクトの表示を制御します。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-104">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane.</span></span> <span data-ttu-id="2f6e9-105">たとえば、データベース オブジェクトの分類方法を変更したり、フィルターを適用して特定のデータベース オブジェクトだけを表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-105">For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="2f6e9-106">設定値</span><span class="sxs-lookup"><span data-stu-id="2f6e9-106">Setting</span></span>

<span data-ttu-id="2f6e9-107">**移動**操作では、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f6e9-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="2f6e9-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2f6e9-109">説明</span><span class="sxs-lookup"><span data-stu-id="2f6e9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f6e9-110"><strong>カテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="2f6e9-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="2f6e9-p102">必ず指定します。ナビゲーション ウィンドウにオブジェクトを表示する際に使用するカテゴリを指定します。[<strong>カテゴリ</strong>] ボックスで [<strong>オブジェクトの種類</strong>]、[<strong>テーブルとビュー</strong>]、[<strong>更新日</strong>]、[<strong>作成日</strong>]、または [<strong>ユーザー設定</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f6e9-114"><strong>グループ</strong></span><span class="sxs-lookup"><span data-stu-id="2f6e9-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="2f6e9-115">省略可能。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-115">Optional.</span></span> <span data-ttu-id="2f6e9-116">カテゴリ内のオブジェクト、<strong>グループ</strong>引数の制限は、ナビゲーション ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="2f6e9-117">引数<strong>Group</strong>を空白のままにする場合、ナビゲーション ウィンドウには、引数<strong>Category</strong>で指定した条件によって分類されるすべてのデータベース オブジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="2f6e9-118">さまざまな<strong>カテゴリ</strong>の引数の有効な<strong>グループ</strong>の引数の例としては、次の表に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2f6e9-119">注釈</span><span class="sxs-lookup"><span data-stu-id="2f6e9-119">Remarks</span></span>

- <span data-ttu-id="2f6e9-120">このアクションは、ナビゲーション ウィンドウのタイトル バーからカテゴリとグループを選択することに似ています。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="2f6e9-121">**グループ**の有効な引数は、どの**カテゴリ**の引数の使用によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-121">Valid **Group** arguments depend on which **Category** argument is used.</span></span> <span data-ttu-id="2f6e9-122">**グループ**の無効な引数を入力すると、エラー メッセージが表示されます。次の表には、各**カテゴリ**の引数に有効な**グループ**の引数の例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-122">If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="2f6e9-123">引数 Category</span><span class="sxs-lookup"><span data-stu-id="2f6e9-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="2f6e9-124">"Group/グループ" 引数の例</span><span class="sxs-lookup"><span data-stu-id="2f6e9-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="2f6e9-125">オブジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="2f6e9-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="2f6e9-126">テーブル、フォーム、クエリ、ページ、マクロ、モジュール</span><span class="sxs-lookup"><span data-stu-id="2f6e9-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="2f6e9-127">テーブルとビュー</span><span class="sxs-lookup"><span data-stu-id="2f6e9-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="2f6e9-128">データベース内の特定のテーブルの名前</span><span class="sxs-lookup"><span data-stu-id="2f6e9-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="2f6e9-129">更新日</span><span class="sxs-lookup"><span data-stu-id="2f6e9-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="2f6e9-130">今日、昨日、先月、先月よりも前の日付</span><span class="sxs-lookup"><span data-stu-id="2f6e9-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="2f6e9-131">作成日</span><span class="sxs-lookup"><span data-stu-id="2f6e9-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="2f6e9-132">今日、昨日、先月、先月よりも前の日付</span><span class="sxs-lookup"><span data-stu-id="2f6e9-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="2f6e9-133">ユーザー設定のカテゴリ</span><span class="sxs-lookup"><span data-stu-id="2f6e9-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="2f6e9-134">指定したユーザー設定のカテゴリに対応する作成済みグループの名前</span><span class="sxs-lookup"><span data-stu-id="2f6e9-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="2f6e9-135">VBA モジュールでは、**移動**操作を実行するには、 **DoCmd**オブジェクトの**NavigateTo**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="2f6e9-136">(**すべてのテーブル**、**すべての Access オブジェクト**、または**すべての日付**など) のカテゴリの最上位レベルに移動するにする必要があります、グループ引数を指定しません。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-136">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank.</span></span> <span data-ttu-id="2f6e9-137">などの引数**Category** **オブジェクトの種類**がある場合は、エラー**グループ**引数の結果として**すべての Access オブジェクト**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e9-137">For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


