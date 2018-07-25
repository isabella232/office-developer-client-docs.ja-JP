---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798975"
---
# <a name="xleventregister"></a><span data-ttu-id="41408-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="41408-103">xlEventRegister</span></span>

 <span data-ttu-id="41408-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="41408-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="41408-p101">Excel 2010 で導入されたイベント ハンドラーの登録に使用します。</span><span class="sxs-lookup"><span data-stu-id="41408-p101">Used to register an event handler. Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="41408-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41408-107">Parameters</span></span>

 <span data-ttu-id="41408-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="41408-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="41408-109">DLL コードで示されている、イベント ハンドラー関数の名前。</span><span class="sxs-lookup"><span data-stu-id="41408-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="41408-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="41408-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="41408-111">_pxProcedure_ パラメーターで指定した関数によって処理されるイベント。</span><span class="sxs-lookup"><span data-stu-id="41408-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="41408-112">Excel 2010 以降の Excel では、次のイベントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="41408-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="41408-113">**イベント**</span><span class="sxs-lookup"><span data-stu-id="41408-113">**Event**</span></span>|<span data-ttu-id="41408-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="41408-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41408-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="41408-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="41408-p102">Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。</span><span class="sxs-lookup"><span data-stu-id="41408-p102">Raised when Excel completes a calculation. You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="41408-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="41408-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="41408-p103">ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、CalculationEnded イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="41408-p103">Raised when the user interrupts the calculation. The XLL should stop any asynchronous activities. The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="41408-122">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="41408-122">Property Value/Return Value</span></span>

<span data-ttu-id="41408-123">成功した場合、**TRUE** (**xltypeBool**) を返します。</span><span class="sxs-lookup"><span data-stu-id="41408-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="41408-124">失敗した場合は、**FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="41408-124">If successful, returns **TRUE** (xltypeBool). If unsuccessful, returns FALSE.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41408-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="41408-125">See also</span></span>



[<span data-ttu-id="41408-126">非同期のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="41408-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

