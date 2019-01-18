---
title: Excel のコマンド、関数、および状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716237"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="f478d-104">Excel のコマンド、関数、および状態</span><span class="sxs-lookup"><span data-stu-id="f478d-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="f478d-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f478d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f478d-106">Microsoft Excel は、コマンドと関数という、2 種類の別々の追加機能を識別します。</span><span class="sxs-lookup"><span data-stu-id="f478d-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="f478d-107">コマンド</span><span class="sxs-lookup"><span data-stu-id="f478d-107">Commands</span></span>

<span data-ttu-id="f478d-108">Excel のコマンドには次のような特性があります。</span><span class="sxs-lookup"><span data-stu-id="f478d-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="f478d-109">ユーザーが行うのと同じ方法でアクションを実行する。</span><span class="sxs-lookup"><span data-stu-id="f478d-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="f478d-110">Excel の設定を変更する、ドキュメントを開く、閉じる、編集する、再計算を開始するなど、ユーザーが実行可能なあらゆる操作 (使用するインターフェイスの制限に依存します) を実行できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="f478d-111">トラップされた特定のイベントが発生したときに、呼び出されるようセットアップできる。</span><span class="sxs-lookup"><span data-stu-id="f478d-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="f478d-112">ダイアログ ボックスを表示でき、ユーザーと対話できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="f478d-113">左クリックなど、オブジェクト上でアクションが行われるときに呼び出されるように、オブジェクトの制御にリンクできる。</span><span class="sxs-lookup"><span data-stu-id="f478d-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="f478d-114">再計算中に Excel がコマンドを呼び出すことはない。</span><span class="sxs-lookup"><span data-stu-id="f478d-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="f478d-115">再計算中に関数がコマンドを呼び出すことはできない。</span><span class="sxs-lookup"><span data-stu-id="f478d-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="f478d-116">関数</span><span class="sxs-lookup"><span data-stu-id="f478d-116">Functions</span></span>

<span data-ttu-id="f478d-117">Excel の関数は、次のことを実行します。</span><span class="sxs-lookup"><span data-stu-id="f478d-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="f478d-118">通常、引数を受け取り、常に結果を返す。</span><span class="sxs-lookup"><span data-stu-id="f478d-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="f478d-119">Excel の式の部分として、1 つ以上のセルに入力できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="f478d-120">定義された名前定義で使用できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="f478d-121">条件付き書式の制限およびしきい値の式で使用できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="f478d-122">コマンドで関数を呼び出せる。</span><span class="sxs-lookup"><span data-stu-id="f478d-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="f478d-123">関数がコマンドを呼び出すことはできない。</span><span class="sxs-lookup"><span data-stu-id="f478d-123">They cannot call commands.</span></span>
    
<span data-ttu-id="f478d-p101">さらに Excel では、ユーザー定義ワークシート関数と、マクロ シート上で動作するよう設計されたユーザー定義関数とを区別しています。Excel では、ユーザー定義のマクロ シート関数がマクロ シートだけで使用されるように制限することはありません。これらの関数は、通常のワークシート関数を使用できる場所であればどこでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f478d-p101">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets. Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="f478d-126">ワークシート関数</span><span class="sxs-lookup"><span data-stu-id="f478d-126">Worksheet Functions</span></span>

<span data-ttu-id="f478d-127">Excel ワークシート関数には、次の事項が当てはまります。</span><span class="sxs-lookup"><span data-stu-id="f478d-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="f478d-128">マクロ シート情報関数にはアクセスできない。</span><span class="sxs-lookup"><span data-stu-id="f478d-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="f478d-129">計算されていないセルの値を取得できない。</span><span class="sxs-lookup"><span data-stu-id="f478d-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="f478d-130">Excel 2007 以降では、スレッド セーフとして作成し、登録できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="f478d-131">マクロシート関数</span><span class="sxs-lookup"><span data-stu-id="f478d-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="f478d-132">Excel マクロシート関数には、次の事項が当てはまります。</span><span class="sxs-lookup"><span data-stu-id="f478d-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="f478d-133">マクロ シート情報関数にアクセスできる。</span><span class="sxs-lookup"><span data-stu-id="f478d-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="f478d-134">呼び出し元のセルの値を含む再計算されたセルの値を取得できる。</span><span class="sxs-lookup"><span data-stu-id="f478d-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="f478d-135">Excel 2007 以降では、スレッド セーフとみなされない。</span><span class="sxs-lookup"><span data-stu-id="f478d-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="f478d-136">どのように Excel でユーザー定義関数 (UDF) を操作するか、関数のどんな動作を許可するか、どのように関数を再計算するかは、関数を登録するときにすべて定義します。</span><span class="sxs-lookup"><span data-stu-id="f478d-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="f478d-137">関数がワークシート関数として登録されているにもかかわらず、マクロシート関数だけが実行できる操作を実行しようとすると、その操作は失敗します。</span><span class="sxs-lookup"><span data-stu-id="f478d-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="f478d-138">Excel 2007 以降、スレッド セーフとして登録されているワークシート関数がマクロ シート関数を呼び出そうとする場合にも、操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="f478d-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="f478d-139">Excel は、Microsoft Visual Basic for Applications (VBA) の UDF をマクロ シート等価の関数として扱います。それらの UDF はワークスペース情報と計算されないセルの値にアクセスでき、Excel 2007 以降、スレッド セーフとはみなされません。</span><span class="sxs-lookup"><span data-stu-id="f478d-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="f478d-140">Excel の状態</span><span class="sxs-lookup"><span data-stu-id="f478d-140">Excel States</span></span>

