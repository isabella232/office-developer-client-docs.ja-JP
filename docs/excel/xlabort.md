---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- xlabort function [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436658"
---
# <a name="xlabort"></a><span data-ttu-id="4979f-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="4979f-104">xlAbort</span></span>

 <span data-ttu-id="4979f-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4979f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4979f-p101">システム内の他のタスクにプロセッサを生成し、ユーザーが **Esc** を押してマクロを取り消したかどうかを確認します。ブックの再計算中にユーザーが **Esc** が押した場合は、この関数を呼び出すことによってワークシート関数内で検出することもできます。</span><span class="sxs-lookup"><span data-stu-id="4979f-p101">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro. If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="4979f-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4979f-108">Parameters</span></span>

 <span data-ttu-id="4979f-109">_pxRetain_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="4979f-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="4979f-p102">(Optional). If **FALSE**, this function checks for the break condition and clears any pending break. This enables the user to continue despite the break condition. If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span><span class="sxs-lookup"><span data-stu-id="4979f-p102">(Optional). If **FALSE**, this function checks for the break condition and clears any pending break. This enables the user to continue despite the break condition. If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4979f-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="4979f-114">Property value/Return value</span></span>

<span data-ttu-id="4979f-115">ユーザーが **Esc** を押した場合は、**TRUE** (**xltypeBool**) が返されます。</span><span class="sxs-lookup"><span data-stu-id="4979f-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4979f-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4979f-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="4979f-117">頻繁な呼び出しが必要な場合</span><span class="sxs-lookup"><span data-stu-id="4979f-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="4979f-118">時間のかかる関数やコマンドでは、この関数を頻繁に呼び出して、プロセッサをシステム内の他のタスクに生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4979f-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="4979f-119">微妙な表現を避ける</span><span class="sxs-lookup"><span data-stu-id="4979f-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="4979f-p103">ユーザー インターフェイスでは "Abort" という用語を使用しないようにします。代わりに "Cancel"、"Halt"、"Break"、"Stop" の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="4979f-p103">Avoid using the term "Abort" in your user interface. Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="4979f-122">例</span><span class="sxs-lookup"><span data-stu-id="4979f-122">Example</span></span>

<span data-ttu-id="4979f-p104">次のコードは、1 分が経過するまで、またはユーザーが **Esc** を押すまで、シート上でアクティブなセルを繰り返し移動し、**xlAbort** 関数を呼び出します。これによりプロセッサが生成され、共同でのマルチタスキングが容易になります。</span><span class="sxs-lookup"><span data-stu-id="4979f-p104">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**. It calls the function **xlAbort** occasionally. This yields the processor, easing cooperative multitasking.</span></span> 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="4979f-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4979f-126">See also</span></span>



[<span data-ttu-id="4979f-127">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="4979f-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

