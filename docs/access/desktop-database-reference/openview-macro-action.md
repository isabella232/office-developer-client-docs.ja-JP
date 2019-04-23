---
title: OpenView マクロ アクション
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 88bebab46cd6b76fb101c86c4fe33c5ab86a3e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288302"
---
# <a name="openview-macro-action"></a><span data-ttu-id="fac7a-102">OpenView マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="fac7a-102">OpenView macro action</span></span>

<span data-ttu-id="fac7a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fac7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fac7a-p101">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.</span><span class="sxs-lookup"><span data-stu-id="fac7a-p101">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.</span></span>

> [!NOTE]
> <span data-ttu-id="fac7a-107">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="fac7a-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="fac7a-108">設定値</span><span class="sxs-lookup"><span data-stu-id="fac7a-108">Setting</span></span>

<span data-ttu-id="fac7a-109">"OpenView/ビューを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fac7a-109">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fac7a-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="fac7a-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fac7a-111">説明</span><span class="sxs-lookup"><span data-stu-id="fac7a-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fac7a-112"><strong>View Name/ビュー名</strong></span><span class="sxs-lookup"><span data-stu-id="fac7a-112"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fac7a-113">開くビューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="fac7a-113">The name of the view to open.</span></span> <span data-ttu-id="fac7a-114">[マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>ビュー名</strong>] ボックスには、カレントデータベースのすべてのビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fac7a-114">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="fac7a-115">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="fac7a-115">This is a required argument.</span></span> <span data-ttu-id="fac7a-116">ライブラリ データベースで "OpenView/ビューを開く" アクションが定義されているマクロを実行すると、この名前のビューが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="fac7a-116">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fac7a-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="fac7a-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="fac7a-p103">ビューを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="fac7a-p103">The view in which the view will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fac7a-121"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="fac7a-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="fac7a-p104">ビューを開くときのデータ入力モードを指定します。これはデータシート  ビューで開いているビューにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="fac7a-p104">The data entry mode for the view. This applies only to views opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fac7a-126">注釈</span><span class="sxs-lookup"><span data-stu-id="fac7a-126">Remarks</span></span>

<span data-ttu-id="fac7a-127">このアクションの動作は、ナビゲーション ウィンドウでビューをダブルクリックした場合や、ナビゲーション ウィンドウでビューを右クリックして目的のコマンドをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="fac7a-127">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

> [!TIP]
> - <span data-ttu-id="fac7a-p105">You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.</span><span class="sxs-lookup"><span data-stu-id="fac7a-p105">You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>
> - <span data-ttu-id="fac7a-130">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span><span class="sxs-lookup"><span data-stu-id="fac7a-130">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="fac7a-131">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="fac7a-131">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

