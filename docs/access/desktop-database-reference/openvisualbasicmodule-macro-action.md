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
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288281"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="6209d-102">OpenVisualBasicModule マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="6209d-102">OpenVisualBasicModule macro action</span></span>

<span data-ttu-id="6209d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6209d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6209d-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span><span class="sxs-lookup"><span data-stu-id="6209d-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="6209d-106">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="6209d-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="6209d-107">設定値</span><span class="sxs-lookup"><span data-stu-id="6209d-107">Setting</span></span>

<span data-ttu-id="6209d-108">"OpenVisualBasicModule/VisualBasicモジュールを開く" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6209d-108">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6209d-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="6209d-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6209d-110">説明</span><span class="sxs-lookup"><span data-stu-id="6209d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6209d-111"><strong>Module Name/モジュール名</strong></span><span class="sxs-lookup"><span data-stu-id="6209d-111"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6209d-112">開くモジュールの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6209d-112">The name of the module you want to open.</span></span> <span data-ttu-id="6209d-113">データベースのすべての標準モジュールでプロシージャを検索して、そのプロシージャに適切なモジュールを開く場合は、この引数を指定しません。</span><span class="sxs-lookup"><span data-stu-id="6209d-113">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="6209d-114">ライブラリ データベースで "OpenVisualBasicModule/VisualBasicモジュールを開く" アクションが定義されているマクロを実行すると、この名前のモジュールが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</span><span class="sxs-lookup"><span data-stu-id="6209d-114">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6209d-115"><strong>Procedure Name/プロシージャ名</strong></span><span class="sxs-lookup"><span data-stu-id="6209d-115"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6209d-p103">モジュールを開いて表示するプロシージャの名前を指定します。この引数を省略すると、モジュールの宣言セクションが開きます。</span><span class="sxs-lookup"><span data-stu-id="6209d-p103">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6209d-118">"Module Name/モジュール名" 引数または有効な "プロシージャ名" 引数のいずれかに有効な名前を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6209d-118">You must enter a valid name in either the **Module Name** or **Procedure Name** argument.</span></span>


## <a name="remarks"></a><span data-ttu-id="6209d-119">注釈</span><span class="sxs-lookup"><span data-stu-id="6209d-119">Remarks</span></span>

<span data-ttu-id="6209d-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span><span class="sxs-lookup"><span data-stu-id="6209d-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="6209d-121">たとえば、フォームの注文で **[** printinvoice] ボタンの click イベントプロシージャを開くには、" **Module name/名前**" 引数を [フォームに設定する] を指定し、 **"** **プロシージャ名**" 引数を**\_printinvoice クリック**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6209d-121">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="6209d-122">To view the event procedure for a form or report, the form or report must be open.</span><span class="sxs-lookup"><span data-stu-id="6209d-122">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="6209d-123">同様に、クラス モジュールでプロシージャを開くには、モジュール名を指定する必要がありますが、そのクラス モジュールを開いておく必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6209d-123">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="6209d-124">プライベート プロシージャを開くには、そのプロシージャを含むモジュールを開いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6209d-124">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="6209d-p105">このアクションの動作は、ナビゲーション ウィンドウでモジュールを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。このアクションを使用すると、プロシージャ名を指定して、データベースの標準モジュールで検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="6209d-p105">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>

> [!TIP]
> <span data-ttu-id="6209d-p106">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span><span class="sxs-lookup"><span data-stu-id="6209d-p106">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span></span>

<span data-ttu-id="6209d-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="6209d-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

