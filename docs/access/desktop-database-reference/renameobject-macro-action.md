---
title: RenameObject マクロ アクション
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306721"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="4f176-102">RenameObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="4f176-102">RenameObject macro action</span></span>

<span data-ttu-id="4f176-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f176-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f176-104">You can use the **RenameObject** action to rename a specified database object.</span><span class="sxs-lookup"><span data-stu-id="4f176-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="4f176-105">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="4f176-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="4f176-106">設定値</span><span class="sxs-lookup"><span data-stu-id="4f176-106">Setting</span></span>

<span data-ttu-id="4f176-107">"RenameObject/オブジェクト名の変更" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4f176-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f176-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="4f176-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4f176-109">説明</span><span class="sxs-lookup"><span data-stu-id="4f176-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f176-110"><strong>New Name/新しい名前</strong></span><span class="sxs-lookup"><span data-stu-id="4f176-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4f176-p101">データベース オブジェクトに付ける新しい名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>新しい名前</strong>] ボックスにオブジェクト名を入力します。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="4f176-p101">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f176-114"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="4f176-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="4f176-p102">名前を変更するオブジェクトの種類を指定します。[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトの名前を変更する場合は、この引数を指定しません。</span><span class="sxs-lookup"><span data-stu-id="4f176-p102">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f176-118"><strong>Old Name/古い名前</strong></span><span class="sxs-lookup"><span data-stu-id="4f176-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4f176-119">名前を変更するオブジェクトの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f176-119">The name of the object to be renamed.</span></span> <span data-ttu-id="4f176-120">[<strong>以前の名前</strong>] ボックスには、<strong>オブジェクトの種類</strong>の引数で選択した種類のデータベースのすべてのオブジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f176-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="4f176-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span><span class="sxs-lookup"><span data-stu-id="4f176-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="4f176-122"><strong>注</strong>: ライブラリデータベースで " <STRONG>Rename/名前の変更</STRONG>" アクションを含むマクロを実行すると、この名前のオブジェクトが、最初にライブラリデータベースで検索され、次にカレントデータベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="4f176-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4f176-123">注釈</span><span class="sxs-lookup"><span data-stu-id="4f176-123">Remarks</span></span>

<span data-ttu-id="4f176-124">データベース オブジェクトの新しい名前は、Access のオブジェクトの名前付け規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f176-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="4f176-125">開いているオブジェクトの名前は変更できません。</span><span class="sxs-lookup"><span data-stu-id="4f176-125">You can't rename an open object.</span></span>

<span data-ttu-id="4f176-p104">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="4f176-p104">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="4f176-p105">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span><span class="sxs-lookup"><span data-stu-id="4f176-p105">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="4f176-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span><span class="sxs-lookup"><span data-stu-id="4f176-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="4f176-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="4f176-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

