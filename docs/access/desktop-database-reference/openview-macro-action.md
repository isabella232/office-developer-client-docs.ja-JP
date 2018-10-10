---
title: "'OpenView/ビューを開く' マクロ アクション"
TOCTitle: OpenView Macro Action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ad607f852f5af21bc2979bd635286b86d18489a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477467"
---
# <a name="openview-macro-action"></a><span data-ttu-id="6cea9-102">"OpenView/ビューを開く" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="6cea9-102">OpenView Macro Action</span></span>


<span data-ttu-id="6cea9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cea9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6cea9-104">Access プロジェクトで、 **OpenView**アクションをデータシート ビュー、デザイン ビュー、または印刷プレビューでビューを開くに使用できます。</span><span class="sxs-lookup"><span data-stu-id="6cea9-104">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="6cea9-105">データシート ビューで開いた場合、その名前のビューが実行されます。</span><span class="sxs-lookup"><span data-stu-id="6cea9-105">This action runs the named view when opened in Datasheet view.</span></span> <span data-ttu-id="6cea9-106">ビューを開くときのデータ入力モードの設定を行ったり、ビューで表示するレコードを制限したりできます。</span><span class="sxs-lookup"><span data-stu-id="6cea9-106">You can select data entry for the view and restrict the records that the view displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6cea9-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cea9-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="6cea9-109">設定値</span><span class="sxs-lookup"><span data-stu-id="6cea9-109">Setting</span></span>

<span data-ttu-id="6cea9-110">**OpenView**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="6cea9-110">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cea9-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="6cea9-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6cea9-112">説明</span><span class="sxs-lookup"><span data-stu-id="6cea9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cea9-113"><strong>View Name/ビュー名</strong></span><span class="sxs-lookup"><span data-stu-id="6cea9-113"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6cea9-114">開くビューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cea9-114">The name of the view to open.</span></span> <span data-ttu-id="6cea9-115">マクロ ビルダー] ウィンドウの [<strong>ビュー名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベース内のすべてのビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="6cea9-115">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="6cea9-116">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="6cea9-116">This is a required argument.</span></span> <span data-ttu-id="6cea9-117">ライブラリ データベースで、 <strong>OpenView</strong>アクションを含むマクロを実行する場合は、最初の検索にライブラリ データベースで、し、[現在のデータベース内にこの名前のビューです。</span><span class="sxs-lookup"><span data-stu-id="6cea9-117">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cea9-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="6cea9-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="6cea9-p104">ビューを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="6cea9-p104">The view in which the view will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cea9-122"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="6cea9-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6cea9-p105">ビューを開くときのデータ入力モードを指定します。これはデータシート  ビューで開いているビューにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="6cea9-p105">The data entry mode for the view. This applies only to views opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6cea9-127">解説</span><span class="sxs-lookup"><span data-stu-id="6cea9-127">Remarks</span></span>

<span data-ttu-id="6cea9-128">このアクションの動作は、ナビゲーション ウィンドウでビューをダブルクリックした場合や、ナビゲーション ウィンドウでビューを右クリックして目的のコマンドをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="6cea9-128">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

<span data-ttu-id="6cea9-129">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="6cea9-129">**Tips**</span></span>

  - <span data-ttu-id="6cea9-130">ナビゲーション ウィンドウからマクロのアクション行にビューをドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="6cea9-130">You can drag a view from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="6cea9-131">ビューをデータシート ビューで開く**OpenView**アクションが自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="6cea9-131">This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>

  - <span data-ttu-id="6cea9-132">(ことを示すビューとレコードの数が影響を受ける)、ビューを実行するときに通常表示されるシステム メッセージが表示されない場合は、これらのメッセージの表示を抑制する**SetWarning**アクションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6cea9-132">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="6cea9-133">**OpenView**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenView**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6cea9-133">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

