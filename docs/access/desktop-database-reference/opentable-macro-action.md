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
ms.openlocfilehash: 451d27f97c0b4f5fc4707d3947e262ba84b9a40e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926102"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="000b8-102">OpenTable マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="000b8-102">OpenTable macro action</span></span>


<span data-ttu-id="000b8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="000b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="000b8-104">**OpenTable**アクションを使用すると、データシート ビュー、デザイン ビュー、または印刷プレビューでテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="000b8-104">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="000b8-105">テーブルを開くときのデータ入力モードを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="000b8-105">You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="000b8-106">設定値</span><span class="sxs-lookup"><span data-stu-id="000b8-106">Setting</span></span>

<span data-ttu-id="000b8-107">**OpenTable**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="000b8-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="000b8-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="000b8-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="000b8-109">説明</span><span class="sxs-lookup"><span data-stu-id="000b8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="000b8-110"><strong>Table Name/テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="000b8-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="000b8-111">開くテーブル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="000b8-111">The name of the table to open.</span></span> <span data-ttu-id="000b8-112">マクロ ビルダー] ウィンドウの [<strong>テーブル名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベース内のすべてのテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="000b8-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="000b8-113">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="000b8-113">This is a required argument.</span></span> <span data-ttu-id="000b8-114">ライブラリ データベースで<strong>OpenTable</strong>アクションを含むマクロを実行する場合 Microsoft Access は、そのライブラリ データベースで、次に現在のデータベースで最初にこの名前のテーブルを探します。</span><span class="sxs-lookup"><span data-stu-id="000b8-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="000b8-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="000b8-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="000b8-p103">テーブルを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="000b8-p103">The view in which the table will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="000b8-119"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="000b8-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="000b8-p104">テーブルを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているテーブルにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="000b8-p104">The data entry mode for the table. This applies only to tables opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="000b8-124">解説</span><span class="sxs-lookup"><span data-stu-id="000b8-124">Remarks</span></span>

<span data-ttu-id="000b8-125">このアクションの動作は、ナビゲーション ウィンドウでテーブルをダブルクリックした場合や、ナビゲーション ウィンドウでテーブルを右クリックしてビューをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="000b8-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>


> [!TIP]
> <P><span data-ttu-id="000b8-126">ナビゲーション ウィンドウからテーブルをドラッグするにはマクロのアクション行にします。</span><span class="sxs-lookup"><span data-stu-id="000b8-126">You can drag a table from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="000b8-127">テーブルをデータシート ビューで開きます<STRONG>OpenTable</STRONG>アクションが自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="000b8-127">This automatically creates an <STRONG>OpenTable</STRONG> action that opens the table in Datasheet view.</span></span></P>



<span data-ttu-id="000b8-128">**OpenTable**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**OpenTable**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="000b8-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

