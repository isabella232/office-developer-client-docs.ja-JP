---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160280"
---
# <a name="xleventregister"></a><span data-ttu-id="7e448-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="7e448-103">xlEventRegister</span></span>

 <span data-ttu-id="7e448-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e448-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7e448-p101">Excel 2010 で導入されたイベント ハンドラーの登録に使用します。</span><span class="sxs-lookup"><span data-stu-id="7e448-p101">Used to register an event handler. Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="7e448-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e448-107">Parameters</span></span>

 <span data-ttu-id="7e448-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="7e448-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="7e448-109">DLL コードで示されている、イベント ハンドラー関数の名前。</span><span class="sxs-lookup"><span data-stu-id="7e448-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="7e448-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="7e448-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="7e448-111">_pxProcedure_ パラメーターで指定した関数によって処理されるイベント。</span><span class="sxs-lookup"><span data-stu-id="7e448-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="7e448-112">Excel 2010 以降の Excel では、次のイベントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7e448-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="7e448-113">**イベント**</span><span class="sxs-lookup"><span data-stu-id="7e448-113">**Event**</span></span>|<span data-ttu-id="7e448-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="7e448-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e448-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="7e448-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="7e448-p102">Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。</span><span class="sxs-lookup"><span data-stu-id="7e448-p102">Raised when Excel completes a calculation. You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="7e448-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="7e448-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="7e448-p103">ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、CalculationEnded イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="7e448-p103">Raised when the user interrupts the calculation. The XLL should stop any asynchronous activities. The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="7e448-122">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="7e448-122">Property value/Return value</span></span>

<span data-ttu-id="7e448-123">成功した場合、pxRes (**Xltypeint**) の値 > 0 になります。</span><span class="sxs-lookup"><span data-stu-id="7e448-123">If successful, pxRes (**xltypeInt**) has a value > 0.</span></span> <span data-ttu-id="7e448-124">失敗した場合は、pxRes = = 0。</span><span class="sxs-lookup"><span data-stu-id="7e448-124">If unsuccessful, pxRes ==0.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e448-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e448-125">See also</span></span>



[<span data-ttu-id="7e448-126">非同期のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="7e448-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

