---
title: RunCode マクロ アクション
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: acf8ed2bd10efd55436b8933a862833b8e49c5f0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926690"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="5a9ad-102">RunCode マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="5a9ad-102">RunCode macro action</span></span>


<span data-ttu-id="5a9ad-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a9ad-104">**RunCode** アクションを使用すると、Visual Basic for Applications (VBA) の Function プロシージャを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="5a9ad-105">設定</span><span class="sxs-lookup"><span data-stu-id="5a9ad-105">Setting</span></span>

<span data-ttu-id="5a9ad-106">**RunCode** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a9ad-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="5a9ad-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5a9ad-108">説明</span><span class="sxs-lookup"><span data-stu-id="5a9ad-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a9ad-109"><strong>Function Name/関数名</strong></span><span class="sxs-lookup"><span data-stu-id="5a9ad-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5a9ad-p101">呼び出す VBA の Function プロシージャの名前を指定します。関数の引数はかっこ ( ) で囲みます。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>関数名</strong>] ボックスに関数名を入力します。この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="5a9ad-p101">The name of the VBA Function procedure to call. Enclose any function arguments in parentheses. Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="5a9ad-p102">Access データベース (.mdb または .accdb) では、[<STRONG>ビルド</STRONG>] をクリックし、式ビルダーを使用してこの引数の関数を選択します。式ビルダーに表示される一覧で目的の関数をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-p102">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to select a function for this argument. Click the desired function in the list in the Expression Builder.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5a9ad-116">解説</span><span class="sxs-lookup"><span data-stu-id="5a9ad-116">Remarks</span></span>

<span data-ttu-id="5a9ad-117">ユーザー定義の Function プロシージャは、Microsoft Access のモジュールに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="5a9ad-118">次の例のように、Function プロシージャに引数を指定しない場合でも、かっこを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="5a9ad-119">イベント プロパティの設定に使用されるユーザー定義関数名とは異なり、引数に**関数名**関数名で始まらない等号 (=) (**=**)。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="5a9ad-120">関数の戻り値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-120">Access ignores the return value of the function.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5a9ad-121">[!メモ] 関数名とモジュール名が同じ場合、マクロから Function プロシージャを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="5a9ad-p103">[!ヒント] Visual Basic で記述した Sub プロシージャまたはイベント プロシージャを実行するには、Sub プロシージャまたはイベント プロシージャを呼び出す Function プロシージャを作成します。その後、 <STRONG>RunCode</STRONG> アクションを使用して、Function プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-p103">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure. Then use the <STRONG>RunCode</STRONG> action to run the Function procedure.</span></span></P>



<span data-ttu-id="5a9ad-p104">**RunCode** アクションを使用して関数を呼び出すと、 **Function Name/関数名** 引数で指定した名前の関数が、データベースの標準モジュールで検索されます。ただし、フォームまたはレポートでメニュー コマンドをクリックしてこのアクションを実行した場合や、フォームまたはレポートのイベントに応じてこのアクションが実行された場合、この関数は、最初にフォームまたはレポートのクラス モジュールで検索され、次に標準モジュールで検索されます。 **Function Name/関数名** 引数で指定した関数は、ナビゲーション ウィンドウの [ **モジュール**] 領域に表示されるクラス モジュールでは検索されません。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-p104">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database. However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules. Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="5a9ad-p105">このアクションは VBA モジュールでは使用できません。VBA では、目的の Function プロシージャを直接実行してください。</span><span class="sxs-lookup"><span data-stu-id="5a9ad-p105">This action isn't available in a VBA module. Instead, run the desired Function procedure directly in VBA.</span></span>

