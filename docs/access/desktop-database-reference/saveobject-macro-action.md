---
title: "\"SaveObject/オブジェクトの保存\" マクロ アクション"
TOCTitle: SaveObject Macro Action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f5cbb47c8c4b1ecc4990ca53835f8ae9f7ed4d1b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886572"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="7d57d-102">"SaveObject/オブジェクトの保存" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="7d57d-102">SaveObject Macro Action</span></span>


<span data-ttu-id="7d57d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7d57d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d57d-104">**SaveObject**アクションを使用するには指定されていない場合、指定された Access オブジェクトまたはアクティブなオブジェクトのいずれかを保存します。</span><span class="sxs-lookup"><span data-stu-id="7d57d-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="7d57d-105">場合によっては (**クイック アクセス ツールバー**の [名前を**付けて**保存] と同じ機能です) に新しい名前を持つアクティブなオブジェクトを保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d57d-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="7d57d-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d57d-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="7d57d-108">設定値</span><span class="sxs-lookup"><span data-stu-id="7d57d-108">Setting</span></span>

<span data-ttu-id="7d57d-109">**SaveObject**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="7d57d-109">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d57d-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="7d57d-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7d57d-111">説明</span><span class="sxs-lookup"><span data-stu-id="7d57d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d57d-112"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="7d57d-112"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="7d57d-113">保存するオブジェクトの型。</span><span class="sxs-lookup"><span data-stu-id="7d57d-113">The type of object you want to save.</span></span> <span data-ttu-id="7d57d-114">[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d57d-114">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="7d57d-115">アクティブなオブジェクトを選択するには、場合は、この引数を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="7d57d-115">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="7d57d-116">この引数でオブジェクト タイプを選択する場合、<strong>オブジェクト名</strong>の引数で既存のオブジェクトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d57d-116">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d57d-117"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="7d57d-117"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7d57d-p104">保存するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数を指定せず、この引数も指定しないと、アクティブ オブジェクトが保存されます。この引数に新しい名前を入力すると、アクティブ オブジェクトが入力した名前で保存されます。 新しい名前を入力する場合は、Microsoft Access オブジェクトの名前付け規則に従う必要があります。  </span><span class="sxs-lookup"><span data-stu-id="7d57d-p104">The name of the object to be saved. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name. If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7d57d-122">解説</span><span class="sxs-lookup"><span data-stu-id="7d57d-122">Remarks</span></span>

<span data-ttu-id="7d57d-123">**SaveObject**アクションは、保存したりするユーザーが明示的に開くことができるすべてのデータベース オブジェクトに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="7d57d-123">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="7d57d-124">指定されたオブジェクトは、オブジェクトには影響を**SaveObject**アクションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d57d-124">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="7d57d-125">このアクションは、オブジェクトを選択して、**クイック アクセス ツールバー**の**保存**をクリックして保存すると同じ効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="7d57d-125">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> <span data-ttu-id="7d57d-126">**オブジェクトの型**引数を指定しないと、[**オブジェクト名**] 引数に新しい名前を入力、**名前を付けて**[**クイック アクセス ツールバー**] をクリックし、アクティブなオブジェクトの新しい名前を入力すると同じ効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="7d57d-126">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="7d57d-127">**SaveObject**アクションを使用して保存し、マクロの**名前を付けて保存**コマンドを実行するオブジェクトを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7d57d-127">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7d57d-128"><STRONG>SaveObject</STRONG>アクションを使用して、次のいずれかを新しい名前で保存できません。</span><span class="sxs-lookup"><span data-stu-id="7d57d-128">You can't use the <STRONG>SaveObject</STRONG> action to save any of the following with a new name:</span></span></P>



  - <span data-ttu-id="7d57d-129">フォーム ビューまたはデータシート ビューで開いたフォーム</span><span class="sxs-lookup"><span data-stu-id="7d57d-129">A form in Form view or Datasheet view.</span></span>

  - <span data-ttu-id="7d57d-130">印刷プレビューで開いたレポート</span><span class="sxs-lookup"><span data-stu-id="7d57d-130">A report in Print Preview.</span></span>

  - <span data-ttu-id="7d57d-131">モジュール</span><span class="sxs-lookup"><span data-stu-id="7d57d-131">A module.</span></span>

  - <span data-ttu-id="7d57d-132">データシート ビューまたは印刷プレビューで開いたサーバー ビュー</span><span class="sxs-lookup"><span data-stu-id="7d57d-132">A server view in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="7d57d-133">ページ ビューで開いたデータ アクセス ページ</span><span class="sxs-lookup"><span data-stu-id="7d57d-133">A data access page in Page view.</span></span>

  - <span data-ttu-id="7d57d-134">データシート ビューまたは印刷プレビューで開いたテーブル</span><span class="sxs-lookup"><span data-stu-id="7d57d-134">A table in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="7d57d-135">データシート ビューまたは印刷プレビューで開いたクエリ</span><span class="sxs-lookup"><span data-stu-id="7d57d-135">A query in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="7d57d-136">データシート ビューまたは印刷プレビューで開いたストアド プロシージャ</span><span class="sxs-lookup"><span data-stu-id="7d57d-136">A stored procedure in Datasheet view or Print Preview.</span></span>

<span data-ttu-id="7d57d-137">**SaveObject**アクション、またはライブラリ データベースでは、現在のデータベースで実行するマクロで行われたものであるかどうか常に指定したオブジェクトまたはアクティブ オブジェクト データベースに保存される、オブジェクトが作成されました。</span><span class="sxs-lookup"><span data-stu-id="7d57d-137">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="7d57d-138">新しい名前を持つアクティブなオブジェクトを保存する名前は、この種類の既存のオブジェクトの名前と同じ場合は、ダイアログ ボックスは、既存のオブジェクトを上書きするかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d57d-138">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object.</span></span> <span data-ttu-id="7d57d-139">**よって**の**警告の**引数を**No**に設定すると、ダイアログ ボックスが表示されていないし、古いオブジェクトが自動的に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7d57d-139">If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="7d57d-140">Visual Basic for Applications (VBA) モジュールに**SaveObject**アクションを実行するには、 **DoCmd**オブジェクトの**Save**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d57d-140">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

