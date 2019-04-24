---
title: CopyObject マクロ アクション
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d1fb13d04691b7bf5e0aafcc484cfc4f471e1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295493"
---
# <a name="copyobject-macro-action"></a><span data-ttu-id="00aa8-102">CopyObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="00aa8-102">CopyObject macro action</span></span>

<span data-ttu-id="00aa8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="00aa8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00aa8-p101">**CopyObject** アクションは、指定したデータベース オブジェクトを別の Access データベースにコピーするか、または同じデータベースや Access プロジェクトに新しい名前でコピーするために使用します。たとえば、既存のオブジェクトを別のデータベースにコピーして使ったり、バックアップ コピーとして保存したりできます。また、多少の変更を加えて類似したオブジェクトを手早く作成することができます。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p101">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name. For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>

> [!NOTE]
> <span data-ttu-id="00aa8-106">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="00aa8-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="00aa8-107">設定値</span><span class="sxs-lookup"><span data-stu-id="00aa8-107">Setting</span></span>

<span data-ttu-id="00aa8-108">**CopyObject** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="00aa8-108">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00aa8-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="00aa8-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="00aa8-110">説明</span><span class="sxs-lookup"><span data-stu-id="00aa8-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00aa8-111"><strong>Destination Database/コピー先データベース</strong></span><span class="sxs-lookup"><span data-stu-id="00aa8-111"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="00aa8-p102">コピー先データベースのパスとファイル名を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>コピー先データベース</strong>] ボックスに、パスとファイル名を入力します。この引数を指定しない場合は、カレント データベースにコピーされます。  </span><span class="sxs-lookup"><span data-stu-id="00aa8-p102">A valid path and file name for the destination database. Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank if you want to select the current database.</span></span></p><p><span data-ttu-id="00aa8-115"><strong>注</strong>: この引数は、Access データベース環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="00aa8-115"><strong>NOTE</strong>: This argument is only available in the Access database environment.</span></span> <span data-ttu-id="00aa8-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span><span class="sxs-lookup"><span data-stu-id="00aa8-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span></p>
<p><span data-ttu-id="00aa8-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span><span class="sxs-lookup"><span data-stu-id="00aa8-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00aa8-118"><strong>New Name/新しい名前</strong></span><span class="sxs-lookup"><span data-stu-id="00aa8-118"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="00aa8-p104">オブジェクトの新しい名前を指定します。別のデータベースにコピーする場合は、この引数が指定されていなければ、元のオブジェクトと同じ名前でコピーされます。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p104">A new name for the object. When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00aa8-121"><strong>Source Object Type/ソース オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="00aa8-121"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="00aa8-p105">コピーするオブジェクトの種類を指定します。[ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトをコピーする場合は、この引数を指定しません。  </span><span class="sxs-lookup"><span data-stu-id="00aa8-p105">The object type you want to copy. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00aa8-125"><strong>Source Object Name/ソース オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="00aa8-125"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="00aa8-p106">コピーするオブジェクトの名前を指定します。[ <strong>ソース オブジェクト名</strong>] ボックスには、データベースのオブジェクトのうち、 <strong>Source Object Type/ソース オブジェクトの種類</strong> 引数で選択された種類のオブジェクトがすべて表示されます。[ <strong>ソース オブジェクト名</strong>] ボックスで、コピーするオブジェクトをクリックします。 <strong>Source Object Type/ソース オブジェクトの種類</strong> 引数を指定しない場合は、この引数も指定しないでください。ライブラリ データベースで <strong>CopyObject</strong> アクションが定義されたマクロを実行する場合は、まずライブラリ データベースでこの名前のオブジェクトが検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="00aa8-p106">The name of the object to be copied. The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument. In the <strong>Source Object Name</strong> box, click the object to copy. If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also. If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="00aa8-131">注釈</span><span class="sxs-lookup"><span data-stu-id="00aa8-131">Remarks</span></span>