<span data-ttu-id="f478d-141">ユーザー、外部プロセス、マクロを実行するトラップされたイベント、または時間指定の Excel のハウスキーピング イベント (**Autosave** など) のアクションによって、Excel はどの時点でも、数ある状態のうちのどれか 1 つに入ります。</span><span class="sxs-lookup"><span data-stu-id="f478d-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="f478d-142">ユーザーは、次のような状態を経験します。</span><span class="sxs-lookup"><span data-stu-id="f478d-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="f478d-p103">**準備完了状態:** 実行中のコマンドやマクロはありません。表示しているダイアログ ボックスはありません。編集されているセルはなく、ユーザーは切り取り、コピー、貼り付けの操作の途中ではありません。フォーカスしている埋め込みオブジェクトはありません。</span><span class="sxs-lookup"><span data-stu-id="f478d-p103">**Ready state:** No commands or macros are being run. No dialog boxes are being displayed. No cells are being edited and the user is not in the middle of a cut/copy and paste operation. No embedded object has focus.</span></span> 
    
- <span data-ttu-id="f478d-147">**編集モード:** ユーザーが、ロック解除されたセル、または保護されていないセルに、有効な入力文字を入力し始めた場合や、1 つ以上のロック解除されたセルまたは保護されていないセルで **F2** キーを押した場合です。</span><span class="sxs-lookup"><span data-stu-id="f478d-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="f478d-148">**切り取り、コピー、貼り付けモード:** ユーザーがセルまたはセル範囲を切り取ったりコピーしたりして、それをまだ貼り付けていない場合や、複数の貼り付け操作が可能な [形式を選択して貼り付け] ダイアログ ボックスを使用して貼り付けた場合です。</span><span class="sxs-lookup"><span data-stu-id="f478d-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="f478d-149">**ポイント モード:** ユーザーは、数式を編集中で、編集している数式にアドレスが追加されるセルを選択しているところです。</span><span class="sxs-lookup"><span data-stu-id="f478d-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="f478d-p104">ユーザーは、編集、ポイント、貼り付け、コピー モードを **[ESC]** キーを押すことによって解除でき、Excel は準備完了状態に戻ります。他のイベントでは、これらの状態を次のように解除することができます。</span><span class="sxs-lookup"><span data-stu-id="f478d-p104">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state. Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="f478d-152">ユーザーがビルトイン ダイアログ ボックスを開く。</span><span class="sxs-lookup"><span data-stu-id="f478d-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="f478d-153">ユーザーが再計算を開始する。</span><span class="sxs-lookup"><span data-stu-id="f478d-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="f478d-154">ユーザーがコマンドを実行する。</span><span class="sxs-lookup"><span data-stu-id="f478d-154">The user runs a command.</span></span>
    
- <span data-ttu-id="f478d-155">Excel が **Autosave** 操作を実行する。</span><span class="sxs-lookup"><span data-stu-id="f478d-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="f478d-156">タイマー イベントがトラップされる。</span><span class="sxs-lookup"><span data-stu-id="f478d-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="f478d-p105">最後の例は、アドイン開発者にとって重要です。タイマー イベント トラップが頻繁に設定され実行されることが、Excel の通常の使いやすさに及ぼす影響を検討する必要があります。この点がアドインの機能性にとって重要な部分である場合、ユーザーが必要に応じて切り取り、コピー、貼り付けの操作を正常に行えるように、アドインの実行を一時的に中断する分かりやすい方法をユーザーに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f478d-p105">The last example is of importance to add-in developers. You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed. When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f478d-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="f478d-160">See also</span></span>



[<span data-ttu-id="f478d-161">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="f478d-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="f478d-162">時間のかかる操作でユーザーによる中断を許可する</span><span class="sxs-lookup"><span data-stu-id="f478d-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

