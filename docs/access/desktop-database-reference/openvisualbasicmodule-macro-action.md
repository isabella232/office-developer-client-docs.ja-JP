---
title: OpenVisualBasicModule マクロ アクション
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 274ec88483066b4e8dd4032501ecfcc6a662b134
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998141"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="cd431-102">OpenVisualBasicModule マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="cd431-102">OpenVisualBasicModule macro action</span></span>

<span data-ttu-id="cd431-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cd431-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd431-104">開くには、指定された Visual Basic for Applications (VBA) モジュールは、指定されたプロシージャでは、 **OpenVisualBasicModule**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd431-104">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure.</span></span> <span data-ttu-id="cd431-105">指定できるのは、Sub プロシージャ、Function プロシージャ、およびイベント プロシージャです。</span><span class="sxs-lookup"><span data-stu-id="cd431-105">This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="cd431-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="cd431-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="cd431-107">設定値</span><span class="sxs-lookup"><span data-stu-id="cd431-107">Setting</span></span>

<span data-ttu-id="cd431-108">**OpenVisualBasicModule**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="cd431-108">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd431-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="cd431-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cd431-110">説明</span><span class="sxs-lookup"><span data-stu-id="cd431-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd431-111"><strong>Module Name/モジュール名</strong></span><span class="sxs-lookup"><span data-stu-id="cd431-111"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cd431-112">開くモジュールの名前。</span><span class="sxs-lookup"><span data-stu-id="cd431-112">The name of the module you want to open.</span></span> <span data-ttu-id="cd431-113">できますこの引数を指定しない場合は、プロシージャがデータベース内のすべての標準モジュールを検索し、そのプロシージャに適切なモジュールを開きます。</span><span class="sxs-lookup"><span data-stu-id="cd431-113">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="cd431-114">ライブラリ データベースで、 <strong>OpenVisualBasicModule</strong>アクションを含むマクロを実行する場合は、最初の検索にライブラリ データベースで、し、[現在のデータベース内に同じ名前のモジュールです。</span><span class="sxs-lookup"><span data-stu-id="cd431-114">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd431-115"><strong>Procedure Name/プロシージャ名</strong></span><span class="sxs-lookup"><span data-stu-id="cd431-115"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cd431-p103">モジュールを開いて表示するプロシージャの名前を指定します。この引数を省略すると、モジュールの宣言セクションが開きます。</span><span class="sxs-lookup"><span data-stu-id="cd431-p103">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="cd431-118">**モジュール名**や**プロシージャ名**のいずれかの引数に有効な名前を入力してください。</span><span class="sxs-lookup"><span data-stu-id="cd431-118">You must enter a valid name in either the **Module Name** or **Procedure Name** argument.</span></span>


## <a name="remarks"></a><span data-ttu-id="cd431-119">解説</span><span class="sxs-lookup"><span data-stu-id="cd431-119">Remarks</span></span>

<span data-ttu-id="cd431-120">**モジュール名**の引数は、**プロシージャ名**の引数を指定することによって、イベント プロシージャを開くには、このアクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd431-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="cd431-121">などを注文フォームの [PrintInvoice] ボタンの**Click**イベント プロシージャを開くには、**モジュール名**の引数を**Form.Orders**に設定し、**プロシージャ名**の引数を設定**PrintInvoice\_をクリックして**。</span><span class="sxs-lookup"><span data-stu-id="cd431-121">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="cd431-122">フォームまたはレポートが、フォームまたはレポートのイベント プロシージャを表示するには、開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd431-122">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="cd431-123">同様に、クラス モジュールでプロシージャを開くには、モジュール名を指定する必要がありますが、そのクラス モジュールを開いておく必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cd431-123">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="cd431-124">プライベート プロシージャを開くには、そのプロシージャを含むモジュールを開いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd431-124">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="cd431-p105">このアクションの動作は、ナビゲーション ウィンドウでモジュールを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。このアクションを使用すると、プロシージャ名を指定して、データベースの標準モジュールで検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd431-p105">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>

> [!TIP]
> <span data-ttu-id="cd431-127">ナビゲーション ウィンドウでモジュールを選択し、マクロのアクション行にドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="cd431-127">You can select a module in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="cd431-128">宣言セクションには、モジュールを開く**OpenVisualBasicModule**アクションが自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="cd431-128">This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span></span>

<span data-ttu-id="cd431-129">VBA モジュールでは、 **OpenVisualBasicModule**アクションを実行するには、 **DoCmd**オブジェクトの**OpenModule**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd431-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

