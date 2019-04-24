---
title: PrintOut マクロ アクション
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301408"
---
# <a name="printout-macro-action"></a><span data-ttu-id="45527-102">PrintOut マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="45527-102">PrintOut macro action</span></span>

<span data-ttu-id="45527-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="45527-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45527-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span><span class="sxs-lookup"><span data-stu-id="45527-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="45527-106">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="45527-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="45527-107">設定値</span><span class="sxs-lookup"><span data-stu-id="45527-107">Setting</span></span>

<span data-ttu-id="45527-108">"PrintOut/印刷" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="45527-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45527-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="45527-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="45527-110">説明</span><span class="sxs-lookup"><span data-stu-id="45527-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45527-111"><strong>Print Range/印刷範囲</strong></span><span class="sxs-lookup"><span data-stu-id="45527-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="45527-p102">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.  </span><span class="sxs-lookup"><span data-stu-id="45527-p102">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45527-115"><strong>Page From/開始ページ</strong></span><span class="sxs-lookup"><span data-stu-id="45527-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="45527-p103">印刷する最初のページを指定します。このページの先頭から印刷が開始されます。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="45527-p103">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45527-119"><strong>Page To/終了ページ</strong></span><span class="sxs-lookup"><span data-stu-id="45527-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="45527-p104">印刷する最後のページを指定します。このページの最後で印刷が終了します。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="45527-p104">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45527-123"><strong>Print Quality/印刷品質</strong></span><span class="sxs-lookup"><span data-stu-id="45527-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="45527-p105">印刷の品質を指定します。[ <strong>高</strong>]、[ <strong>中</strong>]、[ <strong>低</strong>]、[ <strong>簡易</strong>] のいずれかをクリックします。印刷の品質が低いほど、速く印刷されます。既定値は [ <strong>高</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="45527-p105">The print quality. Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>. The lower the quality, the faster the object prints. The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45527-128"><strong>Copies/部数</strong></span><span class="sxs-lookup"><span data-stu-id="45527-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="45527-p106">印刷部数を指定します。既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="45527-p106">The number of copies to print. The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45527-131"><strong>Collate Copies/部単位で印刷</strong></span><span class="sxs-lookup"><span data-stu-id="45527-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="45527-p107">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.  </span><span class="sxs-lookup"><span data-stu-id="45527-p107">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="45527-135">注釈</span><span class="sxs-lookup"><span data-stu-id="45527-135">Remarks</span></span>

<span data-ttu-id="45527-p108">このアクションの動作は、オブジェクトを選択し、[ **ファイル**] タブをクリックして、[ **印刷**] をクリックした場合と同じです。ただし、このアクションを使用する場合は、[ **印刷**] ダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="45527-p108">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="45527-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span><span class="sxs-lookup"><span data-stu-id="45527-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="45527-p109">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span><span class="sxs-lookup"><span data-stu-id="45527-p109">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="45527-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="45527-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

