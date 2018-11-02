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
ms.openlocfilehash: 22d3422a5c00e6caa20003df3574c26ab061ab53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925346"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="902e1-102">OpenStoredProcedure マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="902e1-102">OpenStoredProcedure macro action</span></span>


<span data-ttu-id="902e1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="902e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="902e1-p101">Access プロジェクトで、"OpenStoredProcedure/ストアドプロシージャを開く" アクションを使用すると、データシート ビュー、ストアド プロシージャ デザイン ビュー、または印刷プレビューでストアド プロシージャを開くことができます。データシート ビューで開いた場合、その名前のストアド プロシージャが実行されます。ストアド プロシージャのデータ入力モードの設定を行ったり、表示するレコードを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="902e1-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="902e1-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="902e1-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="902e1-109">設定値</span><span class="sxs-lookup"><span data-stu-id="902e1-109">Setting</span></span>

<span data-ttu-id="902e1-110">"OpenStoredProcedure/ストアドプロシージャを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="902e1-110">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="902e1-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="902e1-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="902e1-112">説明</span><span class="sxs-lookup"><span data-stu-id="902e1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="902e1-113"><strong>Procedure Name/プロシージャ名</strong></span><span class="sxs-lookup"><span data-stu-id="902e1-113"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="902e1-114">開くストアド プロシージャの名前です。</span><span class="sxs-lookup"><span data-stu-id="902e1-114">The name of the stored procedure to open.</span></span> <span data-ttu-id="902e1-115">[<strong>プロシージャ名</strong>] ボックスに<strong>アクションの引数</strong>]、[マクロ ビルダー] ウィンドウのでは、現在のデータベースのすべてのストアド プロシージャを示しています。</span><span class="sxs-lookup"><span data-stu-id="902e1-115">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="902e1-116">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="902e1-116">This is a required argument.</span></span> <span data-ttu-id="902e1-117">ライブラリ データベースで、 <strong>OpenStoredProcedure</strong>アクションを含むマクロを実行すると、最初に検索の最初にライブラリ データベースで、し、[現在のデータベース内に同じ名前のストアド プロシージャ。</span><span class="sxs-lookup"><span data-stu-id="902e1-117">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="902e1-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="902e1-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="902e1-p104">ストアド プロシージャを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="902e1-p104">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="902e1-122"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="902e1-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="902e1-p105">ストアド プロシージャを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているストアド プロシージャにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="902e1-p105">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="902e1-127">解説</span><span class="sxs-lookup"><span data-stu-id="902e1-127">Remarks</span></span>

<span data-ttu-id="902e1-128">このアクションの動作は、ナビゲーション ウィンドウでストアド プロシージャをダブルクリックした場合や、ナビゲーション ウィンドウでストアド プロシージャを右クリックして目的のコマンドをクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="902e1-128">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="902e1-p106">ストアド プロシージャが開いているときにデザイン ビューに切り替えると、ストアド プロシージャの "Data Mode/データ モード" 引数の設定は解除されます。再びデータシート ビューに切り替えても、元の設定には戻りません。</span><span class="sxs-lookup"><span data-stu-id="902e1-p106">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P><span data-ttu-id="902e1-131">ストアド プロシージャをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、ストアド プロシージャをデータシート ビューで開く "OpenStoredProcedure/ストアドプロシージャを開く" アクションが自動的に作成されます。 >  ストアド プロシージャを実行すると、通常は、それがストアド プロシージャであること、および影響を受けるレコード数を示すシステム メッセージが表示されますが、これを表示しないようにするには、"SetWarning/メッセージの設定" アクションを使用します。 ></span><span class="sxs-lookup"><span data-stu-id="902e1-131">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="902e1-132">ストアド プロシージャをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、ストアド プロシージャをデータシート ビューで開く "OpenStoredProcedure/ストアドプロシージャを開く" アクションが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="902e1-132">This automatically creates an <STRONG>OpenStoredProcedure</STRONG> action that opens the stored procedure in Datasheet view.</span></span></P>
> <LI>
> <P><span data-ttu-id="902e1-133">これらの表示を抑制するのに<STRONG>SetWarning</STRONG>アクションを使用するには (それがストアド プロシージャおよび影響を受けるレコードの数)、ストアド プロシージャを実行するときに表示されるシステム メッセージを表示したくない場合メッセージです。</span><span class="sxs-lookup"><span data-stu-id="902e1-133">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the <STRONG>SetWarning</STRONG> action to suppress the display of these messages.</span></span></P></LI></UL>
> <P></P>



<span data-ttu-id="902e1-134">Visual Basic for Applications (VBA) モジュールで "OpenStoredProcedure/ストアドプロシージャを開く" アクションを実行するには、 **DoCmd** オブジェクトの **OpenStoredProcedure** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="902e1-134">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

