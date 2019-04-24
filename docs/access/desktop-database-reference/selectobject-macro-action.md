---
title: SelectObject マクロ アクション
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308730"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="ca11b-102">SelectObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ca11b-102">SelectObject macro action</span></span>

<span data-ttu-id="ca11b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca11b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca11b-104">"SelectObject/オブジェクトの選択" アクションを使用すると、指定したデータベース オブジェクトを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ca11b-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="ca11b-105">Setting</span><span class="sxs-lookup"><span data-stu-id="ca11b-105">Setting</span></span>

<span data-ttu-id="ca11b-106">"SelectObject/オブジェクトの選択" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ca11b-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca11b-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="ca11b-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ca11b-108">説明</span><span class="sxs-lookup"><span data-stu-id="ca11b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca11b-109"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="ca11b-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="ca11b-p101">選択するデータベース オブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="ca11b-p101">The type of database object to select. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca11b-113"><strong>オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="ca11b-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ca11b-114">選択するオブジェクトの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca11b-114">The name of the object to select.</span></span> <span data-ttu-id="ca11b-115">[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のオブジェクトがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca11b-115">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="ca11b-116">"In Navigation Pane/ナビゲーションウィンドウ" 引数を<strong>[Yes/はい]</strong>に設定しない限り、この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="ca11b-116">This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p><p><span data-ttu-id="ca11b-117"><strong>注</strong>:<STRONG>サーバービュー</STRONG>、<STRONG>ダイアグラム</STRONG>、または<STRONG>ストアドプロシージャ</STRONG>オブジェクトのオブジェクト名は、Access プロジェクト (.adp) の [<STRONG>オブジェクト名</STRONG>] ボックスには表示されません。</span><span class="sxs-lookup"><span data-stu-id="ca11b-117"><strong>NOTE</strong>: The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca11b-118"><strong>In Navigation Pane/ナビゲーション ウィンドウ内</strong></span><span class="sxs-lookup"><span data-stu-id="ca11b-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="ca11b-p103">Microsoft Access がオブジェクトをナビゲーション ウィンドウで選択するかどうかを指定します。ナビゲーション ウィンドウでオブジェクトを選択する場合は [<strong>はい</strong>] を、ナビゲーション ウィンドウでオブジェクトを選択しない場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>いいえ</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="ca11b-p103">Specifies whether Microsoft Access selects the object in the Navigation Pane. Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ca11b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="ca11b-122">Remarks</span></span>

<span data-ttu-id="ca11b-p104">The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span><span class="sxs-lookup"><span data-stu-id="ca11b-p104">The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="ca11b-p105">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span><span class="sxs-lookup"><span data-stu-id="ca11b-p105">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="ca11b-p106">Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span><span class="sxs-lookup"><span data-stu-id="ca11b-p106">Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="ca11b-p107">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.</span><span class="sxs-lookup"><span data-stu-id="ca11b-p107">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="ca11b-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="ca11b-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

