---
title: RunMacro マクロ アクション
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d9e86fb7d60af94d6ecde71b2a857a3cc5b9bcb8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712338"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="93f97-102">RunMacro マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="93f97-102">RunMacro macro action</span></span>

<span data-ttu-id="93f97-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="93f97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93f97-p101">**RunMacro** アクションを使用すると、マクロを実行できます。マクロ グループ内のマクロも実行できます。</span><span class="sxs-lookup"><span data-stu-id="93f97-p101">You can use the **RunMacro** action to run a macro. The macro can be in a macro group.</span></span>

<span data-ttu-id="93f97-106">このアクションは、次のような場合に使うと効果的です。</span><span class="sxs-lookup"><span data-stu-id="93f97-106">You can use this action:</span></span>

- <span data-ttu-id="93f97-107">マクロ内から別のマクロを実行する場合</span><span class="sxs-lookup"><span data-stu-id="93f97-107">To run a macro from within another macro.</span></span>

- <span data-ttu-id="93f97-108">特定の条件に基づいてマクロを実行する場合</span><span class="sxs-lookup"><span data-stu-id="93f97-108">To run a macro based on a certain condition.</span></span>

- <span data-ttu-id="93f97-109">独自のメニュー コマンドにマクロを割り当てる場合</span><span class="sxs-lookup"><span data-stu-id="93f97-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="93f97-110">設定</span><span class="sxs-lookup"><span data-stu-id="93f97-110">Setting</span></span>

<span data-ttu-id="93f97-111">**RunMacro** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="93f97-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93f97-112">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="93f97-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="93f97-113">説明</span><span class="sxs-lookup"><span data-stu-id="93f97-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93f97-114"><strong>マクロ名</strong></span><span class="sxs-lookup"><span data-stu-id="93f97-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="93f97-115">実行するマクロの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93f97-115">The name of the macro to run.</span></span> <span data-ttu-id="93f97-116">マクロ ビルダー] ウィンドウの [<strong>マクロ名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベース内のすべてのマクロ (およびマクロ グループ) を示しています。</span><span class="sxs-lookup"><span data-stu-id="93f97-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="93f97-117">マクロがマクロ グループ内にある場合は、リストにマクロ グループ名の下<em>中</em>として表示されます。<em>マクロ名</em>です。</span><span class="sxs-lookup"><span data-stu-id="93f97-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="93f97-118">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="93f97-118">This is a required argument.</span></span> <span data-ttu-id="93f97-119"><strong>ライブラリ データベースでこのアクション</strong>を含むマクロを実行すると、Access はライブラリ データベースでこの名前のマクロを検索し、現在のデータベース内に正しく表示されないです。</span><span class="sxs-lookup"><span data-stu-id="93f97-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93f97-120"><strong>Repeat Count/実行回数</strong></span><span class="sxs-lookup"><span data-stu-id="93f97-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="93f97-p103">マクロの最大実行回数を指定します。この引数および <strong>Repeat Expression/繰り返し条件式</strong> 引数を指定しない場合、マクロは 1 回だけ実行されます。  </span><span class="sxs-lookup"><span data-stu-id="93f97-p103">The maximum number of times the macro will run. If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93f97-123"><strong>Repeat Expression/繰り返し条件式</strong></span><span class="sxs-lookup"><span data-stu-id="93f97-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="93f97-124"><strong>True</strong> (-1) または<strong>False</strong> (0) に評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93f97-124">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0).</span></span> <span data-ttu-id="93f97-125">式が <strong>False</strong> に評価される場合、マクロの実行は停止します。</span><span class="sxs-lookup"><span data-stu-id="93f97-125">The macro stops running if the expression evaluates to <strong>False</strong>.</span></span> <span data-ttu-id="93f97-126">この式は、マクロを実行するたびに評価されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-126">The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="93f97-127">解説</span><span class="sxs-lookup"><span data-stu-id="93f97-127">Remarks</span></span>

<span data-ttu-id="93f97-128">**Macro Name/マクロ名** 引数にマクロ グループ名を入力すると、マクロ グループ内の最初のマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="93f97-p105">このアクションの動作は、[ **データベース ツール**] タブの [ **マクロの実行**] をクリックし、マクロを選択して、[ **OK**] をクリックした場合と同じです。ただし、このコマンドではマクロを 1 回だけ実行するのに対し、 **RunMacro** アクションでは必要なだけ何回でもマクロを実行できます。</span><span class="sxs-lookup"><span data-stu-id="93f97-p105">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**. However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>

> [!TIP]
> <span data-ttu-id="93f97-131">[!ヒント] **Repeat Count/実行回数** 引数および **Repeat Expression/繰り返し条件式** 引数を使用すると、マクロの実行回数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="93f97-131">You can use the **Repeat Count** and **Repeat Expression** arguments to determine how many times the macro runs:</span></span>
> - <span data-ttu-id="93f97-132">どちらの引数も指定しない場合、マクロは 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-132">If you leave both arguments blank, the macro runs once.</span></span>
> - <span data-ttu-id="93f97-133">**Repeat Count/実行回数** を指定し、 **Repeat Expression/繰り返し条件式** 引数を指定しない場合、マクロは指定した回数だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>
> - <span data-ttu-id="93f97-134">**Repeat Count/実行回数** 引数を指定せずに、 **Repeat Expression/繰り返し条件式** 引数に式を入力した場合、マクロは、式が **False** に評価されるまで実行されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>
> - <span data-ttu-id="93f97-135">両方の引数に値を入力した場合、マクロは、 **Repeat Count/実行回数** 引数に指定した回数だけ実行されるか、 **Repeat Expression/繰り返し条件式** 引数が **False** に評価されるまで実行されます。これは、先に当てはまる方が適用されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="93f97-p106">**RunMacro** アクションを含むマクロを実行し、 **RunMacro** アクションに到達すると、呼び出されたマクロが実行されます。呼び出されたマクロの実行が終了すると、元のマクロに戻り、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-p106">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro. When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>

> [!NOTE]
> - <span data-ttu-id="93f97-138">同じマクロ グループ内または別のマクロ グループ内のマクロを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="93f97-138">You can call a macro in the same macro group or in another macro group.</span></span>
> - <span data-ttu-id="93f97-p107">マクロはネストすることができます。たとえば、マクロ A からマクロ B を呼び出し、さらにマクロ B から別のマクロを呼び出すことができます。呼び出されたマクロの実行が終了すると、呼び出し元のマクロに戻り、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="93f97-p107">You can nest macros. That is, you can run macro A, which in turn calls macro B, and so on. In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span>

<span data-ttu-id="93f97-142">Visual Basic for Applications (VBA) モジュールで **RunMacro** アクションを実行するには、 **DoCmd** オブジェクトの **RunMacro** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="93f97-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

