---
title: 汎用 DLL の関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420599"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="15c58-104">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="15c58-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="15c58-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="15c58-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="15c58-p101">サンプル DLL GENERIC.xll をコンパイルするために必要な Microsoft Visual Studio プロジェクト ファイルとソース コード ファイルは、`\EXAMPLES\GENERIC\` フォルダーに格納されています。このプロジェクトをテンプレートとして使用して独自の Microsoft Excel XLL を作成できます。このプロジェクトのソース コードには、Excel C API の多くの機能が示されています。</span><span class="sxs-lookup"><span data-stu-id="15c58-p101">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll. You can use this project as a template for writing your own Microsoft Excel XLLs. The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="15c58-109">GENERIC.xll を読み込むと、次の 4 つのコマンドがある **[Generic]** メニューが作成されます。</span><span class="sxs-lookup"><span data-stu-id="15c58-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="15c58-110">**Dialog** - [Microsoft Excel] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="15c58-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="15c58-111">**Dance** - **ESC** を押すまで選択範囲を移動します。</span><span class="sxs-lookup"><span data-stu-id="15c58-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="15c58-112">**Native Dialog** - [Windows] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="15c58-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="15c58-113">**Exit** - GENERIC.xll をアンロードし、**[Generic]** メニューを削除します。</span><span class="sxs-lookup"><span data-stu-id="15c58-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="15c58-p102">GENERIC.xll には、ワークシート関数 Func1、FuncSum、および FuncFib も用意されています。GENERIC.xll を読み込むと常に、これらの関数を使用できるようになります。GENERIC.xll は、アドイン マネージャーを使用して読み込むことができます。最後の Excel セッションが正常に終了した時点でアクティブになっていた場合は、その次のセッションでも読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="15c58-p102">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded. GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="15c58-116">このプロジェクトでは、フレームワーク ライブラリ (FRMWRK32.lib) を使用します。</span><span class="sxs-lookup"><span data-stu-id="15c58-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="15c58-117">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="15c58-117">In this section</span></span>

[<span data-ttu-id="15c58-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="15c58-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="15c58-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="15c58-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="15c58-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="15c58-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="15c58-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="15c58-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="15c58-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="15c58-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="15c58-123">fDance</span><span class="sxs-lookup"><span data-stu-id="15c58-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="15c58-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="15c58-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="15c58-125">fExit</span><span class="sxs-lookup"><span data-stu-id="15c58-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="15c58-126">Func1</span><span class="sxs-lookup"><span data-stu-id="15c58-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="15c58-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="15c58-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="15c58-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="15c58-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="15c58-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="15c58-129">See also</span></span>



[<span data-ttu-id="15c58-130">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="15c58-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

