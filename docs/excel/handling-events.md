---
title: イベントの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798877"
---
# <a name="handling-events"></a><span data-ttu-id="c4f7a-103">イベントの処理</span><span class="sxs-lookup"><span data-stu-id="c4f7a-103">Handling Events</span></span>

 <span data-ttu-id="c4f7a-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c4f7a-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c4f7a-p101">Excel 2010 以降の XLL は、非同期関数のライフ サイクルを管理するために設計されたイベントを受信できます。これらのイベントは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-p101">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle. The events are as follows:</span></span>
  
- <span data-ttu-id="c4f7a-p102">**CalculationEnded**: Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-p102">**CalculationEnded**: Raised when Excel is finished calculating. After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="c4f7a-p103">**CalculationCanceled**: ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、**CalculationEnded** イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-p103">**CalculationCanceled**: Raised when the user interrupts the calculation. The XLL stops any asynchronous activities. Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="c4f7a-112">これらのイベントを処理するために、XLL では C API 関数の [xlEventRegister](xleventregister.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c4f7a-113">プログラムによる再計算中は、**CalculationEnded** と **CalculationCanceled** は発生しません。</span><span class="sxs-lookup"><span data-stu-id="c4f7a-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

