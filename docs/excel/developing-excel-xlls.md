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
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701096"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="9df20-104">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="9df20-104">Developing Excel XLLs</span></span>

<span data-ttu-id="9df20-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9df20-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9df20-106">Microsoft Excel XLL を記述し、C API を使用する主な理由は、高パフォーマンスなワークシート関数を作成するためです。</span><span class="sxs-lookup"><span data-stu-id="9df20-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="9df20-107">高パフォーマンスの関数のアプリケーション (Excel 2007 以降では強力なサーバー リソースに対するマルチ スレッドのインターフェイスを記述する機能) を考えると、XLL は Excel の機能拡張の非常に重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="9df20-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="9df20-108">XLL のパフォーマンスは、新しいデータ型の追加や、マルチ スレッドのサポート (最重要) により、Excel 2007 でさらに向上しました。</span><span class="sxs-lookup"><span data-stu-id="9df20-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="9df20-p102">C API には、Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework の高度で迅速な開発機能はありません。メモリ管理は低レベルで行われるので、開発者により大きな責任を負わせることになります。COM を通じて公開されている多くの Excel 機能は、VBA と.NET Framework を通じて利用できますが、C API には公開されていません。</span><span class="sxs-lookup"><span data-stu-id="9df20-p102">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework. Memory management is low level, and therefore puts greater responsibility on the developer. Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="9df20-112">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="9df20-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="9df20-113">DLL の操作</span><span class="sxs-lookup"><span data-stu-id="9df20-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="9df20-114">Excel での XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="9df20-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- <span data-ttu-id="9df20-115">[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span><span class="sxs-lookup"><span data-stu-id="9df20-115">[Call XLL Functions from the Function Wizard or Replace Dialog Boxes](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span></span>
  
- [<span data-ttu-id="9df20-116">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="9df20-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="9df20-117">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="9df20-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="9df20-118">名前と他のワークシートの数式を評価する</span><span class="sxs-lookup"><span data-stu-id="9df20-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="9df20-119">マルチスレッド処理とメモリ管理</span><span class="sxs-lookup"><span data-stu-id="9df20-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="9df20-120">非同期のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="9df20-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="9df20-121">クラスター セーフ関数</span><span class="sxs-lookup"><span data-stu-id="9df20-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="9df20-122">時間のかかる操作でユーザーによる中断を許可する</span><span class="sxs-lookup"><span data-stu-id="9df20-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="9df20-123">DLL または XLL ファイルの中からダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="9df20-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="9df20-124">Excel インスタンスとメイン ウィンドウ ハンドルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="9df20-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="9df20-125">下位互換性</span><span class="sxs-lookup"><span data-stu-id="9df20-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

