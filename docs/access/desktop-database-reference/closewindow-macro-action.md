---
title: "\"CloseWindow/ウィンドウを閉じる\" マクロ アクション"
TOCTitle: CloseWindow Macro Action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1d80ac5b545f07d3bd39f69f16c4578e49439cdf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476262"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="31c77-102">"CloseWindow/ウィンドウを閉じる" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="31c77-102">CloseWindow Macro Action</span></span>


<span data-ttu-id="31c77-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="31c77-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="31c77-104">" **CloseWindow/ウィンドウを閉じる** " アクションを使用すると、指定した Access ドキュメント タブを閉じることができます。何も指定しない場合は、アクティブなドキュメント タブが閉じます。</span><span class="sxs-lookup"><span data-stu-id="31c77-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="31c77-105">設定値</span><span class="sxs-lookup"><span data-stu-id="31c77-105">Setting</span></span>

<span data-ttu-id="31c77-106">**CloseWindow**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="31c77-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31c77-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="31c77-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="31c77-108">説明</span><span class="sxs-lookup"><span data-stu-id="31c77-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31c77-109"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="31c77-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="31c77-p101">ドキュメント タブを閉じるオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。アクティブなドキュメント タブを選択する場合は、この引数を指定しません。  </span><span class="sxs-lookup"><span data-stu-id="31c77-p101">The type of object whose document tab you want to close. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="31c77-113">モジュールでは、Visual Basic エディターを終了する場合、<STRONG>オブジェクトの型</STRONG>引数に<STRONG>モジュール</STRONG>を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31c77-113">If you are closing a module in the Visual Basic Editor, you must use <STRONG>Module</STRONG> in the <STRONG>Object Type</STRONG> argument.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c77-114"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="31c77-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="31c77-115">閉じるオブジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="31c77-115">The name of the object to be closed.</span></span> <span data-ttu-id="31c77-116">[ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="31c77-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="31c77-117">閉じるオブジェクトをクリックします。</span><span class="sxs-lookup"><span data-stu-id="31c77-117">Click the object to close.</span></span> <span data-ttu-id="31c77-118"><strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</span><span class="sxs-lookup"><span data-stu-id="31c77-118">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c77-119"><strong>Save/オブジェクトの保存</strong></span><span class="sxs-lookup"><span data-stu-id="31c77-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="31c77-p103">オブジェクトを閉じるときに、オブジェクトに加えた変更を保存するかどうかを指定します。保存する場合は [ <strong>する</strong>]、保存せずに閉じる場合は [ <strong>しない</strong>]、保存するかどうかを毎回確認する場合は [ <strong>確認</strong>] をクリックします。既定値は [ <strong>確認</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="31c77-p103">Whether to save changes to the object when it is closed. Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object). The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="31c77-123">解説</span><span class="sxs-lookup"><span data-stu-id="31c77-123">Remarks</span></span>

<span data-ttu-id="31c77-124">**CloseWindow**アクションは、すべてのユーザーが明示的に開くことができるデータベース オブジェクトまたは閉じる動作します。</span><span class="sxs-lookup"><span data-stu-id="31c77-124">The **CloseWindow** action works on all database objects that the user can explicitly open or close.</span></span> <span data-ttu-id="31c77-125">このアクションは、オブジェクトを選択して、オブジェクトのドキュメント タブを右クリックして [ショートカット] メニューの [**閉じる**] をクリックしてしたり、オブジェクトの**閉じる**ボタンをクリックして終了すると同じ効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="31c77-125">This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="31c77-126">**保存**引数は、**プロンプト**に設定されて、 **CloseWindow**アクションを実行する前にオブジェクトが保存されていない場合は、マクロが終了する前にオブジェクトを保存するのにを求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="31c77-126">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it.</span></span> <span data-ttu-id="31c77-127">**よって**の**警告の**引数を**No**に設定した場合ダイアログ ボックスが表示されないと、オブジェクトが自動的に保存します。</span><span class="sxs-lookup"><span data-stu-id="31c77-127">If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="31c77-128">**CloseWindow**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**CloseWindow**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="31c77-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

