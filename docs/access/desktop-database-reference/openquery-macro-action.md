---
title: OpenQuery マクロ アクション
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709559"
---
# <a name="openquery-macro-action"></a><span data-ttu-id="01f55-102">OpenQuery マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="01f55-102">OpenQuery macro action</span></span>

<span data-ttu-id="01f55-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="01f55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01f55-p101">**OpenQuery** アクションを使用すると、選択クエリまたはクロス集計クエリをデータシート ビュー、デザイン ビュー、印刷プレビューのいずれかで開くことができます。このアクションでは、アクション クエリが実行されます。クエリを開くときのデータ入力モードを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="01f55-p101">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview. This action runs an action query. You can also select a data entry mode for the query.</span></span>

> [!NOTE]
> <span data-ttu-id="01f55-p102">[!メモ] このアクションは、Access データベース (.mdb または .accdb) 環境でのみ使用できます。Access プロジェクト (.adp) 環境で使用する場合は、 **OpenView** アクション、 **OpenStoredProcedure** アクション、または **OpenFunction** アクションのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f55-p102">This action is only available in the Access database environment (.mdb or .accdb). See the **OpenView**, **OpenStoredProcedure**, or **OpenFunction** actions if you are using the Access project environment (.adp).</span></span>

## <a name="setting"></a><span data-ttu-id="01f55-109">設定</span><span class="sxs-lookup"><span data-stu-id="01f55-109">Setting</span></span>

<span data-ttu-id="01f55-110">**OpenQuery** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="01f55-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01f55-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="01f55-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="01f55-112">説明</span><span class="sxs-lookup"><span data-stu-id="01f55-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01f55-113"><strong>Query Name/クエリ名</strong></span><span class="sxs-lookup"><span data-stu-id="01f55-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="01f55-p103">開くクエリの名前を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>クエリ名</strong>] ボックスには、カレント データベース内のクエリがすべて表示されます。この引数は省略できません。ライブラリ データベースで <strong>OpenQuery</strong> アクションが定義されているマクロを実行すると、この名前のクエリが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="01f55-p103">The name of the query to open. The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database. This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01f55-117"><strong>View/ビュー</strong></span><span class="sxs-lookup"><span data-stu-id="01f55-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="01f55-p104">クエリを開くときのビューを指定します。[ <strong>ビュー</strong>] ボックスで、[ <strong>データシート ビュー</strong>]、[ <strong>デザイン ビュー</strong>]、[ <strong>印刷プレビュー</strong>]、[ <strong>ピボットテーブル ビュー</strong>]、または [ <strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [ <strong>データシート ビュー</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="01f55-p104">The view in which the query will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01f55-121"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="01f55-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="01f55-p105">クエリを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているクエリにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [ <strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [ <strong>編集</strong>]、レコードの表示のみを許可する場合は [ <strong>読み取り専用</strong>] をクリックします。既定値は [ <strong>編集</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="01f55-p105">The data entry mode for the query. This applies only to queries opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="01f55-126">解説</span><span class="sxs-lookup"><span data-stu-id="01f55-126">Remarks</span></span>

<span data-ttu-id="01f55-127">**View/ビュー** 引数に [ **データシート ビュー**] を指定すると、選択クエリ、クロス集計クエリ、ユニオン クエリ、または **ReturnsRecords/レコード表示** プロパティが [ **はい** に設定されているパススルー クエリの場合は、クエリの結果セットが表示されます。一方、アクション クエリ、データ定義クエリ、または **ReturnsRecords /レコード表示** プロパティが [ **いいえ** ] に設定されているパススルー クエリの場合は、そのクエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="01f55-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="01f55-p106">**OpenQuery** アクションの動作は、ナビゲーション ウィンドウでクエリをダブルクリックした場合や、ナビゲーション ウィンドウでクエリを右クリックしてビューをクリックした場合と同じです。このアクションにより、別のオプションも選択できます。</span><span class="sxs-lookup"><span data-stu-id="01f55-p106">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view. With this action you can select additional options.</span></span>

> [!TIP]
> - <span data-ttu-id="01f55-p107">クエリをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、クエリをデータシート ビューで開く **OpenQuery** アクションが自動的に作成されます。 クエリが開いているときにデザイン ビューに切り替えると、クエリの **Data Mode/データ モード** 引数の設定は解除されます。再びデータシート ビューに切り替えても、元の設定には戻りません。</span><span class="sxs-lookup"><span data-stu-id="01f55-p107">You can drag a query from the Navigation Pane to a macro action row. This automatically creates an **OpenQuery** action that opens the query in Datasheet view. Switching to Design view while the query is open removes the **Data Mode** argument setting for the query. This setting isn't in effect even if the user returns to Datasheet view.</span></span>
> - <span data-ttu-id="01f55-134">アクション クエリを実行すると、通常は、それがアクション クエリであること、および影響を受けるレコード数を示すシステム メッセージが表示されますが、これを表示しないようにするには、 **SetWarnings** アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f55-134">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="01f55-135">Visual Basic for Applications (VBA) モジュールで **OpenQuery** アクションを実行するには、 **DoCmd** オブジェクトの **OpenQuery** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01f55-135">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

