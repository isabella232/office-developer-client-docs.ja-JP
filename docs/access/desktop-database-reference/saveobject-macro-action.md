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
ms.openlocfilehash: 33180aa296fc40c05a3fc50da697aadbf6ada77e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997162"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="75c68-102">SaveObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="75c68-102">SaveObject macro action</span></span>

<span data-ttu-id="75c68-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="75c68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75c68-104">**SaveObject**アクションを使用するには指定されていない場合、指定された Access オブジェクトまたはアクティブなオブジェクトのいずれかを保存します。</span><span class="sxs-lookup"><span data-stu-id="75c68-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="75c68-105">場合によっては (**クイック アクセス ツールバー**の [名前を**付けて**保存] と同じ機能です) に新しい名前を持つアクティブなオブジェクトを保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="75c68-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="75c68-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="75c68-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="75c68-107">設定値</span><span class="sxs-lookup"><span data-stu-id="75c68-107">Setting</span></span>

<span data-ttu-id="75c68-108">**SaveObject**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="75c68-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75c68-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="75c68-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="75c68-110">説明</span><span class="sxs-lookup"><span data-stu-id="75c68-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75c68-111"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="75c68-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="75c68-112">保存するオブジェクトの型。</span><span class="sxs-lookup"><span data-stu-id="75c68-112">The type of object you want to save.</span></span> <span data-ttu-id="75c68-113">[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="75c68-113">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="75c68-114">アクティブなオブジェクトを選択するには、場合は、この引数を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="75c68-114">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="75c68-115">この引数でオブジェクト タイプを選択する場合、<strong>オブジェクト名</strong>の引数で既存のオブジェクトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="75c68-115">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c68-116"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="75c68-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="75c68-p103">保存するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数を指定せず、この引数も指定しないと、アクティブ オブジェクトが保存されます。この引数に新しい名前を入力すると、アクティブ オブジェクトが入力した名前で保存されます。 新しい名前を入力する場合は、Microsoft Access オブジェクトの名前付け規則に従う必要があります。  </span><span class="sxs-lookup"><span data-stu-id="75c68-p103">The name of the object to be saved. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name. If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="75c68-121">解説</span><span class="sxs-lookup"><span data-stu-id="75c68-121">Remarks</span></span>

<span data-ttu-id="75c68-122">**SaveObject**アクションは、保存したりするユーザーが明示的に開くことができるすべてのデータベース オブジェクトに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="75c68-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="75c68-123">指定されたオブジェクトは、オブジェクトには影響を**SaveObject**アクションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="75c68-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="75c68-124">このアクションは、オブジェクトを選択して、**クイック アクセス ツールバー**の**保存**をクリックして保存すると同じ効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="75c68-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> <span data-ttu-id="75c68-125">**オブジェクトの型**引数を指定しないと、[**オブジェクト名**] 引数に新しい名前を入力、**名前を付けて**[**クイック アクセス ツールバー**] をクリックし、アクティブなオブジェクトの新しい名前を入力すると同じ効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="75c68-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="75c68-126">**SaveObject**アクションを使用して保存し、マクロの**名前を付けて保存**コマンドを実行するオブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="75c68-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="75c68-127">**SaveObject**アクションを使用して、次のいずれかを新しい名前で保存できません。</span><span class="sxs-lookup"><span data-stu-id="75c68-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="75c68-128">フォーム ビューまたはデータシート ビューのフォーム</span><span class="sxs-lookup"><span data-stu-id="75c68-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="75c68-129">印刷プレビューでレポート</span><span class="sxs-lookup"><span data-stu-id="75c68-129">A report in Print Preview</span></span>
> - <span data-ttu-id="75c68-130">モジュール</span><span class="sxs-lookup"><span data-stu-id="75c68-130">A module</span></span>
> - <span data-ttu-id="75c68-131">データシート ビューまたは印刷プレビューで、[サーバー] ビュー</span><span class="sxs-lookup"><span data-stu-id="75c68-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="75c68-132">ページ ビューで、データ アクセス ページ</span><span class="sxs-lookup"><span data-stu-id="75c68-132">A data access page in Page view</span></span>
> - <span data-ttu-id="75c68-133">データシート ビューまたは印刷プレビューでテーブル</span><span class="sxs-lookup"><span data-stu-id="75c68-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="75c68-134">クエリ データシート ビューまたは印刷プレビューで</span><span class="sxs-lookup"><span data-stu-id="75c68-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="75c68-135">データシート ビューまたは印刷プレビューでストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="75c68-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="75c68-136">**SaveObject**アクション、またはライブラリ データベースでは、現在のデータベースで実行するマクロで行われたものであるかどうか常に指定したオブジェクトまたはアクティブ オブジェクト データベースに保存される、オブジェクトが作成されました。</span><span class="sxs-lookup"><span data-stu-id="75c68-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="75c68-137">新しい名前を持つアクティブなオブジェクトを保存する名前は、この種類の既存のオブジェクトの名前と同じ場合は、ダイアログ ボックスは、既存のオブジェクトを上書きするかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="75c68-137">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object.</span></span> <span data-ttu-id="75c68-138">**よって**の**警告の**引数を**No**に設定すると、ダイアログ ボックスが表示されていないし、古いオブジェクトが自動的に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="75c68-138">If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="75c68-139">Visual Basic for Applications (VBA) モジュールに**SaveObject**アクションを実行するには、 **DoCmd**オブジェクトの**Save**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="75c68-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

