---
title: OpenStoredProcedure マクロ アクション
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288309"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="eff61-102">OpenStoredProcedure マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="eff61-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="eff61-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="eff61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eff61-p101">Access プロジェクトで、"OpenStoredProcedure/ストアドプロシージャを開く" アクションを使用すると、データシート ビュー、ストアド プロシージャ デザイン ビュー、または印刷プレビューでストアド プロシージャを開くことができます。データシート ビューで開いた場合、その名前のストアド プロシージャが実行されます。ストアド プロシージャのデータ入力モードの設定を行ったり、表示するレコードを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="eff61-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="eff61-107">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="eff61-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="eff61-108">設定値</span><span class="sxs-lookup"><span data-stu-id="eff61-108">Setting</span></span>

<span data-ttu-id="eff61-109">"OpenStoredProcedure/ストアドプロシージャを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="eff61-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff61-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="eff61-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="eff61-111">説明</span><span class="sxs-lookup"><span data-stu-id="eff61-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff61-112"><strong>Procedure Name/プロシージャ名</strong></span><span class="sxs-lookup"><span data-stu-id="eff61-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="eff61-113">開くストアド プロシージャの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="eff61-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="eff61-114">[マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>プロシージャ名]</strong>ボックスには、カレントデータベースのすべてのストアドプロシージャが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eff61-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="eff61-115">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="eff61-115">This is a required argument.</span></span> <span data-ttu-id="eff61-116">ライブラリ データベースで "OpenStoredProcedure/ストアドプロシージャを開く" アクションが定義されているマクロを実行すると、この名前のストアド プロシージャが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="eff61-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff61-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="eff61-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="eff61-p103">ストアド プロシージャを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="eff61-p103">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff61-121"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="eff61-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="eff61-p104">ストアド プロシージャを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているストアド プロシージャにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="eff61-p104">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="eff61-126">注釈</span><span class="sxs-lookup"><span data-stu-id="eff61-126">Remarks</span></span>

<span data-ttu-id="eff61-127">このアクションの動作は、ナビゲーション ウィンドウでストアド プロシージャをダブルクリックした場合や、ナビゲーション ウィンドウでストアド プロシージャを右クリックして目的のコマンドをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="eff61-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="eff61-p105">ストアド プロシージャが開いているときにデザイン ビューに切り替えると、ストアド プロシージャの "Data Mode/データ モード" 引数の設定は解除されます。再びデータシート ビューに切り替えても、元の設定には戻りません。</span><span class="sxs-lookup"><span data-stu-id="eff61-p105">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="eff61-130">ナビゲーションウィンドウからマクロアクション行にストアドプロシージャをドラッグすることができます。</span><span class="sxs-lookup"><span data-stu-id="eff61-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="eff61-131">これにより、ストアドプロシージャがデータシートビューで開かれる**openstoredprocedure**アクションが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="eff61-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="eff61-132">ストアド プロシージャを実行すると、通常は、それがストアド プロシージャであること、および影響を受けるレコード数を示すシステム メッセージが表示されますが、これを表示しないようにするには、"SetWarning/メッセージの設定" アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="eff61-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="eff61-133">Visual Basic for applications (VBA) モジュールで " **openstoredprocedure/ストアドプロシージャを開く**" アクションを実行するには、 **DoCmd**オブジェクトの**openstoredprocedure**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="eff61-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

