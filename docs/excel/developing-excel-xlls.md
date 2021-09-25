---
title: Excel XLL の開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- アドイン - [excel 2007],XLL の開発 - [Excel 2007],XLL - [Excel 2007],開発
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: c255e973afa7b8a1ae8fa58b567f980b158a82e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614606"
---
# <a name="developing-excel-xlls"></a>Excel XLL の開発

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions. The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility. The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.
  
C API には、Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework の高度で迅速な開発機能はありません。メモリ管理は低レベルで行われるので、開発者により大きな責任を負わせることになります。COM を通じて公開されている多くの Excel 機能は、VBA と.NET Framework を通じて利用できますが、C API には公開されていません。


- [Excel プログラミングの概念](excel-programming-concepts.md)
  
- [DLL の操作](working-with-dlls.md)
  
- [Excel での XLL コードへのアクセス](accessing-xll-code-in-excel.md)
  
- [関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [DLL または XLL から Excel に呼び出す](calling-into-excel-from-the-dll-or-xll.md)
  
- [XLL を作成する](creating-xlls.md)
  
- [名前と他のワークシートの数式を評価する](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [マルチスレッド処理とメモリ管理](multithreading-and-memory-management.md)
  
- [非同期のユーザー定義関数](asynchronous-user-defined-functions.md)
  
- [クラスター セーフ関数](cluster-safe-functions.md)
  
- [時間のかかる操作でユーザーによる中断を許可する](permitting-user-breaks-in-lengthy-operations.md)
  
- [DLL または XLL ファイルの中からダイアログ ボックスを表示する](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス](how-to-access-excel-instance-and-main-window-handles.md)
  
- [下位互換性](backward-compatibility.md)
  

