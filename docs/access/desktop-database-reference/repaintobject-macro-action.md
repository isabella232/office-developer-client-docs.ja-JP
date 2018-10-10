---
title: "'RepaintObject/オブジェクトの再描画' マクロ アクション"
TOCTitle: RepaintObject Macro Action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4371ce5482b775ad9c022eeda8202c4b2e0f800d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478129"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="5720f-102">"RepaintObject/オブジェクトの再描画" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="5720f-102">RepaintObject Macro Action</span></span>


<span data-ttu-id="5720f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5720f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5720f-104">指定されていない場合は、保留中の指定されたデータベース オブジェクトまたはアクティブなデータベース オブジェクトでは、画面の更新を完了する**RepaintObject**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5720f-104">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified.</span></span> <span data-ttu-id="5720f-105">このような更新には、オブジェクトのコントロールの再計算が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5720f-105">Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="5720f-106">設定値</span><span class="sxs-lookup"><span data-stu-id="5720f-106">Setting</span></span>

<span data-ttu-id="5720f-107">**RepaintObject**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="5720f-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5720f-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="5720f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5720f-109">説明</span><span class="sxs-lookup"><span data-stu-id="5720f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5720f-110"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="5720f-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5720f-p102">再描画するオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、または [<strong>関数</strong>] をクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</span><span class="sxs-lookup"><span data-stu-id="5720f-p102">The type of object to repaint. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5720f-114"><strong>オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="5720f-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5720f-115">再描画するオブジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="5720f-115">The name of the object to repaint.</span></span> <span data-ttu-id="5720f-116">[ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="5720f-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="5720f-117"><strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</span><span class="sxs-lookup"><span data-stu-id="5720f-117">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5720f-118">解説</span><span class="sxs-lookup"><span data-stu-id="5720f-118">Remarks</span></span>

<span data-ttu-id="5720f-p104">Microsoft Access では、他の保留中のタスクの実行が終わるまで画面は更新されません。このアクションを使うと、指定したオブジェクトのコントロールを即座に再描画できます。このアクションは、次のような場合に使うと効果的です。</span><span class="sxs-lookup"><span data-stu-id="5720f-p104">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks. With this action, you can force immediate repainting of the controls in the specified object. You can use this action:</span></span>

  - <span data-ttu-id="5720f-122">いくつかのコントロールの値を変更するのには **、アクション**を使用します。</span><span class="sxs-lookup"><span data-stu-id="5720f-122">When you use the **SetValue** action to change values in a number of controls.</span></span> <span data-ttu-id="5720f-123">アクセスの変更をすぐに表示されないことが他のコントロール (演算コントロールなど) が変更されたコントロールの値に依存している場合に特に。</span><span class="sxs-lookup"><span data-stu-id="5720f-123">Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

  - <span data-ttu-id="5720f-p106">表示しているフォームのすべてのコントロールにデータが確実に表示されるようにする場合。たとえば、フォームを開いた直後は、OLE オブジェクトを含むコントロールのデータが表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="5720f-p106">When you want to make sure that the form you are viewing displays data in all of its controls. For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="5720f-126">この動作は、オブジェクトの基になるテーブルまたはクエリからレコードの追加、変更、削除は反映されませんので、データベースの再クエリを発生しません。</span><span class="sxs-lookup"><span data-stu-id="5720f-126">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query.</span></span> <span data-ttu-id="5720f-127">オブジェクトまたはそのコントロールのいずれかのソースを再クエリ<STRONG>再クエリ</STRONG>アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="5720f-127">Use the <STRONG>Requery</STRONG> action to requery the source of the object or one of its controls.</span></span> <span data-ttu-id="5720f-128">最新のレコードを表示し、適用されたフィルターを削除するには、<STRONG>解除</STRONG>を使用します。</span><span class="sxs-lookup"><span data-stu-id="5720f-128">Use the <STRONG>ShowAllRecords</STRONG> action to display the most recent records and remove any applied filters.</span></span></P>
> <LI>
> <P><span data-ttu-id="5720f-129"><STRONG>RepaintObject</STRONG>アクション [<STRONG>ホーム</STRONG>] タブ、フォームやデータシートの現在表示されているレコードにするか、他のユーザーが行った変更をすべてを表示する [<STRONG>レコード</STRONG>] グループで [<STRONG>更新</STRONG>] をクリックと同じ効果がありません。</span><span class="sxs-lookup"><span data-stu-id="5720f-129">The <STRONG>RepaintObject</STRONG> action doesn't have the same effect as clicking <STRONG>Refresh</STRONG> in the <STRONG>Records</STRONG> group on the <STRONG>Home</STRONG> tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span></P></LI></UL>



<span data-ttu-id="5720f-130">**RepaintObject**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**RepaintObject**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5720f-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>
