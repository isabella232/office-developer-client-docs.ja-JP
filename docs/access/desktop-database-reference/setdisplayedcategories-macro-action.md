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
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314625"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="b5148-102">SetDisplayedCategories マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b5148-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="b5148-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5148-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5148-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span><span class="sxs-lookup"><span data-stu-id="b5148-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="b5148-106">Setting</span><span class="sxs-lookup"><span data-stu-id="b5148-106">Setting</span></span>

<span data-ttu-id="b5148-107">"SetDisplayedCategories/表示されるカテゴリの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b5148-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5148-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b5148-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b5148-109">説明</span><span class="sxs-lookup"><span data-stu-id="b5148-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5148-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="b5148-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="b5148-111">カテゴリを表示する場合は [<strong>はい</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5148-111">Select <strong>Yes</strong> to show the category or categories.</span></span> <span data-ttu-id="b5148-112">カテゴリを非表示にする場合は [<strong>いいえ</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5148-112">Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5148-113"><strong>カテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="b5148-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="b5148-114">表示または非表示にするカテゴリの名前を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b5148-114">Enter or select the name of the category you want to show or hide.</span></span> <span data-ttu-id="b5148-115">すべてのカテゴリを表示または非表示にする場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="b5148-115">Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b5148-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b5148-116">Remarks</span></span>

  - <span data-ttu-id="b5148-p104">ナビゲーション ウィンドウのタイトル バーに表示される標題は、現在アクティブなフィルター (使用されている場合) を示します。タイトル バーの任意の場所をクリックすると、ドロップダウン リストが表示されます。[ **カテゴリに移動**] の下に、このマクロ アクションが制御する項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b5148-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="b5148-p105">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span><span class="sxs-lookup"><span data-stu-id="b5148-p105">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="b5148-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="b5148-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

