---
title: 時間のかかる操作でユーザーによる中断を許可する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007],concurrent tasks [Excel 2007],user breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798935"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="68cc2-104">時間のかかる操作でユーザーによる中断を許可する</span><span class="sxs-lookup"><span data-stu-id="68cc2-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="68cc2-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="68cc2-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="68cc2-106">Windows ではプリエンプティブ マルチタスキングを使用しますが、実行に時間のかかる関数やコマンドについては、オペレーティング システムのために時間を確保し、同時実行タスクをもう一度計画できるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="68cc2-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks. Using native Windows calls, you can do this by using the sleep function. Using the C API, you can do it by using the xlAbort function, which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, ESC.</span></span> <span data-ttu-id="68cc2-107">ネイティブ Windows 呼び出しを使用している場合は、Sleep 関数を使って実行できます。</span><span class="sxs-lookup"><span data-stu-id="68cc2-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="68cc2-108">C API を使用している場合は、[xlAbort 関数](xlabort.md) を使って実行できます。これは、一時的なプロセッサを生成するだけではなく、ユーザーがキャンセル キー **Esc** を押したかどうかも確認します。</span><span class="sxs-lookup"><span data-stu-id="68cc2-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="68cc2-p102">その結果、**xlAbort** 関数により、ユーザーがプロセスを終了し、必要なクリーンアップを実行して、Excel にコントロールを返すかどうかをコードで確認できます。また、中断状態を解除することができます。これにより、ユーザーがコマンドを終了するかどうかを確認するダイアログ ボックスをコマンドで表示できます。コマンドを終了しない場合は、引数 *FALSE* で **xlAbort** 関数を呼び出して、中断を解除できます (既定の引数は *TRUE* です。これは状態を確認するだけで解除しません。)。</span><span class="sxs-lookup"><span data-stu-id="68cc2-p102">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel. The function also enables you to clear the break condition. This enables your commands to display a dialog box to verify whether the user wants to end the command. If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break. (The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="68cc2-p103">ユーザー定義関数 (UDF) や XLL コマンドから **xlAbort** 関数を呼び出すことができます。UDF では、ユーザーによる中断が検出されて、**xlAbort** 関数が **TRUE** を返す場合、通常、関数の計算が中断され、計算が完了しなかったことを示す特定の値 (エラーや 0) が返されます。時間のかかる関数の他のインスタンス (同じようにこの状態を確認する) も中断されるように、この中断状態を解除しないでください。Excel は、再計算の終了時にこの状態を暗黙的に解除します。</span><span class="sxs-lookup"><span data-stu-id="68cc2-p103">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command. In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero. You would not clear the break condition so that other instances of lengthy functions that also check this condition also break. Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="68cc2-118">Excel はコマンドの終了時にこの状態を暗黙的に解除しますが、コマンドで中断状態が検出された場合、通常は引数 **FALSE** を指定して **xlAbort** 関数を呼び出して状態を解除します。</span><span class="sxs-lookup"><span data-stu-id="68cc2-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68cc2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="68cc2-119">See also</span></span>



[<span data-ttu-id="68cc2-120">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="68cc2-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="68cc2-121">Excel でのマルチスレッド再計算</span><span class="sxs-lookup"><span data-stu-id="68cc2-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="68cc2-122">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="68cc2-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="68cc2-123">Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="68cc2-123">How to: Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

