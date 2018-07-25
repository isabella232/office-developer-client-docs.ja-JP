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
# <a name="developing-excel-xlls"></a><span data-ttu-id="cb4a1-104">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="cb4a1-104">Developing Excel XLLs</span></span>

<span data-ttu-id="cb4a1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb4a1-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cb4a1-106">Microsoft Excel XLL を記述し、C API を使用する主な理由は、高パフォーマンスなワークシート関数を作成するためです。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="cb4a1-107">高パフォーマンスの関数のアプリケーション (Excel 2007 以降では強力なサーバー リソースに対するマルチ スレッドのインターフェイスを記述する機能) を考えると、XLL は Excel の機能拡張の非常に重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="cb4a1-108">XLL のパフォーマンスは、新しいデータ型の追加や、マルチ スレッドのサポート (最重要) により、Excel 2007 でさらに向上しました。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="cb4a1-p102">C API には、Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework の高度で迅速な開発機能はありません。メモリ管理は低レベルで行われるので、開発者により大きな責任を負わせることになります。COM を通じて公開されている多くの Excel 機能は、VBA と.NET Framework を通じて利用できますが、C API には公開されていません。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-p102">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework. Memory management is low level, and therefore puts greater responsibility on the developer. Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="cb4a1-112">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="cb4a1-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="cb4a1-113">DLL の操作</span><span class="sxs-lookup"><span data-stu-id="cb4a1-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="cb4a1-114">Excel での XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="cb4a1-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- <span data-ttu-id="cb4a1-115">[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span><span class="sxs-lookup"><span data-stu-id="cb4a1-115">[How to: Call XLL Functions from the Function Wizard or Replace Dialog Boxes](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span></span>
  
- [<span data-ttu-id="cb4a1-116">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="cb4a1-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="cb4a1-117">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="cb4a1-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="cb4a1-118">名前と他のワークシートの数式を評価する</span><span class="sxs-lookup"><span data-stu-id="cb4a1-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="cb4a1-119">マルチスレッド処理とメモリ管理</span><span class="sxs-lookup"><span data-stu-id="cb4a1-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="cb4a1-120">非同期のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="cb4a1-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="cb4a1-121">クラスター セーフ関数</span><span class="sxs-lookup"><span data-stu-id="cb4a1-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="cb4a1-122">時間のかかる操作でユーザーによる中断を許可する</span><span class="sxs-lookup"><span data-stu-id="cb4a1-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="cb4a1-123">DLL または XLL ファイルの中からダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="cb4a1-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="cb4a1-124">Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="cb4a1-124">How to: Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="cb4a1-125">下位互換性</span><span class="sxs-lookup"><span data-stu-id="cb4a1-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

