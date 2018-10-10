---
title: DeleteObject マクロ アクション
TOCTitle: DeleteObject Macro Action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 85e9fc888e06a69be6f458ed03ad92b8253b30a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477709"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="145d5-102">DeleteObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="145d5-102">DeleteObject Macro Action</span></span>


<span data-ttu-id="145d5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="145d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="145d5-104">**DeleteObject** アクションを使用すると、指定したデータベース オブジェクトを削除できます。</span><span class="sxs-lookup"><span data-stu-id="145d5-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="145d5-p101">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="145d5-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="145d5-107">設定</span><span class="sxs-lookup"><span data-stu-id="145d5-107">Setting</span></span>

<span data-ttu-id="145d5-108">**DeleteObject** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="145d5-108">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="145d5-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="145d5-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="145d5-110">説明</span><span class="sxs-lookup"><span data-stu-id="145d5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="145d5-111"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="145d5-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="145d5-p102">削除するオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトを削除する場合は、この引数を指定しません。  </span><span class="sxs-lookup"><span data-stu-id="145d5-p102">The type of object to delete. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="145d5-115"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="145d5-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="145d5-p103">削除するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。[ <strong>オブジェクトの種類</strong> ] ボックスに何も指定しない場合は、このボックスにも何も指定しないでください。ライブラリ データベースで " <strong>DeleteObject/オブジェクトの削除</strong> " アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="145d5-p103">The name of the object to delete. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> box blank, leave this box blank also. If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>



> [!WARNING]
> <P><span data-ttu-id="145d5-120">[!注意] [ <STRONG>オブジェクトの種類</STRONG> ] ボックスと [ <STRONG>オブジェクト名</STRONG> ] ボックスに値を指定しない場合、 <STRONG>DeleteObject</STRONG> アクションでは、ナビゲーション ウィンドウで選択したオブジェクトが削除されますが、削除を確認するメッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="145d5-120">If you leave the <STRONG>Object Type</STRONG> and <STRONG>Object Name</STRONG> boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the <STRONG>DeleteObject</STRONG> action.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="145d5-121">解説</span><span class="sxs-lookup"><span data-stu-id="145d5-121">Remarks</span></span>

<span data-ttu-id="145d5-p104">**DeleteObject** アクションを使って、マクロの実行中に一時的に作成したオブジェクトを削除できます。たとえば、 **OpenQuery** アクションを使用してテーブル作成クエリを実行し、一時的なテーブルを作成したとします。この一時的なテーブルは、使用し終わったら、 **DeleteObject** アクションを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="145d5-p104">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro. For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table. When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="145d5-125">このアクションの動作は、ナビゲーション ウィンドウでオブジェクトを選択して DEL キーを押した場合や、ナビゲーション ウィンドウでオブジェクトを右クリックして [ **削除**] をクリックした場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="145d5-125">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="145d5-126">Visual Basic for Applications モジュールで **DeleteObject** アクションを実行するには、 **DoCmd** オブジェクトの **DeleteObject** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="145d5-126">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>
