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
ms.openlocfilehash: 650af14e4e97ebd2642a4442a87965f313d3b556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414691"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>時間のかかる操作でユーザーによる中断を許可する

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks. Using native Windows calls, you can do this by using the sleep function. Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.
  
その結果、**xlAbort** 関数により、ユーザーがプロセスを終了し、必要なクリーンアップを実行して、Excel にコントロールを返すかどうかをコードで確認できます。また、中断状態を解除することができます。これにより、ユーザーがコマンドを終了するかどうかを確認するダイアログ ボックスをコマンドで表示できます。コマンドを終了しない場合は、引数 *FALSE* で **xlAbort** 関数を呼び出して、中断を解除できます (既定の引数は *TRUE* です。これは状態を確認するだけで解除しません。)。 
  
ユーザー定義関数 (UDF) や XLL コマンドから **xlAbort** 関数を呼び出すことができます。UDF では、ユーザーによる中断が検出されて、**xlAbort** 関数が **TRUE** を返す場合、通常、関数の計算が中断され、計算が完了しなかったことを示す特定の値 (エラーや 0) が返されます。時間のかかる関数の他のインスタンス (同じようにこの状態を確認する) も中断されるように、この中断状態を解除しないでください。Excel は、再計算の終了時にこの状態を暗黙的に解除します。
  
Excel はコマンドの終了時にこの状態を暗黙的に解除しますが、コマンドで中断状態が検出された場合、通常は引数 **FALSE** を指定して **xlAbort** 関数を呼び出して状態を解除します。
  
## <a name="see-also"></a>関連項目



[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
  
[Excel XLL の開発](developing-excel-xlls.md)
  
[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)

