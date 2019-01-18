---
title: OpenFunction マクロ アクション
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720213"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="5ad0c-102">OpenFunction マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="5ad0c-102">OpenFunction macro action</span></span>

<span data-ttu-id="5ad0c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ad0c-104">Access プロジェクトで、ユーザー定義関数をデータシート ビュー、インライン関数のデザイン ビュー、ビューの SQL テキスト エディターで開くに**OpenFunction**アクションを使用することができます (スカラーのまたはテーブル ユーザー定義関数)、または印刷プレビューします。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-104">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview.</span></span> <span data-ttu-id="5ad0c-105">このアクションでは、データシート ビューで開くと、ユーザー定義関数を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-105">This action runs the user-defined function when opened in Datasheet view.</span></span> <span data-ttu-id="5ad0c-106">また、ユーザー定義関数に対してデータ入力モードを選択して、ユーザー定義関数を表示するレコードを制限できます。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-106">You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="5ad0c-107">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="5ad0c-108">設定値</span><span class="sxs-lookup"><span data-stu-id="5ad0c-108">Setting</span></span>

<span data-ttu-id="5ad0c-109">**OpenFunction**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ad0c-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="5ad0c-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5ad0c-111">説明</span><span class="sxs-lookup"><span data-stu-id="5ad0c-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ad0c-112"><strong>Function Name/関数名</strong></span><span class="sxs-lookup"><span data-stu-id="5ad0c-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad0c-113">開くユーザー定義関数の名前。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="5ad0c-114">マクロ ビルダー] ウィンドウの [<strong>関数名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベースですべてのユーザー定義関数を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="5ad0c-115">これは、必要な引数です。ライブラリ データベースで<strong>Function</strong>アクションが定義されたマクロを実行すると、Microsoft Access は最初ライブラリ データベースで、[し、[現在のデータベース内にこの名前の関数を検索します。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ad0c-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="5ad0c-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad0c-p103">ユーザー定義関数を開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-p103">The view in which the user-defined function will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ad0c-120"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="5ad0c-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="5ad0c-p104">ユーザー定義関数を開くときのデータ入力モードを指定します。これはデータシート ビューで開いているユーザー定義関数にのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-p104">The data entry mode for the user-defined function. This applies only to user-defined functions opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5ad0c-125">解説</span><span class="sxs-lookup"><span data-stu-id="5ad0c-125">Remarks</span></span>

<span data-ttu-id="5ad0c-126">このアクションの動作は、ナビゲーション ウィンドウでユーザー定義関数をダブルクリックした場合や、ナビゲーション ウィンドウで関数を右クリックしてビューをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="5ad0c-127">ユーザー定義関数を開いているときに、デザイン ビューに切り替え、ユーザー定義関数に対して**データ モード**引数の設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-127">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function.</span></span> <span data-ttu-id="5ad0c-128">再びデータシート ビューに切り替えても、元の設定には戻りません。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-128">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="5ad0c-129">ナビゲーション ウィンドウでユーザー定義関数を選択し、マクロのアクション行にドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-129">You can select a user-defined function in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="5ad0c-130">**OpenFunction**操作、ユーザー定義関数をデータシート ビューに表示を自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-130">This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="5ad0c-131">ユーザー定義関数を実行するときに表示されるシステム メッセージを表示したくない場合 (ユーザー定義関数を示す、レコードの数が影響を受けるアクションを使って、 **SetWarning**の表示を非表示にするこれらのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="5ad0c-132">**OpenFunction**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenFunction**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ad0c-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

