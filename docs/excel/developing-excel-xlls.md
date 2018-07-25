---
title: Excel XLL の開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- アドイン - [excel 2007],XLL の開発 - [Excel 2007],XLL - [Excel 2007],開発
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798780"
---
# <a name="developing-excel-xlls"></a>Excel XLL の開発

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel XLL を記述し、C API を使用する主な理由は、高パフォーマンスなワークシート関数を作成するためです。 高パフォーマンスの関数のアプリケーション (Excel 2007 以降では強力なサーバー リソースに対するマルチ スレッドのインターフェイスを記述する機能) を考えると、XLL は Excel の機能拡張の非常に重要な部分です。 XLL のパフォーマンスは、新しいデータ型の追加や、マルチ スレッドのサポート (最重要) により、Excel 2007 でさらに向上しました。
  
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
  

