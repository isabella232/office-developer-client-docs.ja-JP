---
title: SaveObject マクロ アクション
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308933"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="cb403-102">SaveObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="cb403-102">SaveObject macro action</span></span>

<span data-ttu-id="cb403-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb403-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb403-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span><span class="sxs-lookup"><span data-stu-id="cb403-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="cb403-106">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="cb403-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="cb403-107">設定値</span><span class="sxs-lookup"><span data-stu-id="cb403-107">Setting</span></span>

<span data-ttu-id="cb403-108">"SaveObject/オブジェクトの保存" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cb403-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb403-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="cb403-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cb403-110">説明</span><span class="sxs-lookup"><span data-stu-id="cb403-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb403-111"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="cb403-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="cb403-p102">The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.  </span><span class="sxs-lookup"><span data-stu-id="cb403-p102">The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb403-116"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="cb403-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cb403-p103">保存するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数を指定せず、この引数も指定しないと、アクティブ オブジェクトが保存されます。この引数に新しい名前を入力すると、アクティブ オブジェクトが入力した名前で保存されます。 新しい名前を入力する場合は、Microsoft Access オブジェクトの名前付け規則に従う必要があります。  </span><span class="sxs-lookup"><span data-stu-id="cb403-p103">The name of the object to be saved. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name. If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cb403-121">注釈</span><span class="sxs-lookup"><span data-stu-id="cb403-121">Remarks</span></span>

<span data-ttu-id="cb403-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span><span class="sxs-lookup"><span data-stu-id="cb403-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="cb403-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span><span class="sxs-lookup"><span data-stu-id="cb403-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="cb403-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span><span class="sxs-lookup"><span data-stu-id="cb403-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="cb403-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span><span class="sxs-lookup"><span data-stu-id="cb403-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="cb403-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span><span class="sxs-lookup"><span data-stu-id="cb403-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="cb403-127">You can't use the **SaveObject** action to save any of the following with a new name:</span><span class="sxs-lookup"><span data-stu-id="cb403-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="cb403-128">フォームビューまたはデータシートビューのフォーム</span><span class="sxs-lookup"><span data-stu-id="cb403-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="cb403-129">印刷プレビューのレポート</span><span class="sxs-lookup"><span data-stu-id="cb403-129">A report in Print Preview</span></span>
> - <span data-ttu-id="cb403-130">モジュール</span><span class="sxs-lookup"><span data-stu-id="cb403-130">A module</span></span>
> - <span data-ttu-id="cb403-131">データシートビューまたは印刷プレビューのサーバービュー</span><span class="sxs-lookup"><span data-stu-id="cb403-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="cb403-132">ページビューでのデータアクセスページ</span><span class="sxs-lookup"><span data-stu-id="cb403-132">A data access page in Page view</span></span>
> - <span data-ttu-id="cb403-133">データシートビューまたは印刷プレビューのテーブル</span><span class="sxs-lookup"><span data-stu-id="cb403-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="cb403-134">データシートビューまたは印刷プレビューのクエリ</span><span class="sxs-lookup"><span data-stu-id="cb403-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="cb403-135">データシートビューまたは印刷プレビューのストアドプロシージャ</span><span class="sxs-lookup"><span data-stu-id="cb403-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="cb403-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span><span class="sxs-lookup"><span data-stu-id="cb403-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="cb403-p106">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span><span class="sxs-lookup"><span data-stu-id="cb403-p106">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="cb403-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="cb403-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

