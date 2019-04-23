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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288603"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="72ab5-102">NavigateTo マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="72ab5-102">NavigateTo macro action</span></span>

<span data-ttu-id="72ab5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="72ab5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72ab5-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span><span class="sxs-lookup"><span data-stu-id="72ab5-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="72ab5-106">Setting</span><span class="sxs-lookup"><span data-stu-id="72ab5-106">Setting</span></span>

<span data-ttu-id="72ab5-107">"NavigateTo/移動先" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="72ab5-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72ab5-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="72ab5-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="72ab5-109">説明</span><span class="sxs-lookup"><span data-stu-id="72ab5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72ab5-110"><strong>カテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="72ab5-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="72ab5-p102">必ず指定します。ナビゲーション ウィンドウにオブジェクトを表示する際に使用するカテゴリを指定します。[<strong>カテゴリ</strong>] ボックスで [<strong>オブジェクトの種類</strong>]、[<strong>テーブルとビュー</strong>]、[<strong>更新日</strong>]、[<strong>作成日</strong>]、または [<strong>ユーザー設定</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ab5-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72ab5-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="72ab5-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="72ab5-115">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="72ab5-115">Optional.</span></span> <span data-ttu-id="72ab5-116">"Group/グループ" 引数は、ナビゲーション ウィンドウ内のカテゴリに表示されるオブジェクトを制限します。</span><span class="sxs-lookup"><span data-stu-id="72ab5-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="72ab5-117">引数<strong>Group</strong>を省略すると、引数<strong>Category</strong>に指定した条件によって分類されたすべてのデータベースオブジェクトがナビゲーションウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="72ab5-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="72ab5-118">次の表は、さまざまな "Category/カテゴリ" 引数で使用できる有効な "Group/グループ" 引数の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="72ab5-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="72ab5-119">注釈</span><span class="sxs-lookup"><span data-stu-id="72ab5-119">Remarks</span></span>

- <span data-ttu-id="72ab5-120">このアクションの動作は、ナビゲーションウィンドウのタイトルバーからカテゴリとグループを選択した場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="72ab5-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="72ab5-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span><span class="sxs-lookup"><span data-stu-id="72ab5-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="72ab5-123">引数 Category</span><span class="sxs-lookup"><span data-stu-id="72ab5-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="72ab5-124">"Group/グループ" 引数の例</span><span class="sxs-lookup"><span data-stu-id="72ab5-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="72ab5-125">オブジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="72ab5-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="72ab5-126">テーブル、フォーム、クエリ、ページ、マクロ、モジュール</span><span class="sxs-lookup"><span data-stu-id="72ab5-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="72ab5-127">テーブルとビュー</span><span class="sxs-lookup"><span data-stu-id="72ab5-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="72ab5-128">データベース内の特定のテーブルの名前</span><span class="sxs-lookup"><span data-stu-id="72ab5-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="72ab5-129">更新日</span><span class="sxs-lookup"><span data-stu-id="72ab5-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="72ab5-130">今日、昨日、先月、先月よりも前の日付</span><span class="sxs-lookup"><span data-stu-id="72ab5-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="72ab5-131">作成日</span><span class="sxs-lookup"><span data-stu-id="72ab5-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="72ab5-132">今日、昨日、先月、先月よりも前の日付</span><span class="sxs-lookup"><span data-stu-id="72ab5-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="72ab5-133">ユーザー設定のカテゴリ</span><span class="sxs-lookup"><span data-stu-id="72ab5-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="72ab5-134">指定したユーザー設定のカテゴリに対応する作成済みグループの名前</span><span class="sxs-lookup"><span data-stu-id="72ab5-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="72ab5-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="72ab5-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="72ab5-p105">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span><span class="sxs-lookup"><span data-stu-id="72ab5-p105">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