<span data-ttu-id="00aa8-132">**Destination Database/コピー先データベース**引数と **New Name/新しい名前**引数の少なくとも一方には必ず値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00aa8-132">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="00aa8-p107">**Source Object Type/ソース オブジェクトの種類** 引数と **Source Object Name/ソース オブジェクト名** 引数を指定しないと、ナビゲーション ウィンドウで選択したオブジェクトがコピーされます。ナビゲーション ウィンドウでオブジェクトを選択するには、 **SelectObject** アクションの "In Navigation Pane/ナビゲーション ウィンドウから" 引数を [ **はい** ] に設定します。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p107">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="00aa8-135">**CopyObject** アクションの動作は、次の手順を手動で実行した場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="00aa8-135">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1. <span data-ttu-id="00aa8-136">ナビゲーション ウィンドウでオブジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="00aa8-136">Select an object in the Navigation Pane.</span></span>

2. <span data-ttu-id="00aa8-137">[ Home] タブの [ Clipboard] グループで [ Copy] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00aa8-137">On the Home tab, in the Clipboard group, click Copy.</span></span>

3. <span data-ttu-id="00aa8-p108">同じタブの [ **貼り付け**] をクリックします。[ **貼り付け**] ダイアログ ボックスが表示され、オブジェクトに新しい名前を付けることができます。 **CopyObject** アクションでは、上記の手順すべてが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p108">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name. The **CopyObject** action performs all of these steps automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="00aa8-140">[!メモ] **CopyObject** アクションでデータ アクセス ページをコピーすると、関連付けられた .htm ファイルへのリンクのみがコピーされ、ファイル自体はコピーされません。</span><span class="sxs-lookup"><span data-stu-id="00aa8-140">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>

<span data-ttu-id="00aa8-p109">マクロの **CopyObject** アクションを実行するには、コピー先データベースのパスとファイル名が実在している必要があります。実在しない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p109">The path and file name of the destination database must exist before the macro runs the **CopyObject** action. If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="00aa8-143">Visual Basic for Applications (VBA) モジュールで **CopyObject** アクションを実行するには、 **DoCmd** オブジェクトの **CopyObject** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="00aa8-143">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="00aa8-p110">[ **ファイル**] タブをクリックして、[ **名前を付けて保存**] をクリックすると、ナビゲーション ウィンドウで選択したオブジェクトや現在開いているオブジェクトを手動でコピーできます。このコマンドによってコピーが作成されるのは、カレント データベースのオブジェクトのみです。[ **名前を付けて保存**] ダイアログ ボックスで、コピーに付ける名前を入力し、保存する際のオブジェクトの種類を選択します。元のオブジェクトが既に保存されている場合に、同じオブジェクトをカレント データベースに新しい名前で保存すると、元のバージョンは古い名前でそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p110">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**. This command will make a copy of the object in the current database only. In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as. If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="00aa8-148">オブジェクトを別の Access データベースに手動でコピーするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="00aa8-148">To manually copy an object to a different Access database:</span></span>

1. <span data-ttu-id="00aa8-149">[ **外部データ**] タブの [ **エクスポート**] で [ **その他**] をクリックし、[ **Access データベース**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00aa8-149">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2. <span data-ttu-id="00aa8-150">[ **エクスポート - Access データベース**] ダイアログ ボックスで、コピー先のデータベースのファイル名を入力します。または[ **参照**] をクリックして [ **名前を付けて保存**] ダイアログ ボックスを表示し、コピー先データベースの場所を指定して、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00aa8-150">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3. <span data-ttu-id="00aa8-p111">[ **エクスポート - Access データベース**] ダイアログ ボックスで、[ **OK**] をクリックします。[ **エクスポート**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p111">In the **Export - Access Database** dialog box, click **OK**. The **Export** dialog box appears.</span></span>

4. <span data-ttu-id="00aa8-p112">[ **エクスポート**] ダイアログ ボックスで、コピー先のデータベースでのオブジェクトの名前を入力します。[ **テーブル構造とデータ**] や [ **テーブル構造のみ**] など、テーブルに適用できるオプションを選択します。完了したら、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00aa8-p112">In the **Export** dialog box, enter a name for the object in the destination database. Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables. When you are finished, click **OK**.</span></span>

