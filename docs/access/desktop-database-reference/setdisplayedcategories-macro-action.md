---
title: SetDisplayedCategories マクロ アクション
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 985630f65508f7fca37de24f93649c8cf6047180
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920320"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="8e5de-102">SetDisplayedCategories マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="8e5de-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="8e5de-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8e5de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e5de-104">**SetDisplayedCategories**アクションを使用すると、カテゴリ**のカテゴリに移動**] の下のナビゲーション ウィンドウのタイトル バーに表示を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e5de-104">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane.</span></span> <span data-ttu-id="8e5de-105">などのオブジェクトは**作成日**順が表示されるように、ナビゲーション ウィンドウを切り替えられないようにする場合は、タイトル バーのドロップダウン リスト内のオプションを非表示にする、このアクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e5de-105">For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="8e5de-106">設定値</span><span class="sxs-lookup"><span data-stu-id="8e5de-106">Setting</span></span>

<span data-ttu-id="8e5de-107">**SetDisplayedCategories**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="8e5de-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e5de-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="8e5de-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8e5de-109">説明</span><span class="sxs-lookup"><span data-stu-id="8e5de-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e5de-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="8e5de-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5de-p102">カテゴリを表示する場合は [<strong>はい</strong>] を選択します。カテゴリを非表示にする場合は [<strong>いいえ</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e5de-p102">Select <strong>Yes</strong> to show the category or categories. Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e5de-113"><strong>カテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="8e5de-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="8e5de-p103">表示または非表示にするカテゴリの名前を入力または選択します。すべてのカテゴリを表示または非表示にする場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="8e5de-p103">Enter or select the name of the category you want to show or hide. Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8e5de-116">解説</span><span class="sxs-lookup"><span data-stu-id="8e5de-116">Remarks</span></span>

  - <span data-ttu-id="8e5de-p104">ナビゲーション ウィンドウのタイトル バーに表示される標題は、現在アクティブなフィルター (使用されている場合) を示します。タイトル バーの任意の場所をクリックすると、ドロップダウン リストが表示されます。[ **カテゴリに移動**] の下に、このマクロ アクションが制御する項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e5de-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="8e5de-120">のみこの操作を有効またはカテゴリは、指定したカテゴリの表示を無効になります。任意のナビゲーション ウィンドウの表示の切り替えを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="8e5de-120">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display.</span></span> <span data-ttu-id="8e5de-121">などのオブジェクトは**作成日**順に表示している**SetDisplayedCategories**アクションを使用して、[**作成日**] オプションを無効にする場合は、アクセス、ナビゲーション ウィンドウに切り替わらない別のカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="8e5de-121">For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="8e5de-122">**SetDisplayedCategories**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**SetDisplayedCategories**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8e5de-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

