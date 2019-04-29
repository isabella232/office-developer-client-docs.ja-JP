---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo function [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407796"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="85a9e-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="85a9e-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="85a9e-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="85a9e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="85a9e-p101">アドイン マネージャーが Excel セッションで初めて呼び出されたときに、Microsoft Excel によって呼び出されます。この関数は、ご使用のアドインについての情報をアドイン マネージャーに提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="85a9e-p101">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session. This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="85a9e-p102">Excel 2007 以降のバージョンでは、XLL によってエクスポートされる場合には **xlAddInManagerInfo** ではなく **xlAddInManagerInfo12** が呼び出されます。**xlAddInManagerInfo12** 関数は、**xlAddInManagerInfo** と同じように機能して、XLL の動作におけるバージョン固有の相違点を回避する必要があります。Excel では **xlAddInManagerInfo12** が **XLOPER12** データ型を返し、**xlAddInManagerInfo** は **XLOPER** データ型を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="85a9e-p102">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL. The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL. Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="85a9e-111">**xlAddInManagerInfo12** 関数は Excel 2007 より前の Excel バージョンでは呼び出されません。**XLOPER12** をサポートしていないためです。</span><span class="sxs-lookup"><span data-stu-id="85a9e-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="85a9e-112">Excel では、XLL がこれらいずれかの関数を実装してエクスポートすることは不要です。</span><span class="sxs-lookup"><span data-stu-id="85a9e-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="85a9e-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85a9e-113">Parameters</span></span>

 <span data-ttu-id="85a9e-114">_pxAction:_ 数値 **XLOPER/XLOPER12** (**xltypeInt** または **xltypeNum**) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="85a9e-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="85a9e-115">Excel で要求される情報です。</span><span class="sxs-lookup"><span data-stu-id="85a9e-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="85a9e-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="85a9e-116">Property value/Return value</span></span>

<span data-ttu-id="85a9e-p103">_pxAction_ が数値 1 の場合 (1 になるよう強制することもできます)、この関数を実装すると、アドインについての情報 (通常は名前。バージョン番号が含まれることもあります) が含まれる文字列が返ります。それ以外の場合、#VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="85a9e-p103">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number. Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="85a9e-119">文字列を返さない場合、Excel が戻り値を文字列に変換しようとします。</span><span class="sxs-lookup"><span data-stu-id="85a9e-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85a9e-120">注釈</span><span class="sxs-lookup"><span data-stu-id="85a9e-120">Remarks</span></span>

<span data-ttu-id="85a9e-p104">返される文字列が、動的に割り当てられたバッファーをポイントしている場合は、このバッファーを最終的に解放する必要があります。文字列が Excel によって割り当てられた場合、**xlbitXLFree** を設定して解放します。文字列が DLL によって割り当てられた場合には、**xlbitDLLFree** を設定して解放します。さらに、[xlAutoFree](xlautofree-xlautofree12.md) (**XLOPER** を返す場合) または **xlAutoFree12** (**XLOPER12** を返す場合) も実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="85a9e-p104">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed. If the string was allocated by Excel, you do this by setting **xlbitXLFree**. If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="85a9e-124">例</span><span class="sxs-lookup"><span data-stu-id="85a9e-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="85a9e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="85a9e-125">See also</span></span>



[<span data-ttu-id="85a9e-126">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="85a9e-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

