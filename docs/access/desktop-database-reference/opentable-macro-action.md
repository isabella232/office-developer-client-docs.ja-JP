---
title: OpenTable マクロ アクション
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288295"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="e88e4-102">OpenTable マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="e88e4-102">OpenTable macro action</span></span>

<span data-ttu-id="e88e4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e88e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e88e4-p101">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview. You can also select a data entry mode for the table.</span><span class="sxs-lookup"><span data-stu-id="e88e4-p101">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview. You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="e88e4-106">Setting</span><span class="sxs-lookup"><span data-stu-id="e88e4-106">Setting</span></span>

<span data-ttu-id="e88e4-107">"OpenTable/テーブルを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e88e4-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e88e4-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="e88e4-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e88e4-109">説明</span><span class="sxs-lookup"><span data-stu-id="e88e4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e88e4-110"><strong>Table Name/テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="e88e4-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e88e4-111">開くテーブル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e88e4-111">The name of the table to open.</span></span> <span data-ttu-id="e88e4-112">[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>テーブル名</strong>] ボックスには、カレント データベース内のテーブルがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="e88e4-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="e88e4-113">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="e88e4-113">This is a required argument.</span></span> <span data-ttu-id="e88e4-114">ライブラリ データベースで "OpenTable/テーブルを開く" アクションが定義されているマクロを実行すると、この名前のテーブルが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="e88e4-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e88e4-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="e88e4-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="e88e4-p103">テーブルを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="e88e4-p103">The view in which the table will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e88e4-119"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="e88e4-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="e88e4-p104">テーブルを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているテーブルにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="e88e4-p104">The data entry mode for the table. This applies only to tables opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="e88e4-124">注釈</span><span class="sxs-lookup"><span data-stu-id="e88e4-124">Remarks</span></span>

<span data-ttu-id="e88e4-125">このアクションの動作は、ナビゲーション ウィンドウでテーブルをダブルクリックした場合や、ナビゲーション ウィンドウでテーブルを右クリックしてビューをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="e88e4-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="e88e4-p105">You can drag a table from the Navigation Pane to a macro action row. This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span><span class="sxs-lookup"><span data-stu-id="e88e4-p105">You can drag a table from the Navigation Pane to a macro action row. This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="e88e4-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="e88e4-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

