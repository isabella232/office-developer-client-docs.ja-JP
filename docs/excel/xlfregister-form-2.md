---
title: xlfRegister (形式 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister function [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798973"
---
# <a name="xlfregister-form-2"></a><span data-ttu-id="863b1-104">xlfRegister (形式 2)</span><span class="sxs-lookup"><span data-stu-id="863b1-104">xlfRegister (Form 2)</span></span>

 <span data-ttu-id="863b1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="863b1-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="863b1-p101">Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、Excel XLM マクロ シートからの **REGISTER** の呼び出しと同等です。</span><span class="sxs-lookup"><span data-stu-id="863b1-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **REGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="863b1-108">**xlfRegister** 関数は、次の 2 つの形式で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="863b1-108">The **xlfRegister** function can be called in two forms:</span></span> 
  
- <span data-ttu-id="863b1-109">[xlfRegister (形式 1)](xlfregister-form-1.md): コマンドや関数を個々に登録します。</span><span class="sxs-lookup"><span data-stu-id="863b1-109">[xlfRegister (Form 1)](xlfregister-form-1.md): Registers an individual command or function.</span></span>
    
- <span data-ttu-id="863b1-110">xlfRegister (形式 2): XLL を読み込んでアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="863b1-110">xlfRegister (Form 2): Loads and activates an XLL.</span></span>
    
<span data-ttu-id="863b1-111">この関数を形式 2 で呼び出した場合は、[xlAutoOpen](xlautoopen.md) プロシージャを含む XLL の読み込みとアクティブ化のみ行います。</span><span class="sxs-lookup"><span data-stu-id="863b1-111">Called in Form 2, this function can only be used to load and activate an XLL containing an [xlAutoOpen](xlautoopen.md) procedure.</span></span> 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a><span data-ttu-id="863b1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="863b1-112">Parameters</span></span>

 <span data-ttu-id="863b1-113">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="863b1-113">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="863b1-114">読み込みとアクティブ化を行う DLL 名。</span><span class="sxs-lookup"><span data-stu-id="863b1-114">The name of the DLL to be loaded and activated.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="863b1-115">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="863b1-115">Property Value/Return Value</span></span>

<span data-ttu-id="863b1-116">成功すると、DLL 名 (**xltypeStr**) を返します。</span><span class="sxs-lookup"><span data-stu-id="863b1-116">If successful, this returns the name of the DLL (xltypeStr). Otherwise it returns a #VALUE! error.</span></span> <span data-ttu-id="863b1-117">それ以外の場合は、#VALUE! </span><span class="sxs-lookup"><span data-stu-id="863b1-117">Otherwise it returns a #VALUE!</span></span> <span data-ttu-id="863b1-118">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="863b1-118">Error</span></span>
  
## <a name="see-also"></a><span data-ttu-id="863b1-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="863b1-119">See also</span></span>



[<span data-ttu-id="863b1-120">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="863b1-120">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

