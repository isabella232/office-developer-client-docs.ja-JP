---
title: RepaintObject マクロ アクション
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2ef6c5f38064ae3253cd7e0e58732f63294ceb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306686"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="a88a8-102">RepaintObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a88a8-102">RepaintObject macro action</span></span>

<span data-ttu-id="a88a8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a88a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a88a8-p101">"RepaintObject/オブジェクトの再描画" アクションを使用すると、表示が更新されていないデータベース オブジェクトを再描画できます。データベース オブジェクトが指定されている場合はそのオブジェクトを再描画し、指定されていない場合はアクティブなデータベース オブジェクトを再描画します。このとき、コントロールの再計算も行われます。</span><span class="sxs-lookup"><span data-stu-id="a88a8-p101">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified. Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="a88a8-106">Setting</span><span class="sxs-lookup"><span data-stu-id="a88a8-106">Setting</span></span>

<span data-ttu-id="a88a8-107">"RepaintObject/オブジェクトの再描画" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a88a8-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a88a8-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="a88a8-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a88a8-109">説明</span><span class="sxs-lookup"><span data-stu-id="a88a8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a88a8-110"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="a88a8-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a88a8-p102">再描画するオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、または [<strong>関数</strong>] をクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</span><span class="sxs-lookup"><span data-stu-id="a88a8-p102">The type of object to repaint. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a88a8-114"><strong>オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="a88a8-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a88a8-115">再描画するオブジェクトの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a88a8-115">The name of the object to repaint.</span></span> <span data-ttu-id="a88a8-116">[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のオブジェクトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88a8-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="a88a8-117">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span><span class="sxs-lookup"><span data-stu-id="a88a8-117">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a88a8-118">注釈</span><span class="sxs-lookup"><span data-stu-id="a88a8-118">Remarks</span></span>

<span data-ttu-id="a88a8-p104">Microsoft Access では、他の保留中のタスクの実行が終わるまで画面は更新されません。このアクションを使うと、指定したオブジェクトのコントロールを即座に再描画できます。このアクションは、次のような場合に使うと効果的です。</span><span class="sxs-lookup"><span data-stu-id="a88a8-p104">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks. With this action, you can force immediate repainting of the controls in the specified object. You can use this action:</span></span>

- <span data-ttu-id="a88a8-p105">When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span><span class="sxs-lookup"><span data-stu-id="a88a8-p105">When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

- <span data-ttu-id="a88a8-p106">表示しているフォームのすべてのコントロールにデータが確実に表示されるようにする場合。たとえば、フォームを開いた直後は、OLE オブジェクトを含むコントロールのデータが表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="a88a8-p106">When you want to make sure that the form you are viewing displays data in all of its controls. For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>

> [!NOTE]
> - <span data-ttu-id="a88a8-p107">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the **Requery** action to requery the source of the object or one of its controls. Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.</span><span class="sxs-lookup"><span data-stu-id="a88a8-p107">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the **Requery** action to requery the source of the object or one of its controls. Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.</span></span>
> - <span data-ttu-id="a88a8-129">**RepaintObject**アクションの動作は、[**ホーム**] タブの [**レコード**] グループで [最新の情報に**更新**] をクリックした場合と同じです。これには、フォームおよびデータシートに現在表示されているレコードに対して行った変更やその他のユーザーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a88a8-129">The **RepaintObject** action doesn't have the same effect as clicking **Refresh** in the **Records** group on the **Home** tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span>

<span data-ttu-id="a88a8-130">Visual Basic for applications (VBA) モジュールで**RepaintObject**アクションを実行するには、 **DoCmd**オブジェクトの**RepaintObject**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a88a8-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>

