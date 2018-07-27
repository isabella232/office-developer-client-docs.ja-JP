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
# <a name="permitting-user-breaks-in-lengthy-operations"></a>時間のかかる操作でユーザーによる中断を許可する

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Windows ではプリエンプティブ マルチタスキングを使用しますが、実行に時間のかかる関数やコマンドについては、オペレーティング システムのために時間を確保し、同時実行タスクをもう一度計画できるようにすることをお勧めします。 ネイティブ Windows 呼び出しを使用している場合は、Sleep 関数を使って実行できます。 C API を使用している場合は、[xlAbort 関数](xlabort.md) を使って実行できます。これは、一時的なプロセッサを生成するだけではなく、ユーザーがキャンセル キー **Esc** を押したかどうかも確認します。
  
その結果、**xlAbort** 関数により、ユーザーがプロセスを終了し、必要なクリーンアップを実行して、Excel にコントロールを返すかどうかをコードで確認できます。また、中断状態を解除することができます。これにより、ユーザーがコマンドを終了するかどうかを確認するダイアログ ボックスをコマンドで表示できます。コマンドを終了しない場合は、引数 *FALSE* で **xlAbort** 関数を呼び出して、中断を解除できます (既定の引数は *TRUE* です。これは状態を確認するだけで解除しません。)。 
  
ユーザー定義関数 (UDF) や XLL コマンドから **xlAbort** 関数を呼び出すことができます。UDF では、ユーザーによる中断が検出されて、**xlAbort** 関数が **TRUE** を返す場合、通常、関数の計算が中断され、計算が完了しなかったことを示す特定の値 (エラーや 0) が返されます。時間のかかる関数の他のインスタンス (同じようにこの状態を確認する) も中断されるように、この中断状態を解除しないでください。Excel は、再計算の終了時にこの状態を暗黙的に解除します。
  
Excel はコマンドの終了時にこの状態を暗黙的に解除しますが、コマンドで中断状態が検出された場合、通常は引数 **FALSE** を指定して **xlAbort** 関数を呼び出して状態を解除します。
  
## <a name="see-also"></a>関連項目



[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
  
[Excel XLL の開発](developing-excel-xlls.md)
  
[Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)

